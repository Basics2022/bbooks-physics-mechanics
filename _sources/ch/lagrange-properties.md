(classical-mechanics:lagrange:properties)=
# Properties of the Lagrangian approach to classical mechanics

(classical-mechanics:lagrange:properties:kinetic-energy)=
## Kinetic energy $K$ and potential function $U$

Kinetic energy of each component is a symmetric function of the velocity of its reference point $P$ and its angular velocity $\vec{\omega}$, as shown as an example by the expression of the kinetic energy of a rigid body,

$$\begin{aligned}
  K_P 
  & = \dfrac{1}{2} \vec{v}_P \cdot \vec{Q} + \dfrac{1}{2} \vec{\omega} \cdot \vec{L}_P \\
  & = \dfrac{1}{2} \vec{v}_P \cdot \left[ m \vec{v}_P + \mathbb{S}_P \cdot \vec{\omega} \right] 
    + \dfrac{1}{2} \vec{\omega} \cdot \left[ \mathbb{S}_P^T \cdot \vec{v}_P + \mathbb{I}_P \cdot \vec{\omega} \right] \ ,
\end{aligned}$$

as the tensor of inertia $\mathbb{I}_P$ is symmetric, i.e. $\vec{a} \cdot \mathbb{I}_P \cdot \vec{b} = \vec{b} \cdot \mathbb{I}_P \cdot \vec{a}$, $\forall \vec{a}, \vec{b}$.

**todo** *Treat continuous deformable systems.*

**Kinetic energy of a system**, with no explicit dependence of time of the degrees of freedom is a symmetric positive definite quadratic function.

$$K = \dfrac{1}{2} \sum_{ik} M_{ik}\left(q^l(t)\right) \dot{q}^i \dot{q}^k = \dfrac{1}{2} \dot{\mathbf{q}}^T \mathbf{M}(\mathbf{q}) \dot{\mathbf{q}} \ ,$$

with $M_{ik} = M_{ki}$, and $K \ge 0$.

```{dropdown} Kinetic energy symmetric quadratic form of generalized coordinates.

If degrees of freedom of the system can be written as functions of  the generalized coordinates $q^k(t)$, with no explicit dependence on time $t$, 

$$\vec{r}_P\left( q^k(t)\right) \qquad , \qquad \mathbb{R}\left( q^k(t) \right) \ ,$$

velocities and angular velocities becomes

$$\begin{aligned}
       \vec{v}_P\left( \dot{q}^k(t), q^k(t) \right) & = \dot{q}^k \dfrac{\partial \vec{r}_P}{\partial q^k}\left( q^k(t) \right) \\
  \vec{\omega}_P\left( \dot{q}^k(t), q^k(t) \right) & = \dot{q}^k \dfrac{\partial \vec{\theta}_P}{\partial q^k}\left( q^k(t) \right) \\
\end{aligned}$$

The kinetic energy of the system is the sum of the kinetic energy of its parts and thus

$$\begin{aligned}
  K = \sum_P K_P 
  & = \sum_P \left\{ \dfrac{1}{2} \vec{v}_P \cdot \left[ m \vec{v}_P + \mathbb{S}_P \cdot \vec{\omega} \right] 
                   + \dfrac{1}{2} \vec{\omega} \cdot \left[ \mathbb{S}_P^T \cdot \vec{v}_P + \mathbb{I}_P \cdot \vec{\omega} \right]  \right\} = \\
  & = \sum_P \left\{ \dfrac{1}{2} \sum_i \dot{q}^i \partial_{q^i} \vec{r}_P \cdot \left[ m \sum_k \dot{q}^k \partial_{q^k} \vec{r}_P + \mathbb{S}_P \cdot \sum_k \dot{q}^k \partial_{q^k} \vec{\theta}_P \right] \right. + \\ 
  &  \qquad \left. + \dfrac{1}{2} \sum_i \dot{q}^i \partial_{q^i} \vec{\theta}_P  \cdot \left[ \mathbb{S}_P^T \cdot \sum_k \dot{q}^k \partial_{q^k} \vec{r}_P + \mathbb{I}_P \cdot \sum_k \dot{q}^k \partial_{q^k} \vec{\theta}_P \right]  \right\} = \\
  & = \dfrac{1}{2} \sum_{i,k} \sum_P \left\{ m \partial_i \vec{r}_P \cdot \partial_k \vec{r}_P + \partial_i \vec{r}_P \cdot \mathbb{S}_P \cdot \partial_k \vec{\theta}_P + \partial_i \vec{\theta}_P \cdot \mathbb{S}_P^T \cdot \partial_k \vec{r}_P + \partial_i \vec{\theta}_P \cdot \mathbb{I}_P \cdot \partial_k \vec{\theta}_P  \right\} \dot{q}^i \dot{q}^k = \\
  & = \dfrac{1}{2} \sum_{ik} M_{ik} \dot{q}^i \, \dot{q}^k \ ,
\end{aligned}$$

with the coefficients $M_{ik}(q^l(t))$ symmetric w.r.t. a swap of the indices $i$, $k$ by definition.

```

