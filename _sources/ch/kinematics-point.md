(classical-mechanics:kinematics:point)=
# Cinematica del punto

La cinematica di un punto generalmente si riduce alla determinazione della posizione, della velocità e dell'accelerazione del punto.

## Posizione
La posizione di un punto nello spazio euclideo $E^3$ rispetto a un sistema di riferimento $I$ è identificata dal raggio vettore tra l'origine $O_I$ del sistema di riferimento e il punto stesso,

$$\mathbf{r}_P = (P - O) \ .$$

La posizione è identificata da una quantità vettoriale. Per identificare il punto si possono scegliere diversi sistemi di coordinate, ma la posizione del punto non è influenzata dalla scelta delle coordinate.

Ad esempio, usando un sistema di coordinate Cartesiane associate alla base $\{\hat{\mathbf{x}}_I, \hat{\mathbf{y}}_I, \hat{\mathbf{z}}_I \}$, indipendente dal tempo, la posizione del punto P può essere scritta come combinazione lineare dei vettori della base,

$$\mathbf{r}_P(t) = x_P(t) \hat{\mathbf{x}}_I + y_P(t) \hat{\mathbf{y}}_I + z_P(t) \hat{\mathbf{z}}_I \ .$$

## Velocità
La velocità del punto $P$ rispetto al sistema di riferimento $I$ è la derivata rispetto al tempo della posizione del punto,

$$\mathbf{v}_P(t) = \dot{\mathbf{r}}_P(t) \ .$$

Usando il sistema di riferimento cartesiano, e che i vettori della base sono costanti, la velocità può essere scritta come

$$\mathbf{v}_P(t) = \dot{\mathbf{r}}_P(t) = \dot{x}_P(t) \hat{\mathbf{x}}_I + \dot{y}_P(t) \hat{\mathbf{y}}_I + \dot{z}_P(t) \hat{\mathbf{z}}_I \ .$$

## Accelerazione
L'accelerazione del punto $P$ rispetto al sistema di riferimento $I$ è la derivata rispetto al tempo della velocità del punto, la derivata seconda della posizione

$$\mathbf{a}_P(t) = \dot{\mathbf{v}}_P(t) = \ddot{\mathbf{r}}_P(t) \ .$$

Usando il sistema di riferimento cartesiano, e che i vettori della base sono costanti, l'accelerazione può essere scritta come

$$\begin{aligned}
\mathbf{a}_P(t) & = \ddot{\mathbf{r}}_P(t) = \ddot{x}_P(t) \hat{\mathbf{x}}_I + \ddot{y}_P(t) \hat{\mathbf{y}}_I + \ddot{z}_P(t) \hat{\mathbf{z}}_I \\
                & =  \dot{\mathbf{v}}_P(t) =  \dot{v}_{x,P}(t) \hat{\mathbf{x}}_I + \dot{v}_{y,P}(t) \hat{\mathbf{y}}_I + \dot{v}_{z,P}(t) \hat{\mathbf{z}}_I \ .
\end{aligned}$$

## Parametrizzazione della traiettoria, coordinata naturale e terna di Frenet
Usando i concetti della geometria delle curve, è possibile definire la coordinata naturale $s$ lungo la curva, tale che il vettore unitario tangente alla curva coincide con la derivata della posizione rispetto alla coordinata $s$,

$$\hat{\mathbf{t}}(s) = \dfrac{d \mathbf{r}}{d s} \ .$$

La derivata del versore tangente è ortogonale ad esso, punta verso il centro del cerchio osculatore, il cui raggio $R$ è definito come il raggio di curvatura della curva nel punto; la curvatura è definita come l'inverso del raggio di curvatura, $\kappa = \frac{1}{R}$; il valore assoluto della derivata del versore tangente rispetto alla coordinata $s$ è uguale alla curvatura,

$$\kappa(s) \hat{\mathbf{n}} := \frac{d \hat{\mathbf{t}}}{ d s } =  \frac{d \hat{\mathbf{t}}}{ d s } \ .$$

Il versore binormale che forma la terna di Frenet è definito come il prodotto vettore tra $\hat{\mathbf{t}}$ e $\hat{\mathbf{n}}$,

$$\hat{\mathbf{b}}(s) := \hat{\mathbf{t}}(s) \times \hat{\mathbf{n}}(s) \ .$$

Usando le regole per la derivazione di funzioni composte, si può scrivere la velocità come

$$\mathbf{v}_P(t) = \dfrac{d}{dt} \mathbf{r}_P = \dfrac{d s}{d t} \dfrac{d}{ds} \mathbf{r}_P = v_P \hat{\mathbf{t}} \ ,$$

essendo $v_P$ il modulo della velocità, sempre tangente alla traiettoria.

L'accelerazione diventa quindi

$$\begin{aligned}
  \mathbf{a}_P(t) & = \dfrac{d}{dt} \mathbf{v}_P(t) = \\
                  & = \dfrac{d}{dt} \left( v_P \hat{\mathbf{t}} \right) = \\
                  & = \dfrac{d}{dt} v_P \hat{\mathbf{t}} + v_P \dfrac{ds}{dt} \dfrac{d}{ds} \hat{\mathbf{t}}= \\
                  & = a_P \hat{\mathbf{t}} + \kappa \, v^2_P \hat{\mathbf{n}}  \ .
\end{aligned}$$
