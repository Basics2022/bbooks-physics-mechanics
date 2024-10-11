```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-mechanics:actions:work-power)=
# Lavoro e potenza

## Lavoro e potenza di una forza

**Lavoro.** Il lavoro elementare di una forza $\mathbf{F}$ applicata in un punto di applicazione $\mathbf{r}_P$ che subisce uno spostamento $d\mathbf{r}$ viene definito come 

$$d L = \mathbf{F} \cdot d \mathbf{r} \ .$$

Per uno spostamento finito del punto $P$ dal punto $\mathbf{r}_A$ al punto $\mathbf{r}_B$ lungo la linea $\ell_{AB}$, è necessario sommare i contributi elementari (e quindi integrare) lungo il percorso $\ell_{AB}$

$$L = \int_{\ell_{AB}} dL = \int_{\ell_{AB}} \mathbf{F} \cdot d \mathbf{r}_P \ .$$

**todo** In generale il lavoro di una forza o di un campo di forze **dipende dal percorso di integrazione** $\ell_{AB}$. Sarebbe meglio usare $\delta L$ per ricordare questa proprietà del lavoro, che quindi non è un **differenziale esatto**.

**Potenza.** La potenza di una forza $\mathbf{F}$ applicata in un punto di applicazione $\mathbf{r}_P$ che ha velocità $\mathbf{v}_P$ viene definita come

$$P = \mathbf{F} \cdot \mathbf{v}_P \ ,$$

cioè come la derivata nel tempo del lavoro,

$$\dfrac{dL}{dt} = \mathbf{F} \cdot \dfrac{d \mathbf{r}_P}{d t} = \mathbf{F} \cdot \mathbf{v}_P = P \ .$$

## Lavoro e potenza di una coppia di forze

Una coppia di forze è definita come il momento generato da due forze con uguale intensità e verso opposto, $\mathbf{F}_1 = - \mathbf{F}_2$,

$$\mathbf{C} = (\mathbf{r}_1 - \mathbf{r}_2) \times \mathbf{F}_1 \ .$$

**Potenza.** La potenza di una coppia di forze è la somma della potenza generata da entrambe le forze,

$$P = P_1 + P_2 = \mathbf{F}_1 \cdot \mathbf{v}_1 + \mathbf{F}_2 \cdot \mathbf{v}_2 = \mathbf{F}_1 \cdot (\mathbf{v}_1 - \mathbf{v}_2) \ .$$

Se la coppia di forze è applicata a una coppia di punti che descrivono un atto di moto rigido,

$$\mathbf{v}_1 - \mathbf{v}_2 = \symbf{\omega} \times (\mathbf{r}_1 - \mathbf{r}_2) \ ,$$

si può riscrivere la potenza della coppia di forze come

$$\begin{aligned}
P & = \mathbf{F}_1 \cdot symbf{\omega} \times (\mathbf{r}_1 - \mathbf{r}_2) = \\
  & = \symbf{\omega} \cdot ( \mathbf{r}_1 - \mathbf{r}_2 ) \times \mathbf{F}_1 = \\
  & = \symbf{\omega} \cdot \mathbf{C}
\end {aligned}$$

