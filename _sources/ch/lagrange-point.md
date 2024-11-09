```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-mechanics:lagrange:point)=
# Punto materiale

**Equazione in forma forte.** Dalla meccanica di Newton, l'equazione del moto per un punto materiale $P$ può essere scritta come

$$m \dot{\mathbf{v}}_P = \mathbf{R}^e \ ,$$

avendo indicato con $m$ la massa del sistema, $\mathbf{v}_P$ la velocità del punto, $\mathbf{a}_P = \dot{\mathbf{v}}_P$ la sua accelerazione e $\mathbf{R}^{e}$ la risultante delle forze esterne agenti sul sistema.

**Equazione in forma debole.** La forma debole dell'equazione si ottiene moltiplicando scalarmente l'equazione del moto per una funzione arbitraria $\mathbf{w}$

$$\mathbf{0} = \mathbf{w} \cdot \left( m \dot{\mathbf{v}} - \mathbf{R}^e\right)  \qquad \forall \mathbf{w}$$

**Formulazione della meccanica di Lagrange.** La formulazione di Lagrange della meccanica si ottiene scrivendo la posizione del punto materiale come funzione delle coordinate generalizzate $q(t)$ e del tempo $t$,

$$\mathbf{r}_P(t) = \mathbf{r}(q_k(t),t) \ .$$

Di conseguenza, usando la definizione di velocità e la regola di derivazione di funzioni composte, si può ottenere un'espressione della velocità in funzione del tempo, delle coordinate generalizzate e della loro derivata prima rispetto al tempo,

$$\mathbf{v}_P(t) := \frac{d\mathbf{r}_P}{dt} = \dot{q}_k(t) \underbrace{\frac{\partial \mathbf{r}}{\partial q_k}}_{\frac{\partial \mathbf{v}}{\partial \dot{q}_k}} + \frac{\partial \mathbf{r}}{\partial t} = \mathbf{v}\left(\dot{q}_k(t), q_k(t), t \right) \ ,$$

grazie alla quale si può riconoscere la relazione 

$$\dfrac{\partial \mathbf{r}}{\partial q_k} = \dfrac{\partial \mathbf{v}}{\partial \dot{q}_k} \ .$$ (classical-mechanics:lagrange:point:mixed-der)

Scegliendo come funzione test $\mathbf{w} = \dfrac{\partial \mathbf{r}}{\partial q_k} = \dfrac{\partial \mathbf{v}}{\partial \dot{q}_k}$, applicando la regola di derivazione del prodotto e usando il teorema di Schwartz per invertire l'ordine delle derivate e la relazione {eq}`classical-mechanics:lagrange:point:mixed-der`, si può manipolare l'equazione in forma debole

$$\begin{aligned}
\mathbf{0} & = \frac{\partial \mathbf{v}}{\partial \dot{q}_k} \cdot \left( m \dot{\mathbf{v}} - \mathbf{R}^e \right) = \\
& = \frac{d}{dt} \left( \frac{\partial \mathbf{v}}{\partial \dot{q}_k} \cdot m \mathbf{v} \right) - \frac{d}{dt} \frac{\partial \mathbf{r}}{\partial q_k} \cdot m \mathbf{v} - \frac{\partial \mathbf{r}}{\partial q_k} \cdot ( \mathbf{R}^{e,c} + \mathbf{R}^{e,nc} ) \\
& = \frac{d}{dt} \left( \frac{\partial \mathbf{v}}{\partial \dot{q}_k} \cdot m \mathbf{v} \right) - \frac{\partial \mathbf{v}}{\partial q_k} \cdot m \mathbf{v} - \frac{\partial \mathbf{r}}{\partial q_k} \cdot ( \nabla U + \mathbf{R}^{e,nc} ) \\
& = \frac{d}{dt} \left( \frac{\partial K}{\partial \dot{q}_k} \right) - \frac{\partial K}{\partial q_k} - \frac{\partial U}{\partial q_k} - \underbrace{\frac{\partial \mathbf{r}}{\partial q_k} \cdot \mathbf{R}^{e,nc}}_{=: Q_k} \ . \\
\end{aligned}$$

Introducendo la funzione lagrangiana, $\mathscr{L}(\dot{q}_k(t), q_k(t), t) := K(\dot{q}_k(t), q_k(t), t) + U(q_k(t),t)$, e ricordando che la funzione potenziale non dipende dalle velocità e quindi dalle derivate delle coordinate generalizzate $\dot{q}_k$, si possono raccogliere i termini e scrivere le equazioni di Lagrange come

$$\frac{d}{dt}\left(\frac{\partial \mathscr{L}}{\partial \dot{q}_k} \right) - \frac{\partial \mathscr{L}}{\partial q_k} = Q_k \ ,$$

essendo $Q_k$ la **forza generalizzata non conservativa**, $Q_k = \dfrac{\partial \mathbf{r}}{\partial q_k} \cdot \mathbf{R}^{e,nc}$.





