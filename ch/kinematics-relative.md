(classical-mechanics:kinematics:relative)=
# Relative Kinematics

Relative kinematics is discussed here using two Cartesian reference frames.

$$P   - O_0 = x^{0i}_{  P/O_0} \hat{e}^0_i$$
$$O_1 - O_0 = x^{0i}_{O_1/O_0} \hat{e}^0_i$$
$$P   - O_1 = x^{1i}_{  P/O_1} \hat{e}^1_i$$

$$\begin{aligned}
  \hat{e}^1_i 
  = \hat{e}^{1}_i \cdot \hat{e}^0_k \, \hat{e}^0_k
  & = \hat{e}^{1}_j \cdot \hat{e}^0_k \, \hat{e}^0_k \otimes \hat{e}^0_j \cdot \hat{e}^0_i = \\
  & = R^{0\rightarrow 1}_{kj} \hat{e}^0_k \otimes \hat{e}^0_j \cdot \hat{e}^0_i 
    = \mathbb{R}^{0\rightarrow 1} \cdot \hat{e}^0_i  \ .
\end{aligned}$$

(classical-mechanics:kinematics:relative:points)=
## Points

**Position.**
Given two reference frames $Ox^i$, $O' x^{i'}$, for the position of a point $P$ reads

$$(P - O_0) = ( O_1 - O_0 ) + ( P - O_1) \ ,$$ (eq:relative:point:pos)

$$x^0_{P/O_0,i} \hat{e}^0_i = x^0_{O_1/O_0,i} \hat{e}^0_i + x^1_{P/O_1,k} \hat{e}^1_k \ ,$$

i.e. the position vector $P-O$ of the point $P$ w.r.t. point $O$ - origin of the reference frame $O x^i$ - is the sum of the position vector $P-O'$ of the point $P$ w.r.t. to the point $O'$ - origin of the reference frame $O' x^{'i}$ -  and the position vector $O' - O$, of the origin $O'$ w.r.t. to $O$.

**Velocity.** Time derivative of relative position relation {eq}`eq:relative:point:pos` w.r.t. to reference frame $0$ is performed keeping $\hat{e}^0_i$ constant.

$$\begin{aligned}
  \dfrac{{}^0 d}{dt} (P-O_0)
  & = \dfrac{{}^0 d}{dt} \left[ (O_1 - O_0) + (P - O_1) \right] = \\
  & = \dfrac{{}^0 d}{dt} \left( x^0_{O_1/O_0,i} \hat{e}^0_i  \right) + \dfrac{{}^0 d}{dt} \left( x^1_{P/O_1,k} \hat{e}^1_k \right) = \\
  & = \dfrac{{}^0 d}{dt} x^0_{O_1/O_0,i} \, \hat{e}^0_i + \dfrac{{}^0 d}{dt} x^1_{P/O_1,k} \, \hat{e}^1_k + x^1_{P/O_1,k} \, \dfrac{{}^0 d}{dt}  \hat{e}^1_k = \\
  & = \vec{v}^0_{O_1/O_0} + \vec{v}^1_{P/O_1} + \vec{\omega}_{1/0} \times  \hat{e}^1_k x^1_{P/O_1,k} = \\
  & = \vec{v}^0_{O_1/O_0} + \vec{v}^1_{P/O_1} + \vec{\omega}_{1/0} \times ( P - O_1 )  \ ,
\end{aligned}$$

so that

$$ \vec{v}^0_{P/O} = \vec{v}^0_{O_1/O_0} + \vec{v}^1_{P/O_1} + \vec{\omega}_{1/0} \times ( P - O_1 )  \ .$$ (eq:relative:point:vel)

**Acceleration.** Time derivative of relative velocity relation {eq}`eq:relative:point:vel` w.r.t. reference frame $0$ reads

$$\begin{aligned}
  \dfrac{{}^0 d}{dt} \vec{v}^0_{P/O_0}
  & = \dfrac{{}^0 d}{dt} \left[ \vec{v}^0_{O_1/O_0} + \vec{v}^1_{P/O_1} + \vec{\omega}_{1/0} \times ( P - O_1 ) \right] = \\
  & = \dots \\
  & = \vec{a}^0_{O_1/O_0} + \vec{a}^{1}_{P/O_1} + 2 \vec{\omega}_{1/0} \times \vec{v}^1_{P/O_1} + \vec{\alpha}_{1/0} \times (P - O_1) + \vec{\omega}_{1/0} \times [ \, \vec{\omega}_{1/0} \times (P - O_1) \, ]
\end{aligned}$$

so that

$$
\vec{a}^0_{P/O_0} = \vec{a}^0_{O_1/O_0} + \vec{a}^{1}_{P/O_1} + \underbrace{\vec{\alpha}_{1/0} \times (P - O_1)}_{\text{tangential}} + \underbrace{2 \vec{\omega}_{1/0} \times \vec{v}^1_{P/O_1}}_{\text{Coriolis}} + \underbrace{\vec{\omega}_{1/0} \times [ \, \vec{\omega}_{1/0} \times (P - O_1) \, ]}_{\text{centripetal}} \ .
$$ (eq:relative:point:acc)

where:
- the "tangential component" is orthogonal to the instantaneous angular acceleration and radius,
- the "centripetal component" is orthogonal w.r.t. the instantaneous angular velocity

**todo** *tangent to what, centripetal w.r.t. what?* **state it clearly, otherwise delete this**

## Rigid bodies

**Orientation.**

**Angular velocity.**

**Angular acceleration.**


