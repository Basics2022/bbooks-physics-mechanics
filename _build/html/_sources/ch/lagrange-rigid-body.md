(classical-mechanics:lagrange:rigid)=
# Rigid Body

**Newton dynamical equations - strong form.** Dynamical equations governing the motion of a rigid body, referred to its center of mass $G$ read

$$\begin{cases}
  \dot{\vec{Q}} = \vec{R}^{e} \\
  \dot{\vec{\Gamma}}_G = \vec{M}^e_G \ ,
\end{cases}$$

with momentum $\vec{Q} = m \vec{v}_G$ and angular momentum $\vec{\Gamma}_G = \mathbb{I}_G \cdot \vec{\omega}$.

**Weak form.** Weak form of dynamical equations is derived with scalar multiplication of the strong form by an arbitrary test functions $\vec{w}_t$, $\vec{w}_r$

$$\vec{0} = \vec{w}_t \cdot \left( m \dot{\vec{v}}_G - \vec{R}^e\right) + \vec{w}_r \cdot \left( \dot{\vec{\Gamma}}_G - \vec{M}^e_G \right) \qquad \forall \vec{w}_t, \, \vec{w}_r$$ (eq:lagrange:rigid:weak)

**Lagrange equations.** Lagrange equations are derived from the weak form, with a proper choice of the weak test functions. The "translational part" is recasted after choosing

$$\vec{w}_t = \frac{\partial \vec{r}}{\partial q^k} = \frac{\partial \vec{v}}{\partial \dot{q}^k} \ .$$

Following the same steps show to derive [Lagrange equations for a point system](classical-mechanics:lagrange:point), the translational part becomes

$$\dfrac{d}{dt}\frac{\partial K^{tr}}{\partial \dot{q}^k} - \frac{\partial K^{tr}}{\partial q^k} - \frac{\partial U^{tr}}{\partial q^{k}} = Q^{tr}_{k} \ ,$$

being $K^{tr} = \frac{1}{2} m |\vec{v}_G|^2$ the contribution to kinetic energy of the velocity of the center of mass $G$ deriving from the momentum equation, $U^{tr}$ the contribution to the potential energy $U$ from the momentum equation, and $Q^{tr}_{k}$ the contribution to the generalized force from the momentum equation.

The "rotational part" is recasted after choosing 

$$\vec{w}_r = \frac{\partial \vec{\theta}}{\partial q^k} = \frac{\partial \vec{\omega}}{\partial \dot{q}^k} $$

Angular velocity $\vec{\omega}$ can be written w.r.t the inertial $\{ \hat{e}_i \}$ or the material reference frame $\{ \hat{E}_i \}$,

$$\vec{\omega} = \omega_i \hat{e}_i = \sigma_j \hat{E}_j \ ,$$

and the inertia tensor as

$$\mathbb{I}_G = I_{ij} \, \hat{E}_i \otimes \hat{E}_j \ ,$$

being the components $I_{ij}$ constant.

$$0 = \frac{\partial \vec{\omega}}{\partial \dot{q}^k} \cdot \dfrac{d}{d t} \left( \mathbb{I}_G \cdot \vec{\omega} \right) - \frac{\partial \vec{\omega}}{\partial \dot{q}^k } \cdot \vec{M}^e_G = \dfrac{d}{dt}\left( \frac{\partial \vec{\omega}}{\partial \dot{q}^k} \cdot \mathbb{I}_G \cdot \vec{\omega} \right) - \dfrac{d}{dt} \frac{\partial \vec{\omega}}{\partial \dot{q}^k} \cdot \mathbb{I}_G \cdot \vec{\omega} - \frac{\partial \vec{\theta}}{\partial q^k} \cdot \vec{M}^e_G$$

The first term becomes

