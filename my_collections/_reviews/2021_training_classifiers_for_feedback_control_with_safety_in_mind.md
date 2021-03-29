---
class: "journal"
authors: "Poonawala, H.A.; Lauffer, N.;Topcu, U.;"
title: "Training Classifiers For Feedback Control With Safety In Mind"
venue: "Automatica"
year: "2021"
layout: page
---

### Broad area/overview
This paper deals with controlling mobile robots directly from sensor data or measurements. It uses tools from supervised machine learning to learn these controllers from data, and Lyapunov-based methods to analyze the correctness of these learned controllers.

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
Instead of estimating the state of the system for feedback control of the form $u = k(x)$, the approach tries to classify measurements into classes that indicate the control to be used. The control design problem becomes a classifier design problem, often solved using supervised machine learning.  

Supervised machine learning uses generalization error to evaluate the learning, where the error is related to a loss function. For control systems, we evaluate controllers based on closed-loop stability and behavior. The paper formulates a supervised learning problem where the closed-loop stability properties also affect the learning.  


### Solution Ideas
* The paper distinguishes between the measurement space $Y$ and the state space $X$ of the dynamical system being controlled. It assumes that there is a relationship $Y = \mathcal H(x)$, which is unknown but implictly captured by data comprising pairs of states ann measurements in those states. For example, the camera image a robot gets when it is some position and heading in a room.
* The classifier $C_X$ it learns is parametrized by a collection of hyperplanes $W$, that divides the state space into polyhedral regions. In effect, multiple binary classifiers are combined to get a multi-label classifier.
* Given this division of the state space $X$, they parametrize a piecewise Linear Lyapunov function $V$, and formulate stability conditions for the pieces.
* Using some mathematical results, these stability conditions become constraints on the the classifier hyperplanes $W$ and the Lyapunov function $V$.
* The constraints define an optimization problem, so that they can be combined with the supervised learning constraints to create a single optimization problem.
* If the solution has a certain value, then the controller design is correct in the state space.
* The classifier $C_X$ designed in state-space needs to be converted into a classifier $C_Y$ of measurements, which is done using another supervised learning problem
* Since this transformation is imperfect, the authors account for potential inaccuracies by solving a robust version of the optimization problem to train $W^\Delta$.

### Comments
* The paper focuses on a single example of a path-following robot.
* For this method to work, we must know the state space dynamics and also have data that describes measurements obtained in a state. Both assumptions are impractical.
* The paper casts training as a bilinear optimization problem, which are often unreliable to solve. It's not clear if the optimization will succeed in other problems.
* The piecewise approach might be impractical in high dimensional systems

### Recent Papers
*Note: This section makes more sense for papers published 1-2 years ago or earlier, unlike this paper that is still in press.*
* The [BADGER system](https://bair.berkeley.edu/blog/2020/03/12/badgr/) seems to solve this specific problem of navigation from complex sensor data without state estimation using reinforcement learning. There is no stability analysis, however.
