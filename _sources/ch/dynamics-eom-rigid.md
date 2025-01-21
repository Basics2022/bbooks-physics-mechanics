<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-mechanics:dynamics:eom:rigid)=
# Equations of motion of a rigid body

With different choices of the reference point $H$, the general expression of dynamical equations may have different, but equivalent, forms.

## General equations
**Momentum balance equation.**

$$\dfrac{d}{dt} \vec{Q} = \vec{R}^e$$

**Angular momentum balance equation.**

$$\dfrac{d}{dt} \vec{L}_H + \dot{\vec{x}}_H \times \vec{Q} = \vec{M}_H^e$$

**Kinetic energy balance equation.**

$$\dfrac{d}{dt} K = P^{tot}$$

## Dynamical equations w.r.t. the center of mass $G$

**Momentum, angular momentum and kinetic energy**

$$
\begin{cases}
 \vec{Q} = m \vec{v}_G \\
 \vec{L}_G = \mathbb{I}_G \cdot \vec{\omega} \\
 K = \frac{1}{2} m |\vec{v}_G|^2 + \frac{1}{2} \vec{\omega} \cdot \mathbb{I}_G \cdot \vec{\omega} \\
\end{cases}
\qquad , \qquad
\begin{cases}
 \dot{\vec{Q}} = m \dot{\vec{v}}_G \\
 \dot{\vec{L}}_G = \mathbb{I}_G \cdot \dot{\vec{\omega}} + \vec{\omega} \times \mathbb{I}_G \cdot \vec{\omega} \\
 \dot{K} = m \vec{v}_G \cdot \dot{\vec{v}}_G + \vec{\omega} \cdot \mathbb{I}_G \cdot \dot{\vec{\omega}}
\end{cases}
$$

**Equations of motion.**

$$
\begin{cases}
 \dot{\vec{Q}} = \vec{R}^e \\
 \dot{\vec{L}}_G = \vec{M}_G^e \\
\end{cases}
\qquad , \qquad
\begin{cases}
 m \dot{\vec{v}}_G = \vec{R}^e \\
 \mathbb{I}_G \cdot \dot{\vec{\omega}} + \vec{\omega} \times \mathbb{I}_G \cdot \vec{\omega} = \vec{M}_G^e \\
\end{cases}
$$


```{dropdown} Time derivative of kinetic energy

$$\begin{aligned}
  \dfrac{d K}{dt}
  & = \dfrac{1}{2} \dfrac{d}{dt} \left( \vec{v}_G \cdot \vec{Q} + \vec{\omega}_G \cdot \vec{L}_G \right) = \\
  & = \dfrac{1}{2} \left( \dot{\vec{v}}_G \cdot m \vec{v}_G + \vec{v}_G \cdot m \dot{\vec{v}}_G + \dot{\vec{\omega}} \cdot \mathbb{I}_G \cdot \vec{\omega} + \vec{\omega} \cdot \left(  \mathbb{I} \cdot \dot{\vec{\omega}} + \vec{\omega} \times \mathbb{I}_G \cdot \vec{\omega} \right) \right) \\
  & = \vec{v}_G \cdot m \dot{\vec{v}}_G + \vec{\omega} \cdot \mathbb{I}_G \cdot \dot{\vec{\omega}} \\
  & = \vec{v}_G \cdot \dot{\vec{Q}} + \vec{\omega} \cdot \dot{\vec{L}}_G \\
  & = \dot{\vec{v}}_G \cdot \vec{Q} + \dot{\vec{\omega}} \cdot \vec{L}_G \ .
\end{aligned}$$

```

## Dynamical equations w.r.t. a material point $Q$

**Momentum, angular momentum and kinetic energy**

$$
\begin{cases}
 \vec{Q} = m \vec{v}_Q + \mathbb{S}_Q \cdot \vec{\omega} \\
 \vec{L}_Q = \mathbb{S}_Q^T \cdot \vec{v}_Q + \mathbb{I}_Q \cdot \vec{\omega} \\
 K = \dfrac{1}{2} \vec{v}_Q \cdot \vec{Q} + \dfrac{1}{2} \vec{\omega} \cdot \vec{L}_Q
\end{cases}
\qquad , \qquad
\begin{cases}
 \dot{\vec{Q}} = m \dot{\vec{v}}_Q + \mathbb{S}_Q \cdot \dot{\vec{\omega}} + \vec{\omega} \times \mathbb{S}_Q \cdot \vec{\omega} \\
 \dot{\vec{L}}_Q =
   \left[ \mathbb{S}_Q^T \cdot \left( \dot{v}_Q - \vec{\omega} \times \vec{v}_Q \right) + \mathbb{I} \cdot \dot{\vec{\omega}} \right] 
 + \vec{\omega} \times ( \mathbb{S}_Q^T \cdot \vec{v}_Q + \mathbb{I}_Q \cdot \vec{\omega} ) \\
 \dot{K} = \dots
\end{cases}
$$

**Equations of motion.**

$$
\begin{cases}
 \dot{\vec{Q}} = \vec{R}^e \\
 \dot{\vec{L}}_Q + \vec{v}_Q \times \vec{Q} = \vec{M}_Q^e \\
\end{cases}
$$
$$
\begin{cases}
 m \dot{\vec{v}}_Q + \mathbb{S}_Q \cdot \dot{\vec{\omega}} + \vec{\omega} \times \mathbb{S}_Q \cdot \vec{\omega} = \vec{R}^e \\
 \left[ \mathbb{S}_Q^T \cdot \left( \dot{v}_Q - \vec{\omega} \times \vec{v}_Q \right) + \mathbb{I} \cdot \dot{\vec{\omega}} \right] 
 + \vec{\omega} \times ( \mathbb{S}_Q^T \cdot \vec{v}_Q + \mathbb{I}_Q \cdot \vec{\omega} ) + \vec{v}_Q \times \left[  m \vec{v}_Q + \mathbb{S}_Q \cdot \vec{\omega}   \right] = \vec{M}_Q^e \\
\end{cases}
$$

or using the "material time derivative"

$$\dfrac{{}^0 d}{dt} \underline{\hspace{10pt}} = \dfrac{d}{dt} \underline{\hspace{10pt}} - \vec{\omega} \times \underline{\hspace{10pt}} \ ,$$

and matrix formalism to write these two vector equations

$$
\begin{bmatrix} m \mathbb{I} & \mathbb{S}_Q \\ \mathbb{S}_Q^T & \mathbb{I}_Q \end{bmatrix} \, \dfrac{{}^0 d}{dt} \begin{bmatrix} \vec{v}_Q \\ \vec{\omega} \end{bmatrix} + \begin{bmatrix} \vec{\omega}_\times & \vec{0} \\ \vec{v}_{Q \times} & \vec{\omega}_{\times} \end{bmatrix} \begin{bmatrix} m \mathbb{I} & \mathbb{S}_Q \\ \mathbb{S}_Q^T & \mathbb{I}_Q \end{bmatrix} \begin{bmatrix} \vec{v}_Q \\ \vec{\omega} \end{bmatrix} = \begin{bmatrix} \vec{R}^e \\ \vec{M}_Q^e \end{bmatrix} \ .
$$



```{dropdown} Starting from differential equations

**todo**


```
