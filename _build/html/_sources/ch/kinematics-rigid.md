(classical-mechanics:kinematics:rigid-body)=
# Rigid Body

## Rigid motion

Rigid motion preserves distance between any pair of points, and thus angles. The motion of two material points $P$, $Q$ performing a rigid motion obeys

$$\vec{v}_P - \vec{v}_Q = \vec{\omega} \times (P - Q) \ ,$$  (eq:kin:rigid:vel)

being $\vec{v}_P$, $\vec{v}_Q$ the velocity of the points and $\vec{\omega}$ the **angular velocity** of the rigid motion. Taking a point $Q$ as the reference point of the motion, the velocity of all other points can be found 

$$\vec{v}_P = \vec{v}_Q + \vec{\omega} \times (P-Q) \ ,$$

as a function of the velocity of $Q$, the angular velocity of the rigid motion, and the relative position $P-Q$.

```{dropdown} Proof.
Given 3 points $P(t)$, $Q(t)$, $R(t)$, the distance bewteen each pair of points is constant and thus its time derivative zero,

$$0 = \dfrac{d}{dt} |P(t)-Q(t)|^2 = 2 \left(P - Q\right) \cdot \left( \vec{v}_P - \vec{v}_Q \right) \quad \rightarrow \quad \Delta \vec{v}_{QP} = \vec{\omega}_{QP} \times \Delta \vec{r}_{QP}$$
$$0 = \dfrac{d}{dt} |P(t)-R(t)|^2 = 2 \left(P - R\right) \cdot \left( \vec{v}_P - \vec{v}_R \right) \quad \rightarrow \quad \Delta \vec{v}_{RP} = \vec{\omega}_{RP} \times \Delta \vec{r}_{RP}$$
$$\begin{aligned}
  0 = \dfrac{d}{dt} \left[ (P-Q) \cdot (P-R) \right] 
  & = \Delta \vec{v}_{QP} \cdot \Delta \vec{r}_{RP} + \Delta \vec{r}_{QP} \cdot \Delta \vec{v}_{RP} = \\
  & = \vec{\omega}_{QP} \times \Delta \vec{r}_{QP} \cdot \Delta \vec{r}_{RP} + \Delta \vec{r}_{QP} \cdot \Delta \vec{\omega}_{RP} \times \Delta \vec{r}_{RP} = \\
  & = \Delta \vec{r}_{QP} \times \Delta \vec{r}_{RP} \cdot ( \vec{\omega}_{QP} - \vec{\omega}_{RP} ) \ ,
\end{aligned}$$

and since $\Delta \vec{r}_{QP}$, $\Delta \vec{r}_{RP}$ are arbitrary it follows that the vector $\vec{\omega} = \vec{\omega}_{QP} = \vec{\omega}_{RP}$ is unique for all the points performing a rigid motion.
```

The configuration of a material vector $\vec{a}$ undergoing a rotation is described by the product of the rotation tensor $\mathbb{R}$ by the reference configuration $\vec{a}^0$,

$$
\vec{a} = \mathbb{R} \cdot \vec{a}^0 
\qquad , \qquad
\vec{b} = \mathbb{R} \cdot \vec{b}^0 \ .
$$

In order to preserve distance, and angles

$$\begin{cases}
 |\vec{a}|^2 = & \vec{a} \cdot \vec{a} = \vec{a}^0 \cdot \mathbb{R}^T \cdot \mathbb{R} \cdot \vec{a}^0 = \vec{a}^0 \cdot \vec{a}^0 = |\vec{a}|^2 \\
               & \vec{a} \cdot \vec{b} = \vec{a}^0 \cdot \mathbb{R}^T \cdot \mathbb{R} \cdot \vec{b}^0 = \vec{a}^0 \cdot \vec{a}^0
\end{cases}
\qquad \rightarrow \qquad \mathbb{R}^T \cdot \mathbb{R} = \mathbb{I}
$$

the **rotation tensor** is **unitary**

$$\mathbb{I} = \mathbb{R}^T \cdot \mathbb{R} = \mathbb{R} \cdot \mathbb{R}^T$$ (eq:rot:unitary)

