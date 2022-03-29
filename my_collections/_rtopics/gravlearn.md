---
title: Learning Robot Models
layout: rtopic
thumb: robot-arm.png
date: 2018-06-01
status: current
---
## Learning Robot Models
<div class = "justified">
<p>Traditional controller design for robots either uses model-free motor-level PID controllers or model-based controllers based on the Euler-Lagrangian models
\[
M(q) \ddot q + C(q,\dot q) \dot q + G(q) = u,
\]
where \(q\) represents the robot's joint angles and \(u\) represents the torques applied on the corresponding joint axes.</p>
</div>
<div class = "justified">
<p> In practice, model-free PID controllers for robots work well only over a limited range operating conditions. In contrast, model-based controllers are far superior, but these models are difficult to obtain. This research direction seeks to develop algorithms that efficiently learn these models, without relying on a parametric model provided by a human.</p>
</div>


<!--div align="center"><img src="{{site.url}}/{{site.baseurl}}/assets/img/panda.jpeg" alt="Pic"  width="846px"></div-->

<h3> Self-Supervised Learning of The Conservative Force Vector</h3>
<div class="flex-container">
<div align="center"><img src="{{site.url}}/{{site.baseurl}}/assets/img/robot-arm.png" alt="Pic"  width="846px">

  <div class = "justified">
  <p> We are developing sample-efficient algorithms for learning the vector of conservative forces acting on a robot, without any explicit specification of the number of passive energy-storing elements on the robot. This development uses the MuJoCo multi-contact physics engine, with validation on a real Franka Emika Panda robot.
 </p>
</div>
  <!--div> <a href="autolyap_example.png"><img src="{{site.url}}/{{site.baseurl}}/assets/img/autolyap_example.png" alt="Classifier in a Loop" width = "450px"></a></div-->
</div>
