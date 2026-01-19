---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

[Download CV](https://drive.google.com/file/d/1jIBV1XhUjE2TqQ_CcZb66__aUG3ZyDns/view?usp=sharing).

**Education**
======
* Ph.D in Mechanical Engineering - Robotics, minor in Computer Science, Stony Brook University 2026 (expected)
* M.S. in Mechanical Engineering, Stony Brook University, 2019
* B.E. in Mechanical Engineering, Savitribai Phule Pune University, 2012

**Work experience**
======

* **Research Assistant** (June 2020 - Present)
  * **Grasping and Optimization:** Formulated a novel task-dependent grasp metric as a Second-Order Cone Program (SOCP) to evaluate grasps (antipodal and multifingered) based on their feasibility to impart the desired
  motion after grasping. Proposed formulation incorporates object-environment contact and dynamics withoutapproximating the friction cone.
  * **Grasp Synthesis:** Developed novel analytical and data-driven approaches for task-oriented grasp (regrasp) synthesis directly from sensor data while considering the motion to be imparted to the object.
  * **Constrained Planning:** Developed novel motion planning, force planning, and trajectory optimization approaches incorporating environmental contact constraints.
  * **Perception and Manipulation:** Engineered a perception and manipulation stack using ROS in Python and C++, integrating state-of-the-art deep learning-based perception alongside novel screw geometry-based methods for manipulation.
  * **Foundation Models for Task and Motion Planning:** Exploring the integration of foundation models, such as VLMs and LLMs, with screw geometry-based approaches to enhance a robot’s manipulation capabilities,
  particularly for tasks involving end-effector motion constraints.
  * **Supervisors:** [Dr. Nilanjan Chakraborty](https://www.cs.stonybrook.edu/people/faculty/nilanjanchakraborty), [Dr. CR Ramakrishnan](https://www.cs.stonybrook.edu/people/faculty/crramakrishnan) and [Dr. IV Ramakrishnan](https://www.cs.stonybrook.edu/people/faculty/ivramakrishnan)

* **Robotics and Emboided AI PhD Fellow** (June 2025 - August 2025)
  * Associated with: [GE Aerospace Research](https://www.geaerospace.com/?utm_source=google&utm_medium=cpc&utm_campaign=GE+Aerospace+%7C+Brand&gad_source=1), Niskayuna, NY, USA
  * Part of the Autonomous Systems Research Group at GE Aerospace Research. 
  * **NVIDIA Robotics Stack Validation:** Evaluated state-of-the-art NVIDIA algorithms for High-Mix Low-Volume industrial automation. Specifically validated cuRobo for collision-free motion planning and FoundationPose/SyntheticDETR within Isaac ROS for 6D pose estimation.
  * **Synthetic Data Generation:** Developed a procedural defective part generation pipeline to evaluate perception systems for defect detection. Engineered a Python package to synthetically inject realistic ”bubble-like” defects onto a CAD model of a ceramic-composite platform in simulation, enabling the rigorous testing of perception and planning algorithms.
  * **Planning for Autonomous Scanning:** Designed a perception-driven motion planning framework for scanning tubes and ducts. Integrated SAM (Segment Anything Model) for segmentation to extract point clouds and compute an Oriented Bounding Box (OBB) to assign a local object reference frame. Integrated ScLERP-based motion planning to track 6-DoF scanning poses generated using the bounding box.

* **Research Intern - Robotics and 3D Modelling** (June 2024 -  August 2024)
  * Associated with: [Nokia Bell Labs](https://www.bell-labs.com/#gref), Murray Hill, NJ, USA 
  * Investigated techniques for representing and understanding large indoor physical spaces using radiance
  field techniques like NeRFs and 3D Gaussian Splatting to develop corresponding digital twins.
  * Developed efficient pipelines for generating 3D reconstructions of large indoor environments (warehouses) using data collected from fisheye cameras (Qoocam, Insta360, Kodak pixpro SP360), ceiling
  cameras (Axis), and RGB-D cameras (Intel Realsense D435i) mounted on a mobile robot.
  * Diagnosed and resolved key issues in camera calibration and data acquisition from RGB-D cameras
  on a moving mobile robot, leading to a **30%** improvement in PSNR during training for radiance field
  generation.
  * Supervisors: [Dr. Matthew Andrews](https://www.bell-labs.com/about/researcher-profiles/matthewandrews/) and [Dr.Jeongran Lee](https://www.bell-labs.com/about/researcher-profiles/jeongranlee/) ([Modelling and Opimization Group, AIRL](https://www.bell-labs.com/research-innovation/projects-and-initiatives/air-lab/modelling-optimization/#gref))

* Teaching Assistant
  * Associated with: Stony Brook University
  * MEC 310 - Introduction to Machine Design (Fall 2019)
  * MEC 410 - Design of Machine Elements (Spring 2020)
  * MEC 559 - Mobile Robotics and Autonomous Vehicles (Spring 2024)

* Mechanical Design Intern (Nov 2016 - April 2017)
  * Associated with: Integrated Systems, Chinchwad, Maharashtra, India
  * Successfully designed and assembled special-purpose machines and fixtures, applying mechanical design principles to improve production processes.
  * Effectively coordinated with vendors for raw material procurement and component manufacturing, ensuring smooth project execution and meeting project deadlines.

Skills
======
* Programming Languages: Python, C++, MATLAB, Prolog 
* Frameworks: ROS, PyTorch, git, TensorFlow
* Application Software and CAD: PyBullet, Gazebo, Isaac Sim, CoppeliaSim, SolidWorks, AutoCAD, Inkscape, Blender
* Libraries: Numpy, OpenCV, Open3D, cvx, cvxpy, YALMIP, nerfstudio, Eigen, scikit-learn, PCL, OpenGL 

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
<!-- Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul> -->
  
<!-- Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul> -->

Academic Projects
======
  
* RRT Motion Planner for Differential Drive Robots
  * Implemented a modified RRT (Rapidly-exploring Random Trees) using bidirectional search trees with node expansion heuristics and region-based sampling of the goal configuration.[[report]](https://drive.google.com/file/d/1t-eNTLpaBPZZ2SubyXm5LxXQmw2CrnbT/view?usp=sharing)[[code]](https://github.com/apat20/mobile-robot-rrt-planner)

* Transforming Constraint Satisfaction Problems from MiniZinc to QUBO
  * Implemented a pipeline, in Python, for converting Constraint Satisfaction Problems (CSPs) modelled using MiniZinc into their equivalent Quadratic Unconstrained Binary Optimization (QUBO) formulations. [[code]](https://drive.google.com/file/d/1-_Kd3WMGHBAQmqCgSZlOCanuHsUg0Hg7/view?usp=sharing)

* Newton-Euler Inverse Dynamics
    * Implemented the forward and backward iteration stage of the recursive Newton-Euler Inverse Dynamics algorithm. [[code]](https://github.com/apat20/Manipulator_Dynamics)

* Visual Odometry using Deep Recurrent Convolutional Neural Networks
  * Implemented an end-to-end framework for Monocular Visual Odometry using Deep Recurrent Convolutional Neural Networks trained on the KITTI Dataset. [[code]](https://github.com/shubpate/DeepVO)
  
Service and Leadership
======

* Reviewer
  * IEEE Transactions on Robotics: 2021
  * IEEE International Conference on Robotics and Automation: 2020 - 2024
  * IEEE/RSJ International Conference on Intelligent Robots and Systems: 2020, 2024
* Session Chair
  * Grasping - IEEE/RSJ International Conference on Intelligent Robots and Systems, 2021

* Mentoring Experience:  Actively participated in mentoring high-school, undergraduate and graduate students
  * Simmons Summer Research Program - Stony Brook University: 2021
  * Garcia Summer Research Program - Stony Brook University: 2021-2023
  * CSE 523-524 Advanced Project in Computer Science: 2021 - Present

* Leadership Experience
  * Graduate Student Organisation (SBU) - Secretary (Executive Board): July 2020 - May 2021
    * Elected by the graduate student body at Stony Brook University.
    * Responsible for maintaining GSO documents and records pertaining to the E-board and Senate
    * Chaired the Elections Committee charged with conducting campus-wide elections in tandem with University administration
    * Kickstarted various initiatives during COVID-19 to increase student and alumni engagement while fostering a strong community spirit
  * Graduate Housing Residents Association (SBU) - Treasurer (Executive Board): Sept 2019 - Sept 2021 
    * Elected by the graduate student body residing on-campus to serve as a member of the Executive Board
    * Responsible for maintaining expenditure records and procuring funds from programming
  * Graduate Student Organisation (SBU) - Senator: Sept 2019 - May 2020
    * Represented the Department of Mechanical Engineering as the primary Senator at the GSO Senate meetings.
  * Indian Graduate Student Association (SBU) - President (Executive Board): Nov 2017 -  Dec 2018
    * Organized and conducted various cultural events and student orientations for the Indian graduate student community at SBU.
  
Honors and Awards
====== 

* Winner - Graduate Research Symposium, Stony Brook University: March 2023 & 2025
  Topic: Task-Oriented Grasping with Point Cloud Representation of Objects

* Technology Innovation Award Runner Up, SAE Baja India: Feb 2016

* Ranked 34th in the Maharashtra Talent Search Examination 2008 conduted by Modern Education Society's Center for Talent Search and Excellence.


References will be provided on request. 
