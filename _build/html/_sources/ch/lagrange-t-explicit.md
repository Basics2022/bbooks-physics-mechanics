(classical-mechanics:lagrange:time:dependent)=
# Lagrangian functions and time dependence

Some problems may have a Lagrangian function with an explicit dependence on time,

$$\mathscr{L}(\dot{q}^k(t),q^k(t),t) \ .$$

Using the general form {eq}`eq:lagrange-eq` of Lagrange equations, the time derivative of the Lagrange function reads

$$\begin{aligned}
\dfrac{d \mathscr{L}}{dt}
 & =
  \ddot{q}^k \dfrac{\partial \mathscr{L}}{\partial \dot{q}^k}
 + \dot{q}^k \dfrac{\partial \mathscr{L}}{\partial       q^k}
 + \dfrac{\partial \mathscr{L}}{\partial  t} = && \qquad \text{(IxP)} \\
 & = \dfrac{d}{dt} \left( \dot{q}^k \dfrac{\partial \mathscr{L}}{\partial \dot{q}^k} \right) - \dot{q}^k \dfrac{d}{dt} \dfrac{\partial \mathscr{L}}{\partial \dot{q}^k}
 + \dot{q}^k \dfrac{\partial \mathscr{L}}{\partial       q^k}
 + \dfrac{\partial \mathscr{L}}{\partial  t} = && \qquad \text{(Lagrange eq.)} \\
 & = \dfrac{d}{dt} \left( \dot{q}^k \dfrac{\partial \mathscr{L}}{\partial \dot{q}^k} \right) - \dot{q}^k Q_k
 + \dfrac{\partial \mathscr{L}}{\partial  t} \ .
\end{aligned}$$

This latter relation can be recast as

$$\dfrac{d}{dt} \left[ \dot{q}^k \dfrac{\partial \mathscr{L}}{\partial \dot{q}^k} - \mathscr{L} \right] = \dot{q}^k Q_k - \dfrac{\partial \mathscr{L}}{\partial t} \ ,$$ (eq:euler-beltrami)

i.e. time derivative of a physical quantity equals the power of actions not included in the potential, $\dot{q}^k Q_k$ and a contribution of partial derivative of the Lagrangian function, $\partial_t \mathscr{L}$.

As it's discusseed below, **when the Lagrangian function of the system is not an explicit function of time** **todo** *discuss the cases when $\partial_t \mathscr{L} \ne 0$, the equation {eq}`eq:euler-beltrami` is nothing but the balance equation of mechanical energy. 

(classical-mechanics:lagrange:time:independent)=
## Lagrangian function with no explicit dependence on time
Let's analyse first some properties of systems, whose Lagrangian function are not an explicit function of time,

$$\mathscr{L}(\dot{q}^k(t), q^k(t)) = K(\dot{q}^k(t), q^k(t)) + U(q^k(t)) \ ,$$

and then go back to the most general case. 

As the Lagrange equation is not an explicit function of time, [Euler-Beltrami equations](https://basics2022.github.io/bbooks-math-miscellanea/ch/calculus-variations/intro.html#euler-beltrami-equation) hold,

$$\mathscr{L} - \dot{q}^k \dfrac{\partial \mathscr{L}}{\partial \dot{q}^k} = C \quad \text{const.}$$

Since the Lagrangian doesn't expliclty depend on time, and potential is not a function of time, relation {eq}`eq:lagrange:time:ind:dqdK_dq` gives $\dfrac{\partial \mathscr{L}}{\partial \dot{q}^k} = 2 T$, and thus

$$C = \mathscr{L} - \dot{q}^k \dfrac{\partial \mathscr{L}}{\partial \dot{q}^k} = T + U - 2 T = - T + U =: - E^{mec}$$


### Properties of kinetic energy and potential
This section collects some properties of the kinetic energy and potential of systems, where physical coordinates of the system are written as a function of generalized coordinates only, $q^k(t)$. As an example, coordinates of point masses, material points of rigid bodies and the rotation tensor representing their orientation in space can be written as

$$\vec{r}_P\left(q^k(t)\right) \quad , \quad \mathbb{R} \left( q^k(t) \right) \ ,$$

so that velocities and angular velocities become

$$\begin{aligned}
  \vec{v}_P\left(\dot{q}^k(t), q^k(t)\right) & = \dfrac{d \vec{r}_P}{dt} = \dot{q}^k \dfrac{\partial \vec{r}}{\partial q^k}\left(q^k(t)\right) \\ 
  \vec{\omega}_{\times}\left(\dot{q}^k(t), q^k(t)\right) & = \dfrac{d \mathbb{R}}{d t} \cdot \mathbb{R}^T = \dot{q}^k(t) \, \dfrac{\partial \mathbb{R}}{\partial q^k} \cdot \mathbb{R}^T = \dot{q}^k(t) \, \dfrac{\partial \vec{\theta}_{\times}}{\partial q^k}\left(q^k(t)\right) \ ,
\end{aligned}$$

As the kinetic energy of a mechanical system is a quadratic function of velocity and angular velocity of its sub-systems, the kinetice energy can be written as

$$K\left( \dot{q}^k(t), q^k(t) \right) = \frac{1}{2} A_{ij}\left(q^k(t)\right) \, \dot{q}^i(t) \, \dot{q}^j(t) \ .$$

Since $A_{ij}$ is symmetric w.r.t. the swap of indices (or it can be written in a symmetric form), partial derivative of the kinetic energy w.r.t. $\dot{q}^l$ reads

$$\dfrac{\partial K}{\partial \dot{q}^l} = A_{lj} \dot{q}^j \ ,$$

and 

$$\dot{q}^l \dfrac{\partial K}{\partial \dot{q}^l} = \dot{q}^l A_{lj} \dot{q}^j = 2 T \ .$$ (eq:lagrange:time:ind:dqdK_dq)


```{dropdown} Proofs

$$\begin{aligned}
  \dfrac{\partial K}{\partial \dot{q}^l} 
    = \dfrac{\partial }{\partial \dot{q}^l} \left[ \frac{1}{2} A_{ij} \dot{q}^i \dot{q}^j \right] 
    = \frac{1}{2} A_{ij} \bigg[ \underbrace{ \dfrac{\partial \dot{q}^i}{\partial \dot{q}^l} }_{\delta^i_l} \dot{q}^j + \dot{q}^i \underbrace{ \dfrac{\partial \dot{q}^j}{\partial \dot{q}^l}}_{\delta^j_l} \bigg]  
    = \frac{1}{2} \left[ A_{lj} \dot{q}^j + A_{il} \dot{q}^i \right]
    = A_{lj} \dot{q}^j
\end{aligned}$$


```


(classical-mechanics:lagrange:time:dependent)=
## Lagrangian function with explicit dependence on time
