(classical-mechanics:kinematics:rotations:euler)=
# Rotation parametrization: Euler's angles

A generic rotation tensor can be written as a combination of 3 successive rotations. **Euler's angle parametrizations** are built with three successive rotations around 1 axis of the intermediate reference frames. Two families of angles exist:
- proper Euler's angles, with the first and the last rotation around axes with the same labels (e.g. $zxz$, $xyx$, $yzy$, $zyz$, $xzx$, $yxy$)
- Tait-Bryan (or Cardan) angles, with three rotations around three axes with different labels (e.g. $xyz$, $yzx$, $zxy$, $xzy$, $yxz$, $zyx$)

Here, the expressions of rotation tensor and angular velocity are explicitly treated for the set of angles $(\psi, \theta, \phi)$ around axes $zyx$.

```{admonition} Euler's angle parametrization is not regular: *gimbal lock*
:class: warning

Euler's angles can represent any rotation, but there this parametrization is not one-to-one: some rotations may be represented by many (infinite) set of parameters, as shown below. Thus, for some rotations it's not possible to recover a unique set of Euler's angles.

**todo**
- *add link*
- *add picture?*

```


(classical-mechanics:kinematics:rotations:euler:rotation-tensor)=
## Rotation tensor

Three successive rotations are

$$
\begin{aligned}
& \begin{cases}
 \hat{x}_1 = \ \ \cos \psi \, \hat{x}_0 + \sin \psi \, \hat{y}_0 \\
 \hat{y}_1 = -   \sin \psi \, \hat{x}_0 + \cos \psi \, \hat{y}_0 \\
 \hat{z}_1 =                  \hat{z}_0                          \\
\end{cases} \\
& \begin{cases}
 \hat{x}_2 = \ \ \cos \theta \, \hat{x}_1 - \sin \theta \, \hat{z}_1  \\
 \hat{y}_2 =                    \hat{y}_1                             \\
 \hat{z}_2 = \ \ \sin \theta \, \hat{x}_1 + \cos \theta \, \hat{z}_1  \\
\end{cases} \\
& \begin{cases}
 \hat{x}_3 =                  \hat{x}_2                          \\ 
 \hat{y}_3 = \ \ \cos \phi \, \hat{y}_2 + \sin \phi \, \hat{z}_2 \\
 \hat{z}_3 = -   \sin \phi \, \hat{y}_2 + \cos \phi \, \hat{z}_2 \\ 
\end{cases} \\
\end{aligned}
\quad , \quad
\begin{aligned}
& \begin{cases}
 \hat{x}_0 = \ \ \cos \psi \, \hat{x}_1 - \sin \psi \, \hat{y}_1 \\
 \hat{y}_0 = \ \ \sin \psi \, \hat{x}_1 + \cos \psi \, \hat{y}_1 \\
 \hat{z}_0 =                  \hat{z}_1                          \\
\end{cases} \\
& \begin{cases}
 \hat{x}_1 = \ \ \cos \theta \, \hat{x}_2 + \sin \theta \, \hat{z}_2  \\
 \hat{y}_1 =                    \hat{y}_2                             \\
 \hat{z}_1 =   - \sin \theta \, \hat{x}_2 + \cos \theta \, \hat{z}_2  \\
\end{cases} \\
& \begin{cases}
 \hat{x}_2 =                  \hat{x}_3                          \\ 
 \hat{y}_2 = \ \ \cos \phi \, \hat{y}_3 - \sin \phi \, \hat{z}_3 \\
 \hat{z}_2 = \ \ \sin \phi \, \hat{y}_3 + \cos \phi \, \hat{z}_3 \\ 
\end{cases} \\
\end{aligned}
$$

Rotation of vector $\vec{v}^0 = v_x \hat{x}_0 + v_y \hat{y}_0 + v_z \hat{z}_0$ into vector $\vec{v} = v_x \hat{x}_3 + v_y \hat{y}_3 + v_z \hat{z}_3$

