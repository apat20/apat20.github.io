---
title: "Motion planning from demonstrations"
excerpt: "Extracting the constraints of a task like pouring or scooping from a kinesthetic demonstration, and reusing them for new object positions, new objects, and harvesting in vertical farms."
teaser: /images/teasers/transfer-clip.mp4
hero: /images/teasers/transfer-clip.mp4
order: 4
permalink: /research/demonstrations/
redirect_from:
  - /portfolio/portfolio-2/
papers:
  - Transferring_Kinesthetic_Demonstrations_2025
  - Vertical_Farming_ICRA_2024
  - Motion_Generalization_IROS_2023
  - Caregiver_SLD_IROS_2023
---

Representing complex manipulation tasks, like scooping and pouring, as a sequence of constant screw motions in SE(3)
allows us to extract the task-related constraints on the end-effector's motion from kinesthetic demonstrations and
transfer them to new instances of the same task. The motion plans are computed with screw linear interpolation
(ScLERP), which satisfies these constraints kinematically.

<figure class="project__figure">
{% include media.html src="/images/research/motion-planning-demo.mp4" alt="A Franka Emika Panda pouring into a bowl" %}
<figcaption>Pouring with a Franka Emika Panda.</figcaption>
</figure>

We have evaluated this approach on scooping and pouring, and in containerized vertical farms for transplanting and
harvesting leafy crops.

<figure class="project__figure">
{% include media.html src="/images/teasers/vertical-farming.mp4" alt="A cobot harvesting leafy crops from a vertical farming tower" %}
<figcaption>Harvesting leafy crops in a containerized vertical farm.</figcaption>
</figure>

We have also developed an approach to transfer the task-related constraints between objects that are functionally
similar but have different geometries. The notion of functional similarity is captured by a knowledge base.

<figure class="project__figure">
{% include media.html src="/images/teasers/schematic_overview_dibyendu.png" alt="Knowledge-enabled motion generation pipeline" %}
<figcaption>Knowledge-enabled motion generation: the robot queries a knowledge base for a relevant demonstration and the object's geometric attributes, then plans with ScLERP.</figcaption>
</figure>

More recently, we developed a self-evaluation-based approach that lets the robot compute the minimal set of
kinesthetic demonstrations needed to perform tasks like pouring and scooping reliably over a region of its workspace.
See [How many demonstrations are enough?](/research/how-many-demonstrations/)
