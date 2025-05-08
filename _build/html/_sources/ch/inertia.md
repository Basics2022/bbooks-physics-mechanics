(classical-mechanics:inertia)=
# Inertia

Inertia deals with mass and mass distribution of systems.

**But what is mass?** Mass is a physical quantity, a property of the system, that manifests itself:
- in [gravitational attraction](classical-mechanics:actions:gravitation) (being both the origin of gravitational force and the property that makes a system sensible to gravitational attraction),
- in resistance to change of motion of a system under external [actions](classical-mechanics:actions), as it will be clear from principles and equations of motions in [dynamics](classical-mechanics:dynamics)

In the range of application of classical mechanics **mass conservation** holds, as stated by **Lavoisier principle**: the mass of a closed system is constant.

Beside mass, three main **additive dynamical quantities** are introduced: **momentum**, **angular momentum**, and **kinetic energy**. Even though their meaning could not be clear in this chapter, it would be clear in the following chapters, in the derivation of [equations of motion](classical-mechanics:dynamics:eom:eom) of mechanical systems, like [point mass](classical-mechanics:dynamics:eom:point), [system of point masses](classical-mechanics:dynamics:eom:points) and [rigid bodies](classical-mechanics:dynamics:eom:rigid),...


## Point mass

## Discrete masses

**Momentum.**

$$\vec{Q} := \sum_k m_k \vec{v}_k $$

**Angular momentum.**

$$\vec{L}_H := \int_{V_t} (P_k - H) \times m_k \vec{v}_k $$

**Kinetic energy.**

$$K := \sum_k \dfrac{1}{2} m_k |\vec{v}_k|^2$$

## Continuous systems

**Momentum.**

$$\vec{Q} := \int_{V_t} \rho \vec{v} $$

**Angular momentum.**

$$\vec{L}_H := \int_{V_t} (P - H) \times \rho \vec{v} $$

**Kinetic energy.**

$$K := \int_{V_t} \dfrac{1}{2} \rho |\vec{v}|^2$$

## Rigid systems

The expression of dynamical quantities for rigid bodies can be written in terms of the velocity $\vec{v}_Q$ of a point $Q$ of the rigid body and its angular velocity $\vec{\omega}$, exploiting the law of rigid motion {eq}`eq:kin:rigid:vel` to write the velocity of each points of the rigid system as functions of $\vec{v}_Q$ and $\vec{\omega}$,

$$\vec{v}_P = \vec{v}_Q + \vec{\omega} \times (P - Q) \ .$$

### Discrete systems

**Momentum.**

$$\begin{aligned}
  \vec{Q} = \sum_k m_k \vec{v}_k 
  & = \sum_k m_k \left( \vec{v}_Q + \vec{\omega} \times (P_k - Q) \right) = \\
  & = m \vec{v}_Q - \sum_k m_k (P_k - Q) \times \vec{\omega} = \\
  & = m \vec{v}_Q + \mathbb{S}_Q \cdot \vec{\omega} \ ,
\end{aligned}$$

having defined the static moment of inertia (a $2^{nd}$-order antisymmetric tensor)

$$\mathbb{S}_Q := \vec{s}_{P \times} := - \sum_k m_k (P_k - Q)_{\times} \ .$$

**Angular momentum.**

$$\begin{aligned}
  \vec{L}_H = \sum_k (P_k-H) \times  m_k \vec{v}_k 
  & = \underbrace{\sum_k (P_k-Q) \times m_k \vec{v}_k}_{\vec{L}_Q} + (Q - H) \times \vec{Q}
\end{aligned}$$

and

$$\begin{aligned}
\vec{L}_Q = \sum_k (P_k - Q) \times m_k \vec{v}_k 
 & = \sum_k (P_k - Q) \times m_k \left( \vec{v}_Q - (P_k - Q) \times \vec{\omega} \right) = \\
 & = \mathbb{S}_Q^T \cdot \vec{v}_Q + \mathbb{I}_Q \cdot \vec{\omega}  \ ,
\end{aligned}$$

having recognized the transpose of the static moment of inertia, and introduced the tensor of inertia w.r.t. reference point $Q$

$$\mathbb{I}_Q := - \sum_k m_k \left( P_k - Q \right)_{\times} \left( P_k - Q \right)_{\times} \ .$$


**Kinetic energy.**