**Vectors of basis $3$ w.r.t. basis $0$.**

$$\begin{aligned}
 \hat{x}_3 & =                  \hat{x}_2                          = \\
           & = \ \ \cos \theta \, \hat{x}_1 - \sin \theta \, \hat{z}_1  = \\
           & = \ \ \cos \theta \, \left( \cos \psi \, \hat{x}_0 + \sin \psi \, \hat{y}_0 \right) - \sin \theta \, \left( \hat{z}_0 \right)  = \\
 \hat{y}_3 & = \cos \phi \, \hat{y}_2 + \sin \phi \, \hat{z}_2 = \\ 
           & = \cos \phi \, \left( \hat{y}_1 \right) + \sin \phi \, \left( \sin \theta \, \hat{x}_1 + \cos \theta \, \hat{z}_1  \right) = \\ 
           & = \hat{x}_0 \left( -\cos\phi \sin \psi + \sin \phi \sin \theta \cos \psi \right) + \hat{y}_0 \left( \cos \phi \cos \psi + \sin \phi \sin \theta \sin \psi \right) + \hat{z}_0 \left( \sin \phi \cos \theta \right) \\
 \hat{z}_3 & = - \sin \phi \, \hat{y}_2 + \cos \phi \, \hat{z}_2 = \\ 
           & = - \sin \phi \, \left( \hat{y}_1 \right) + \cos \phi \, \left( \sin \theta \, \hat{x}_1 + \cos \theta \, \hat{z}_1  \right) = \\    
           & =  \hat{x}_0 \left( \sin \phi \sin \psi + \cos \phi \sin \theta \cos \psi \right) + \hat{y}_0 \left(-\sin \phi \cos \psi + \cos \phi \sin \theta \sin \psi \right) + \hat{z}_0 \left( \cos \phi \cos \theta \right)
\end{aligned}$$

The components $R_{ij}^{0 \rightarrow 3} := \hat{e}^0 \cdot \hat{e}^3_j$ of the rotation tensor, transforming the basis $0$ into the basis $3$, referred either to basis $0$ or basis $3$,

$$\mathbb{R}^{0 \rightarrow 3} = R^{0 \rightarrow 3}_{ij} \hat{e}^0_i \otimes \hat{e}^0_j =  R^{0 \rightarrow 3}_{ij} \hat{e}^3_i \otimes \hat{e}^3_j$$

can be **collected in an array** $\mathbf{R}^{0 \rightarrow 3}$, $[\mathbf{R}^{0 \rightarrow 3}]_{ij} = R^{0 \rightarrow 3}_{ij} = \hat{e}^0_i \cdot \hat{e}^3_j$,

$$\mathbf{R}^{0 \rightarrow 3}_{321}(\psi,\theta,\phi) = 
\begin{bmatrix}
  \cos \theta \cos \psi                                &   \cos \theta \sin \psi                               &  -\sin \theta          \\
 -\cos\phi \sin \psi + \sin \phi \sin \theta \cos \psi & \cos \phi \cos \psi + \sin \phi \sin \theta \sin \psi & -\sin \phi \cos \theta \\ 
  \sin\phi \sin \psi + \cos \phi \sin \theta \cos \psi &-\sin \phi \cos \psi + \cos \phi \sin \theta \sin \psi &  \cos \phi \cos \theta \\ 
\end{bmatrix}$$

This is the matrix of change of basis discussed in Math:Vector and Tensor Algebra:...

