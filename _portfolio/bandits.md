---
title: "How many demonstrations are enough?"
excerpt: "Letting the robot evaluate its own plans and ask for kinesthetic demonstrations incrementally, so it can pour and scoop reliably over a region of its workspace with as few demonstrations as possible."
teaser: /images/teasers/bandits-clip.mp4
hero: /images/teasers/bandits-clip.mp4
order: 5
permalink: /research/how-many-demonstrations/
paper: Screw_Geometry_Bandits_ICRA_2026
papers:
  - Screw_Geometry_Bandits_ICRA_2026
  - Self_Evaluation_IROS_2023
  - Transferring_Kinesthetic_Demonstrations_2025
---

## The problem

Kinesthetic demonstrations are an easy way to teach a robot tasks like pouring and scooping, but each one takes time,
and the person teaching has no good way of knowing how many are needed. A demonstration given in one part of the
workspace may not be enough for the task to succeed everywhere the robot needs to do it.

## Approach

Each demonstration is represented as a sequence of constant screw motions, which can be used to generate motion plans
for new positions of the objects with screw linear interpolation
([more on this](/research/demonstrations/)). The robot evaluates these plans itself over a specified region of its
workspace, and demonstrations are acquired incrementally, only where the existing ones are not enough. The
self-evaluation draws on multi-armed bandits, and the aim is the minimal set of demonstrations needed to perform the
task reliably over that region.

<figure class="project__figure">
{% include media.html src="/images/teasers/bandits-motivation.png" alt="Top view of the robot's workspace with the region where the task should succeed" %}
<figcaption>The region of the robot's workspace (x<sub>min</sub> to x<sub>max</sub>, y<sub>min</sub> to y<sub>max</sub>) over which the task should succeed.</figcaption>
</figure>

## Experiments

We evaluated the approach on pouring and scooping with a Baxter robot.

{% include youtube.html id="R-qICICdEos" title="Screw geometry meets bandits: incremental acquisition of demonstrations" %}
