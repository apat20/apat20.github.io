---
title: "Manipulation with environment contact"
excerpt: "Motion, force and trajectory planning for tasks where the object stays in contact with the environment, such as pivoting a heavy box about its edge."
teaser: /images/teasers/pivoting.png
order: 6
permalink: /research/contact/
redirect_from:
  - /portfolio/portfolio-4/
papers:
  - Trajectory_Planning_IROS_2024
  - Motion_Force_Planning_IROS_2021
  - Contact_Force_Synthesis_IROS_2020
---

To grasp and manipulate a wide range of objects, robotic hands and manipulators can make effective use of the
environment. Many tasks are accomplished by using contacts between the grasped object and the environment, for
example pivoting a heavy box about one of its edges instead of lifting it. We have developed algorithmic approaches
for motion and force planning for manipulating objects this way, while considering the nonlinear contact constraints.

<figure class="project__figure">
{% include media.html src="/images/teasers/pivoting.png" alt="A robot pivoting a box through intermediate poses" %}
<figcaption>Object gaiting: pivoting a box through a sequence of intermediate poses.</figcaption>
</figure>

More recently, we developed a general formulation for path-constrained, time-optimized trajectory planning with
environmental and object contacts.

<figure class="project__figure">
{% include media.html src="/images/teasers/traj-opt-clip.mp4" alt="Time-optimized trajectory for tilting a tray with a cube on it" %}
<figcaption>A time-optimized trajectory for tilting a tray with a cube on it, with the contact forces over time.</figcaption>
</figure>
