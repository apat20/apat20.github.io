---
title: "Sensor-based Task Oriented Grasp Synthesis"
excerpt: "One of the key challenges in task-oriented grasp synthesis is to mathematically represent a task. In our work, we represent a task as a sequence of constant screw motions. Given a grasp (pair of antipodal contact locations) we can evaluate its feasibility for imparting the desired constant screw motion using our proposed task-dependent grasp metric. More recently, we have developed a neural network-based approach which solves the inverse problem, i.e. given an object representation in terms of a partial point cloud, obtained from an RGBD sensor, and a task in terms of a screw axis, compute a good grasping region for the robot to grasp the object and impart the desired constant screw motion. For more details please the [project page](https://irsl-sbu.github.io/Task-Oriented-Grasping-from-Point-Cloud-Representation/).
<img src='/images/conditioner.gif'> <br/>

More recently, we have formalized the notion of regrasping in order to satify the motion constraints. Using our task-dependent grasp metric and a manipulation plan we are able to compute whether there is a need to regrasp an object while executing the manipulation plan or a single grasp would suffice."

collection: portfolio
---

My PhD research focuses on task-oriented grasping from sensor data. There are a few key aspects to this problem: the first one is the mathematical definition of a task, the second key aspect is using this definition of a task, how do we formalise the notion of grasping to perform a task, and the last part is incorporating noisy sensor data in the form of partial point clouds from an RGBD camera. In our work, we define a task as a constant screw motion or a sequence of constant screw motions to be specific. Using this definition of a task, we have developed a task-dependent grasp metric as a second-order cone program which evaluates the feasibility of object-robot contact locations to impart a specific constant screw motion. We have developed algorithmic approaches which use this notion of a task and a grasp to perform grasp synthesis on point cloud data using its simplest possible geometric representation i.e. a bounding box. 

Related Papers: 
* A. Fakhari, A. Patankar, J.Xie and N. Chakraborty. Computing a Task-Dependent Grasp Metric Using Second-Order Cone Programs. <i>IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)</i>, Prague, Czech Republic, 2021.

* A. Patankar, K.Phi, D. Mahalingam,  N. Chakraborty and I.V. Ramakrishnan. Task-Oriented Grasping with Point Cloud Representation of Objects. <i>IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)</i>, Detroit, MI, US, 2023.

* D. Mahalingam, A. Patankar, D. Das, N. Chakraborty, C.R. Ramakrishnan and I.V. Ramakrishnan. Caregiver-Guided Robotic Manipulation to Promote Independence of People with Significant Locomotor Disability. Workshop on Assistive Robotics for Citizens, <i>IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)</i> 2023.