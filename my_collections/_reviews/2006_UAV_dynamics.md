---
class: "Article"
authors: "A. North; S. Bouabdallah; R. Siegwart;"
title: "Dynamic Modeling of Fixed-Wing UAVs"
venue: "Autonomous Systems Laboratory, ETH Zurich"
year: "2006"
layout: page
---
### Motivation for this review
This review of the article mentioned is just one of the series of documents that will talk about modelling the dynamics of a fixed-wing UAV. By the end of this document, one should be able to write thew equations of motion of a fixed wing aircraft given the control surfaces.

The dynamics of the Sky-Sailor aircraft has been described as mentioned in the reference article.




### Notation as used in the article
* $\psi$: yaw angle
* $\phi$: roll angle
* $\theta$: pitch angle
* $\sigma$: Density of fluid (Air)
* $C_{L}$: Lift coefficient
* $C_{D}$: Drag coefficient
* $C_{M}$: Moment coefficient
* $\rho$: Density of fluid
* $S$: wing area
* $\nu$: Flight speed (relative to surrounding fluid).
* $C_{L}$: Lift coefficient.
* $C_{D}$: Drag coefficient.
* $C_{M}$: Moment coefficient.


### Objectives
- Shows the control surfaces of this airplane.
- Models the Sky-Sailor airplane which is a fixed-wing aircraft with a v-tail.


### Rotation parameters

The most commom form of representing angles in aerospace is the Tait-Bryan notations. In tait-bryan notations, unlike the Euler notations, each Euler angle triplet specify the rotation around a different Cartesian axis {See Reference 2}. To define the rotations, order of the rotation matters. The complete rotation matrix is given by:


$R(\phi,\theta,psi) =
\begin{bmatrix}cos\psi cos\theta & cos\psi sin\theta sin\phi - sin\psi cos\phi  &cos\psi sin\theta cos\phi+sin\psi sin\phi\\sin\psi cos\theta & sin\psi sin\theta sin\phi + cos\psi cos\phi & sin\psi sin\theta cos\phi - sin\phi cos\psi\\-sin\theta &cos\theta sin\phi& cos\theta cos\phi \end{bmatrix}$

The above rotation matrix denotes the rotation around $\overrightarrow{x}$, $\overrightarrow{y}$ and $\overrightarrow{z}$ by an angle of $\phi$, $\theta$ and $\psi$ respectively.

Similarly, the rate of change of the Trait-Bryan angles is denoted by $(\dot{\phi},\dot{\theta},\dot{\psi})$, then the body angular rate of change is given by (p,q,r) where:
$\begin{bmatrix}p  \\q \\ r \end{bmatrix} = R_{r}\begin{bmatrix}\dot{\phi}  \\\dot{\theta} \\\dot{\psi} \end{bmatrix}$

where $R_{r}$ is equal to:

$R_{r}=
\begin{bmatrix}1 & 0 &-sin\theta\\0& cos\phi & sin\phi cos\theta\\0&-sin\phi& cos\theta cos\phi \end{bmatrix}$


The derivation of the above equality can be found in Reference 3.



### Example of the airplane

The contributions of the forces and moments acting on an airplane are made by three factors:
- Aerodynamic,
- Gravitational, and
- Propulsive.

The control surfaces of the aircraft considered in this article are:
- The two ailerons attached on the wing, and
- The V-tail.


### Dynamics modelling

In the Sky-sailor aircraft, the forces acting on it are:
- the weight (acting at the centre of gravity).
- the thrust of the propeller acting in the x direction which coincides with the axis of the fuselage of the aircraft.
- aerodynamic forces of each part of the airplane.


### Aerodynamic forces of an airfoil

The aerodynamic forces acting on the airfoil are given by:

* $F_{l} = C_{L}\frac{\rho}{2}Sv^{2}$

* $F_{d} = C_{d}\frac{\rho}{2}Sv^{2}$

* $M = C_{m}\frac{\rho}{2}Sv^{2}.chord$

where chord is the line joining the leading and trailing edge of the wing.

### Final model of the airplane is given by the following equations:

* $\ddot{x} = \frac{F_{total,x}}{m}-gsin\theta$

* $\ddot{y} = \frac{F_{total,y}}{m}-gsin\phi cos\theta$

* $\ddot{z} = \frac{F_{total,z}}{m}-gcos\phi cos\theta$

* $\ddot{\phi} = \frac{I_{xx}-I_{zz}}{I_{xx}} \dot{\psi}\dot{\theta} + \frac{M_{total,x}}{I_{xx}}$

* $\ddot{\theta} = \frac{I_{zz}-I_{xx}}{I_{yy}} \dot{\psi}\dot{\phi} + \frac{M_{total,y}}{I_{yy}}$

* $\ddot{\psi} = \frac{I_{xx}-I_{yy}}{I_{zz}} \dot{\theta}\dot{\phi} + \frac{M_{total,z}}{I_{zz}}$


### Comments
This article serves as a good starting point for before exploring the system identification methods as it gives a dynamic model for a v tail fixed wing aircraft.


### References
1. Noth, A., Bouabdallah, S. and Siegwart, R., 2006. Dynamic modeling of fixed-wing uavs. Swiss Federal institute of technology, version, 2.

2. Nelson, R.C., 1998. Flight stability and automatic control (Vol. 2). New York: WCB/McGraw Hill.

3. Danceswithcode.net. 2021. 3D Rotations-Part 1. [online] Available at: <http://danceswithcode.net/engineeringnotes/rotations_in_3d/rotations_in_3d_part1.html> [Accessed 1 March 2021].