$$\begin{aligned}
 K = \sum_k \dfrac{1}{2} m_k |\vec{v}_k|^2 
 & = \sum_k \dfrac{1}{2} m_k \left( \vec{v}_Q + \vec{\omega} \times (P_k - Q)  \right) \cdot \left( \vec{v}_Q + \vec{\omega} \times (P_k - Q) \right) = \\
 & = \sum_k \dfrac{1}{2} m_k | \vec{v}_Q |^2 + \dfrac{1}{2} \sum_k 2 m_k \vec{v}_Q \cdot \left( - (P_k - Q) \times \vec{\omega} \right) + \dfrac{1}{2} \sum_k \vec{\omega} \cdot (P_k - Q)_{\times} (P_k - Q)_\times \cdot \vec{\omega} = \\
 & = \dfrac{1}{2} \left[\sum_k m_k \right] | \vec{v}_Q |^2 
   + \dfrac{1}{2} \vec{v}_Q \cdot \left[ - \sum_k m_k (P_k - Q)_\times \right] \cdot \vec{\omega} + \\
 & + \dfrac{1}{2} \vec{\omega} \cdot \left[ \sum_k m_k (P_k - Q)_\times \right] \cdot \vec{v}_Q
   + \dfrac{1}{2} \vec{\omega} \cdot \left[ \sum_k m_k (P_k - Q)_{\times} (P_k - Q)_\times \right] \cdot \vec{\omega} = \\
 & = \dfrac{1}{2} m |\vec{v}_Q|^2 + \dfrac{1}{2} \vec{v}_Q \cdot \mathbb{S}_Q \cdot \vec{\omega} + \dfrac{1}{2} \vec{\omega} \cdot \mathbb{S}^T \cdot \vec{v}_Q + \dfrac{1}{2} \vec{\omega} \cdot \mathbb{I}_Q \cdot \vec{\omega} = \\
 & = \dfrac{1}{2} \vec{v}_Q \cdot \left[ m \vec{v}_Q + \mathbb{S}_Q \cdot \vec{\omega} \right] + \dfrac{1}{2} \vec{\omega} \cdot \left[  \mathbb{S}_Q^T \cdot \vec{v}_Q + \mathbb{I}_Q \cdot \vec{\omega} \right] = \\
 & = \dfrac{1}{2} \vec{v}_Q \cdot \vec{Q} + \dfrac{1}{2} \vec{\omega} \cdot \vec{L}_Q \ .
\end{aligned}$$ (eq:rigid:discrete:k)

having used the vector identities

$$\vec{a} \cdot \vec{b} \times \vec{c} = \vec{b} \cdot \vec{c} \times \vec{a}$$
$$\vec{a} \times \vec{b} = - \vec{b} \times \vec{a}$$

and having introduced the expression of momentum and angular momentum in the last step.


```{note}
The components of static moment of inertia and tensor of inertia in a material basis - following the motion of the system - are constant.
```


### Continuous systems

**Momentum.**

$$\begin{aligned}
  \vec{Q} = \int_{V_t} \rho \vec{v}
  & = \int_{V_t} \rho \left( \vec{v}_Q + \vec{\omega} \times (P - Q) \right) = \\
  & = m \vec{v}_Q - \int_{V_t} \rho (P_k - Q) \times \vec{\omega} = \\
  & = m \vec{v}_Q + \mathbb{S}_Q \cdot \vec{\omega} \ ,
\end{aligned}$$

having defined the static moment of inertia (a $2^{nd}$-order antisymmetric tensor) for continuous systems,

$$\mathbb{S}_Q := \vec{s}_{P \times} := - \int_{V_t} \rho (P - Q)_{\times} \ .$$

```{note}
Using the definition of the center of mass $G$,

$$G = \dfrac{1}{m} \int_{V_t} \rho P \ ,$$

the static moment of inertia can be written as

$$\mathbb{S}_Q = - \int_{V_t} \rho (P-Q)_{\times} = - m (G - Q)_{\times} \ .$$
```

