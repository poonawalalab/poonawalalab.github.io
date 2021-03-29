---
class: "journal"
authors: "Montalvo, W.; Escobar-Naranjo, J.; Garcia, C.A.; Garcia, M.V.;"
title: "Low-Cost Automation for Gravity Compensation of Robotic Arm"
venue: "Applied Sciences"
year: "2020"
layout: page
---

\toc
### Broad area/overview
This article presents research using a low-cost setup to represent Proportional Derivative (PD) Control with gravity compensation as a robost method for a robotic arm. A raspberry pi microcontroller and the open source Robot Operating System (ROS) software is used for the development of the control algorithm. Gravity compensation is defined in the article as "a term proportional to the position error, to which a damping consisting of the speed of movement is added. [Gravity Compensation] consists of a mechanical retention that absorbs the impulses resulting from the response, suppressing peaks and oscillations. For the stationary stage it is estimated that the position of the effector or terminal tool is constant, assuming a value of zero at the speed of movement."

### Notation
* $x$: state, $X$: State space
* $y$: measurement, $Y$: Measurement Space
* Controller $u = g(y)$
* $L$: Set of labels
* $C_X \colon X \to L$: Classifier in state space
* $C_Y \colon Y \to L$: Classifier in measurement space
* $V$: Lyapunov function
* $W$: set of hyperplanes that parametrizes $C_X$
* $W^\Delta$: set of hyperplanes that parametrizes a robust version of $C_X$

### Specific Problem
The authors main research goal is to exhibit the strengths of modern, low-cost methods of controls based gravity compensation. They outline ROS as a versatile tool available for the development of such systems.


### Solution Ideas
Section 3 of the article outlines the state of the technology. This research makes use of the *KUKA youBot Robotic Arm* manipulator which is a 5 DoF robotic arm with a two-finger end effector and an omnidirectional base. This manipulator comes system comes equipped with a library that allows for control and monitoring of actuators and sensors. The kinematic equations related to gravity compensation are outlined in section 3.3:
* model af a rigid robot with n links:
  - $M(q)q'' + C(q,q')q' + G(q) + F(q') = \tau$
* derivative proportional control derived by correction of error in joint positioning:
  - $\tau = Kp(\tilde q) - Kd(\tilde q') + G(q)$
In section 4, the authors outline the study case of this project as the implementation of control strategies using ROS and the Raspberry Pi with the common use of a robotic arm for positioning of objects.

In section 5 both the ROS node architecture and the cascaded PID regulation block diagram are outlined and illustrated. The ROS node infrastrcucture consists of 5 nodes: the Graphical User Interface (GUI), the controller node, the robot arm state node, and the youBot hardware node. The GUI takes user input which the control node filters to a controlled command and communicates to the robot arm state node. The arm state node then uses the robot driver to make move the mechanism according to the controlled input from the user.

Section 5.5 describes the ROS class used for gravity compensation called Module Gravity Compensation and its three subclasses:
* Controller Module Class: contains methods for inverse kinematics and trajectory planning
* Arm Dynamics Class: contains methods that handle the dynamical relationships between the robot and gravity and inertial forces. This class computes the calculations for gravity compensation
* youBotKinematics sub-Class: contains more specific information and methods that pertain to the robot used for this research

In the results section, the authors summarize the performance of the system after completing 20 executions of a pick and place task. The delay necessary for the study case to complete its gravity compensation computations is calculated for each iteration. The delays are just above .01 seconds for most of the tasks, with a few outliers approaching .07 seconds.

### Comments
* This article provides extensive details about the communication infrastrcucture between the robot, Raspberry Pi and ROS as well as details outlining the programming libraries and classes used.
