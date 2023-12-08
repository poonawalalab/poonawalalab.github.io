---
title: Robust contact-rich manipulation using Bayesian learning of passivity-based controllers
layout: rtopic
date: 2023-07-01
status: current
thumb: kitchen_panda.gif
---
## Goal
The project aims to advance the state-of-the-art in contact-rich manipulation by combining planning, control, and machine learning techniques to enable robust execution of contact-rich motion plans. 
This project is a collaboration between the Dr. Poonawala's group at the University of Kentucky and Dr. Aykut Satici's group at Boise State University. 

## Challenge
Planning algorithms can solve contact-rich manipulation problems when using quasi-static (zero velocity) or quasi-dynamic (constant velocity) models. Executing these plans using standard control techniques has generally been unsuccessful except in simple cases. A key challenge is that actual mode sequences can diverge from the plan very quickly. Techniques to control contact mode transitions are necessary. 
![Non-robust Plan]({{site.url}}/{{site.baseurl}}/assets/pdf/nonrobust_plan.pdf)

## Main Approach
The project will use Bayesian learning to train passivity-based neural network controllers (PBNNC). This technique, developed by Aykut Satici at Boise State University, is effective at finding controllers for mechanical systems that are robust to unkown parameters. This robustness to dynamic parameters will be critical for controlling contact. Bayesian learning can be positively impacted by using good priors. Dr. Poonawala will extend prior techniques for automated controller synthesis to identify a prior over the weights of the PBNNC. 
