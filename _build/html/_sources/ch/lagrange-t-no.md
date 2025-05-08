(classical-mechanics:lagrange:time:independent)=
# Lagrangian function with no explicit dependence on time
Let's analyse first some properties of systems, whose Lagrangian function are not an explicit function of time,

$$\mathscr{L}(\dot{q}^k(t), q^k(t)) = K(\dot{q}^k(t), q^k(t)) + U(q^k(t)) \ ,$$

and then go back to the most general case. 
As the Lagrange equation is not an explicit function of time, relation {eq}`eq:euler-beltrami` reads

$$\dfrac{d}{dt} \left[ \dot{q}^k \dfrac{\partial \mathscr{L}}{\partial \dot{q}^k} - \mathscr{L} \right] = \dot{q}^k Q_k \ .$$

Since the Lagrangian doesn't expliclty depend on time, and potential is not a function of time, relation {eq}`eq:lagrange:time:ind:dqdK_dq` gives $\dot{q}^k \frac{\partial \mathscr{L}}{\partial \dot{q}^k} = 2 K$, and thus the content of the braces is the mechanical energy of the system, 

$$\dot{q}^k \dfrac{\partial \mathscr{L}}{\partial \dot{q}^k} - \mathscr{L} = 2 K - \mathscr{L} = 2 K - K - U = K - U = E^{mec} \ ,$$

and it becomes clear that the relation is nothhing but the balance equation of mechanical energy

$$\dfrac{d E^{mec}}{dt} = \dot{q}^k Q_k \ ,$$

that becomes conservation of mechanical energy, in absence of non-conservative actions, $Q_k = 0$,

$$E^{mec} = \overline{E}^{mec} \quad \text{const.}$$


## Properties of kinetic energy and potential
This section collects some properties of the kinetic energy and potential of systems, where physical coordinates of the system are written as a function of generalized coordinates only, $q^k(t)$. As an example, coordinates of point masses, material points of rigid bodies and the rotation tensor representing their orientation in space can be written as

$$\vec{r}_P\left(q^k(t)\right) \quad , \quad \mathbb{R} \left( q^k(t) \right) \ ,$$

so that velocities and angular velocities become

$$\begin{aligned}
  \vec{v}_P\left(\dot{q}^k(t), q^k(t)\right) & = \dfrac{d \vec{r}_P}{dt} = \dot{q}^k \dfrac{\partial \vec{r}}{\partial q^k}\left(q^k(t)\right) \\ 
  \vec{\omega}_{\times}\left(\dot{q}^k(t), q^k(t)\right) & = \dfrac{d \mathbb{R}}{d t} \cdot \mathbb{R}^T = \dot{q}^k(t) \, \dfrac{\partial \mathbb{R}}{\partial q^k} \cdot \mathbb{R}^T = \dot{q}^k(t) \, \dfrac{\partial \vec{\theta}_{\times}}{\partial q^k}\left(q^k(t)\right) \ ,
\end{aligned}$$

As the kinetic energy of a mechanical system is a quadratic function of velocity and angular velocity of its sub-systems, the kinetic energy can be written as

$$K\left( \dot{q}^k(t), q^k(t) \right) = \frac{1}{2} A_{ij}\left(q^k(t)\right) \, \dot{q}^i(t) \, \dot{q}^j(t) \ .$$

Since $A_{ij}$ is symmetric w.r.t. the swap of indices (or it can be written in a symmetric form), partial derivative of the kinetic energy w.r.t. $\dot{q}^l$ reads

$$\dfrac{\partial K}{\partial \dot{q}^l} = A_{lj} \dot{q}^j \ ,$$

and 

$$\dot{q}^l \dfrac{\partial K}{\partial \dot{q}^l} = \dot{q}^l A_{lj} \dot{q}^j = 2 K \ .$$ (eq:lagrange:time:ind:dqdK_dq)


```{dropdown} Proofs

$$\begin{aligned}
  \dfrac{\partial K}{\partial \dot{q}^l} 
    = \dfrac{\partial }{\partial \dot{q}^l} \left[ \frac{1}{2} A_{ij} \dot{q}^i \dot{q}^j \right] 
    = \frac{1}{2} A_{ij} \bigg[ \underbrace{ \dfrac{\partial \dot{q}^i}{\partial \dot{q}^l} }_{\delta^i_l} \dot{q}^j + \dot{q}^i \underbrace{ \dfrac{\partial \dot{q}^j}{\partial \dot{q}^l}}_{\delta^j_l} \bigg]  
    = \frac{1}{2} \left[ A_{lj} \dot{q}^j + A_{il} \dot{q}^i \right]
    = A_{lj} \dot{q}^j
\end{aligned}$$


```