```{note}
From relation {eq}`eq:rot:unitary`, it follows that

$$1 = |\mathbb{I}| = |\mathbb{R}^T| |\mathbb{R}| = |\mathbb{R}|^2 \ ,$$

and thus $|\mathbb{R}| = \mp 1$. If $|\mathbb{R}| = 1$, $\mathbb{R}$ represents a rotation, and implies conservation of orientation of space; if $|\mathbb{R}| = -1$ represents a reflection w.r.t. a plane, and implies inversion of orientation of space.

Orientation of space is determined by the transformation of a RHS triad of vectors: if the transform triad is RHS, then orientation of space is preserved; if it becomes LHS, then orientation of space is inverted.

```
```{note}
Rotation tensor $\mathbb{R}$ is not singular and its determinant equals $|\mathbb{R}| = 1$. Thus, $\mathbb{R}^T \cdot \mathbb{R} = \mathbb{I}$ implies $\mathbb{R} \cdot \mathbb{R}^T = \mathbb{I}$. Multiplying {eq}`eq:rot:unitary` by $\mathbb{R}$ on the left

$$\mathbb{0} = \mathbb{R} \cdot \mathbb{R}^T \cdot \mathbb{R} - \mathbb{R} \cdot \mathbb{I} = (\mathbb{R} \cdot \mathbb{R}^T - \mathbb{I}) \cdot  \mathbb{R} \ ,$$

and since $\mathbb{R}$ is non-singular, it follows that $\mathbb{R} \cdot \mathbb{R}^T = \mathbb{I}$.

```

Time derivative of the relation {eq}`eq:rot:unitary` reads

$$\mathbb{0} = \dfrac{d}{dt} \left( \mathbb{R} \cdot \mathbb{R}^T \right) = \dot{\mathbb{R}} \cdot \mathbb{R}^T + \mathbb{R} \cdot \dot{\mathbb{R}}^T$$

It follows that the 2-nd order tensor $\dot{\mathbb{R}} \cdot \mathbb{R}^T = - \mathbb{R} \cdot \dot{\mathbb{R}}^T$ is anti-symmetric, and thus it can be written as 

$$\dot{\mathbb{R}} \cdot \mathbb{R}^T =: \vec{\omega}_{\times} \ ,$$ (eq:omegax:def)

being the vector $\vec{\omega}$ the angular velocity. Since $\mathbb{R}$ is unitary by {eq}`eq:rot:unitary`, multiplying {eq}`eq:omegax:def` with the dot-product on the right by $\mathbb{R}$, it follows

$$\dot{\mathbb{R}} = \vec{\omega}_{\times} \cdot \mathbb{R} \ ,$$

and the expression of the time derivative of a material vector $\vec{a}$,

$$\dfrac{d \vec{a}}{d t} = \dot{\mathbb{R}} \cdot \vec{a}^0 = \vec{\omega}_{\times} \cdot \mathbb{R} \cdot \vec{a}^0 = \vec{\omega}_{\times} \cdot \vec{a} = \vec{\omega} \times \vec{a} \  .$$ (eq:material-v:time-derivative)

<!--
## Kinematics of rigid body
Rigid motion allows to describe the kinematics of a rigid body - determining position, velocity and acceleration of all of its points - given the position of a material point $P$ and its orientation with respect to the reference frame, as an example using a rotation tensor $\mathbb{R}$.
-->

**Position and Orientation.**
The most general rigid motion is the combination of the translation of a reference point $Q$ and the rotation w.r.t. this point of other material points,

$$\begin{aligned}
  \vec{r}_P
  & = \vec{r}_Q + (P - Q) = \\
  & = \vec{r}_Q + \mathbb{R} \cdot (P-Q)^0 
\end{aligned}$$  (eq:rigid:pos)

**Velocity and Angular velocity.**
Time derivative of the relation {eq}`eq:rigid:pos` between positions of material points gives again {eq}`eq:kin:rigid:vel`

$$\begin{aligned}
  \vec{v}_P
  & = \vec{v}_Q + \dot{\mathbb{R}} \cdot (P-Q)^0 = \\
  & = \vec{v}_Q + \vec{\omega}_{\times} \mathbb{R} \cdot (P-Q)^0 = \\
  & = \vec{v}_Q + \vec{\omega} \times (P-Q)
\end{aligned}$$ (eq:rigid:vel)

**Acceleration and Angular acceleration.**
Time derivatives of the relation {eq}`eq:rigid:vel` gives

$$\begin{aligned}
\vec{a}_P 
 & = \vec{a}_Q + \vec{\alpha} \times (P-Q) + \vec{\omega} \times \left( \vec{v}_P - \vec{Q} \right) = \\
 & = \vec{a}_Q + \vec{\alpha} \times (P-Q) + \vec{\omega} \times \left[ \, \vec{\omega} \times (P - Q) \, \right] \ .
\end{aligned}$$



<!--

