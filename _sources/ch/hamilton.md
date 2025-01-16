<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-mechanics:hamilton)=
# Hamiltonian Mechanics

Riformulazione ulteriore della meccanica di Newton, a partire dalla meccanica di Lagrange.
Fornisce le basi per un approccio moderno anche in altre teorie della Fisica. **dots...**

Starting from Lagrange equations derived in [Lagrangian mechanics](classical-mechanics:lagrange),

$$\dfrac{d}{dt}\Big( \frac{\partial \mathscr{L}}{\partial \dot{q}} \Big) - \frac{\partial \mathscr{L}}{\partial q} = Q_q$$

the **generalized moment** is defined as

$$p_k := \frac{\partial \mathscr{L}}{\partial \dot{q}^k} \ ,$$

and the **Hamiltonian function** as

$$\mathscr{H}(q^k(t), p_k(t), t) := p_k \dot{q}^k - \mathscr{L}(\dot{q}^l(q^k, p_k, t), q^l(t), t) \ ,$$

its differential reads

$$\begin{aligned}
d\mathscr{H} & = dq^k \, \frac{\partial \mathscr{H}}{\partial q^k} + dp_k \, \frac{\partial \mathscr{H}}{\partial p_k} + dt \,  \frac{\partial \mathscr{H}}{\partial t} = \\
& = d p_k \, \dot{q}^k + \underbrace{ p_k \, d \dot{q}^k - d \dot{q}^k \, \frac{\partial \mathscr{L}}{\partial \dot{q}^k}}_{=0} - d q^k \, \frac{\partial \mathscr{L}}{\partial q^k} - dt \, \frac{\partial \mathscr{L}}{\partial t}
\end{aligned}$$

and thus it follows

$$\begin{cases}
 \dot{q}^k & = \dfrac{\partial \mathscr{H}}{\partial p_k} \\
 \dfrac{\partial \mathscr{H}}{\partial q^k} & = - \dfrac{\partial \mathscr{L}}{\partial q^k} \\
 \dfrac{\partial \mathscr{H}}{\partial t} & = - \dfrac{\partial\mathscr{L}}{\partial t} \ .
\end{cases}$$

Recasting Lagrange equations as

$$\frac{\partial \mathscr{L}}{\partial q^k} = - Q_{q^k} + \dfrac{d}{dt}\Big( \frac{\partial \mathscr{L}}{\partial \dot{q}^k} \Big) = -Q_{q^k} + \dot{p}_k$$

**Hamilton equations** follow

$$\begin{cases}
 \dot{q}^k & = \dfrac{\partial H}{\partial p_k} \\
 \dot{p}_k & =-\dfrac{\partial H}{\partial q^k} + Q_{q^k} \ .
\end{cases}$$

