---
class: "journal"
authors: "Poonawala, H.A."
title: "Stability Analysis of Conewise Affine Dynamical Systems Using Conewise Linear Lyapunov Functions"
venue: "Control Systems Letter"
year: "2020"
layout: page
---
### Broad area/overview
This paper proposes automated algorithms to verify the stability of conewise affine dynamical systems using conewise linear Lyapunov functions. The conewise refers to a piecewise function. The pieces or cells in the state space are all unbounded cones, each with apex at the origin.

### Notation
* $x$: state, $X$: State space
* $\mathcal P = \{X_i\}$: Partition of $X$ into cones $X_i$
* $\Omega_{\mathcal P}$: Conewise dynamical system with partition $\mathcal P $
* $V_{\mathcal Q}(x)$: Conewise Lyapunov function with partition $\mathcal Q = \{Z_j \}$
* $p_j$: vector associated with $Z_j$ so that $V_{\mathcal Q}(x) = p_j^T x$ when $x \in Z_j$

### Specific Problem
Most methods for Lyapunov-based analysis formulate stability conditions given a parametrization for the dynamical system and the Lyapunov function. Switched systems are often a good model for many nonlinear dynamical systems. Many approaches search for piecewise Lyapunov functions $V_{\mathcal Q}(x)$ to analyze piecewise dynamical systems $\Omega_{\mathcal P}$. Often, the $\mathcal P = \mathcal Q$, and there is no reason to expect this Lyapunov function to be suitable. A natural idea is to refine the partition, however the refinement process is often heuristic.


### Solution Ideas
* The paper reformulates Lyapunov stability conditions that include the state as a variable into an alternative set of conditions that do not contain the state as a variable. Unlike the S-procedure, this conversion is exact.
* Unlike other methods, the stability conditions account for the case where the dynamics in regions adjacent to the origin are affine.
* This paper uses the stability conditions to provide a better criterion for selecting which cells to refine. In contrast, previous conditions refined any cell for which the stability condition does not hold.

### Comments
* The paper appears to solve new problems unsolved by other methods, due to the specific stability conditions chosen
* The paper claims that the refinement criterion is not heuristic, however a comparison to the heuristic methods is not provided
* The examples have dimension 2 or 3. It is not clear if the computational framework will be able to solve higher dimension systems.

### Recent Papers
*Note: This section makes more sense for papers published 1-2 years ago or earlier, unlike this paper.*
* [Hongkai Dai's paper](http://groups.csail.mit.edu/robotics-center/public_papers/Dai20.pdf) in CDC 2020 uses a conewise linear Lyapunov function defined through a ReLU neural network . They Define a loss function for violation of Lyapunov functions at points and max violation, and trains the network using it. This training has to include a Mixed Integer Linear Program. The common idea is to use partitions not defined by the dynamics, however there is no refinement, or advice on selecting the number of nodes.
