(classical-mechanics:actions:conservative)=
# Conservative Actions

A conservative force field is defined by the work it performs. In general, the work of a force field acting on a point $P$ moving in space from point $A$ to point $B$ along a path $\ell_{AB}$ depends on the path. (**todo** add reference)

If the work of a force field does not depend on the path $\ell_{AB}$ but only on the endpoints $A$, $B$, for all pairs of points within a region of space $\Omega$, the **force field** is said to be **conservative** in the region $\Omega$ of space.

In this case, the work done can be expressed as the difference of a scalar field, $U(P)$ or its opposite $V(P) := - U(P)$,

$$\begin{aligned}
  W_{AB} &  = U(B) - U(A) = \Delta_{AB} U  \\
         &  = V(A) - V(B) = -\Delta_{AB} V  \\
\end{aligned}$$

The functions $U$, $V$ are respectively defined as the **potential** and **potential energy** of the force field.

The elementary work can thus be expressed in terms of the differential of these functions,

$$\begin{aligned}
  \delta W & = \ \ \ d U =\ \ \ d \vec{r} \cdot \nabla U  = \\
           & =     - d V =    - d \vec{r} \cdot \nabla V \\
\end{aligned}$$

Comparing this relation with the definition of work $\delta W = d \vec{r} \cdot \vec{F}$, it is possible to identify the force field with the gradient of the potential function, and the opposite of the gradient of the potential energy,

$$\vec{F} = \nabla U = - \nabla V \ .$$

