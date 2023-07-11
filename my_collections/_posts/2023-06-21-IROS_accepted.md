---
layout: post
title:  "Paper provably correct path-following accepted to IROS 2023 "
date:   2023-04-07
---

Our [paper](https://arxiv.org/abs/2303.12182) on provably-correct sensor driven control has been accepted to to IROS 2023 to be held in Detroit, MI. Benton Clark is the lead on this work. 

Controllers for mobile robots that convert high-dimensional sensor models into control inputs are increasingly data-driven. How do we know if these controllers will work, given the variability of environments that the mobile robot may be in? 

This paper presents a framework for defining such controllers with the ability to guarantee path-following behaviors. Most guarantees rely on controllers that are good at estimating the state from sensor readings, or a high-fidelity simulator that can generate the sensor reading corresponding to a state. Our work requires neither, paving the way for state-free and sensor-model-free verification of path-following control. This verification ability means a mobile robot can learn new controllers and verify them online, reducing the impact of distribution shift. 