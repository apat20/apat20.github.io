---
title: "Task-dependent grasp metric"
excerpt: "Scoring a grasp by whether it can produce the motion a task needs, such as turning a knob or pivoting a box about its edge, computed as a second-order cone program."
teaser: /images/teasers/Grasp_Metric.png
order: 1
permalink: /research/grasp-metric/
paper: Grasp_Metric_IROS_2021
code: https://github.com/apat20/tograsp-socp
papers:
  - Grasp_Metric_IROS_2021
  - Grasp_Metric_Dynamics_ICRA_2025_LBR
  - Task_Oriented_Grasping_IROS_2023
  - Grasp-Regrasp-for-Complex-Manipulation-ICRA-2025
---

## The problem

A grasp that is good for lifting an object can be useless for turning a knob, opening a drawer, or pivoting a heavy
box about one of its edges. Whether a grasp is good depends on what the robot has to do with the object after
grasping it, so we need a way to score grasps against a specific task.

## Approach

We describe the task as the constant screw motion the object has to go through after it is grasped: a pure
translation to open a drawer, a rotation about the knob's axis, or a rotation about the box's edge.

<figure class="project__figure">
{% include media.html src="/images/teasers/Grasp_Metric.png" alt="A drawer, a knob and a box, each with its task screw axis s" %}
<figcaption>Tasks as constant screw motions about an axis s: opening a drawer, turning a knob, and pivoting a box about its edge.</figcaption>
</figure>

Given a pair of contact locations, the metric is the largest force the grasp can apply along the screw axis (for a pure
translation), or the largest moment it can apply about the screw axis (for any other screw motion). This is subject to:

- friction at each finger contact, and a limit on each finger's normal force,
- the object's weight, and
- friction where the object touches the environment, for tasks like pivoting.

Friction cones are second-order cones, so computing the metric is a second-order cone program (SOCP), and the friction
cones do not have to be approximated. Later work (ICRA 2025, late-breaking results) adds the dynamics of the object and
the manipulator.

<figure class="project__figure">
{% include media.html src="/images/teasers/grasp_metric_with_dynamics.png" alt="Four grasps on a box with their metric values" %}
<figcaption>With the object and manipulator dynamics included: the metric value for four different grasps.</figcaption>
</figure>

## Where it is used

The metric is the basis for the rest of my grasping work. We trained a neural network to predict it on point clouds
for [task-oriented grasping](/research/task-oriented-grasping/), and used it to decide when a task needs
[a regrasp](/research/grasps-and-regrasps/).

## Video

{% include youtube.html id="xM9ETHeR4O0" title="Computing a task-dependent grasp metric using second-order cone programs" %}

## Code

[tograsp-socp](https://github.com/apat20/tograsp-socp) is a Python implementation. Given an object point cloud and a
task screw, it computes the metric for antipodal contacts sampled on the object's bounding box, extracts the grasping
region, and computes candidate end-effector poses for a Franka Emika Panda.

```bash
git clone https://github.com/apat20/tograsp-socp.git && cd tograsp-socp
conda env create -f environment.yml && conda activate tograsp_socp
# pure translation: largest force along the screw axis
python main_pickup.py --filename nontextured.ply
# any other screw motion: largest moment about the screw axis
python main_gcsm.py --filename nontextured.ply
```

## Citation

```bibtex
@inproceedings{fakhari2021computing,
  title={Computing a task-dependent grasp metric using second-order cone programs},
  author={Fakhari, Amin and Patankar, Aditya and Xie, Jiayin and Chakraborty, Nilanjan},
  booktitle={2021 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)},
  pages={4009--4016},
  year={2021},
  organization={IEEE}
}
```
