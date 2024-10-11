```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-mechanics:dynamics:eom)=
# Equazioni cardinali della dinamica

Utilizzando i concetti di quantità di moto, momento della quantità di moto ed energia cinetica di un sistema, si possono scrivere le 3 equazioni cardinali della dinamica in una forma valida per **ogni sistema chiuso**. Nel caso siano soddisfatte alcune condizioni, e solo in questo caso, le equazioni cardinali della dinamica rappresentano dei principi di conservazione delle quantità dinamiche: osservando le espressioni delle equazioni cardinali, è facile intuire che la condizione da soddisfare per otenere un principio di conservazione è l'annullamento di tutti i termini ad eccezione della derivata temporale della quantità conservata.

## Equazioni cardinali

**Bilancio della quantità di moto.** La derivata nel tempo della quantità di moto è uguale alla risultante delle forze esterne,

$$\dot{\mathbf{Q}} = \mathbf{R}^e \ .$$ (principle:q)

**Bilancio del momento della quantità di moto rispetto a un polo $H$.** La derivata nel tempo del momento della quantità di moto rispetto a un punto $H$, a meno di "un termine di trasporto" è uguale alla risultate dei momenti esterni rispetto al polo $H$

$$\dot{\mathbf{L}}_H + \dot{\mathbf{x}}_H \times \mathbf{Q} = \mathbf{M}_H^e \ .$$ (principle:l)

**Bilancio dell'energia cinetica.** La derivata nel tempo dell'energia cinetica è uguale alla potenza totale agente sul sistema, risultato della somma della potenza delle azioni esterne e della potenza delle azioni interne al sistema

$$\dot{K} = P^{tot} = P^e + P^i$$ (principle:k)

## Principi di conservazione

**Conservazione della quantità di moto, in presenza di forze esterne con risultante nulla.** Se la risultante delle forze esterne è nulla, $\mathbf{R}^e = \mathbf{0}$, dal bilancio della quantità di moto segue immediatamente

$$\dot{\mathbf{Q}} = \mathbf{0} \qquad \rightarrow \qquad \mathbf{Q} = \bar{\mathbf{Q}} = \text{cost.}$$

**Conservazione del momento della quantità di moto, in presenza di momenti esterni con risultante nulla.** Se la scelta del polo $H$ rende nullo il termine di trasporto, $\dot{\mathbf{r}}_H \times \mathbf{Q} = \mathbf{0}$, se la risultante dei momenti esterni è nulla, $\mathbf{M}^e_H = \mathbf{0}$, dal bilancio del momento della quantità di moto segue immediatamente

$$\dot{\mathbf{L}}_H = \mathbf{0} \qquad \rightarrow \qquad \mathbf{L}_H = \bar{\mathbf{L}}_H = \text{cost.}$$

**Conservazione dell'energia cinetica, in presenza di potenza totale nulla.** Se la potenza totale delle azioni sul sistema è nulla, $P^{tot} = 0$, dal bilancio dell'energia cinetica segue immediatamente

$$\dot{K} = 0 \qquad \rightarrow \qquad K = \bar{K} = \text{cost.}$$

**Conservazione dell'energia meccanica, in assenza di azioni non conservative.** Ai tre principi di conservazione direttamente ottenibili dalle equazioni cardinali, si aggiunge il principio della conservazione dell'energia meccanica, somma dell'energia cinetica e dell'energia potenziale del sistema,

$$E^{mech} = K + V \ ,$$

in assenza di azioni non conservative. Se non ci sono forze non conervative, la potenza delle azioni agenti sul sistema può essere scritta come l'opposto della derivata nel tempo dell'energia potenziale del sistema,

$$P^{tot} = -\dot{V}$$

Dal bilancio dell'energia cinetica segue

$$\dot{K} = - \dot{V} \qquad \rightarrow \qquad \dfrac{d}{dt}(K+V) = 0 \qquad \rightarrow \qquad \dot{E}^{mech = 0} \qquad \rightarrow \qquad E^{mech} = \bar{E}^{mech} = \text{const.}$$
