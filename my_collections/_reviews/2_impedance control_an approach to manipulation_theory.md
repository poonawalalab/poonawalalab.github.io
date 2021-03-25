---
class: "Journal paper"
authors: "Hogan, N.;"
title: "Impedance Control: An Approach to Manipulation: Part I-Theory"
venue: "Journal of dynamic systems, Measurement and Control"
year: "1985"
layout: page
---

### Broad area/overview
Manipulation fundamentally requires the manipulator to be mechanically coupled to the object being manipulated; the manipulator may not be treated as an isolated system. in this paper an approach is developed by considering the mechanics of interaction between physical systems. it was shown that control of position or force alone is inadequate; control of dynamic behavior is also required. It is shown that as manipulation is a fundamentally nonlinear problem, the distinction between impedance and admittance is essential, and given the environment contains inertial objects, the manipulator must be an impedance. A generalization of a Norton equivalent network is defined for a broad class of nonlinear manipulators which separates the control of motion from the control of impedance while preserving the superposition properties of the Norton network.
### Notation
* $W$: Mechanical work
* $F$: Force
* $T$: Torque
* $: { {c } } $: Modulation by command set
* $S_e$: Effort(force) source
* $S_f$: Flow(Velocity) control
* $Z$: Impedance
* $Y$: Admittance
* $Z_o$: nodic Impedance
* $Z_n$: Nonnodic impedance
* $X_o$: virtual position
* $V_o$: virtual velocity


### Specific Problem
This paper has presented a unified approach to manipulation termed "impedance control." Because by its nature manipulation requires mechanical interaction between systems, the focus of the approach is on the characterization and control of interaction. By assuming that no control algorithm may make a physical system behave like anything other than a physical system the network concepts of bond graphs may be applied to describe the way the controller may modify the behavior of the manipulator.

### Basic Ideas and definitions
* The manipulator is some collection of physical structures, sensors, and actuators (hardware) combined with some set of control algorithms (software). A unified framework for considering the action of both hardware and software in the control of dynamic behavior can be obtained by making the reasonable assumption that no controller can make the manipulator appear to the environment as anything other than a physical system.
 ![](/assets/img/Capture_1.png)
*  in this paper admittances is defined as a system accepting effort (e.g., force) inputs and yielding flow (e.g., motion) outputs; and impedances accepting flow (e.g., motion) inputs and yielding effort (e.g., force) outputs.
* The distinction between admittance and impedance is fundamental: Real physical systems exist which can be described in one form and not the other.
* The most important consequence of dynamic interaction between two physical systems is that one must physically complement the other: Along any degree of freedom, if one is an impedance, the other must be an admittance and vice versa.
* the controller should be capable of modulating the impedance of the manipulator as appropriate for a particular phase of a task.
* The simplest equivalent physical network representing impedance control is shown in the following figure. The position commanded by the high-level supervisor is represented by a flow source, an ideal element which may impose any time history of velocity on the rest of the system. To prevent causal conflict between this element and the environmental admittance (which must experience an impressed effort) a zero junction is interposed between the two. The impedance coupled to this zero-junction represents the relation between force and motion commanded by the supervisor and includes both the static force/displacement relation plus the possible dynamic terms required to ensure controlled dynamic behavior.
![](/assets/img/Capture_2.png)
* The only assumptions made were that the manipulator is sufficiently controllable to be able to determine an equilibrium position of an unconstrained inertial object such as a mass, that the port impedance is nodic, and that its static component is such that if its gradient is nonzero then zero force defines an unique position—not a restrictive set of assumptions.

 1. $dz/dt=Z_s[z,(V_o:$\{c\}-Y_o(y))]:\{c\}$

 1. $dy/dt=Y_s[y,Z_o(z,V_o:$\{c}-Y_o(y))]:\{c\}$

 1. $F=Z_o(z,[V_o:\{c\}-Y_o(y)]):\{c\}$

 1. $V=Y_o(y)$

### Conclusion
* The most interesting consequence of the assumptions underlying impedance control is that if the dynamic behavior of the manipulator is dissected into a set of component impedances, these may be reassembled by simple addition even when the behavior of any or all of the components is nonlinear. This is a direct consequence of the assumption that the environment is an admittance.
* When the manipulator is decoupled from its environment the terms in the dynamic equations due to the environmental admittance disappear and in principle the manipulator alone need exhibit no inertial behavior. In practice the uncoupled manipulator still has inertia. Because of the inevitable inertial dynamics of the isolated manipulator the superposition of impedances holds even when the manipulator is uncoupled from its environment as there is always an admittance to sum forces and impedances.
### Recent Papers
* Yang, Z., Peng, J., & Liu, Y. (2019). Adaptive neural network force tracking impedance control for uncertain robotic manipulator based on nonlinear velocity observer. Neurocomputing, 331, 263-280.
* Peng, J., Yang, Z., & Ma, T. (2019). Position/force tracking impedance control for robotic systems with uncertainties based on adaptive jacobian and neural network. Complexity, 2019.
