```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-mechanics:dynamics:eom:points)=
# Equazioni cardinali della dinamica: sistemi discreti di punti materiali

Partendo dalle equazioni dinamiche per un punto, si calcolano le equazioni dinamiche per un sistema di punti, sfruttando il terzo principio della dinamica di azione/reazione. Lo sviluppo delle equazioni permette di comprendere che la natura additiva delle grandezze dinamiche (quantità di moto, momento della quantità di moto, energia cinetica) segue direttamente dalla loro definizione.

**Bilancio della quantità di moto.**
E' possibile scrivere il bilancio della quantità di moto per ogni punto $i$ del sistema, scrivendo la risultante delle forze esterne agente sul punto come la somma delle forze esterne all'intero sistema agenti sul punto e le forze interne scambiate con gli altri punti del sistema,

$$\mathbf{R}_i{ext,i} = \mathbf{F}_i^{ext} + \sum_{j \ne i} \mathbf{F}_{ij} \ .$$

L'equazione di bilancio per la $i$-esima massa diventa quindi

$$\dot{\mathbf{Q}}_i = \mathbf{R}_i{ext,i} = \mathbf{F}_i^{ext} + \sum_{j \ne i} \mathbf{F}_{ij} \ .$$

Sommando le equazioni di bilancio di tutte le masse, si ottiene

$$\begin{aligned}
\sum_{i} \dot{\mathbf{Q}}_i & = \sum_i \mathbf{F}_{i}^{ext} + \sum_i \sum_{j \ne i} \mathbf{F}_{ij} = \\
                            & = \sum_i \mathbf{F}_{i}^{ext} + \sum_{\{i,j\}} \underbrace{\left( \mathbf{F}_{ij} + \mathbf{F}_{ji} \right)}_{=\mathbf{0}} 
\end{aligned}$$

e definendo la quantità di moto di un sistema come la somma delle quantità di moto delle sue parti e la risultante delle forze esterne come somma delle forze esterne agenti sulle parti del sistema, 

  $$\mathbf{Q} := \sum_i \mathbf{Q}$$
  $$\mathbf{R}^e := \sum_i \mathbf{F}_i^{ext}$$

si ritrova la forma generale del bilancio della quantità di moto,

$$\dot{\mathbf{Q}} = \mathbf{R}^e \ .$$

**Bilancio del momento della quantità di moto.**
E' possibile scrivere il bilancio del momento della quantità di moto per ogni punto $i$ del sistema, scrivendo la risultante dei momenti esterni agente sul punto come la somma dei momenti esterni all'intero sistema agenti sul punto e i momenti interni scambiati con gli altri punti del sistema,

$$\mathbf{M}_{H,i}^{ext,i} = \mathbf{M}_{H,i}^{ext} + \sum_{j \ne i} \mathbf{M}_{H,ij} \ .$$

Nel caso le parti del sistema interagiscano tramite forze, il momento rispetto al polo $H$ generato dalla massa $j$ sulla massa $i$ vale

$$\mathbf{M}_{H,ij} = (\mathbf{r}_i - \mathbf{r}_H) \times \mathbf{F}_{ij} \ .$$

L'equazione di bilancio per la $i$-esima massa diventa quindi

$$\dot{\mathbf{L}}_{H,i} + \dot{\mathbf{r}}_H \times \mathbf{Q}_i = \mathbf{M}_{H,i}^{ext,i} = \mathbf{M}_{H,i}^{ext} + \sum_{j \ne i} \mathbf{M}_{H,ij} \ .$$

Sommando le equazioni di bilancio di tutte le masse, si ottiene

$$\begin{aligned}
\sum_{i} \left( \dot{\mathbf{L}}_i + \dot{\mathbf{r}}_H \times \mathbf{Q}_i \right) & = \sum_i \mathbf{M}_{H,i}^{ext} + \sum_i \sum_{j \ne i} \mathbf{M}_{H,ij} = \\
                            & = \sum_i \mathbf{M}_{H,i}^{ext} + \sum_{\{i,j\}} \underbrace{\left( \mathbf{M}_{H,ij} + \mathbf{M}_{H,ji} \right)}_{=\mathbf{0}} 
\end{aligned}$$

e riconoscendo la quantità di moto del sistema e derinendo il momento della quantità di moto di un sistema come la somma delmomento della quantità di moto delle sue parti e la risultante dei momenti esterni come somma dei momenti esterni agenti sulle parti del sistema, 

  $$\mathbf{L}_H := \sum_i \mathbf{L}_{H,i}$$
  $$\mathbf{M}_H^e := \sum_i \mathbf{M}_{H,i}^{ext}$$

si ritrova la forma generale del bilancio del momento della quantità di moto,

$$\dot{\mathbf{L}}_{H} + \dot{\mathbf{r}}_H \times \mathbf{Q} = \mathbf{M}_H^e \ .$$

**Bilancio dell'energia cinetica.**

