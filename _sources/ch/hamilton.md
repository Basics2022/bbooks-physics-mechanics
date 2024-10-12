```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-mechanics:hamilton)=
# Meccanica analitica: formulazione di Hamilton

Riformulazione ulteriore della meccanica di Newton, a partire dalla meccanica di Lagrange.
Fornisce le basi per un approccio moderno anche in altre teorie della Fisica. **dots...**

Partendo dalle equazioni di Lagrange,

$$\dfrac{d}{dt}\Big( \frac{\partial \mathscr{L}}{\partial \dot{q}} \Big) - \frac{\partial \mathscr{L}}{\partial q} = Q_q$$

si definisce il **momento generalizzato** (dall'inglese, momentum = quantità di moto)

$$p := \frac{\partial \mathscr{L}}{\partial \dot{q}} \ ,$$

e la funzione **hamiltoniana**

$$H(q(t), p(t), t) := p_k \dot{q}^k - \mathscr{L} \ .$$

$$\begin{aligned}
dH & = dq^k \, \frac{\partial H}{\partial q^k} + dp_k \, \frac{\partial H}{\partial p_k} + dt \,  \frac{\partial H}{\partial t} = \\
& = d p_k \, \dot{q}^k + \underbrace{ p_k \, d \dot{q}^k - d \dot{q}^k \, \frac{\partial \mathscr{L}}{\partial \dot{q}^k}}_{=0} - d q^k \, \frac{\partial \mathscr{L}}{\partial q^k} - dt \, \frac{\partial \mathscr{L}}{\partial t}
\end{aligned}$$

e quindi segue

$$\begin{cases}
 \dot{q}^k & = \dfrac{\partial H}{\partial p_k} \\
 \dfrac{\partial \mathscr{H}}{\partial q^k} & = - \dfrac{\partial \mathscr{L}}{\partial q^k} \\
 \dfrac{\partial H}{\partial t} & = - \dfrac{\partial\mathscr{L}}{\partial t} \ .
\end{cases}$$

Riscrivendo le equazioni di Lagrange come

$$\frac{\partial \mathscr{L}}{\partial q^k} = - Q_{q^k} + \dfrac{d}{dt}\Big( \frac{\partial \mathscr{L}}{\partial \dot{q}^k} \Big) = -Q_{q^k} + \dot{p}_k$$

si ottengono le **equazioni di Hamilton**

$$\begin{cases}
 \dot{q}^k & = \dfrac{\partial H}{\partial p_k} \\
 \dot{p}_k & =-\dfrac{\partial H}{\partial q^k} + Q_{q^k} \\
\end{cases}$$

