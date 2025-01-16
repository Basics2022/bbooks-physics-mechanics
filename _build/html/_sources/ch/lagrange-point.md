<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-mechanics:lagrange:point)=
# Point

**Newton dynamical equations - strong form.** Dynamical equation governing the motion of a point $P$ reads

$$m \dot{\vec{v}}_P = \vec{R}^e \ ,$$

being $m$ the mass of the system, $\vec{v}_P$ the velocity of point $P$, $\vec{a}_P = \dot{\vec{v}}_P$ its acceleration and $\vec{R}^{e}$ the net external force acting on the system..

**Weak form.** Weak form of dynamical equations is derived with scalar multiplication of the strong form by an arbitrary test function $\vec{w}$,

$$\vec{0} = \vec{w} \cdot \left( m \dot{\vec{v}} - \vec{R}^e\right)  \qquad \forall \vec{w}$$ (eq:lagrange:point:weak)

**Lagrange equations.** Lagrange equations are derived from a proper choice of the test function. The position of the point $P$ is written as a function of the generalized coordinates $q^k(t)$ and time $t$

$$\vec{r}_P(t) = \vec{r}(q^k(t),t) \ ,$$

so that its velocity can be written as

$$\vec{v}_P(t) := \frac{d\vec{r}_P}{dt} = \dot{q}^k(t) \underbrace{\frac{\partial \vec{r}}{\partial q^k}}_{\frac{\partial \vec{v}}{\partial \dot{q}^k}}(q^l(t), t) + \frac{\partial \vec{r}}{\partial t}(q^l(t), t) = \vec{v}\left(\dot{q}^k(t), q^k(t), t \right) \ ,$$

from which the relation between partial derivatives

$$\dfrac{\partial \vec{r}}{\partial q^k} = \dfrac{\partial \vec{v}}{\partial \dot{q}^k} \ .$$ (classical-mechanics:lagrange:point:mixed-der)

follows. Choosing the test function $\vec{w}$ as 

$$\vec{w} = \dfrac{\partial \vec{r}}{\partial q^k} = \dfrac{\partial \vec{v}}{\partial \dot{q}^k} \ ,$$

applying the rule of derivative of product, using Schwartz theorem to switch order of derivation, and exploiting relation {eq}`classical-mechanics:lagrange:point:mixed-der` it's possible to recast weak form {eq}`eq:lagrange:point:weak` as

$$\begin{aligned}
\vec{0} & = \frac{\partial \vec{v}}{\partial \dot{q}^k} \cdot \left( m \dot{\vec{v}} - \vec{R}^e \right) = \\
& = \frac{d}{dt} \left( \frac{\partial \vec{v}}{\partial \dot{q}^k} \cdot m \vec{v} \right) - \frac{d}{dt} \frac{\partial \vec{r}}{\partial q^k} \cdot m \vec{v} - \frac{\partial \vec{r}}{\partial q^k} \cdot ( \vec{R}^{e,c} + \vec{R}^{e,nc} ) \\
& = \frac{d}{dt} \left( \frac{\partial \vec{v}}{\partial \dot{q}^k} \cdot m \vec{v} \right) - \frac{\partial \vec{v}}{\partial q^k} \cdot m \vec{v} - \frac{\partial \vec{r}}{\partial q^k} \cdot ( \nabla U + \vec{R}^{e,nc} ) \\
& = \frac{d}{dt} \left( \frac{\partial K}{\partial \dot{q}^k} \right) - \frac{\partial K}{\partial q^k} - \frac{\partial U}{\partial q^k} - \underbrace{\frac{\partial \vec{r}}{\partial q^k} \cdot \vec{R}^{e,nc}}_{=: Q^k} \ . \\
\end{aligned}$$

Introducing the **Lagrangian function**

$$\mathscr{L}(\dot{q}^k(t), q^k(t), t) := K(\dot{q}^k(t), q^k(t), t) + U(q^k(t),t) \ ,$$

and recalling that potential function $U$ is not a function of velocity and thus of time derivatives of the generalized coordinates $\dot{q}^k$, it's possible to recast the dynamical equation as the **Lagrange equations**

$$\frac{d}{dt}\left(\frac{\partial \mathscr{L}}{\partial \dot{q}^k} \right) - \frac{\partial \mathscr{L}}{\partial q^k} = Q^k \ ,$$

being $Q^k$ the **generalized force** not included in the gradient of the potential $\nabla U$ - usually a non conservative contribution -, $Q^k = \dfrac{\partial \vec{r}}{\partial q^k} \cdot \vec{R}^{e,nc}$.