```{admonition} Gimbal lock
:class: warning

For $\theta = \mp \frac{\pi}{2}$, the components of the rotation tensor are

$$\begin{aligned}
 \mathbf{R}^{0 \rightarrow 3}_{321}(\psi, 0, \phi) 
 & = 
 \begin{bmatrix}
             0 &         0 & \pm 1 \\
    -\cos \phi \sin \psi \mp \sin \phi \cos \psi &  \cos \phi \cos \psi \mp \sin \phi \sin \psi & 0 \\
     \sin \phi \sin \psi \mp \cos \phi \cos \psi & -\sin \phi \cos \psi \mp \cos \phi \sin \psi & 0 \\
 \end{bmatrix} = \\
 & = 
 \begin{bmatrix}
             0 &         0 & \pm 1 \\
      - \sin(\psi \pm \phi) &     \cos(\psi \pm \phi) & 0 \\
    \mp \cos(\psi \pm \phi) & \mp \sin(\psi \pm \phi) & 0 \\
 \end{bmatrix} \ ,
\end{aligned}$$

i.e. orientations with $\theta = - \frac{\pi}{2}$ are determined by the sum $\psi + \phi$, while with $\theta = \frac{\pi}{2}$ by the difference $\psi - \phi$. In both situations, for a given orientation it's not possible to retrieve a unique pair of values $(\psi, \phi)$, but only their sum or difference.


```

<!--
$$\begin{aligned}
  &  R_{xx}^{0\rightarrow3} = \hat{e}^0_x \cdot \hat{e}^3_x =  \ \ \cos \theta \cos \psi  
  && R_{xy}^{0\rightarrow3} = \hat{e}^0_x \cdot \hat{e}^3_y =  \ \ \cos \theta \sin \psi 
  && R_{xz}^{0\rightarrow3} = \hat{e}^0_x \cdot \hat{e}^3_z =     -\sin \theta \\
  &  R_{yx}^{0\rightarrow3} = \hat{e}^0_y \cdot \hat{e}^3_x =     -\cos\phi \sin \psi + \sin \phi \sin \theta \cos \psi
  && R_{yy}^{0\rightarrow3} = \hat{e}^0_y \cdot \hat{e}^3_y =  \ \ \cos \phi \cos \psi + \sin \phi \sin \theta \sin \psi 
  && R_{yz}^{0\rightarrow3} = \hat{e}^0_y \cdot \hat{e}^3_z =     -\sin \phi \cos \theta   \\
  &  R_{zx}^{0\rightarrow3} = \hat{e}^0_z \cdot \hat{e}^3_x =  
  && R_{zy}^{0\rightarrow3} = \hat{e}^0_z \cdot \hat{e}^3_y =  
  && R_{zz}^{0\rightarrow3} = \hat{e}^0_z \cdot \hat{e}^3_z =  \\
\end{aligned}$$
-->



(classical-mechanics:kinematics:rotations:euler:angular-velocity)=
## Angular velocity