$$\dfrac{d}{dt}\left( \frac{\partial \vec{\omega}}{\partial \dot{q}^k} \cdot \mathbb{I}_G \cdot \vec{\omega} \right) = \dfrac{d}{dt} \left( \frac{\partial \sigma_a}{\partial \dot{q}^k} I_{ab} \sigma_b \right) = \dfrac{d}{dt} \dfrac{\partial}{\partial \dot{q}^k}\left( \dfrac{1}{2} \vec{\omega} \cdot \mathbb{I}_G \cdot \vec{\omega} \right) = \dfrac{d}{dt}\dfrac{\partial K^{rot}}{\partial \dot{q}^k}$$

The second term becomes

$$\begin{aligned}
 \dfrac{d}{dt} \frac{\partial \vec{\theta}}{\partial q^k} \cdot \mathbb{I}_G \cdot \vec{\omega} 
  & = \dfrac{\partial }{\partial q^k} \underbrace{\dfrac{d \vec{\theta}}{d t}}_{\vec{\omega}} \cdot \mathbb{I}_G \cdot \vec{\omega} = \\
  & = \dfrac{\partial \vec{\omega}}{\partial q^k} \cdot \mathbb{I}_G \cdot \vec{\omega} = \\
  & = \dfrac{\partial}{\partial q^k} \left( \sigma_a \hat{E}_a \right) \cdot \hat{E}_b \, I_{bc} \sigma_c = \\
  & = \dfrac{\partial \sigma_a}{\partial q^k} \underbrace{\hat{E}_a \cdot \hat{E}_b}_{= \delta_{ab}} \, I_{bc} \sigma_c 
    + \sigma_a \underbrace{\dfrac{\partial \hat{E}_a}{\partial q^k}  \cdot \hat{E}_b}_{= 0} \, I_{bc} \sigma_c = \\
  & = \dfrac{\partial}{\partial q^k} \left( \frac{1}{2} \sigma_a \, I_{ab} \sigma_b \right) = \\
  & = \dfrac{\partial }{\partial q^k} \left( \frac{1}{2} \vec{\omega} \cdot \mathbb{I}_G \cdot \vec{\omega} \right) 
    = \dfrac{\partial K^{rot}}{\partial q^k} \ .
\end{aligned}$$

The third term can be written as the sum of the derivative of a potential function and a generalized force,

$$\frac{\partial \vec{\theta}}{\partial q^k} \cdot \vec{M}_G^e = \frac{\partial U^{rot}}{\partial q^k} + Q^{rot}_{q^k}$$

The rotational part of the wak form becomes

$$\dfrac{d}{dt}\frac{\partial K^{rot}}{\partial \dot{q}^k} - \frac{\partial K^{rot}}{\partial q^k} - \frac{\partial U^{rot}}{\partial q^{k}} = Q^{rot}_{q^k} \ ,$$

being $K^{rot} = \frac{1}{2} \vec{\omega} \cdot \mathbb{I}_G \cdot \vec{\omega}$ the contribution to kinetic energy of the rotation aroung the center of mass $G$ deriving from the angular momentum equation, $U^{rot}$ the contribution to the potential energy $U$ from the angular momentum equation, and $Q^{rot}_{k}$ the contribution to the generalized force from the angular momentum equation.

Adding together the contributions of the momentum and the angular momentum equations, the Lagrange equation can be formally written with the same expression found for the system of points,

$$\dfrac{d}{dt}\left(\frac{\partial \mathscr{L}}{\partial \dot{q}^k}\right) - \frac{\partial \mathscr{L}}{\partial q^k} = Q_{q^k} \ ,$$

being $\mathscr{L} = K + U$ the Lagrangian function of the system, and $K = K^{tr} + K^{rot}$, $U = U^{tr} + U^{rot}$, $Q_{q^k} = Q_{q^k}^{tr} + Q_{q^k}^{rot}$ the kinetic energy the potential function and the generalized force of the system, defined as the sum of the contributions coming from the momentum and the angular momentum equations.

<!--
$$\vec{w}_r = \frac{\partial \theta_l}{\partial q^k} \, \hat{e}_l = - \frac{1}{2} \varepsilon_{lab} \dfrac{\partial R_{ac}}{\partial q^k} R_{bc} \, \hat{e}_l$$
-->
