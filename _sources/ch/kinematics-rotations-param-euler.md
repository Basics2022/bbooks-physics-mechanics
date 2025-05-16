(classical-mechanics:kinematics:rotations:euler)=
# Rotation parametrization: Euler's angles

A generic rotation tensor can be written as a combination of 3 successive rotations. **Euler's angle parametrizations** are built with three successive rotations around 1 axis of the intermediate reference frames. Two families of angles exist:
- proper Euler's angles, with the first and the last rotation around axes with the same labels (e.g. $zxz$, $xyx$, $yzy$, $zyz$, $xzx$, $yxy$)
- Tait-Bryan (or Cardan) angles, with three rotations around three axes with different labels (e.g. $xyz$, $yzx$, $zxy$, $xzy$, $yxz$, $zyx$)

Here, the expressions of rotation tensor and angular velocity are explicitly treated for the set of angles $(\psi, \theta, \phi)$ around axes $zyx$.

(classical-mechanics:kinematics:rotations:euler:rotation-tensor)=
## Rotation tensor

Three successive rotations are

$$\begin{aligned}
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
 \hat{x}_3 = \ \ \cos \phi \, \hat{x}_2 + \sin \phi \, \hat{y}_2 \\
 \hat{y}_3 = -   \sin \phi \, \hat{x}_2 + \cos \phi \, \hat{y}_2 \\
 \hat{z}_3 =                  \hat{z}_2                          \\
\end{cases} \\
\end{aligned}$$

Rotation of vector $\vec{v}^0 = v_x \hat{x}_0 + v_y \hat{y}_0 + v_z \hat{z}_0$ into vector $\vec{v} = v_x \hat{x}_3 + v_y \hat{y}_3 + v_z \hat{z}_3$

$$\begin{aligned}
 \hat{x}_3 & = \ \ \cos \phi \, \hat{x}_2 + \sin \phi \, \hat{y}_2 = \\
           & = \ \ \cos \phi \, \left( \cos \theta \, \hat{x}_1 - \sin \theta \, \hat{z}_1 \right) + \sin \phi \, \hat{y}_1 = \\
           & = \ \ \cos \phi \, \left( \cos \theta \left( \cos \psi \, \hat{x}_0 + \sin \psi \,  \hat{y}_0 \right) - \sin \theta \, \hat{z}_0 \right) + \sin \phi \left( - \sin \psi \, \hat{x}_0 + \hat{y}_0 \, \cos \psi \right) \\ 
 \hat{y}_3 & = -   \sin \phi \, \hat{x}_2 + \cos \phi \, \hat{y}_2 = \\
           & = -   \sin \phi \, \left( \cos \theta \, \hat{x}_1 - \sin \theta \, \hat{z}_1 \right) + \cos \phi \, \hat{y}_1 = \\
           & = -   \sin \phi \, \left( \cos \theta \left( \cos \psi \, \hat{x}_0 + \sin \psi \, \hat{y}_0 \right) - \sin \theta \, \hat{z}_0 \right) + \cos \phi \left(  -   \sin \psi \, \hat{x}_0 + \cos \psi \, \hat{y}_0 \right) = \\
 \hat{z}_3 & =                  \hat{z}_2                          = \\
           & = \sin \theta \, \hat{x}_1 + \cos \theta \, \hat{z}_1 = \\
           & = \sin \theta \left( \cos \psi \, \hat{x}_0 + \sin \psi \, \hat{y}_0 \right) + \cos \theta \hat{z}_0 \ .
\end{aligned}$$

(classical-mechanics:kinematics:rotations:euler:angular-velocity)=
## Angular velocity

