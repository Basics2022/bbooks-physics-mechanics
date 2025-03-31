(classical-mechanics:lagrange:time:dependent)=
# Lagrangian function with explicit dependence on time

Some problems may have a Lagrangian function with an explicit dependence on time,

$$\mathscr{L}\left(\dot{q}^k(t),q^k(t),t\right) \ ,$$

in some cases like:
1. time-dependent contraints, whose motion is prescribed
2. time-dependent forces that can be included in the potential energy
3. choice of coordinates $q^k(t)$ that gives an explicit dependence on time of the physical coordinates, like positions and orientations of rigid bodies

    $$\vec{r}_P\left(q^k(t),t \right) \quad , \quad \mathbb{R}_P\left( q^{k}(t), t \right)$$

    and leading to an explicit dependence on time of the velocities and angular velocities

    $$\begin{aligned}
      \vec{v}_P\left(\dot{q}^k(t), q^k(t),t \right)  = \dot{q}^i(t) \dfrac{\partial \vec{r}_P}{\partial q^i} \left(q^k(t),t \right) + \dfrac{\partial \vec{r}_P}{\partial t} \left(q^k(t),t \right)  \\
      \vec{\omega}_P\left(\dot{q}^k(t), q^{k}(t), t \right) = \dot{q}^i(t) \dfrac{\partial \vec{\theta}_P}{\partial q^i} \left(q^k(t),t \right) + \dfrac{\partial \vec{\theta}_P}{\partial t}\left(q^k(t),t \right) 
    \end{aligned}$$

    and thus of the kinetic energy.

In general, external actions with net power are required for conditions 1., 2., i.e. for moving constraints or for changing potential fields acting on the system: even if variable constraints or external forcing acting on a system are prescribed and thus add no degree of freedom to the system, they're not free in general but requires external actions and power, as it can be realized looking at the balance equation of mechanica energy.

Condition 3. is usually a result of a choice of coordinates in a non-inertial reference frame, whose motion is not described by the coordinates themselves.


## Energy balance

$$\begin{aligned}
  \dfrac{d E}{d t}
  & = \dfrac{d K}{d t} - \dfrac{d U}{d t} = \\
  & = 2 \dfrac{d K}{d t} - \dfrac{d \mathscr{L}}{dt} = \\
  & = 2 \dfrac{d K}{d t} - \ddot{q}^k \dfrac{\partial \mathscr{L}}{\partial \dot{q}^k} - \dot{q}^k \dfrac{\partial \mathscr{L}}{\partial q^k} - \dfrac{\partial \mathscr{L}}{\partial t} = \\
  & = 2 \dfrac{d K}{d t} - \dfrac{d}{dt} \left( \dot{q}^k \dfrac{\partial \mathscr{L}}{\partial \dot{q}^k} \right) + \dot{q}^k \dfrac{d}{dt}\dfrac{\partial \mathscr{L}}{\partial \dot{q}^k} - \dot{q}^k \dfrac{\partial \mathscr{L}}{\partial q^k} - \dfrac{\partial \mathscr{L}}{\partial t} = \\
  & = \dfrac{d }{d t} \left[ 2 K - \dot{q}^k \dfrac{\partial \mathscr{L}}{\partial \dot{q}^k} \right] + \dot{q}^k \underbrace{ \left[ \dfrac{d}{dt}\dfrac{\partial \mathscr{L}}{\partial \dot{q}^k} - \dfrac{\partial \mathscr{L}}{\partial q^k} \right]}_{= Q_k} - \dfrac{\partial \mathscr{L}}{\partial t} = \\
  & = \dot{q}^k Q_k - \dfrac{\partial \mathscr{L}}{\partial t} + \dfrac{d}{dt} \left[ \dot{q}^k B_k + 2C \right]
\end{aligned}$$

## Properties of kinetic energy and potential

The kinetic energy has a general expression

$$K = \frac{1}{2} \dot{q}^i \dot{q}^j A_{ij}\left(q^k(t),t\right) + \dot{q}^i B_{i}\left(q^k(t),t\right) + C\left(q^k(t),t\right)$$

$$\dot{q}^k \dfrac{\partial K}{\partial \dot{q}^k} = \dot{q}^k \left( A_{kj} \dot{q}^j + B_k \right)$$

$$\begin{aligned}
  2K - \dot{q}^k \dfrac{\partial K}{\partial \dot{q}^k}
  & = \dot{q}^k A_{kj} \dot{q}^j + 2 \dot{q}^k B_k + 2 C - \left[ \dot{q}^k \left( A_{kj} \dot{q}^j + B_k \right) \right] = \\
  & = \dot{q}^k B_k + 2 C
\end{aligned}$$




```{prf:example}

```

