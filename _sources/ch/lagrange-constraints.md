(classical-mechanics:lagrange:constraints)=
# Constraints classification

## Holonomic vs. non-holonomic constraints

```{prf:definition} Holonomic constraint
:label: holonomic-constraint

A holonomic constraints can be written in a form

$$g(q^k(t), t) = 0 \ .$$

```

```{prf:definition} Non-holonomic constraint
:label: non-holonomic-constraint

Every constraint that is not holonomic, is non-holonomic. (**wow!**)

```

**todo** *Add some examples...; even some constraints that looks like a non-holonomic constraint that are holonomic: "integrable constraints", Pfaffian method?...*

(classical-mechanics:lagrange:constraints:ideal)=
## Ideal constraints

```{prf:definition} Ideal constraint

An ideal constraint produces no net power.

```

Given the generalized actions $\mathbf{f}_c$ introduced in the dynamical systems by constraints,

$$\mathbf{M} \ddot{\mathbf{q}} = \mathbf{f} + \mathbf{f}_c \ ,$$

power of ideal constraints reads

$$\dot{\mathbf{q}}^T \mathbf{f}_c = 0 \ .$$


(classical-mechanics:lagrange:constraints:ideal:holonomic)=
### Ideal holonomic constraints

If constraints don't have explicit dependence (what happens if there's explicit [time dependence](classical-mechanics:lagrange:time:dependent)? Treat in the proper section...) from time $t$

$$\begin{aligned}
  & \mathbf{M} \ddot{\mathbf{q}} = \mathbf{f} + \mathbf{f}_c \\
  & \mathbf{g}(\mathbf{q}(t)) = \mathbf{0}
\end{aligned}$$

with $\mathbf{q} \in \mathbb{R}^N$, $\mathbf{g} \in \mathbb{R}^C$.

**Power of ideal constraint.** Power of ideal constraints is zero, and this condition provides the most general form of constraint reactions $\mathbf{f}_c$ as a linear combination of the gradient of the constraints, and a set of well-defined (*extra conditions?*) and determined DAEs, with equal number of equations and unknowns. Power of contraint reactions of ideal constrains is zero,

$$0 = \dot{\mathbf{q}}^T \mathbf{f}_c$$

Time derivative of the constraint equation reads $0 = g_i (q^k) = \dot{q}^k \frac{\partial g_i}{\partial q^k}$, and thus for every $\mathbf{s} \in \mathbb{R}^C$,

$$0 = \dot{\mathbf{q}}^T \nabla_{\mathbf{q}} \mathbf{g} \, \mathbf{s} \ ,$$ (eq:constraint:reaction:holonomic)

and thus constraint reactions can be written as a linear combination of the (columns of the) gradient of the constraint equation w.r.t. the generalized coordiantes,

$$\mathbf{f}_c = \nabla_\mathbf{q} \mathbf{g} \, \mathbf{s}$$

or

$$\begin{aligned}
  \mathbf{f}_c = \nabla_{\mathbf{q}} g_i \, s_i \qquad , \qquad
  f_{c,k}      = \dfrac{\partial\mathbf{g}^T}{\partial q^k} \mathbf{s} = \dfrac{\partial g^i}{\partial q^k} \, s_i \ .
\end{aligned}$$

**Determined set of DAEs.** Introducing the expression {eq}`eq:constraint:reaction:holonomic` of the constraint reactions in the original set of DAEs, the set of equations governing the constrained system reads

$$\begin{aligned}
  & \mathbf{M} \ddot{\mathbf{q}} = \mathbf{f} + \nabla_{\mathbf{q}} \mathbf{g} \, \mathbf{s} \\
  & \mathbf{g}(\mathbf{q}) = \mathbf{0}
\end{aligned}$$

(classical-mechanics:lagrange:constraints:ideal:non-holonomic)=
### Ideal non-holonomic constraints

The equations of a constrained system with non-holonomic constraints in semi-linear form and no explicit time dependence reads

$$\begin{aligned}
  & \mathbf{M} \ddot{\mathbf{q}} = \mathbf{f} + \mathbf{f}_c \\
  & \mathbf{a}(\mathbf{q}(t)) \, \dot{\mathbf{q}}(t) = \mathbf{0}
\end{aligned}$$

**Power of ideal constraints.** As done in the [section about holonomic constraints](classical-mechanics:lagrange:constraints:ideal:holonomic), the condition of zero power of ideal constraints provides the most general form of constraint reactions $\mathbf{f}_c$ as a linear combination of the gradient of the constraints, and thus a determined set of DAEs.

$$0 = \dot{\mathbf{q}}^T \, \mathbf{f}_c$$

compared with the (transpose of the) non-holonomic constraint,

$$0 = \dot{\mathbf{q}}^T \mathbf{a}^T(\mathbf{q}) \mathbf{s}  \ , \qquad \forall \mathbf{s} \in \mathbb{R}^C$$ 

and thus constraint reactions can be written as the linear combination of the columns of the transpose of matrix $\mathbf{a}(\mathbf{q})$,

$$\mathbf{f} = \mathbf{a}^T(\mathbf{q}) \mathbf{s} \ .$$ (eq:constraint:reaction:non-holonomic)

**Determined set of DAEs.** Introducing the expression {eq}`eq:constraint:reaction:non-holonomic` of the constraint reactions in the original set of DAEs, the determined set of equations governing the constrained system reads

$$\begin{aligned}
  & \mathbf{M} \ddot{\mathbf{q}} = \mathbf{f} + \mathbf{a}^T(\mathbf{q}) \, \mathbf{s} \\
  & \mathbf{a}(\mathbf{q}) \, \dot{\mathbf{q}}(t) = \mathbf{0}
\end{aligned}$$







