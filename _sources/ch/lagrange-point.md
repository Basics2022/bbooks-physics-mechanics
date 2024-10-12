```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-mechanics:lagrange:point)=
# Punto materiale

**Equazione in forma forte.** Dalla meccanica di Newton, l'equazione del moto per un punto materiale è

$$m \dot{\boldsymbol{v}} = \boldsymbol{R}^e \ .$$

**Equazione in forma debole.** La forma debole dell'equazione si ottiene moltiplicando scalarmente l'equazione del moto per una funzione arbitraria $\boldsymbol{w}$

$$\boldsymbol{0} = \boldsymbol{w} \cdot \Big( m \dot{\boldsymbol{v}} - \boldsymbol{R}^e\Big)  \qquad \forall \boldsymbol{w}$$

**Formulazione della meccanica di Lagrange.** La formulazione di Lagrange della meccanica si ottiene scrivendo la posizione del punto materiale come funzione delle coordinate generalizzate $q(t)$ e del tempo $t$,

$$\boldsymbol{r}(q(t),t)$$

e, di conseguenza, la velocità del punto

$$\boldsymbol{v}(\dot{q}(t), q(t), t) = \frac{d\boldsymbol{r}}{dt} = \dot{q}(t) \underbrace{\frac{\partial \boldsymbol{r}}{\partial q}}_{\frac{\partial \boldsymbol{v}}{\partial \dot{q}}} + \frac{\partial \boldsymbol{r}}{\partial t} \ ,$$

dove si è riconosciuta l'uguaglianza $\frac{\partial \boldsymbol{r}}{\partial q} = \frac{\partial \boldsymbol{v}}{\partial \dot{q}}$.

Scegliendo come funzione test $\boldsymbol{w} = \frac{\partial \boldsymbol{r}}{\partial q} = \frac{\partial \boldsymbol{v}}{\partial \dot{q}}$,

$$\begin{aligned}
\boldsymbol{0} & = \frac{\partial \boldsymbol{v}}{\partial \dot{q}} \cdot \Big( m \dot{\boldsymbol{v}} - \boldsymbol{R}^e \Big) = \\
& = \frac{d}{dt} \Big( \frac{\partial \boldsymbol{v}}{\partial \dot{q}} \cdot m \boldsymbol{v} \Big) - \frac{d}{dt} \frac{\partial \boldsymbol{r}}{\partial q} \cdot m \boldsymbol{v} - \frac{\partial \boldsymbol{r}}{\partial q} \cdot ( \boldsymbol{R}^{e,c} + \boldsymbol{R}^{e,nc} ) \\
& = \frac{d}{dt} \Big( \frac{\partial \boldsymbol{v}}{\partial \dot{q}} \cdot m \boldsymbol{v} \Big) - \frac{\partial \boldsymbol{v}}{\partial q} \cdot m \boldsymbol{v} - \frac{\partial \boldsymbol{r}}{\partial q} \cdot ( \nabla U + \boldsymbol{R}^{e,nc} ) \\
& = \frac{d}{dt} \Big( \frac{\partial K}{\partial \dot{q}} \Big) - \frac{\partial K}{\partial q} - \frac{\partial U}{\partial q} - \underbrace{\frac{\partial \boldsymbol{r}}{\partial q} \cdot \boldsymbol{R}^{e,nc}}_{=Q_q} \ . \\
\end{aligned}$$

Introducendo la funzione lagrangiana, $\mathscr{L}(\dot{q}(t), q(t), t) := K(\dot{q}(t), q(t), t) + U(q(t),t)$, si può quindi scrivere le equazioni di Lagrange come

$$\frac{d}{dt}\Big(\frac{\partial \mathscr{L}}{\partial \dot{q}} \Big) - \frac{\partial \mathscr{L}}{\partial q} = Q_q \ ,$$

essendo $Q_q$ la forza generalizzata non conservativa, $Q_q = \frac{\partial \boldsymbol{r}}{\partial q} \cdot \boldsymbol{R}^{e,nc}$.





