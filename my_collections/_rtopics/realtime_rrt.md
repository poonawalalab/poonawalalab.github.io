---
title: Real-Time Path Planning
layout: rtopic
date: 2023-05-10
thumb: Reroute_Routine.png
status: current
---
## Motivation
Path planning algorithms are highly effective for generating collision free motion. However, they take a few seconds to find plans. In static environments with constant goals, this planning time is not an issue. In environments with moving obstacles or changing goals, the robot will never be able to find and execute a valid plan in time. 

![Reroute Routine]({{site.url}}/{{site.baseurl}}/assets/img/Reroute_Routine.png)

## Challenge
Algorithms like RRT* spend a majority of time in collision checking operations. These checks must be conducted during sampling and tree extension operations. 

## Approach
One way to reduce *re-planning* time is to preserve the tree for use in future re-planning steps, with intelligent update operations when re-planning is not demanded. Our lab has developed and implemented algorithms that enable real-time re-planning of collaborative robot arm motions in response to changes in obstacle and goal locations. 

However, the initial plan still take seconds to compute. This time can be reduced by using GPU acceleration to speed up collision checking operations. This is an active area of research.
