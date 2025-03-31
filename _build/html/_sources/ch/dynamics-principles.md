(classical-mechanics:dynamics:principles)=
# Principles of Newtonian Mechanics

Newton's principle of dynamics are first established for **closed systems**, i.e. systems that don't exchange mass with the external environment and thus have constant mass.
Balance equations for mass, momentum, angular momentum and other quantities for arbitary systems (closed or open) are derived in [Continuum Mechanics](https://basics2022.github.io/bbooks-physics-continuum-mechanics/intro.html):[Governing Equations](https://basics2022.github.io/bbooks-physics-continuum-mechanics/ch/continuum/governing-equations.html), exploiting [Reynolds' transport theorem](https://basics2022.github.io/bbooks-math-miscellanea/ch/tensor-algebra-calculus/time-derivative-of-integrals.html#volume-density).[^reynolds-transport]

[^reynolds-transport]: Reynolds's transport theorem provides the rules for time derivatives of integrals on arbitrary domains in Euclidean space, that allows to change representation to and from closed systems (material volume, a geometric volume moving with the physical system) and open systems (usually control volumes of some regions of the system that can exchage mass with the exterrnal environment).

**Mass conservation.** In the regime of classical mechanics, Lavoisier principle states that the mass of a closed system is constant. Roughly speaking "nothing is created nothing is destroyed".

**First Principle of Dynamics (Newton's First Law): inertia and Galileian invariance.** A body (more precisely, the center of mass of a body) on which no net force acts remains in its state of rest or uniform rectilinear motion relative to an [inertial reference frame](classical-mehcanics:dynamics:principles:inertial-ref-frame).

<!--
**todo** discuss the role/definition of **inertial reference frames** in classical mechanics and **Galileian invariance** (equations of motions are invariant under Galileian transformations)
-->

**Second Principle of Dynamics (Newton's Second Law): momentum balance.** Relative to an [inertial reference frame](classical-mehcanics:dynamics:principles:inertial-ref-frame), the change in momentum of a system is equal to the impulse of *true external forces* (see {prf:ref}`def:true-forces`) acting on it,

$$\Delta \vec{Q} = \vec{I}^e \ .$$

In the case of smooth motion, where the momentum can be represented as a continuous and differentiable function of time, the second principle of dynamics can be expressed in differential form,

$$\dot{\vec{Q}} = \vec{R}^e \ ,$$

where the resultant of the external forces, $\vec{R}^e = \frac{d \vec{I}^e}{dt}$, is the time derivative of the impulse.

**Third Principle of Dynamics (Newton's Third Law): action-reaction.** If a system $i$ exerts a force $\vec{F}_{ji}$ on a system $j$, then system $j$ exerts an "equal and opposite" force $\vec{F}_{ij}$ on system $i$, with equal magnitude and opposite direction,

$$\vec{F}_{ij} = - \vec{F}_{ji} \ .$$


(classical-mehcanics:dynamics:principles:inertial-ref-frame)=
## Inertial reference frame

Force sensors in an inertial reference frame measure only *true forces*, as defined in {prf:ref}`def:true-forces`.

<!--
But what's a "true force"? In classical mechanics, true forces are due to gravitational interactions and electromagnetic interactions. Electromangetic interactions between charged systems; electromangetic interactions between electrically neutral systems as contact forces...
-->

Here the effect of non-inertial reference frame in the description of the motion is shown on the **dynamics of a point system**, using $2^{nd}$ principle for the description of the dynamics for an inertial observer, and the rules for the [relative kinematics of a point](classical-mechanics:kinematics:relative:points).

Here, an inertial reference frame is referred as 0, while the generic reference frame is referred as 1. The equation of motion of a point system $P$ w.r.t. the inertial reference frame is governed by Newton's second principle,

$$m \vec{a}^{0}_{P/O_0} = \vec{F} \ ,$$

being $\vec{a}^0_{P/O_0}$ the acceleration of point $P$ w.r.t. the origin $O_0$ of the inertial reference frame $0$, as seen by the same reference frame $0$ (the meaning of the apex).
From relative kinematics, {eq}`eq:relative:point:acc`

$$\begin{aligned}
  m \vec{a}^{1}_{P/O_1} & =  \vec{F}  + \\
   & \quad - m \left[ \vec{a}^0_{O_1/O_0} + \vec{\alpha}_{1/0} \times (P - O_1) + 2 \vec{\omega}_{1/0} \times \vec{v}^1_{P/O_1} + \vec{\omega}_{1/0} \times [ \, \vec{\omega}_{1/0} \times (P - O_1) \right]
\end{aligned}$$

In order for the reference frame $1$ to agree with the acceleration of any point $P$ with the inertial reference frame $0$, the content of the square brackets must vanish, and thus:
- $\vec{a}^0_{O_1/O_0} = \vec{0}$, i.e. the acceleration of the origin of the reference frame $O_1$ w.r.t. to the reference frame $0$ must be zero
- $\vec{\omega}_{1/0} = \vec{0}$, and thus implying $\vec{\alpha}_{1/0}= \vec{0}$, i.e. the angular velocity of the reference frame $1$ w.r.t. the reference frame $0$ are zero.

Thus, reference frame $1$ agrees with the measurements of accelerations and forces of an inertial reference frame if:
- its origin $O_1$ is in uniform motion w.r.t. $O_0$
- its orientation $\mathbb{R}^{1/0}$ is constant in time, so that angular velocity and acceleration are identically zero.

```{prf:definition} Class of inertial reference frames
If these conditions hold, it's not possible to find which reference frame is "more absolute" than the other, but all the reference frames with constant relative orientation and origin in uniform relative motion are inertial reference frames, w.r.t. which the governing equations have the same expression.
```