```{note}
The components of static moment of inertia w.r.t. a material reference frame are constant. Using a material Carteisan reference frame the tensor reads

$$\begin{aligned}
\mathbb{S}_{Q} 
 & = - \int_{V_t} \rho (P - Q)_{\times} = \\
 & = - \int_{V_t} \rho \left[ ( x^0 - x_Q^0 ) \hat{x}^0 +  ( y^0 - y_Q^0 ) \hat{y}^0 +  ( z^0 - z_Q^0 ) \hat{z}^0 \right]_\times
 = S_{ij} \hat{e}^0_i \hat{e}^0_j \ ,
\end{aligned}$$

whose components can be collected in the **antisymmetric matrix**

$$\underline{\underline{S}}_Q = \left[ S_{Q,ij} \right] = - \int_{V_0} \rho \begin{bmatrix} 0 & -(z^0-z^0_Q) & (y^0-y^0_Q) \\ (z^0 - z_Q^0) & 0 & -(x^0-x_Q^0) \\ -(y^0-y^0_Q) & (x^0-x^0_Q) & 0 \end{bmatrix} \ ,$$

so that the vector product between $-\int_V \rho (P-Q)$ and a vector $\vec{a}$ reads

$$\begin{aligned}
  - \int_{V} \rho (P-Q) \times a
  & = - \int_V \rho \left[ \hat{x}^0 \left( \Delta y^0 a_z - \Delta z^0 a_y \right) + \hat{y}^0 \left( \Delta z^0 a_x - \Delta x^0 a_z \right) + \hat{z}^0 \left( \Delta x^0 a_y - \Delta y^0 a_x  \right) \right] \\
  & = \mathbb{S} \cdot \vec{a} \ .
\end{aligned}$$

```

**Angular momentum.**

$$\begin{aligned}
  \vec{L}_H = \int_{V_t} (P-H) \times  \rho \vec{v}
  & = \underbrace{\int_{V_t}(P-Q) \times \rho \vec{v}_k}_{\vec{L}_Q} + (Q - H) \times \vec{Q}
\end{aligned}$$

and

$$\begin{aligned}
\vec{L}_Q = \int_{V_t} (P - Q) \times \rho \vec{v}
 & = \int_{V_t} (P - Q) \times \rho \left( \vec{v}_Q - (P - Q) \times \vec{\omega} \right) = \\
 & = \mathbb{S}_Q^T \cdot \vec{v}_Q + \mathbb{I}_Q \cdot \vec{\omega}  \ ,
\end{aligned}$$

having recognized the transpose of the static moment of inertia, and introduced the tensor of inertia w.r.t. reference point $Q$

$$\begin{aligned}
  \mathbb{I}_Q
  & := - \int_{V_t} \rho \left( P - Q \right)_{\times} \left( P - Q \right)_{\times}  = \\
  & := \int_{V_t} \rho \left[ |P-Q|^2 \mathbb{I} - (P-Q) \otimes (P-Q) \right] \ ,
\end{aligned}$$

having used the tensor identity

$$- \vec{a}_{\times} \cdot \vec{a}_{\times} = |\vec{a}|^2 \mathbb{I} - \vec{a} \otimes \vec{a}$$


```{note}
The components of tensor of inertia w.r.t. a material reference frame are constant. Using a material Carteisan reference frame the tensor reads

$$\begin{aligned}
\mathbb{I}_{Q} 
 & = - \int_{V_t} \rho (P - Q)_{\times} (P-Q)_{\times} = \\
 & = - \int_{V_t} \rho \left[ |P-Q|^2 \mathbb{I} - (P-Q) \otimes (P-Q) \right] = \\
 & = I^0_{Q,ij} \hat{e}^0_i \hat{e}^0_j \ ,
\end{aligned}$$

whose components can be collected in the **symmetric matrix**

$$\underline{\underline{I}}^0_Q = \left[ I^0_{Q,ij} \right] = \int_{V_0} \rho \begin{bmatrix} \Delta y_0^2 + \Delta z_0^2 & -\Delta x_0 \Delta y_0 & -\Delta x_0 \Delta z_0 \\ -\Delta y_0 \Delta x_0 & \Delta x_0^2 + \Delta y_0^2 & -\Delta y_0 \Delta z_0 \\ -\Delta z_0 \Delta x_0 & - \Delta z_0 \Delta y_0 & \Delta x_0^2 + \Delta z_0^2 \end{bmatrix} \ ,$$

being $\Delta x^0 := x^0_P - x_Q^0$.

```

### Properties of inertia tensors of rigid bodies

#### Static inertia

**Center of mass, $G$.** Center of mass of of a rigid body is defined as the point $G$ for which $\mathbb{S}_G \equiv \mathbb{0}$, whose coordinates are given by

$$G = \dfrac{1}{m} \int_{V_t} \rho \, P$$

**Anti-symmetric.** From the definition of the static inertia tensor

$$\mathbb{S}_Q \cdot \vec{a} = \int_{V_t} \rho (P-Q) \times \vec{a} = - \vec{a} \times \int_{V_t} \rho (P-Q) = - \vec{a} \cdot \mathbb{S}_Q = - \mathbb{S}^T \cdot \vec{a} \ .$$

**Transport.**

$$\begin{aligned}
  \mathbb{S}_Q 
  & = - \int_{V_t} \rho (P - Q)_{\times} = \\
  & = - \int_{V_t} \rho (P - R)_{\times} - \int_{V_t} \rho (R - Q)_{\times} = \\
  & = \mathbb{S}_R - m (R-Q)_{\times} \ ,
