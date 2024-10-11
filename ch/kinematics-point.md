(classical-mechanics:kinematics:point)=
# Cinematica del punto

La cinematica di un punto generalmente si riduce alla determinazione della posizione, della velocità e dell'accelerazione del punto.

**Posizione.** La posizione di un punto nello spazio euclideo $E^3$ rispetto a un sistema di riferimento $I$ è identificata dal raggio vettore tra l'origine $O_I$ del sistema di riferimento e il punto stesso,

$$\mathbf{r}_P = (P - O) \ .$$

La posizione è identificata da una quantità vettoriale. Per identificare il punto si possono scegliere diversi sistemi di coordinate, ma la posizione del punto non è influenzata dalla scelta delle coordinate.

Ad esempio, usando un sistema di coordinate Cartesiane associate alla base $\{\hat{\mathbf{x}}_I, \hat{\mathbf{y}}_I, \hat{\mathbf{z}}_I \}$, indipendente dal tempo, la posizione del punto P può essere scritta come combinazione lineare dei vettori della base,

$$\mathbf{r}_P(t) = x_P(t) \hat{\mathbf{x}}_I + y_P(t) \hat{\mathbf{y}}_I + z_P(t) \hat{\mathbf{z}}_I \ .$$

**Velocità.** La velocità del punto $P$ rispetto al sistema di riferimento $I$ è la derivata rispetto al tempo della posizione del punto,

$$\mathbf{v}_P(t) = \dot{\mathbf{r}}_P(t) \ .$$

Usando il sistema di riferimento cartesiano, e che i vettori della base sono costanti, la velocità può essere scritta come

$$\mathbf{v}_P(t) = \dot{\mathbf{r}}_P(t) = \dot{x}_P(t) \hat{\mathbf{x}}_I + \dot{y}_P(t) \hat{\mathbf{y}}_I + \dot{z}_P(t) \hat{\mathbf{z}}_I \ .$$

**Accelerazione.** L'accelerazione del punto $P$ rispetto al sistema di riferimento $I$ è la derivata rispetto al tempo della velocità del punto, la derivata seconda della posizione

$$\mathbf{a}_P(t) = \dot{\mathbf{v}}_P(t) = \ddot{\mathbf{r}}_P(t) \ .$$

Usando il sistema di riferimento cartesiano, e che i vettori della base sono costanti, l'accelerazione può essere scritta come

$$\begin{aligned}
\mathbf{a}_P(t) & = \ddot{\mathbf{r}}_P(t) = \ddot{x}_P(t) \hat{\mathbf{x}}_I + \ddot{y}_P(t) \hat{\mathbf{y}}_I + \ddot{z}_P(t) \hat{\mathbf{z}}_I \\
                & =  \dot{\mathbf{v}}_P(t) =  \dot{v}_{x,P}(t) \hat{\mathbf{x}}_I + \dot{v}_{y,P}(t) \hat{\mathbf{y}}_I + \dot{v}_{z,P}(t) \hat{\mathbf{z}}_I \ .
\end{aligned}$$
