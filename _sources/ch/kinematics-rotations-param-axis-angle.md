(classical-mechanics:kinematics:rotations:axis-angle)=
# Rotation parametrization: axis and angle

Rotation tensor

  $$\mathbb{R} = \mathbb{I} + \sin \theta \, \hat{n}_\times + ( 1 - \cos \theta ) \, \hat{n}_\times \hat{n}_\times \ ,$$ (eq:R:aa)

Angular velocity

  $$\vec{\omega}_\times = \dot{\mathbb{R}} \cdot \mathbb{R}^T = $$

Linearization


(classical-mechanics:kinematics:rotations:axis-angle:rotation-tensor)=
## Rotation tensor

The expression of the rotation tensor $\mathbb{R}$ that rotates vector $\vec{v}^0$ into $\vec{v}$,

$$\vec{v} = \mathbb{R} \cdot \vec{v}^0 \ ,$$

comes from little geometry and vector algebra. The rotation of an angle $\theta$ around the axis determined by the  unit vector $\hat{n}$ reads

$$\vec{v} = \hat{n} v^0_{\parallel} + \hat{x} v^0_{\perp} \cos \theta + \hat{y} v^0_{\perp} \sin \theta \ ,$$ (eq:rotation:angle-axis:0)

with
- $v^0_{\parallel} = \hat{n} \cdot \vec{v}^0$,
- $\hat{n} \times \vec{v}^0 = \hat{y} v^0_{\perp}$, and thus $\hat{y} = \frac{\hat{n} \times \vec{v}^0}{v^0_{\perp}}$,
- $\hat{x} = \hat{y} \times \hat{n}$, and thus $v^0_{\perp} \hat{x} = v^0_{\perp} \frac{(\hat{n} \times \vec{v}^0)}{v^0_{\perp}} \times \hat{n} = - \hat{n} \times \left( \hat{n} \times \vec{v}^0 \right) = - \hat{n}_{\times} \hat{n}_{\times} \cdot \vec{v}^0$, where the dot product is meant between the $\hat{n}_\times$ tensors representing vector products.

Exploiting these expressions, the relation {eq}`eq:rotation:angle-axis:0` between the vectors $\vec{v}$, $\vec{v}^0$ can be written in implicit tensor form. Different equivalent tensor expressions follows from the identity $\hat{v}_\times \hat{v}_\times =  \vec{v} \otimes \vec{v} - |\vec{v}|^2 \mathbb{I} $,

$$\begin{aligned}
  \vec{v}
  & = \hat{n} v^0_{\parallel} + \hat{x} v^0_{\perp} \cos \theta + \hat{y} v^0_{\perp} \sin \theta = \\
  & = \hat{n} \hat{n} \cdot \vec{v}^0 - \cos \theta \hat{n}_\times \hat{n}_\times \cdot \vec{v}^0 + \sin \theta \hat{n}_\times \cdot \vec{v}^0 = \\
  & = \left[ \hat{n} \hat{n} - \cos \theta \hat{n}_\times \hat{n}_\times + \sin \theta \hat{n}_\times \right] \cdot \vec{v}^0 = \\
\end{aligned}$$

and thus

$$\begin{aligned}
 \mathbb{R}
 & = \hat{n} \hat{n} - \cos \theta \hat{n}_\times \hat{n}_\times + \sin \theta \hat{n}_\times = \\
 & = \mathbb{I}  + \sin \theta \, \hat{n}_\times + (1 - \cos \theta ) \, \hat{n}_\times \hat{n}_\times \ .
\end{aligned}$$


```{dropdown} Proof of relation $\ \hat{v}_\times \hat{v}_{\times} = \vec{v} \otimes \vec{v} - |\vec{v}|^2 \mathbb{I} $

$$\begin{aligned}
  \hat{v}_\times \hat{v}_{\times}
  & = \hat{e}^i \hat{e}_m \varepsilon_{ijk} v_j \varepsilon_{klm} v_l = \\
  & = \hat{e}^i \hat{e}_m \left( \delta_{il} \delta_{jm} - \delta_{im} \delta_{jl} \right) v_j v_l  \ ,
  & = \hat{e}^i \hat{e}_m \left( v_i v_m - v_j v_j \delta_{im} \right) = \\
  & = \vec{v} \otimes \vec{v} - |\vec{v}|^2 \mathbb{I}
\end{aligned}$$


```

(classical-mechanics:kinematics:rotations:axis-angle:angular-velocity)=
## Angular velocity
