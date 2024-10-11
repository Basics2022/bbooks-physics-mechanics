```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-mechanics:actions:conservative)=
# Azioni conservative

In generale, il lavoro di una forza o di un campo di forze dipende dalla traiettoria $\ell_{AB}$ del punto di applicazione tra i punti iniziale e finale $\mathbf{r}_A$, $\mathbf{r}_B$.

In alcuni casi, il lavoro è indipendente dal percorso $\ell_{AB}$, ma dipende solo dai suoi punti estremi. Se questo è vero per tutti i percorsi, il lavoro è svolto da una **forza conservativa**.

In questo caso, l'integrale di linea può essere riscritto senza indicare esplicitamente la dipendenza dal percorso $\ell_{AB}$, ma indicandone solo gli estremi

$$L = \int_{\mathbf{r}_A}^{\mathbf{r}_B} \mathbf{F} \cdot d\mathbf{r} \ ,$$

e il suo valore può essere calcolato come differenza di una funzione scalare della variabile spaziale $U(\mathbf{r}) = -V(\mathbf{r})$ valutata nei due estremi del percorso,

$$L_{AB} = U(\mathbf{r}_B) - U(\mathbf{r}_A) = - V(\mathbf{r}_B) + V(\mathbf{r}_A) .$$

o in forma differenziale,

$$dL = dU = - dV \ .$$

Sotto l'ipotesi di sufficiente regolarità (**todo**), e confrontando le espressioni del lavoro infinitesimale di un campo di forze $\mathbf{F}(\mathbf{r})$,

$$dL = dU = \mathbf{F} \cdot \mathbf{r} \ ,$$

si può scrivere il campo di forze come il gradiente della funzione $U$,

$$\mathbf{F}(\mathbf{r}) = \nabla U(\mathbf{r}) = - \nabla V(\mathbf{r} )\ .$$

Per le proprietà dei campi e degli operatori vettoriali, se un campo vettoriale può essere scritto come gradiente di una funzione scalare, il suo rotore è nullo,

$$\nabla \times \mathbf{F} = \mathbf{0} \ .$$



