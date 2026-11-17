(classical-mechanics:dynamics:equivalence-principle)=
# Equivalence principle in classical mechanics

Without going deep into the details of the most general case, it's possible to state that

> It's not possible tell if one is at rest in a uniform gravitational field, or uniformly accelerating in empty space

In this section only a **uniform gravitational field** is considered. This condition can be meant to be an approximation of more general cases, but it could be a good approximation if the size of the region of space of interest is not large enough to appreciated gradients of the gravitational field. In this **local** approximation, tidal effects and spatial variations of the gravitational field are neglected (and the approximation is a good model if these effects are negligible).

Indeed, focusing on a point mass $P$ with mass $m$, the dynamic equation of motion w.r.t. an inertial frame $0$ is provided by Newton's second principle,

$$m \mathbf{a}^0_{P/O} = \mathbf{F}^0_P \ ,$$

with $\mathbf{a}^0_{P/O}$ the acceleration of point $P$ w.r.t. $O$, as seen in the $0$ ref frame, i.e. as seen by $O$, and $\mathbf{F}^0_P$ the total force acting on the point $P$.

[Relative kinematics for a point](classical-mechanics:kinematics:relative:points) gives the relation between the point of view of the observer at the origin $O$ of the inertial reference frame, and the point of view of the observer at the origin $Q$ of a general reference frame

$$\begin{aligned}
  \mathbf{v}^0_{P/O} & = \mathbf{v}^0_{Q/O} + \mathbf{v}^1_{P/Q} + \boldsymbol\omega_{1/0} \times \mathbf{r}_{QP} \\
  \mathbf{a}^0_{P/O} & = \mathbf{a}^0_{Q/O} + \mathbf{a}^1_{P/Q} + \boldsymbol\alpha_{1/0} \times \mathbf{r}_{QP} + 2 \boldsymbol\omega_{1/0} \times \mathbf{v}_{P/Q}^1 + \boldsymbol\omega_{1/0} \times \boldsymbol\omega_{1/0} \times \mathbf{r}_{QP}
\end{aligned}$$

**Non-rotating (relative rotation) reference frames.** Let the relative angular velocity and the angular acceleration of the two reference frames be identically zero, $\boldsymbol\omega_{1/0} = \mathbf{0}$, and $\boldsymbol\alpha_{1/0} = \mathbf{0}$. Then, the dynamical equation describing the motion as seen by $Q$ is

$$m \mathbf{a}^1_{P/Q} = \mathbf{F}^0_P - m \mathbf{a}^0_{Q/O} \ .$$

**Example 1.** Let $P$ be at rest w.r.t. $Q$, implying $\mathbf{a}^1_{P/Q} = \mathbf{0}$, and the total force $\mathbf{F}^0_P$ be the sum of a gravitational action $m \mathbf{g}$ and a force of a measurement instrument $\mathbf{R}$ - or any kind of reaction force that's required to prescribe the desired motion. The equation of motion becomes

$$0 = m \mathbf{g} + \mathbf{R} - m \mathbf{a}^0_{Q/O} \ ,$$

so that the reaction/measurement of the instrument reads

$$\mathbf{R} = m \left( \mathbf{a}^0_{Q/O} - \mathbf{g} \right) \ .$$

Without any additional information about the relative motion of the reference frames, i.e. no information about $\mathbf{a}_{Q/O}^0$, the measuremenent of the instrument can't discern from the conditions $( \mathbf{a}^0_{Q/O}, \mathbf{g} ) = \left( \tfrac{\mathbf{R}}{m}, 0 \right)$ and $( \mathbf{a}^0_{Q/O}, \mathbf{g} ) = \left( 0, - \tfrac{\mathbf{R}}{m} \right)$, or any other condition of the form  $( \mathbf{a}^0_{Q/O}, \mathbf{g} ) = \left( a \tfrac{\mathbf{R}}{m}, - ( 1 - a ) \tfrac{\mathbf{R}}{m} \right)$.

**Example 2 - Empty space or free fall in gravitational field?.** Let the measurement of the instrument be $\mathbf{R} = \mathbf{0}$ - same condition as unconstrained system, so there's no reaction. Thus, $\mathbf{a}^0_{Q/O} = \mathbf{g}$, i.e. the observer is accelerating w.r.t. the inertial reference frames with uniform acceleration $\mathbf{g}$. Without any information about the gravitational field $\mathbf{g}$ or the acceleration $\mathbf{a}^0_{Q/O}$ their value is undeterminate: it's not possible to tell if you're in uniform motion in an empty space ($\mathbf{g} = \mathbf{a}^0_{Q/O}$), or accelerating w.r.t. inertial reference frames with the uniform acceleration of the gravitational field with arbitrary value $\mathbf{g}$.


