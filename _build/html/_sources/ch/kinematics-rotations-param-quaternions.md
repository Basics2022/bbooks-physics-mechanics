(classical-mechanics:kinematics:rotations:quaternions)=
# Rotation parametrization: quaternions

Here quaternion parametrization of rotations is introducing the unitary quaternion

$$\mathbf{q} = q_0 + \vec{q} = \cos \frac{\theta}{2} + \sin \frac{\theta}{2} \vec{q} \ ,$$ (eq:q:rot)

into [axis and angle parametrization](classical-mechanics:kinematics:rotations:axis-angle).


**Normalization condition.**

  $$1 = q_0^2 + \vec{q} \cdot \vec{q}$$

**Rotation tensor**

  $$\mathbb{R} = \mathbb{I} + 2 q_0 \vec{q}_\times + 2 \vec{q}_{\times} \vec{q}_{\times} \ ,$$

**Linearization**

  $$\Delta \mathbb{R} = 2 \Delta q_0 \vec{q}_\times + 2 q_0 \Delta \vec{q}_\times + 2 \Delta \vec{q}_\times \vec{q}_\times + 2 \vec{q}_\times \Delta \vec{q}_\times$$

  $$\begin{aligned}
    \vec{\theta}_{\Delta, \times} := & \ \Delta \mathbb{R} \cdot \mathbb{R}^T \\
    \vec{\theta}_{\Delta} = & - 2 \vec{q} \Delta q_0 + 2 q_0 \Delta \vec{q} - 2 \vec{q}_\times \Delta \vec{q}
  \end{aligned}$$

**Angular velocity**

  $$\begin{aligned}
    \vec{\omega}_\times := & \ \dot{\mathbb{R}} \cdot \mathbb{R}^T  \\
    \vec{\omega} = & - 2 \vec{q} \dot{q}_0 + 2 q_0 \dot{\vec{q}} - 2 \vec{q}_\times \dot{\vec{q}}
  \end{aligned}$$


(classical-mechanics:kinematics:rotations:quaternions:rotation-tensor)=
## Rotation tensor

Introducing the expression {eq}`eq:q:rot` of the unitary quaternion into expression {eq}`eq:R:aa` of the rotation tensor written using [axis and angle parametrization](classical-mechanics:kinematics:rotations:axis-angle), and using trigonometric identities

$$\begin{aligned}
  \sin \theta = \sin \left( 2 \frac{\theta}{2} \right) & = 2 \sin \frac{\theta}{2} \cos \frac{\theta}{2} \\
  \cos \theta = \cos \left( 2 \frac{\theta}{2} \right) & =   \cos^2 \frac{\theta}{2} -   \sin^2 \frac{\theta}{2} = \\
                                                       & = 2 \cos^2 \frac{\theta}{2} - 1                         = \\
                                                       & = 1                         - 2 \sin^2 \frac{\theta}{2}
\end{aligned}$$

the expression of the rotation tensor becomes

$$\begin{aligned}
  \mathbb{R}
  & = \mathbb{I} + \sin \theta \hat{n}_\times + ( 1 - \cos \theta ) \hat{n}_{\times} \hat{n}_{\times} = \\
  & = \mathbb{I} + 2 \sin \frac{\theta}{2} \cos \frac{\theta}{2} \hat{n}_\times + 2 \sin^2 \frac{\theta}{2} \hat{n}_{\times} \hat{n}_{\times} = \\
  & = \mathbb{I} + 2 q_0 \vec{q}_\times + 2 \vec{q}_{\times} \vec{q}_{\times} \\
\end{aligned}$$

(classical-mechanics:kinematics:rotations:quaternions:angular-velocity)=
## Angular velocity