\end{aligned}$$

or w.r.t. the center of mass $G$,

$$\mathbb{S}_Q = \mathbb{S}_G - m (G-Q)_{\times} \ .$$

#### Tensor of inertia

**Symmetric (semi)-definite positive.** Inertia tensor is symmetric

$$\vec{v} \cdot \mathbb{I}_Q \cdot \vec{w} = \vec{v} \cdot \int_{V_t} \rho \left[ |\Delta \vec{r}|^2 \mathbb{I} - \Delta \vec{r} \otimes \Delta \vec{r} \right] \cdot \vec{w} = \vec{w} \cdot \mathbb{I}_Q \cdot \vec{v} \ .$$

for all $\forall \vec{v}, \vec{w}$, and semi-definite positive

$$\begin{aligned}
  \vec{v} \cdot \mathbb{I}_Q \cdot \vec{v} 
  & = - \vec{v} \cdot \int_{V_t} \rho \Delta \vec{r}_{\times} \Delta \vec{r}_{\times} \cdot \vec{v} = \\
  & = - \int_{V_t} \rho \vec{v} \cdot \Delta \vec{r}_{\times} \Delta \vec{r}_{\times} \cdot \vec{v} = \\
  & = - \int_{V_t} \rho \vec{v} \cdot \left[ \Delta \vec{r} \times \left( \Delta \vec{r} \times \cdot \vec{v} \right) \right] = \\
  & = - \int_{V_t} \rho \left( \Delta \vec{r} \times \vec{v} \right) \cdot \left( \vec{v} \times  \Delta \vec{r} \right) = \\
  & =   \int_{V_t} \rho \left( \Delta \vec{r} \times \vec{v} \right) \cdot \left( \Delta \vec{r} \times \vec{v} \right) = \\
  & =   \int_{V_t} \rho | \Delta \vec{r} \times \vec{v} |^2 \ge 0 \\
\end{aligned}$$

**Principal axes of inertia.** As the tensor of inertia is symmetric and definite positive, a set of orthogonal vectors $\hat{E}^0_i$ so that it can be written in diagonal form,

$$\mathbb{I}_Q = I^0_{XX} \, \hat{E}^0_X \otimes \hat{E}^0_X +  I^0_{YY} \, \hat{E}^0_Y \otimes \hat{E}^0_Y + I^0_{ZZ} \, \hat{E}^0_Z \otimes \hat{E}^0_Z \ ,$$

with $I_{ii}^0 \ge 0$ (no sum).

```{prf:theorem} Transport - Huygens' theorem.
:label: thm:huygens

$$\begin{aligned}
  \mathbb{I}_Q 
  & = - \int_{V_t} \rho (P - Q)_{\times} (P-Q)_{\times} = \\
  & =    - \int_{V_t} \rho (P - R)_{\times} (P - R)_{\times}     
         - \int_{V_t} \rho (P - R)_{\times} (R - Q)_{\times} \\  
& \quad  - \int_{V_t} \rho (R - Q)_{\times} (P - R)_{\times}     
         - \int_{V_t} \rho (R - Q)_{\times} (R - Q)_{\times} = \\ 
  & = \mathbb{I}_R + \mathbb{S}_R \cdot (R-Q)_{\times} + (R-Q)_{\times} \cdot \mathbb{S}_R - m (R - Q)_{\times} (R - Q)_{\times}
\end{aligned}$$

or w.r.t. the center of mass $G$,

$$ \mathbb{I}_Q = \mathbb{I}_G - m (Q-G)_\times (Q-G)_\times \ .$$

```

### Time derivatives of dynamical quantities

Time derivatives of dynamical quantities are easily evaluated using a Cartesian material reference frame.

**Momentum.**

$$\begin{aligned}
\dfrac{d}{dt} \vec{Q} 
  & = \dfrac{d}{dt} \left( m \vec{v}_Q + \mathbb{S}_Q \cdot \vec{\omega} \right) =  \\
  & =  m \dot{\vec{v}}_Q + \dfrac{d}{dt} \left( \vec{E}^0_i S^0_{ij} \omega^0_j \right) = \\
  & =  m \dot{\vec{v}}_Q + \dfrac{d\vec{E}^0_i }{dt} S^0_{ij} \omega^0_j + \vec{E}^0_i S^0_{ij} \dfrac{d} \omega^0_j{dt} = \\
  & =  m \dot{\vec{v}}_Q + \vec{\omega} \times \vec{E}^0_i S^0_{ij} \omega^0_j + \vec{E}^0_i S^0_{ij} \dfrac{d}{dt}\omega^0_j = \\
  & =  m \dot{\vec{v}}_Q + \vec{\omega} \times \left( \mathbb{S}_Q \cdot \vec{\omega} \right) + \mathbb{S}_Q \cdot \dot{\vec{\omega}} \ .
