---
title: "Grasps and regrasps for multi-step tasks"
excerpt: "Deciding whether one grasp can carry out a whole manipulation plan, and where the robot needs to regrasp when it can't."
teaser: /images/teasers/Grasp_Regrasp.mp4
hero: /images/teasers/Grasp_Regrasp.mp4
order: 3
permalink: /research/grasps-and-regrasps/
paper: Grasp-Regrasp-for-Complex-Manipulation-ICRA-2025
papers:
  - Grasp-Regrasp-for-Complex-Manipulation-ICRA-2025
  - Grasp_Metric_IROS_2021
  - Task_Oriented_Grasping_IROS_2023
---

## The problem

Many tasks are more than one motion. Pivoting a box several times in a row is a sequence of constant screw motions,
and a grasp that works for the first motion may not work for a later one. The robot needs to know whether a single
grasp will do for the whole plan, and if not, where to regrasp and which grasps to use.

## Approach

We formalize regrasping in terms of the task. Starting from the object's point cloud and a manipulation plan given as
a sequence of constant screw motions, we use the [task-dependent grasp metric](/research/grasp-metric/) to find which
grasps can impart each motion. From this we compute whether a single grasp is enough for the whole plan or the robot
needs to regrasp along the way, and synthesize the grasps.

<figure class="project__figure">
{% include media.html src="/images/teasers/grasp-regrasp.png" alt="A plan of three pivots with a regrasp before the last one" %}
<figcaption>A plan with three pivots of a box: the robot grasps the box, pivots it twice, regrasps, and pivots it again.</figcaption>
</figure>

## Experiments

We ran the approach on a Franka Emika Panda. The clip at the top shows two trials, sped up 8×.

{% include youtube.html id="zVutzfO9Ev4" title="Synthesizing grasps and regrasps for complex manipulation tasks" %}