**Potential function** is a function of generalized coordinates only, $U(\mathbf{q})$.

(classical-mechanics:lagrange:properties:lagrange-equations)=
## Lagrange equations

**Lagrangian function** is

$$L(\dot{\mathbf{q}}, \mathbf{q}) = K(\dot{\mathbf{q}}, \mathbf{q}) + U(\mathbf{q}) = \dfrac{1}{2} \dot{\mathbf{q}}^T \mathbf{M}(\mathbf{q}) \dot{\mathbf{q}} + U\left(\mathbf{q} \right)$$

(classical-mechanics:lagrange:properties:lagrange-equations:ii)=
### Lagrange equations of the II kind

**Lagrange equations of the II kind** read

$$\begin{aligned}
  \mathbf{Q}_{\mathbf{q}}
  & = \dfrac{d}{dt} \left( \partial_{\dot{\mathbf{q}}} L  \right) - \partial_{\mathbf{q}} L =  \\
  & = \dfrac{d}{dt} \left( \mathbf{M}(\mathbf{q}) \dot{\mathbf{q}} \right) - \partial_{\mathbf{q}} \left( \dfrac{1}{2} \dot{\mathbf{q}}^T \mathbf{M}(\mathbf{q}) \dot{\mathbf{q}} + U (\mathbf{q}) \right) \ ,
\end{aligned}$$

$$\begin{aligned}
 Q_i 
 & = \dfrac{d}{dt} \left( M_{ij}(q^k) \dot{q}^j \right) - \partial_{q^i} \left( \dfrac{1}{2} \dot{q}^a M_{ab}(q^k) \dot{q}^b + U(q^k) \right) = \\
 & = \partial_{q^k} M_{ij}(q^l) \dot{q}^k \dot{q}^j + M_{ij} \ddot{q}^j - \dfrac{1}{2} \partial_{q^i} M_{kj}(q^l) \dot{q}^k \dot{q}^j - \partial_{q^i} U(q^l) \\
\end{aligned}$$

$$\begin{aligned}
  M_{ij} (q^l) \ddot{q}^j - \partial_{q^i} U(q^l) + \partial_{q^k} M_{ij}(q^l) \dot{q}^k \dot{q}^j - \frac{1}{2} \partial_{q^i} M_{kj}(q^l) \dot{q}^k \dot{q}^j & = Q_i \\
  \mathbf{M}(\mathbf{q}) \ddot{\mathbf{q}} - \nabla_{\mathbf{q}} U(\mathbf{q}) + \dot{\mathbf{q}}^T \nabla_{\mathbf{q}} \left( \mathbf{M} \dot{\mathbf{q}} \right) - \frac{1}{2} \nabla_{\mathbf{q}} \left( \dot{\mathbf{q}}^T \mathbf{M} \dot{\mathbf{q}} \right) & = \mathbf{Q}
\end{aligned}$$

**Equilibrium conditions** correspond to steady solutions of the equations of motion,

$$-\nabla_{\mathbf{q}} U (\overline{\mathbf{q}}) = \mathbf{Q}(\overline{\mathbf{q}}) \ .$$

**Linearized system** around a (stable) equilibrium follows from the approximation 

$$\begin{aligned}
  \mathbf{q}        & = \overline{\mathbf{q}} + \mathbf{q}'  \\
  \dot{\mathbf{q}}  & =                    \dot{\mathbf{q}}' \\
  \ddot{\mathbf{q}} & =                   \ddot{\mathbf{q}}' \ ,
\end{aligned}$$

and neglecting higher-order contributions in $\mathbf{q}'$,

$$\begin{aligned}
Q_i (\mathbf{q})
  & = M_{ij}(\mathbf{q}) \ddot{q}^j - \partial_i U(\mathbf{q}) + \dot{q}^k \partial_k M_{ij}(\mathbf{q}) \dot{q}^j - \frac{1}{2} \partial_i M_{jk}(\mathbf{q}) \dot{q}^j \dot{q}^k  \\
  Q_i(\overline{\mathbf{q}}) + {q^{k}}' \partial_{q^k} Q_i(\overline{\mathbf{q}}) & \sim M_{ij}(\overline{\mathbf{q}}) \ddot{q}^j - \partial_i U(\overline{\mathbf{q}}) - q^{j'} \partial_{ij} U(\overline{\mathbf{q}}) \\
\end{aligned}$$

