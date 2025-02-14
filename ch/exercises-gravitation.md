(classical-mechanics:exercise:gravitation)=
# Gravitation

```{exercise} Ball falling in a tunnel through a planet
A ball of mass $m$ moves through a tunnel drilled through a planet of radius $R$, mass $M$ and uniform mass distribution. Neglecting the "mas defect" due to the tunnel in the planet,
- provide the expression of the force acting on the ball in the tunnel
- assuming no rotation of the planet, and zero initial velocity of the ball, provide the dynamical equation governing the motion of the ball and integrate it to find the lwa of motion

```

Uniform mass density reads $\rho = \frac{M}{V} = \frac{M}{\frac{4}{3}\pi R^3}$.
Exploiting symmetry, the gravitational field can be a function of the distance $r$ of the center of the planet only, and have radial direction,

$$\vec{g} = - g(r) \hat{r} \ .$$ (eq:g:radial)

Formula {eq}`eq:g:flux:V` of the flux of the gravitational field,

$$  \oint_{\vec{r} \in \partial V} \vec{g}(\vec{r}) \cdot \hat{n}(\vec{r}) = - G \int_{\vec{r} \in V} 4 \pi \rho(\vec{r}) $$

across the surface of a sphere of radius $r$ - that has outward pointing unit normal vector $\hat{n}(\vec{r}) = \hat{r}(\vec{r})$ -, exploting expression {eq}`eq:g:radial` from symmetry, becomes for $r < R$

$$- g(r) 4 \pi r^2 = - G \, 4  \pi \rho \frac{4}{3} \pi r^3 = - 4 \pi G M \frac{r^3}{R^3}$$

and thus

$$g(r) = \frac{GM}{R^3} r \ \qquad \rightarrow \qquad \vec{g}(\vec{r}) = - m \frac{G M}{R^3} r \hat{r} = - m \frac{GM}{R^3} \vec{r} \ .$$

Force acting on the ball of mass $m$ thus reads $\vec{F}(\vec{r}) = m \vec{g}(\vec{r})$. The equation of motion becomes

$$m \ddot{\vec{r}} = \vec{F}(\vec{r}) = - m \frac{G M}{R^3} \vec{r} \ ,$$

a linear second-order ODE with constant coefficients, whose solution provides an harmonic motion with pulsation $\Omega = \sqrt{\frac{GM}{R^3}}$.
The solution of this equation, with initial conditions at rest on the surface of the planet,

$$\begin{cases}
  \vec{r}(0) = \vec{r}_0 = R \hat{r} \\
  \dot{\vec{r}}(0) = \vec{0}
\end{cases}$$

reads

$$\vec{r}(t) = \vec{r}_0 \cos \left( \sqrt{\dfrac{GM}{R^3}} \, t \right) = \hat{r} \, R \cos \left( \sqrt{\dfrac{GM}{R^3}} \, t \right) \ .$$


```{exercise}
Investigate the dynamics of the ball in the previous problem, if the rotational motion of the planet around its axis is considered and if the ball is thrown in the tunnel with non-zero velocity.

- Normal actions of the wall of the tunnel on the ball
- At the end of the tunnel, the ball moves above the planet surface while it's attracted "downwards". When the ball comes back to the planet surface, does it target the tunnel?
```
