```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-mechanics:kinematics:rigid-body)=
# Cinematica del corpo rigido

I punti di corpi estesi che compiono un atto di moto rigido (**todo** definizione di atto di moto? E' utile?) mantengono costante la propria distanza. Poiché questa condizione vale per ogni coppia di punti, vengono mantenuti costanti anche gli angoli tra segmenti che congiungono punti materiali, cioè appartenenti al copo e che si muovono con esso.

Affinché queste condizioni siano soddisfatte, un vettore materiale si trasforma con una rotazione. Il moto di un corpo rigido può quindi essere descritto come la composizione di un moto di traslazione di un punto $P$ e la rotazione del corpo attorno ad esso.

$$\mathbf{r}_P - \mathbf{r}_Q = \mathbb{R} \cdot (\mathbf{r}_P - \mathbf{r}_Q)_0 \ ,$$

dove $(\mathbf{r}_P - \mathbf{r}_Q)_0$ rappresenta il vettore materiale nella posizione di riferimento, ed $\mathbb{R}$ è il tensore di rotazione che rappresenta la rotazione del corpo rigido dalla posizione di riferimento alla posizione corrente. La posizione di ogni punto materiale $P$ può essere scritta come la posizione di un punto materiale di riferimento $Q$ e il vettore di riferimento $(\mathbf{r}_P - \mathbf{r}_Q)_0$ ruotato.

## Tensore di rotazione
**Proprietà**
- definizione con due sistemi di riferimento cartesiani in moto relativo. Dati due basi ortonormali, $\{\hat{\mathbf{e}}^0_i\}$, $\{\hat{\mathbf{e}}^1_j\}$, è possibile scrivere i vettori di una base come

$$\begin{aligned}
  \hat{\mathbf{e}}^1_j & = (\hat{\mathbf{e}}^1_j \cdot \hat{\mathbf{e}}^0_i ) \hat{\mathbf{e}}^0_i = \\
                       & = (\hat{\mathbf{e}}^0_i \cdot \hat{\mathbf{e}}^1_k ) \hat{\mathbf{e}}^0_i \otimes \hat{mathbf{e}}^0_k \cdot \hat{mathbf{e}}^0_k = \\
                       & = R^{0\rightarrow 1} \hat{\mathbf{e}}^0_i \otimes \hat{mathbf{e}}^0_k \cdot \hat{mathbf{e}}^0_k = \\
                       & = \mathbb{R}^{0 \rightarrow 1} \cdot \hat{mathbf{e}}^0_k = \\
\end{aligned}$$



- unitarietà

$$\mathbb{R}^T \cdot \mathbb{R}  = \mathbb{I}$$
$$\mathbb{R} \cdot \mathbb{R}^T  = \mathbb{I}$$

- derivata del tensore di rotazione e definizione del vettore velocità angolare

$$\mathbb{0} = \dot{\mathbb{R}} \cdot \mathbb{R}^T + {\mathbb{R}} \cdot \dot{\mathbb{R}}^T \qquad \rightarrow \qquad
\dot{\mathbb{R}} \cdot \mathbb{R}^T = - \mathbb{R} \cdot \dot{\mathbb{R}}^T =: \omega_{\times}$$

$$\dot{\mathbb{R}} = \omega_{\times} \cdot \mathbb{R}$$

- composizione di rotazioni (qui o nella cinematica relativa? o in un'appendice apposita per le rotazioni?)




