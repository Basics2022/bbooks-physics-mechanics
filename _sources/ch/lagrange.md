```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-mechanics:lagrange)=
# Lagrangian Mechanics

Classical mechanics can be re-formulated starting from variational principles, usually referred as **analytical mechanics**. Under some assumptions, that will be discussed during the derivation, analytical mechanics is equivalent to Newton mechanics.

Here, the equivalence of analytical mechanics and Newton mechanics is stressed, by means of the derivation of the principle of analytical mechanics starting from the equations of motions derived in Newtonian mechanics, relying on the conservation of mass and the three principles of Newton mechanics. The process is shown in the following sections for [point systems](classical-mechanics:lagrange:point), [systems of points](classical-mechanics:lagrange:points), [extended rigid bodies](classical-mechanics:lagrange:rigid) and follows these steps:
- **strong form of equations.** Starting point is the dynamical equations of Newton mechanics, here also referred as the strong form of equations
- **weak form of equations.** Strong form are recast in weak form, also referred as **D'Alembert approach** or **virtual work formulation**, multiplying strong form of equations for arbitrary test functions
- **Lagrange equations.** A proper choice of test functions as a function of generalized coordinates, and some manipulation, leads to Lagrange equations. While the choice of test functions depends on the nature of the system, their expression always reads

   $$\dfrac{d}{dt}\left( \frac{\partial \mathscr{L}}{\partial \dot{q}} \right) - \frac{\partial \mathscr{L}}{\partial q} = Q_q$$

   being $\mathscr{L} = K + U$ the Lagrangian function of the system, defined as the sum of the kinetic energy $K$ and the potential function $U = - V$, being $V$ the potential energy - s.t. the conservative vector field reads $\vec{F} = - \nabla V$, and $Q_q$ the generalized force.


Riformulazione della meccanica di Newton:
- **forma debole** delle equazioni: approccio di D'Alembert, lavori virtuali
- **equazioni di Lagrange**

con $\mathscr{L}(\dot{q}(t), q(t), t) = K(\dot{q}(t), q(t), t) + U(q(t), t)$.

- **principi di stazionarietà del funzionale azione $S$**

Nel caso non ci siano azioni non conservative, $Q_q = 0$, è possibile interpretare le equazioni di Lagrange come risultato di un principio di stazionarietà. Chiamando $\delta q(t)$ la variazione della funzion $q(t)$, moltiplicandola per le equazioni di Lagrange e integrando in tempo per $t \in [t_0, t_1]$,

$$\begin{aligned}
  0 & = \int_{t_0}^{t_1} \delta q (t) \left[ \dfrac{d}{dt}\left( \frac{\partial \mathscr{L}}{\partial \dot{q}} \right) - \frac{\partial \mathscr{L}}{\partial q} \right] \, dt = \\
    & = \delta q(t) \left.\left( \frac{\partial \mathscr{L}}{\partial \dot{q}} \right)\right|_{t_0}^{t_1} - \int_{t_0}^{t_1} \left[ \delta \dot{q}(t) \, \frac{\partial \mathscr{L}}{\partial \dot{q}} + \delta q(t) \, \frac{\partial \mathscr{L}}{\partial q} \right] \, dt \ . \\
\end{aligned}$$

Imponendo che la variazione $\delta q(t)$ sia nulla per $t_0$ e $t_1$, il primo termine si annulla, e si può dimostrare che

$$\begin{aligned}
    0 & = - \int_{t_0}^{t_1} \left[ \delta \dot{q}(t) \, \frac{\partial \mathscr{L}}{\partial \dot{q}} + \delta q(t) \, \frac{\partial \mathscr{L}}{\partial q} \right] \, dt \\
    & = - \delta \int_{t_0}^{t_1} \mathscr{L}(\dot{q}(t), q(t), t) \, dt =: - \delta S \ ,
\end{aligned}$$

cioè le equazioni di Lagrange sono equivalenti alla condizione di stazionarietà del funzionale **azione**

$$S:= \int_{t_0}^{t_1} \mathscr{L}(\dot{q}(t), q(t), t) \, dt \ .$$

