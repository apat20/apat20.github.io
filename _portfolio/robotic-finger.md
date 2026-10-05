---
title: "Design of a robotic finger"
excerpt: "A compact 3-DoF series-parallel finger with abduction/adduction and flexion/extension, with closed-form kinematics so the fingertip's motion and force can be controlled."
teaser: /images/teasers/hybrid-finger.jpg
hero: /images/teasers/hybrid-finger.jpg
order: 7
permalink: /research/robotic-finger/
redirect_from:
  - /portfolio/portfolio-3/
papers:
  - Gripper_Design_IDETC_2024
---

Dexterous robotic hands are key to using robots in many applications, including service robotics, assistive robotics,
and healthcare. These applications require robots to manipulate objects designed for humans, with capabilities beyond
pick-and-place. A key to making a robotic hand dexterous is fingers whose fingertip motion and forces are controllable,
while keeping the fingers compact, close to the size of a human finger. Although a wide range of hands have been
proposed, there is no readily available robotic hand that is compact, dexterous, reliable, and cost-effective.

We present a novel series-parallel 3-DoF finger mechanism with abduction/adduction as well as flexion/extension, for
which we derive the position kinematics and the Jacobian. This lets us control the position and velocity of the
fingertip, and do force control because the Jacobian is in closed form. To the best of our knowledge, this is the
first 3-DoF finger with both abduction/adduction and flexion/extension whose kinematics is well understood. An earlier
version of this work appeared at ASME IDETC 2024.

{% include youtube.html id="GsIMyZjH4Vg" title="Series-parallel hybrid finger for robotic hands" %}