```{dropdown} Angular velocity of simple rotation around a vector of the basis

Let $\mathbb{R}^{0\rightarrow 1}$ the rotation tensor representing a rotation of an angle $\psi$ around the unit vector $\hat{z}^0 = \hat{z}^1$,

$$\mathbb{R}^{0\rightarrow 1} = \cos \psi \hat{x}^0 \hat{x}^0 - \sin \psi \hat{x}^0 \hat{y}^0 + \sin \psi\hat{y}^0 \hat{x}^0 + \cos \psi \hat{y}^0 \hat{y}^0 + 1 \hat{z}^0 \hat{z}^0 \ ,$$

Its time derivative at constant $0$ reads

$$\dfrac{{}^0 d}{dt} \mathbb{R}^{0\rightarrow 1} = \dot{\psi} \left( -\sin \psi \hat{x}^0 \hat{x}^0 - \cos \psi \hat{x}^0 \hat{y}^0 + \cos \psi\hat{y}^0 \hat{x}^0 - \sin \psi \hat{y}^0 \hat{y}^0 \right ) \ ,$$

and thus the angular velocity reads

$$\begin{aligned}
  \vec{\omega}_\times 
  & := \dfrac{{}^0 d}{dt} \mathbb{R}^{0 \rightarrow 1} \cdot \mathbb{R}^{1 \rightarrow 0} = \\
  & := \dot{\psi} \left( -\sin \psi \hat{x}^0 \hat{x}^0 - \cos \psi \hat{x}^0 \hat{y}^0 + \cos \psi\hat{y}^0 \hat{x}^0 - \sin \psi \hat{y}^0 \hat{y}^0 \right) \cdot \\
  & \quad \cdot \left( \cos \psi \hat{x}^0 \hat{x}^0 - \sin \psi \hat{x}^0 \hat{y}^0 + \sin \psi\hat{y}^0 \hat{x}^0 + \cos \psi \hat{y}^0 \hat{y}^0 + 1 \hat{z}^0 \hat{z}^0  \right)^T =  \\
  & := \dot{\psi} \left( -\sin \psi \hat{x}^0 \hat{x}^0 - \cos \psi \hat{x}^0 \hat{y}^0 + \cos \psi\hat{y}^0 \hat{x}^0 - \sin \psi \hat{y}^0 \hat{y}^0 \right) \cdot \\
  & \quad \cdot \left( \cos \psi \hat{x}^0 \hat{x}^0 + \sin \psi \hat{x}^0 \hat{y}^0 - \sin \psi\hat{y}^0 \hat{x}^0 + \cos \psi \hat{y}^0 \hat{y}^0 + 1 \hat{z}^0 \hat{z}^0  \right) =  \\
  & = \dot{\psi} \left[ \hat{x}^0 \hat{x}^0 \left( - \sin \psi \cos \psi + \cos \psi \sin \psi \right) + 
                        \hat{x}^0 \hat{y}^0 \left( - \sin^2 \psi - \cos^2 \psi  \right) \right. + \\ 
  & + \left.            \hat{y}^0 \hat{x}^0 \left(   \cos^2 \psi + \sin^2 \psi  \right) + 
                        \hat{y}^0 \hat{y}^0 \left( \cos \psi \sin \psi - \sin \psi \cos \psi \right) \right] = \\
  & = - \dot{\psi} \, \hat{x}^0 \hat{y}^0 + \dot{\psi} \, \hat{y}^0 \hat{x}^0  \ .
\end{aligned}$$

and thus 

$$\vec{\omega} = \dot{\psi} \hat{z}^0 \ .$$

If the rotation occurs around the vector of the original basis, the components of the angular velocity don't change when referred to either bases, as $\hat{z}^1 = \mathbb{R} \cdot \hat{z}^0 = \hat{z}^0$, and thus

$$\vec{\omega} = \dot{\psi} \hat{z}^0 = \dot{\psi} \hat{z}^1 \ .$$

**This is not true for generic rotations!**


```

```{dropdown} Relative angular velocities of intermediate Euler's rotations

As shown for the "yaw" angle $\psi$ before, it's easy to prove that

$$\begin{aligned}
  \vec{\omega}^{1/0} & = \dot{\psi}  \, \hat{z}_0  =  \dot{\psi}  \, \hat{z}_1 \\ 
  \vec{\omega}^{2/1} & = \dot{\theta}\, \hat{y}_1  =  \dot{\theta}\, \hat{y}_2 \\ 
  \vec{\omega}^{3/2} & = \dot{\phi}  \, \hat{x}_2  =  \dot{\phi}  \, \hat{x}_3 \\ 
\end{aligned}$$

```

