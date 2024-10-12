```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-mechanics:lagrange)=
# Meccanica analitica: formulazione di Lagrange

Riformulazione della meccanica di Newton:
- **forma debole** delle equazioni: approccio di D'Alembert, lavori virtuali
- **equazioni di Lagrange**

$$\dfrac{d}{dt}\Big( \frac{\partial \mathscr{L}}{\partial \dot{q}} \Big) - \frac{\partial \mathscr{L}}{\partial q} = Q_q$$

con $\mathscr{L}(\dot{q}(t), q(t), t) = K(\dot{q}(t), q(t), t) + U(q(t), t)$.

- **principi di stazionarietà del funzionale azione $S$**

Nel caso non ci siano azioni non conservative, $Q_q = 0$, è possibile interpretare le equazioni di Lagrange come risultato di un principio di stazionarietà. Chiamando $\delta q(t)$ la variazione della funzion $q(t)$, moltiplicandola per le equazioni di Lagrange e integrando in tempo per $t \in [t_0, t_1]$,

$$\begin{aligned}
  0 & = \int_{t_0}^{t_1} \delta q (t) \Big[ \dfrac{d}{dt}\Big( \frac{\partial \mathscr{L}}{\partial \dot{q}} \Big) - \frac{\partial \mathscr{L}}{\partial q} \Big] \, dt = \\
    & = \delta q(t) \Big( \frac{\partial \mathscr{L}}{\partial \dot{q}} \Big) \Big|_{t_0}^{t_1} - \int_{t_0}^{t_1} \Big[ \delta \dot{q}(t) \, \frac{\partial \mathscr{L}}{\partial \dot{q}} + \delta q(t) \, \frac{\partial \mathscr{L}}{\partial q} \Big] \, dt \ . \\
\end{aligned}$$

Imponendo che la variazione $\delta q(t)$ sia nulla per $t_0$ e $t_1$, il primo termine si annulla, e si può dimostrare che

$$\begin{aligned}
    0 & = - \int_{t_0}^{t_1} \Big[ \delta \dot{q}(t) \, \frac{\partial \mathscr{L}}{\partial \dot{q}} + \delta q(t) \, \frac{\partial \mathscr{L}}{\partial q} \Big] \, dt \\
    & = - \delta \int_{t_0}^{t_1} \mathscr{L}(\dot{q}(t), q(t), t) \, dt =: - \delta S \ ,
\end{aligned}$$

cioè le equazioni di Lagrange sono equivalenti alla condizione di stazionarietà del funzionale **azione**

$$S:= \int_{t_0}^{t_1} \mathscr{L}(\dot{q}(t), q(t), t) \, dt \ .$$

