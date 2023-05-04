---
layout: post
title:  "David Yackzan defends his MS Thesis"
date:   2023-04-14
---

David Yackzan successfully defended his MS Thesis titled "Parallel Real-Time RRT\*: An RRT\*-based path planning process".

Traditional motion generation requires a few seconds to obtain a plan, during which a robot is often still. If goals or obstacles move, the process repeats. The goal of the work is develop responsive planning algorithms that are able to update safe motion plans on-the-fly in response to changing environments (with moving obstacles) or changing goals (such as when interacting with a human).

His work develops a multi-threaded version of the Real-Time RRT* algorithm that enables it to run at 1000 Hz on a 7 degree-of-freedom robot arm. The code is based on ROS and [available on github](https://github.com/dwya222/robo_demo_ws). The planning, control, sensing, and collision checking run on separate threads to obtain high responsiveness while still benefitting from the validity provided by motion planning. 