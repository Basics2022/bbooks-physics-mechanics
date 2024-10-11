```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-mechanics:dynamics:eom:point)=
# Equazioni cardinali della dinamica: punto materiale

**Quantità dinamiche.**

$$\begin{aligned}
  \mathbf{Q}_P & := m_P \mathbf{v}_P \\
$$\mathbf{L}_{P,H} & := (\mathbf{r}_P - \mathbf{r}_H) \times \mathbf{Q} = m_P (\mathbf{r}_P - \mathbf{r}_H) \times \mathbf{v}_P \\
  K := \frac{1}{2} m_P \mathbf{v}_P \cdot \mathbf{v}_P = \frac{1}{2} m_P |\mathbf{v}_P|^2
\end{aligned}$$

**Bilancio della quantità di moto.** Il bilancio della quantità di moto di un punto materiale $P$, $\mathbf{Q}_P = m \mathbf{v}_P$ segue direttamente dal secondo principio della dinamica di Newton,

$$\dot{\mathbf{Q}}_P = \mathbf{R}^e_P$$

**Bilancio del momento della quantità di moto.** La derivata nel tempo del momento della quantità di moto viene calcolata usando la regola del prodotto,

$$\begin{aligned}
\dot{\mathbf{L}}_{P,H} & = \dfrac{d}{dt} \left[ m_P (\mathbf{r}_P - \mathbf{r}_H) \times \mathbf{v}_P \right] = \\
& = m \left[ ( \dot{\mathbf{r}}_P - \dot{\mathbf{r}}_H ) \times \mathbf{v}_P + m_P (\mathbf{r}_P - \mathbf{r}_H) \times \dot{\mathbf{v}}_P \right] = \\
& = - m_P \dot{\mathbf{r}}_H \times \mathbf{v}_P + m_P (\mathbf{r}_P - \mathbf{r}_H) \times \dot{\mathbf{v}}_P = \\
& = - \dot{\mathbf{r}}_H \times \mathbf{Q} + \mathbf{M}_H^{ext} \ .
\end{aligend}$$

**Bilancio dell'energia cinetica.**

$$\begin{aligned}
\dot{K}_{P} & = \dfrac{d}{dt} \left( \frac{1}{2} m_P \mathbf{v}_P \cdot \mathbf{m}_P \right) = \\
            & = m_P \dot{\mathbf{v}}_P \cdot \mathbf{m}_P = \\
            & = \mathbf{R}^e \cdot \mathbf{m}_P = \\
            & = \mathbf{R}^{tot} \cdot \mathbf{m}_P = P^{tot} \ .
\end{aligend}$$


