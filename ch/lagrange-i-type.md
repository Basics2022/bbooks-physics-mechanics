(classical-mechanics:lagrange:ii-type)=
# Lagrange Equations of the First Kind

Explicitly making appear constraint forces, due to constraints

$$\begin{aligned}
 & \dfrac{d}{dt}\frac{\partial L}{\partial \dot{q}^k} - \frac{\partial L}{\partial q^k} = Q^e_k + Q^c_k \\
 & g^j \left(q^k(t), t\right) = 0
\end{aligned}$$

```{prf:example}
Pendulum with point mass $m$ and length $\ell$, with hinge position $x_H(t)$ w.r.t. an inertial reference frame, in a gravitational field $\vec{g} = g \hat{y}$

Position, and velocity of the point mass in $P$

$$\begin{aligned}
  & \vec{r}_P(t) = x_P(t) \, \hat{x} + y_P(t) \, \hat{y} = \left( x_H(t) + \ell \sin \theta(t) \right) \, \hat{x} + \ell \cos \theta(t) \, \hat{y} \\
  & \vec{v}_P(t) = \dot{x}_P(t) \, \hat{x} + \dot{y}_P(t) \, \hat{y} = (\dot{x}_H + \ell \dot{\theta}(t) \cos \theta(t)) \, \hat{x} - \ell \dot{\theta}(t) \sin \theta(t) \, \hat{y} \\
\end{aligned}$$

**Approach 1. LE of the II Kind.** LE of the II Kind provides free equations of motion. The system has one degree of freedom. Here the angle $\theta(t)$ is chosen as the generalized dof. Kinetic energy $K$ and potential function $U$,

$$\begin{aligned}
  K & = \frac{1}{2} m \left( \dot{x}_H^2 + 2 \ell \dot{x}_H \dot \theta \cos \theta + \ell^2 \dot{\theta}^2  \right) \\
  U & = m g \ell \cos \theta \\
\end{aligned}$$

and Lagrange equation of the II-kind provides a free equation of motion, that immediately follows from direct evaluation of the required derivatives

$$\begin{aligned}
  \dfrac{d}{dt}\frac{\partial L}{\partial \dot{\theta}}
  & = \dfrac{d}{dt} \left[ m (\ell \dot{x}_H \cos \theta + \ell^2 \dot{\theta} ) \right]
    = m \ell \ddot{x}_H \cos \theta - m \ell \dot{x}_H \dot{\theta} \sin \theta + m \ell^2 \ddot{\theta} \\
  \frac{\partial L}{\partial \theta}
  & = - m \ell \dot{x}_H \dot{\theta} \sin \theta - m g \ell \sin \theta
\end{aligned}$$

Thus, Lagrange equation reads

$$
  0 = \dfrac{d}{d t} \frac{\partial L}{\partial \dot{\theta}} - \frac{\partial L}{\partial \theta}
    = m \ell^2 \ddot{\theta} + m g \ell \sin \theta - m \ell \ddot{x}_H (t) \cos \theta
$$ 

**Approach 2. LE of the I Kind.**

```

