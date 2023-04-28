---
layout: post
title:  "Stability Analysis and Controller Synthesis using Single-hidden-layer ReLU Neural Networks"
date:   2023-04-07
---

Our [paper](https://ieeexplore.ieee.org/document/10108069) on analyzing and controlling dynamical systems modeled using rectified neural networks has been accepted to the IEEE Transactions on Automatic Control. 

We show how to computationally evaluate or search for piecewise affine Lyapunov functions parametrized as a rectified neural networks. The advantage of such Lyapunov functions is that the stability analysis is exact when the dynamics are also piecewise affine. By contrast, polynomial Lyapunov functions are conservative, due to issues with quantifier elimination. We present 2D, 3D, and 4D examples where the method does better than other available approaches for stability verification. However, scaling to higher dimensions will need further work.
