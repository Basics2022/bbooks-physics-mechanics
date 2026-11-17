(classical-mechanics:dynamics:equivalence-principle)=
# Equivalence principle in classical mechanics

(classical-mechanics:dynamics:equivalence-principle:uniform)=
## Uniform gravitational field

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

(classical-mechanics:dynamics:equivalence-principle:non-uniform)=
## Non-uniform gravitational field

Let the observer be subject to the local gravitational field as well. If it's not constrained, thus it's subject to an acceleration $\mathbf{a}_{Q/O}^0 = \mathbf{g}\left( Q \right)$ w.r.t. the inertial reference frames.

Let's the reference frame have no relative rotation so that $\boldsymbol\omega_{1/0} = \mathbf{0}$. Then the equations of motion governing the motion of $P$ and $Q$ only subject to the gravitational field $\mathbf{g}$ w.r.t. the inertial reference frames are

$$\begin{aligned}
  m_P \mathbf{a}^0_{P/O} & = m_P \mathbf{g}\left( P \right) \\
  m_Q \mathbf{a}^0_{Q/O} & = m_Q \mathbf{g}\left( Q \right) \ .
\end{aligned}$$

Thus the relative acceleration of $P$ w.r.t. $Q$ as seen by the observer $Q$ is

$$\begin{aligned}
  \mathbf{a}^1_{P/Q} 
  & = \mathbf{a}^0_{P/O} - \mathbf{a}^0_{Q/O} = \\
  & = \mathbf{g}(P) - \mathbf{g}(Q) = \\
  & = \left( P - Q \right) \cdot \nabla \mathbf{g}(Q) + o(|P-Q|) \ ,
\end{aligned}$$

**Cartesian coordinates.** Exploiting a set of Cartesian coordinates $\{ \xi^k \}$ that are stationary w.r.t. the observer $Q$, the origin identified by $\xi^k = 0$, then

$$\begin{aligned}
  \mathbf{a}^1_{P/Q} & = \ddot{\xi}^k \hat{\mathbf{e}}_k \\
  \mathbf{r}_{P/Q} \cdot \nabla \mathbf{g} & = \xi^k_P \hat{\mathbf{e}}_k \cdot \hat{\mathbf{e}}^j \partial_{\xi^j} \left( g^l \hat{\mathbf{e}}_l \right) = \xi^k_P(t) \, \partial_{\xi^k} g^l \hat{\mathbf{e}}_l \ ,
\end{aligned}$$

so that the $k^{\rm th}$ component of the equation reads

$$\ddot{\xi}^k_P = \xi^\ell_P \, \partial_{\xi^\ell} \left. g^k\right|_{\xi=0} \ ,$$

**General coordinates.** Exploiting a set of coordinates $\{ \xi^k \}$ that are stationary w.r.t. the observer $Q$, then a point $P$ in space w.r.t. $Q$ can be identified by the values of its coordinates as $ (P-Q) = (P-Q)(\xi^k_P(t))$. It's velocity reads

$$\mathbf{u}^1_{P/Q} = \dfrac{d}{dt} ( P - Q ) = \dot{\xi}^k_P(t) \, \partial_{\xi^k} (P-Q) = \dot{\xi}^k_P(t) \, \mathbf{b}_k \ .$$

The acceleration becomes

$$\mathbf{a}^1_{P/Q} = \left\{ \ddot{\xi}^k_P + \Gamma^{k}_{ij} \dot{\xi}^i \dot{\xi}^j \right\} \mathbf{b}_k$$

The directional derivative for small displacement $P-Q =$  $X(\xi_P^k(t)) - X(\xi_Q^k(t))\sim$  $d \xi^k_P \partial_{\xi^k} X =$  $d \xi^k_P \mathbf{b}_k$,

$$\begin{aligned}
  d \mathbf{r}_{P/Q} \cdot \nabla \mathbf{g}
  & = d \xi^k_P \mathbf{b}_k \cdot \mathbf{b}^j \partial_j \mathbf{g} = \\
  & = d \xi^k_P \partial_k \left( g^i \mathbf{b}_i \right) = \\
  & = \left\{ d \xi^k_P \partial_k g^i + d \xi^k_P \Gamma^i_{jk} g^j \right\} \mathbf{b}_i
\end{aligned}$$

so that the $k^{\rm th}$ component of the linear approximation of the equation of motion is

$$\ddot{\xi}^k_P + \Gamma^{k}_{ij} \dot{\xi}^i \dot{\xi}^j = \xi^k_P \left.\left( \partial_k g^i + \Gamma^{i}_{jk} g^j \right)\right|_{\xi=0} \ .$$