\end{aligned}$$

$$\begin{aligned}
 \dfrac{d}{dt} \vec{\omega} 
 & = \dfrac{d}{dt} \left( \hat{E}^0_i \omega_i^0 \right) = \\
 & = \vec{\omega} \times \hat{E}^0_i \omega_i^0 + \hat{E}^0_i \dfrac{d \omega^0_i}{dt} = \\
 & = \underbrace{\vec{\omega} \times \vec{\omega}}_{=\vec{0}} + \hat{E}^0_i \dfrac{d \omega^0_i}{dt} \ .
\end{aligned}$$

$$\begin{aligned}
 \dfrac{d}{dt} \vec{v} 
 & = \dfrac{d}{dt} \left( \hat{E}^0_i v_i^0 \right) = \\
 & = \vec{\omega} \times \hat{E}^0_i v_i^0 + \hat{E}^0_i \dfrac{d v^0_i}{dt} = \\
 & = \vec{\omega} \times \vec{v}  + \dfrac{{}^0 d}{dt} \vec{v} \\
\end{aligned}$$


**Angular momentum.**

$$\begin{aligned}
\dfrac{d}{dt} \vec{L}_H
& =  \dfrac{d}{dt} \left( (Q-H) \times \vec{Q} + \vec{L}_Q  \right) \ ,
\end{aligned}$$

and

$$\dfrac{d}{dt} \left( (Q-H) \times \vec{Q} \right) = ( \vec{v}_Q - \dot{\vec{x}}_H ) \times \vec{Q} + ( Q - H ) \times \dot{\vec{Q}}$$

and

$$\begin{aligned}
 \dfrac{d \vec{L}_Q}{dt} 
 & = \dfrac{d}{dt} \left( \mathbb{S}^T_Q \cdot \vec{v}_Q + \mathbb{I}_Q \cdot \vec{\omega} \right) = \\
 & = \dfrac{d}{dt} \left[ \hat{E}_i^0 \left( S^0_{ji} v^0_{Q,j} + I^0_{ij} \omega^0_j \right) \right] = \\
 & = \vec{\omega} \times \hat{E}_i^0 \left( S^0_{ji} v^0_{Q,j} + I^0_{ij} \omega^0_j \right)
   + \hat{E}^0_i \left( S_{ji}^0 \dot{v}^0_{Q,j} + I^0_{ij} \dot{\omega}^0_j \right) = \\
 & = \vec{\omega} \times ( \mathbb{S}_Q^T \cdot \vec{v}_Q + \mathbb{I}_Q \cdot \vec{\omega} )
   + \left( \mathbb{S}_Q^T \cdot \dfrac{{}^0 d}{dt} \vec{v}_Q + \mathbb{I} \cdot \dot{\vec{\omega}} \right) = \\
 & = \vec{\omega} \times ( \mathbb{S}_Q^T \cdot \vec{v}_Q + \mathbb{I}_Q \cdot \vec{\omega} )
   + \left( \mathbb{S}_Q^T \cdot \left( \dot{v}_Q - \vec{\omega} \times \vec{v}_Q \right) + \mathbb{I} \cdot \dot{\vec{\omega}} \right) \\
 & = \left( \mathbb{S}_Q^T \cdot \left( \dot{v}_Q - \vec{\omega} \times \vec{v}_Q \right) + \mathbb{I} \cdot \dot{\vec{\omega}} \right) 
    + \vec{\omega} \times ( \mathbb{S}_Q^T \cdot \vec{v}_Q + \mathbb{I}_Q \cdot \vec{\omega} )
\end{aligned}$$

#### Dynamical quantities and time derivatives with $G$ as reference point

$$
\begin{cases}
  \vec{Q} = m \vec{v}_G \\
  \vec{L}_G = \mathbb{I}_G \cdot \vec{\omega}
\end{cases}
\qquad , \qquad
\begin{cases}
  \dot{\vec{Q}} = m \dot{\vec{v}}_G \\
  \dot{\vec{L}}_G = \mathbb{I}_G \cdot \dot{\vec{\omega}} + \vec{\omega} \times \mathbb{I}_G \cdot \vec{\omega}
\end{cases}$$






