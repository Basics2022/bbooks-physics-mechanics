<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-mechanics:lagrange)=
# Lagrangian Mechanics

Classical mechanics can be re-formulated starting principles of [calculus of variations](https://basics2022.github.io/bbooks-math-miscellanea/ch/calculus-variations/intro.html), usually referred as **analytical mechanics**. Under some assumptions, that will be discussed during the derivation, analytical mechanics is equivalent to Newton mechanics.

[**Lagrange equations - II kind**](classical-mechanics:lagrange:ii-type). Lagrange equations of the II kind provides **pure equations of motion**, in which constraint forces do not appear. Given a system with $N$ degrees of freedom, that can be described with $N$ independent generalized coordinates $\{ q^k \}_{k=1:N}$, Lagrange equations of the II kind are a set of $N$ **$2^{nd}$ order ODEs** in the generalized coordinates.

The equivalence with Newton's approach to classical mechanics is discussed in detail for different kind of systems (points, rigid bodies,...): starting from Newton's dynamical equations of motion (strong form), D'Alembert approach (weak form) is derived, and Lagrange equations are derived from that with a proper choice of test functions. Lagrange equations are then recast as the stationariety condition of a functional, providing a variational approach to classical mechanics.

```{tip}
Lagrange equations of the II kind could be the best approach for small-dimensional problems, when there's no interest in evaluating constraint reactions.
```

[**Lagrange equations - I kind**](classical-mechanics:lagrange:i-type). Lagrange equations of the I kind provides a set of **DAEs**, explicitly including constraints as independent equations and adding their effects - their constraint reactions - in the dynamical equations of the degrees of freedom as **Lagrange multipliers**.

```{tip}
Lagrange equations of the I kind could be the best approach for numerical approach to generic mechanical systems, as it is a less problem-dependent approach, without any case-dependent manipulation.
```

[**Lagrangian mechanics, with expliicitly time-dependent Lagrangian function**](classical-mechanics:lagrange:time:dependent). Energy conservation is related to explicit time independent of its Lagrangian function, and can be related - beside the absence of non-conservative actions - to the absence of any time-dependent external input, or the choice of an inertial reference frame. Consequence of explicit time dependence in the Lagrangian functions are discussed, with examples.

[**Constraints in Lagrangian mechanics**](classical-mechanics:lagrange:constraints). Constraints in Lagrangian mechanics are discussed: holonomic and non-holonomic are discussed, and an approach to ideal non-holonomic (semi-linear?) constraints in Lagrange mechanics is outlined.

[**Properties**](classical-mechanics:lagrange:properties). Some properties of Lagrangian approach to mechanics are discussed. As an example, Lagrange mechanics provides a **symmetric form** of the (linearised?) governing equations, without any additional effort. This could be quite useful, especially for exploiting numerical methods for symmetric (and definite positive, sometimes) matrices.

<!--
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
-->
