---
title: "Task-oriented grasping from point clouds"
excerpt: "Finding a good grasping region for a task directly from a partial point cloud, using a neural network trained on the grasp metric instead of labeled grasps."
teaser: /images/teasers/ToGRASP.mp4
hero: /images/teasers/ToGRASP.mp4
order: 2
permalink: /research/task-oriented-grasping/
redirect_from:
  - /portfolio/portfolio-1/
code: https://github.com/irsl-sbu/Task-Oriented-Grasping-from-Point-Cloud-Representation
project: https://irsl-sbu.github.io/Task-Oriented-Grasping-from-Point-Cloud-Representation/
papers:
  - Task_Oriented_Grasping_IROS_2023
  - Point_Cloud_Decomposition_ICRA_2025
---

My PhD research focused on task-oriented grasping from sensor data. The problem has three parts: defining the task
mathematically, using that definition to say what makes a grasp good for the task, and working with noisy sensor
data in the form of partial point clouds from an RGB-D camera.

We define a task as a constant screw motion, or a sequence of them, to be imparted to the object after grasping. The
[task-dependent grasp metric](/research/grasp-metric/) evaluates whether a pair of contact locations can impart that
motion. Here we solve the inverse problem: given a partial point cloud of the object and a task screw, find a good
region to grasp.

We use the simplest geometric representation of the point cloud, a bounding box, and train a neural network to
predict the grasp metric on a cuboid. The predicted grasping region on the bounding box is then used to compute an
antipodal grasp on the actual object. The approach does not use any manually labeled data or grasping simulator, and
because the task is a screw motion, it couples directly with screw linear interpolation-based motion planners.
Follow-up work (ICRA 2025) extends this with point cloud decomposition.

<figure class="project__figure">
{% include media.html src="/images/teasers/task-oriented-grasping.mp4" alt="Point cloud of a conditioner bottle, the task screw, and the predicted grasping region" %}
<figcaption>Conditioner bottle: simulated point cloud and task screw, the pure rotation about the screw, and the predicted grasping region (yellow).</figcaption>
</figure>

For more results, see the [lab project page](https://irsl-sbu.github.io/Task-Oriented-Grasping-from-Point-Cloud-Representation/).
