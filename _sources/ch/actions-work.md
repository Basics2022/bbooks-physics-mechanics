(classical-mechanics:actions:work)=
# Work and Power

In mechanics, as will become clearer later (**todo** add reference), the concept of work is linked to the concept of energy. **todo**

## Work and Power of a Force

**Work.** The elementary work of a force $\vec{F}$ applied at point $P$ that undergoes an elementary displacement $d \vec{r}_P$ is defined as the dot product between the force and the displacement,

$$\delta W := \vec{F} \cdot d \vec{r}_P \ .$$ (eq:work:diff)

The work done by the force $\vec{F}$ applied at point $P$ moving from point $A$ to point $B$ along the path $\ell_{AB}$ is the sum of all elementary contributions - and hence, in the limit for elementary displacements $\rightarrow 0$ for continuous variations, the line integral,

$$W_{\ell_{AB}} = \int_{\ell_{AB}} \delta W = \int_{\ell_{AB}} \vec{F} \cdot d \vec{r}_{P} \ .$$ (eq:work:int)

In general, the work of a force or a field of forces depends on the path ${\ell}_{AB}$. In cases where the work is independent of the path but depends only on the endpoints, we talk about [conservative actions](classical-mechanics:actions:conservative).

**Power.** The power of the force is defined as the time derivative of the work,

$$P := \frac{\delta W}{dt} = \vec{F} \cdot \frac{d \vec{r}_P}{d t} = \vec{F} \cdot \vec{v}_P \ , $$

and coincides with the dot product between the force and the velocity of the point of application. <span style="color:red">Be cautious if a force is applied to geometric points rather than material points, such as in the case of a disk rolling without slipping on a surface: at every instant, the (new) material contact point has zero velocity, while the geometric contact point is the projection of the center of the disk and moves with the same velocity, $v = R \theta$</span>

## Work and Power of a System of Forces

**Work.** The work of a system of forces is the sum of the works of the individual forces,

$$\delta W = \sum_{n=1}^{N} \delta W_n = \sum_{n=1}^{N} \vec{F}_n \cdot d \vec{r}_n$$

**Power.** The power of a system of forces is the sum of the powers of the individual forces,

$$P = \sum_{n=1}^{N} P_n = \sum_{n=1}^{N} \vec{F}_n \cdot \vec{v}_n \ .$$

## Work and Power of a Couple of Forces

**Work.** The elementary work of a couple of forces is the sum of the elementary works,

$$\begin{aligned}
  \delta W & = \vec{F}_1 \cdot d \vec{r}_1 + \vec{F}_2 \cdot d \vec{r}_2 = \\
           & = \vec{F}_1 \cdot ( d \vec{r}_1 - d \vec{r}_2 ) = 
\end{aligned}$$

**Power.** The power of a couple of forces,

$$P = \vec{F}_1 \cdot (\vec{v}_1 - \vec{v}_2)$$

can be rewritten if the points of application perform a rigid motion act (**todo** verify the definition of motion act and if it should be introduced),

$$\vec{v}_1 - \vec{v}_2 = \vec{\omega} \times (P_1 - P_2) \ ,$$

as

$$\begin{aligned}
  P & =  \vec{F}_1 \cdot (\vec{v}_1 - \vec{v}_2) = \\
    & =  \vec{F}_1 \cdot \left[ \vec{\omega} \times (P_1 - P_2) \right] = \\
    & =  \vec{\omega} \cdot \left[ (P_1 - P_2) \times \vec{F}_1\right] = \\
    & =  \vec{\omega} \cdot \vec{C} \ . 
\end{aligned}$$

