(classical-mechanics:actions:conservative)=
# Conservative Actions

In general, the work of a force field acting on a point $P$ moving in space from point $A$ to point $B$ along a path $\ell_{AB}$ represented by integral {eq}`eq:work:int` depends on the path, and this dependence on the path is usually highlighted with the use of the symbol $\delta$ in the elementary work {eq}`eq:work:diff`.

If the work of a force field does not depend on the path $\ell_{AB}$ but only on the endpoints $A$, $B$, for all pairs of points within a region of space $\Omega$, the **force field** is said to be **conservative** in the region $\Omega$ of space. In this case, the work integral can be written as the difference of a scalar field, $U(P)$ or its opposite $V(P) := - U(P)$,

$$\begin{aligned}
  W_{AB} &  = \int_{\ell_{AB}} \vec{F} \cdot d \vec{r} = \\
         &  = \int_{\ell_{AB}} \delta W = \\
         &  = U(B) - U(A) = \Delta_{AB} U  \\
         &  = V(A) - V(B) = -\Delta_{AB} V  \\
\end{aligned}$$

The functions $U$, $V$ are respectively defined as the **potential** and **potential energy** of the force field. From the definition of a conservative force field it readily follows that

$$\oint_{\ell} \vec{F} \cdot d \vec{r} = 0 \ .$$

The elementary work can thus be expressed in terms of the differential of these functions,

$$\begin{aligned}
  \delta W & = \ \ \ d U =\ \ \ d \vec{r} \cdot \nabla U  = \\
           & =     - d V =    - d \vec{r} \cdot \nabla V \\
\end{aligned}$$

Comparing this relation with the definition of work $\delta W = d \vec{r} \cdot \vec{F}$, it is possible to identify the force field with the gradient of the potential function, and the opposite of the gradient of the potential energy,

$$\vec{F} = \nabla U = - \nabla V \ .$$

Since the force field can be written as the gradient of a scalar field, and the curl of a gradient is identically zero, the curl of a potential force field is identically zero,

$$\nabla \times \vec{F} = \vec{0} \ .$$


```{note}
The reverse logical process - $\nabla \times \vec{F} = \vec{0}$ implies $\vec{F} = \nabla U$ implies $\vec{F}$ conservative, i.e. independence of the work from the path - requires the domain continaing the integration path $\ell$ to be simply connected.
```
```{prf:example} Force fields in non-simply connected domains

In a region of $E^2$, described with Cartesian coordinates, containing the origin $O \equiv (x_0, y_0) \equiv (0,0)$ the vector field

$$\vec{F}_1(\vec{r}) = \frac{x}{x^2 + y^2} \hat{x} + \frac{y}{x^2+y^2} \hat{y}$$

is conservative, while the vector field

$$\vec{F}_2(\vec{r}) = -\frac{y}{x^2 + y^2} \hat{x} + \frac{x}{x^2+y^2} \hat{y}$$

is not conservative, even though their curl is zero in all the points of the domain where the field is defined - they're not defined in the origin.

```