$$\begin{aligned}
  \vec{\omega}_{\times} 
  & = \dot{\mathbb{R}} \cdot \mathbb{R}^T = \\
  & = \left( 2 \dot{q}_0 \vec{q}_\times + 2 q_0 \dot{\vec{q}}_{\times} + 2 \dot{\vec{q}}_\times \vec{q}_\times + 2 \vec{q}_\times \dot{\vec{q}}_\times \right) \cdot \left( \mathbb{I} - 2 q_0 \vec{q}_\times + 2 \vec{q}_{\times} \vec{q}_{\times} \right) = \\
  & = 2 \dot{q}_0 \vec{q}_\times + 2 q_0 \dot{\vec{q}}_{\times} + 2 \dot{\vec{q}}_\times \vec{q}_\times + 2 \vec{q}_\times \dot{\vec{q}}_\times + \\
  & \ \ - 4 \dot{q}_0 q_0 \vec{q}_\times \vec{q}_\times - 4 q_0^2 \dot{\vec{q}}_{\times} \vec{q}_\times - \underbrace{4 q_0 \dot{\vec{q}}_\times \vec{q}_\times \vec{q}_\times}_{(a)} - \underbrace{4 q_0 \vec{q}_\times \dot{\vec{q}}_\times \vec{q}_\times}_{-4 q_0 \left( \dot{\vec{q}} \cdot \vec{q} \right) \vec{q}_\times} +  \\
  & \ \ + 4 \dot{q}_0 \underbrace{\vec{q}_\times \vec{q}_\times \vec{q}_\times}_{-|\vec{q}|^2 \vec{q}_\times} + \underbrace{4 q_0 \dot{\vec{q}}_{\times} \vec{q}_\times \vec{q}_\times}_{(a)} + 4 \dot{\vec{q}}_\times \underbrace{\vec{q}_\times \vec{q}_\times \vec{q}_\times}_{-|\vec{q}|^2 \vec{q}_\times} + \underbrace{4 \vec{q}_\times \dot{\vec{q}}_\times \vec{q}_\times \vec{q}_\times}_{-\left( \dot{\vec{q}} \cdot \vec{q} \right) \vec{q}_\times \vec{q}_\times} = \\
  & = \underbrace{ 2 \dot{q}_0 \vec{q}_\times}_{(e)} + 2 q_0 \dot{\vec{q}}_{\times} + \underbrace{2 \dot{\vec{q}}_\times \vec{q}_\times}_{(c.1)} + 2 \vec{q}_\times \dot{\vec{q}}_\times + \\
  & \ \ - 4 \underbrace{\dot{q}_0 q_0 \vec{q}_\times \vec{q}_\times}_{-(b)} - \underbrace{4 q_0^2 \dot{\vec{q}}_{\times} \vec{q}_\times}_{(c.2)} + \underbrace{4 q_0 \left( \dot{\vec{q}} \cdot \vec{q} \right) \vec{q}_\times}_{(d)} +  \\
  & \ \ - \underbrace{4 \dot{q}_0 |\vec{q}|^2 \vec{q}_\times}_{ 4\dot{q}_0 \vec{q}_\times - 4 \dot{q}_0 q_0^2 \vec{q}_\times = 2(e)-(d)} - \underbrace{4 |\vec{q}|^2 \dot{\vec{q}}_\times \vec{q}_\times}_{(c.3)} - \underbrace{4\left( \dot{\vec{q}} \cdot \vec{q} \right) \vec{q}_\times \vec{q}_\times}_{(b)} = \\
  & = -2 \dot{q}_0 \vec{q}_\times + 2 q_0 \dot{\vec{q}}_\times - 2 \dot{\vec{q}}_\times \vec{q}_\times + 2 \vec{q}_\times \dot{\vec{q}}_\times =  \\
  & = \left[ - 2 \vec{q} \dot{q}_0 + 2 q_0 \dot{\vec{q}} - 2 \vec{q}_\times \dot{\vec{q}} \right]_\times
\end{aligned}$$


having used
- $\vec{q}_\times^T = - \vec{q}_\times$, $\left( \vec{q}_\times \vec{q}_\times \right)^T = \vec{q}_\times \vec{q}_\times$
- $1 = q_0^2 + |\vec{q}|^2$, and thus $\vec{q} \cdot \dot{\vec{q}} = - q_0 \dot{q}_0$
- $\vec{q}_\times \vec{q}_\times = \vec{q} \otimes \vec{q} - |\vec{q}|^2 \mathbb{I}$
- $\vec{q}_\times \vec{q}_\times \vec{q} = \underbrace{\vec{q}_\times \vec{q} \otimes \vec{q}}_{=\mathbb{0}} - |\vec{q}|^2 \vec{q}_{\times} = -|\vec{q}|^2 \vec{q}_{\times} $
- $\dot{\vec{q}}_\times \vec{q}_\times = \vec{q} \, \dot{\vec{q}} - \left( \dot{\vec{q}} \cdot \vec{q} \right) \, \mathbb{I}$ 
- $\vec{q}_\times \dot{\vec{q}}_\times = \dot{\vec{q}} \, \vec{q} - \left( \dot{\vec{q}} \cdot \vec{q} \right) \, \mathbb{I}$

```{dropdown} Proof - todo
```
- $(\vec{a}_\times \vec{b})_{\times} = \vec{a}_{\times} \vec{b}_\times - \vec{b}_\times \vec{a}_\times $

```{dropdown} Proof $\ (\vec{a}_\times \vec{b})_{\times} = \vec{a}_{\times} \vec{b}_\times - \vec{b}_\times \vec{a}_\times $

Using

$$(\vec{a} \times \vec{b}) \times \vec{c} + (\vec{b} \times \vec{c}) \times \vec{a} + (\vec{c} \times \vec{a}) \times \vec{b} = \vec{0} $$

(todo, prove it with index notation) it immediately follows the desired relation

$$\begin{aligned}
  (\vec{a}_\times \vec{b})_{\times} \vec{v}
  & = ( \vec{a} \times \vec{b} ) \times \vec{v} = \\
  & = - ( \vec{b} \times \vec{v} ) \times \vec{a} - ( \vec{v} \times \vec{a} ) \times \vec{b} = \\
  & = \vec{a} \times ( \vec{b} \times \vec{v} ) - \vec{b} \times ( \vec{a} \times \vec{v} ) = \\
  & = \left( \vec{a}_{\times} \vec{b}_\times - \vec{b}_\times \vec{a}_\times \right) \vec{v}
\end{aligned}$$

```