```{dropdown} Angular velocity as the sum of relative angular velocity of intermediate rotations

Using addition of relative angular velocity of intermediate rotations,

$$\begin{aligned}
  \vec{\omega}^{3/0} 
  & = \vec{\omega}^{3/2} + \vec{\omega}^{2/1} + \vec{\omega}^{1/0} \ ,
\end{aligned}$$

and it can be expressed w.r.t. vectors of reference frame $0$

$$\begin{aligned}
  \vec{\omega}^{3/0} 
  & = \dot{\phi} \, \hat{x}_2 + \dot{\theta} \, \hat{y}_1 + \dot{\psi} \, \hat{z}_0 = \\
  & = \dot{\phi} \, \left( \cos \theta \cos \psi \, \hat{x}^0 + \cos \theta \sin \psi \, \hat{y}^0 - \sin \theta \, \hat{z}^0  \right) + \dot{\theta} \, \left( - \sin \psi \, \hat{x}^0 + \cos \psi \, \hat{y}^0 \right) + \dot{\psi} \, \hat{z}_0 = \\
  & = \left( - \dot{\theta} \, \sin \psi + \dot{\phi} \, \cos \theta \cos \psi \right) \hat{x}^0 + \left( \dot{\theta} \, \cos \psi + \dot{\phi} \, \cos \theta \sin \psi  \right) \hat{y}^0 + \left( - \dot{\phi} \, \sin \theta + \dot{\psi}  \right) \hat{z}^0
\end{aligned}$$

or w.r.t. vectors of reference frame $3$

$$\begin{aligned}
  \vec{\omega}^{3/0} 
  & = \dot{\phi} \, \hat{x}_3 + \dot{\theta} \, \hat{y}_2 + \dot{\psi} \, \hat{z}_1 = \\
  & = \dot{\phi} \, \hat{x}_3 + \dot{\theta} \, \left( \cos \phi \, \hat{y}_3 - \sin \phi \, \hat{z}_3 \right) + \dot{\psi} \, \left( - \sin \theta \, \hat{x}_3 + \cos \theta \sin \phi \, \hat{y}_3 + \cos \theta \cos \phi \, \hat{z}_3  \right) = \\
  & = \left( \dot{\phi} - \dot{\psi} \, \sin \theta  \right) \hat{x}_3 + \left(  \dot{\theta} \, \cos \phi + \dot{\psi} \, \cos \theta \sin \phi \right) \hat{y}_3 + \left( - \dot{\theta} \, \sin \phi + \dot{\psi} \, \cos \theta \cos \phi  \right) \hat{z}_3
\end{aligned}$$

```

```{dropdown} Relation between components of angular velocity and rotation parameters and their time derivative

Let $3$ a body reference frame, and $0$ a global reference frame; let $p$, $q$, $r$ the components of the angular velocity $\vec{\omega}$ w.r.t. the body reference frame

$$\vec{\omega} = p \, \hat{x}_3 + q \, \hat{y}_3 + r \, \hat{z}_3 \ .$$

Exploiting matrix formalism, the relation between the components of the angular velocity in the body reference frame, Euler's angles and thier time derivative is

$$
\begin{bmatrix} p \\ q \\ r \end{bmatrix} = 
\begin{bmatrix} 1 & \cdot & - \sin \theta \\ \cdot & \cos \phi & \cos \theta \sin \phi \\ \cdot & - \sin \phi & \cos \theta \cos \phi \end{bmatrix}
\begin{bmatrix} \dot{\phi} \\ \dot{\theta} \\ \dot{\psi} \end{bmatrix}
$$

The inverse relation exists for $\cos \theta \ne 0$ (**gimbal lock**),

$$
\begin{bmatrix} \dot{\phi} \\ \dot{\theta} \\ \dot{\psi} \end{bmatrix} = 
\frac{1}{\cos \theta}
\begin{bmatrix} 1 & \sin \theta \sin \phi & \sin \theta \cos \phi \\ \cdot & \cos \theta \cos \phi & - \cos \theta \sin \phi \\ \cdot & \sin \phi & \cos \phi \end{bmatrix}
\begin{bmatrix} p \\ q \\ r \end{bmatrix} 
$$

Thus, collecting the body components of the angular velocity in $\boldsymbol{\omega} = (p,q,r)^T$, calling $\mathbf{S}(\mathbf{q})$ the matrix collecing the coefficients depending on the rotation parameters $\mathbf{q} = (\phi, \theta, \psi)$, and $\dot{\mathbf{q}}$ their time derivatives, it remains proved that using Euler's angles the relation

$$\boldsymbol{\omega} = \mathbf{S}(\mathbf{q}) \, \dot{\mathbf{q}}$$

always exists, but the inverse relation exists only for $\theta \ne \mp \frac{\pi}{2}$.

```


## Linearization
...