I punti di corpi estesi che compiono un atto di moto rigido (**todo** definizione di atto di moto? E' utile?) mantengono costante la propria distanza. Poiché questa condizione vale per ogni coppia di punti, vengono mantenuti costanti anche gli angoli tra segmenti che congiungono punti materiali, cioè appartenenti al copo e che si muovono con esso.

Affinché queste condizioni siano soddisfatte, un vettore materiale si trasforma con una rotazione. Il moto di un corpo rigido può quindi essere descritto come la composizione di un moto di traslazione di un punto $P$ e la rotazione del corpo attorno ad esso.

$$\mathbf{r}_P - \mathbf{r}_Q = \mathbb{R} \cdot (\mathbf{r}_P - \mathbf{r}_Q)_0 \ ,$$

dove $(\mathbf{r}_P - \mathbf{r}_Q)_0$ rappresenta il vettore materiale nella posizione di riferimento, ed $\mathbb{R}$ è il tensore di rotazione che rappresenta la rotazione del corpo rigido dalla posizione di riferimento alla posizione corrente. La posizione di ogni punto materiale $P$ può essere scritta come la posizione di un punto materiale di riferimento $Q$ e il vettore di riferimento $(\mathbf{r}_P - \mathbf{r}_Q)_0$ ruotato.

## Tensore di rotazione
**Proprietà**
- definizione con due sistemi di riferimento cartesiani in moto relativo. Dati due basi ortonormali, $\{\hat{\mathbf{e}}^0_i\}$, $\{\hat{\mathbf{e}}^1_j\}$, è possibile scrivere i vettori di una base come

$$\begin{aligned}
  \hat{\mathbf{e}}^1_j & = (\hat{\mathbf{e}}^1_j \cdot \hat{\mathbf{e}}^0_i ) \hat{\mathbf{e}}^0_i = \\
                       & = (\hat{\mathbf{e}}^0_i \cdot \hat{\mathbf{e}}^1_k ) \hat{\mathbf{e}}^0_i \otimes \hat{\mathbf{e}}^0_k \cdot \hat{\mathbf{e}}^0_k = \\
                       & = R^{0\rightarrow 1}_{ik} \hat{\mathbf{e}}^0_i \otimes \hat{\mathbf{e}}^0_k \cdot \hat{\mathbf{e}}^0_j = \\
                       & = \mathbb{R}^{0 \rightarrow 1} \cdot \hat{\mathbf{e}}^0_j = \\
\end{aligned}$$



- unitarietà

$$\mathbb{R}^T \cdot \mathbb{R}  = \mathbb{I}$$
$$\mathbb{R} \cdot \mathbb{R}^T  = \mathbb{I}$$

- derivata del tensore di rotazione e definizione del vettore velocità angolare

$$\mathbb{0} = \dot{\mathbb{R}} \cdot \mathbb{R}^T + {\mathbb{R}} \cdot \dot{\mathbb{R}}^T \qquad \rightarrow \qquad
\dot{\mathbb{R}} \cdot \mathbb{R}^T = - \mathbb{R} \cdot \dot{\mathbb{R}}^T =: \omega_{\times}$$

$$\dot{\mathbb{R}} = \omega_{\times} \cdot \mathbb{R}$$


- composizione di rotazioni (qui o nella cinematica relativa? o in un'appendice apposita per le rotazioni?)

## Velocità
La derivata nel tempo della legge dell'atto di moto rigido permette di ricavare la relazione tra le velocità di due punti materiali di un corpo rigido,

$$\begin{aligned}
  \mathbf{v}_P - \mathbf{v}_Q & = \frac{d}{dt} \left( \mathbb{R} \cdot (\mathbf{r}_P - \mathbf{r}_Q)_0 \right) = \\
                              & = \dot{\mathbb{R}} \cdot (\mathbf{r}_P - \mathbf{r}_Q)_0 = \\
                              & = \symbf{\omega}_{\times} \cdot \mathbb{R} \cdot (\mathbf{r}_P - \mathbf{r}_Q)_0 = \\
                              & = \symbf{\omega} \times ( \mathbf{r}_P - \mathbf{r}_Q ) 
\end{aligned}$$

## Accelerazione
Derivando nuovamente nel tempo, si trova la relazione tra l'accelerazione di una coppia di punti materiali del corpo rigido,

$$\begin{aligned}
  \mathbf{a}_P - \mathbf{a}_Q & = \frac{d}{dt} \left( \symbf{\omega} \times ( \mathbf{r}_P - \mathbf{r}_Q )  \right) = \\
                              & = \frac{d \symbf{\omega}}{dt} \times ( \mathbf{r}_P - \mathbf{r}_Q ) + \symbf{\omega} \times \dfrac{d}{dt}( \mathbf{r}_P - \mathbf{r}_Q ) = \\
                              & = \symbf{\alpha} \times ( \mathbf{r}_P - \mathbf{r}_Q ) + \symbf{\omega} \times \left ( \symbf{\omega} \times ( \mathbf{r}_P - \mathbf{r}_Q ) \right) = \\
                              & = \symbf{\alpha} \times ( \mathbf{r}_P - \mathbf{r}_Q ) + \symbf{\omega}_{\times} \cdot  \symbf{\omega}_{\times} \cdot ( \mathbf{r}_P - \mathbf{r}_Q ) \ . 
\end{aligned}$$

-->



