(classical-mechanics:lagrange:time)=
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

As it's discusseed in the [section for systems with Lagrangian function with no explicit dependence on time](classical-mechanics:lagrange:time:independent)  **when the Lagrangian function of the system is not an explicit function of time** **todo** *discuss the cases when $\partial_t \mathscr{L} \ne 0$, the equation {eq}`eq:euler-beltrami` is nothing but the **balance equation of mechanical energy**. 

When there is no generalized force, that can't be included in the potential, $Q_k  = 0$, and no explicit dependence of Lagrangian function on time, $\partial_t \mathscr{L} = 0$, the equation {eq}`eq:euler-beltrami` can be recast as an [Euler-Beltrami equation](https://basics2022.github.io/bbooks-math-miscellanea/ch/calculus-variations/intro.html#euler-beltrami-equation),

$$\dot{q}^k \dfrac{\partial \mathscr{L}}{\partial \dot{q}^k} - \mathscr{L} = \overline{E} \quad \text{const.}$$

describing the conservation of mechanical energy w.r.t. an inertial reference frame, in absence of non-conservative forces, as discussed in the .