$$\begin{aligned}
    M_{ij}(\overline{\mathbf{q}}) \ddot{q}'_j + \left[ - \partial_{ij} U(\overline{\mathbf{q}}) - \partial_j Q_i(\overline{\mathbf{q}}) \right] q'_j  & = 0 \\
    \mathbf{M}(\overline{\mathbf{q}}) \ddot{\mathbf{q}}' + \left[ - \nabla \nabla U(\overline{\mathbf{q}}) \right] \mathbf{q}' & = \nabla \mathbf{Q}^T (\overline{\mathbf{q}}) \mathbf{q}' \\
    \mathbf{M}(\overline{\mathbf{q}}) \ddot{\mathbf{q}}' + \mathbf{K}(\overline{\mathbf{q}}) \mathbf{q}' & = \nabla \mathbf{Q}^T(\overline{\mathbf{q}})\mathbf{q}' \ .
\end{aligned}$$

**Matrices are symmetric.** Mass matrix is symmetric by construction, as already proved. Stiffness matrix is symmetric as well, due to Schwarz's theorem, as its the Hessian of a scalar function, $\left[ \nabla \nabla U \right]_{ij} = \partial_{ij} U$

**Matrices are (semi)-definite positive.** Mass matrix is definite positive by definition, $\mathbf{M} > 0$, as already proved above as the kinetic energy is a non-negative scalar physical quantity. Stiffness matrix is definite positive if the **equilibrium $\overline{\mathbf{q}}$ is stable**: $\nabla \nabla U(\overline{\mathbf{q}}) < 0$ implies $\mathbf{K} > 0$.

**Spectrum of a stable system.** **todo** *add a link to structure mechanics in continuum mechanics, and modal approach*


(classical-mechanics:lagrange:properties:lagrange-equations:i)=
### Lagrange equations of the I kind

Recasting the expression of the dynamical equations of an "uncostrained" system (or with some constraints treated implicitly with Lagrange equations of II kind),

$$\mathbf{M}(\mathbf{q}) \ddot{\mathbf{q}} = \mathbf{f}(\mathbf{q}, \dot{\mathbf{q}}) \ ,$$

and then adding constraints - at least holonomic or semi-linear non-holonomic constraints - and the costraint reactions, the system becomes

$$\begin{aligned}
  & \mathbf{M}(\mathbf{q}) \ddot{\mathbf{q}} = \mathbf{f}(\mathbf{q}, \dot{\mathbf{q}}) + \nabla_\mathbf{q} \mathbf{g}(\mathbf{q}) \, \mathbf{s} \\
  & \mathbf{g}(\mathbf{q}, \dot{\mathbf{q}}) = \mathbf{0}
\end{aligned}$$

with either $\mathbf{g}(\mathbf{q}) = \mathbf{0}$ for holonomic time-independent constraints, or $\mathbf{g}(\mathbf{q}, \dot{\mathbf{q}}) = \mathbf{a}(\mathbf{q}) \dot{\mathbf{q}} = \mathbf{0}$ for semi-linear non-holonomic time-independent constraints, with the forcing term $\mathbf{f}$ containing the non-conservative forces $\mathbf{Q}$ (or at least contributions not included in the potential $U(\mathbf{q})$), the conservative forces $\nabla_{\mathbf{q}} U(\mathbf{q})$, and the (*quadratic!* Important for neglecting them in linearization) contributions from time derivative of kinetic energy,

$$\mathbf{f}(\mathbf{q}, \dot{\mathbf{q}}) = \mathbf{Q} + \nabla_{\mathbf{q}} U(\mathbf{q}) - \dot{\mathbf{q}}^T \nabla_{\mathbf{q}} \left( \mathbf{M}(\mathbf{q}) \dot{\mathbf{q}} \right) + \frac{1}{2} \nabla_{\mathbf{q}} \left( \dot{\mathbf{q}}^T \mathbf{M}(\mathbf{q}) \dot{\mathbf{q}} \right) \ .$$

**Linearized equations** become

$$\begin{aligned}
 & \mathbf{M}(\overline{\mathbf{q}}) \ddot{\mathbf{q}}' + \mathbf{K}(\overline{\mathbf{q}}) \mathbf{q}' = \mathbf{Q}' + \nabla_{\mathbf{q}} \mathbf{g}(\overline{\mathbf{q}}) \mathbf{s}' + \mathbf{q}' \nabla_{\mathbf{q}} \nabla_{\mathbf{q}} \mathbf{g}(\overline{\mathbf{q}}) \mathbf{s} \\
 & \nabla_{\dot{\mathbf{q}}}^T \mathbf{g}(\overline{\mathbf{q}}, \mathbf{0}) \, \dot{\mathbf{q}}' + \nabla_{\mathbf{q}}^T \mathbf{g}(\overline{\mathbf{q}}, \mathbf{0}) \, \mathbf{q}' = \mathbf{0}
\end{aligned}$$






