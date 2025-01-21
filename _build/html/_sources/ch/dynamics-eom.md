(classical-mechanics:dynamics:eom)=
# Equations of Motion

Starting from the [principles of Newtonian mechanics](classical-mechanics:dynamics:principles), it is possible to derive the dynamical equations governing the motion of mechanical systems. These equations governs the change of dynamical quantities, **momentum**, **angular momentum**, **kinetic energy**, linking them to (external) **forces**, (external) **moments** and (total) **power**. Under certain conditions, and only in these cases, the [cardinal equations](classical-mechanics:dynamics:eom:eom) of dynamics become[principles of conservation of dynamic quantities](classical-mechanics:dynamics:eom:conservation): by observing the expressions of the cardinal equations, it is easy to infer that the condition to obtain a conservation principle is the vanishing of all terms except for the time derivative of the conserved quantity.

<!--
The general form of these equations is easily expressed in terms of the dynamical quantities discussed in the inertia section,

$$\begin{aligned}
 \dfrac{d \vec{Q}       }{dt} & = \vec{R}^e                               & \qquad \text{(momentum balance equation)} \\
 \dfrac{d \vec{\Gamma}_H}{dt} & = -\vec{r}_H \times \vec{Q} + \vec{M}^e_H & \qquad \text{(angular momentum balance equation)} \\
 \dfrac{d      K        }{dt} & = P^{tot}                                 & \qquad \text{(kinetic energy balance equation)} \\
\end{aligned}$$

for every mechanical (closed) system. These equations will be derived for different systems in the following sections: point mass, system of particles, rigid body.

Using the concepts of momentum, angular momentum, and the kinetic energy of a system, we can write the 3 cardinal equations of dynamics in a form valid for **every closed system**. Under certain conditions, and only in these cases, the cardinal equations of dynamics represent principles of conservation of dynamic quantities: by observing the expressions of the cardinal equations, it is easy to infer that the condition to obtain a conservation principle is the vanishing of all terms except for the time derivative of the conserved quantity.
-->

(classical-mechanics:dynamics:eom:eom)=
## Cardinal Equations

The general form of these equations is easily expressed in terms of the dynamical quantities discussed in the section about [inertia](classical-mechanics). Cardinal equations, or equations of motion, are collected here in their most general form for closed systems, and derived in the following sectinos for different systems: [point mass](classical-mechanics:dynamics:eom:point), [systems of point masses](classical-mechanics:dynamics:eom:points), [rigid body](classical-mechanics:dynamics:eom:rigid),...

**Momentum Balance.** The time derivative of the momentum is equal to the resultant of the external forces,

$$\dot{\vec{Q}} = \vec{R}^e \ .$$ (principle:q)

**Angular Momentum Balance with respect to a point $H$.** The time derivative of the angular momentum with respect to a point $H$, minus the "transport term," is equal to the resultant of the external moments with respect to the point $H$,

$$\dot{\vec{L}}_H + \dot{\vec{x}}_H \times \vec{Q} = \vec{M}_H^e \ .$$ (principle:l)

**Kinetic Energy Balance.** The time derivative of the kinetic energy is equal to the total power acting on the system, which is the sum of the power of the external actions and the power of the internal actions within the system,

$$\dot{K} = P^{tot} = P^e + P^i$$ (principle:k)

(classical-mechanics:dynamics:eom:conservation)=
## Conservation Principles
Under certain condiitons, equations of motion become principles of conservation of dynamical quantities. These conditions are easily derived by inspection of the equations of motion, nullyfing the causes of change of the dynamical quantities. Beside the conservation of momentum, angular momentum and kinetic energy, a **principle of conservation of mechanical energy** arises when actions acting on the system are [conservative](classical-mechanics:actions:conservative), so that its power can be written as a time derivative of a potential energy.

**Conservation of Momentum in the presence of zero net external forces.** If the resultant of the external forces is zero, $\vec{R}^e = \vec{0}$, from the momentum balance, we immediately obtain

$$\dot{\vec{Q}} = \vec{0} \qquad \rightarrow \qquad \vec{Q} = \bar{\vec{Q}} = \text{const.}$$

**Conservation of Angular Momentum in the presence of zero net external moments.** If the choice of the point $H$ nullifies the transport term, $\dot{\vec{r}}_H \times \vec{Q} = \vec{0}$, and if the resultant of the external moments is zero, $\vec{M}^e_H = \vec{0}$, from the angular momentum balance, we immediately obtain

$$\dot{\vec{L}}_H = \vec{0} \qquad \rightarrow \qquad \vec{L}_H = \bar{\vec{L}}_H = \text{const.}$$

**Conservation of Kinetic Energy in the presence of zero total power.** If the total power of the actions on the system is zero, $P^{tot} = 0$, from the kinetic energy balance, we immediately obtain

$$\dot{K} = 0 \qquad \rightarrow \qquad K = \bar{K} = \text{const.}$$

**Conservation of Mechanical Energy in the absence of non-conservative forces.** In addition to the three conservation principles directly derived from the cardinal equations, we add the principle of the conservation of mechanical energy, which is the sum of the system's kinetic and potential energy,

$$E^{mech} = K + V \ ,$$

in the absence of non-conservative actions. If there are no non-conservative forces, the power of the actions on the system can be written as the negative of the time derivative of the system's potential energy,

$$P^{tot} = -\dot{V}$$

From the kinetic energy balance, we get

$$\dot{K} = - \dot{V} \qquad \rightarrow \qquad \dfrac{d}{dt}(K+V) = 0 \qquad \rightarrow \qquad \dot{E}^{mech} = 0 \qquad \rightarrow \qquad E^{mech} = \bar{E}^{mech} = \text{const.}$$

