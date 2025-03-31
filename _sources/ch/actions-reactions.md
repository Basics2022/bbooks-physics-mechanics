(classical-mechanics:actions:reactions)=
# Constraint Reactions

Kinematic constraints act on a system by limiting its possible movements, exerting forces and moments, which are defined as constraint reactions.

In general, at an **ideal** constraint (**todo** provide definition of ideal constraint and discuss/mention/refer to friction), a constraint reaction corresponds to each constrained degree of freedom: for example, the constraint of translation of a point in a direction has a corresponding reaction force in that direction; the constraint of rotation around an axis has a corresponding moment aligned with that axis.

These conditions can be derived from the equations of dynamics for massless systems, as often considered in the ideal constraint model.

(classical-mechanics:actions:reactions:contact)=
## Contact Actions

(classical-mechanics:actions:reactions:contact:ideal)=
### Constraint Reactions of Ideal Constraints
Ideal constraints are models that **do not perform net work**, and are thus **conservative elements**. As should become evident in the subsequent sections from the expressions of relative velocities and exchanged actions,

$$\begin{aligned}
P & = \vec{v}_1     \cdot \vec{F}_{21} + \vec{v}_2     \cdot \vec{F}_{12} 
    + \vec{\omega}_1 \cdot \vec{M}_{21} + \vec{\omega}_2 \cdot \vec{M}_{12} = \\ 
  & = ( \vec{v}_1 - \vec{v}_2 ) \cdot \vec{F}_{21}
    + ( \vec{\omega}_1 - \vec{\omega}_2 ) \cdot \vec{M}_{21} = \\ 
  & = \vec{v}^{rel}_{21} \cdot \vec{F}_{21}
    + \vec{\omega}^{rel}_{21} \cdot \vec{M}_{21} \ ,
\end{aligned}$$

both terms are zero either because the relative motion is zero, or the actions act orthogonally to the relative motions.

#### Fixed Joint
The fixed joint constraint prevents both relative motion and relative rotation,

$$
\begin{cases}
  \vec{0} = \vec{v}^{rel}_{21}     = \vec{v}_{2}     - \vec{v}_{1} \\
  \vec{0} = \vec{\omega}^{rel}_{21} = \vec{\omega}_{2} - \vec{\omega}_{1} \\
\end{cases}
\qquad , \qquad
\begin{cases}
  \qquad \vec{F}_{12} = - \vec{F}_{21} \\
  \qquad \vec{M}_{12} = - \vec{M}_{21} \\
\end{cases}
$$

#### Slider
The slider constraint prevents relative motion in one direction and relative rotation.

$$
\begin{cases}
  \quad \forall \ \vec{v}^{rel}_{\hat{t},21}     = \vec{v}_{\hat{t},2}     - \vec{v}_{\hat{t},1} \\
          0  = v^{rel}_{\hat{n},21}     = v_{\hat{n},2}     - v_{\hat{n},1} \\
  \vec{0} = \vec{\omega}^{rel}_{21} = \vec{\omega}_{2} - \vec{\omega}_{1} \\
\end{cases}
\qquad , \qquad
\begin{cases}
  \vec{0} = \vec{F}_{\hat{t},12} = \vec{F}_{\hat{t},21} \\
  \qquad F_{\hat{n},12} = - F_{\hat{n},21} \\
  \qquad \vec{M}_{12} = - \vec{M}_{21} \\
\end{cases}
$$

#### Cylindrical Joint
The cylindrical joint constraint prevents relative motion and allows rotation around one axis.

$$
\begin{cases}
  \vec{0} = \vec{v}^{rel}_{21}     = \vec{v}_{2}     - \vec{v}_{1} \\
  \quad \forall \ \omega^{rel}_{\hat{t},21} = \omega_{\hat{t},2} - \omega_{\hat{t},1} \\
  \vec{0} = \vec{\omega}^{rel}_{\hat{n},21} = \vec{\omega}_{\hat{n},2} - \vec{\omega}_{\hat{n},1} \\
\end{cases}
\qquad , \qquad
\begin{cases}
  \qquad \vec{F}_{12} = - \vec{F}_{21} \\
  0 =  M_{\hat{t},12} = M_{\hat{t},21} \\
  \qquad \vec{M}_{\hat{n},12} = - \vec{M}_{\hat{n},21} \\
\end{cases}
$$

#### Spherical Joint
The spherical joint constraint prevents relative motion but allows general rotation.

$$
\begin{cases}
  \vec{0} = \vec{v}^{rel}_{21}     = \vec{v}_{2}     - \vec{v}_{1} \\
  \quad \forall \vec{\omega}^{rel}_{21} = \vec{\omega}_{2} - \vec{\omega}_{1} \\
\end{cases}
\qquad , \qquad
\begin{cases}
  \qquad \vec{F}_{12} = - \vec{F}_{21} \\
  \vec{0} =  \vec{M}_{12} = \vec{M}_{21} \\
\end{cases}
$$

#### Roller
The roller constraint can be thought of as a combination of a slider and a cylindrical joint.

$$
\begin{cases}
  \quad \forall \ \vec{v}^{rel}_{\hat{t},21}     = \vec{v}_{\hat{t},2}     - \vec{v}_{\hat{t},1} \\
          0  = v^{rel}_{\hat{n},21}     = v_{\hat{n},2}     - v_{\hat{n},1} \\
  \quad \forall \ \omega^{rel}_{\hat{t},21} = \omega_{\hat{t},2} - \omega_{\hat{t},1} \\
  \vec{0} = \vec{\omega}^{rel}_{\hat{n},21} = \vec{\omega}_{\hat{n},2} - \vec{\omega}_{\hat{n},1} \\
\end{cases}
\qquad , \qquad
\begin{cases}
  \vec{0} = \vec{F}_{\hat{t},12} = \vec{F}_{\hat{t},21} \\
  \qquad F_{\hat{n},12} = - F_{\hat{n},21} \\
  0 =  M_{\hat{t},12} = M_{\hat{t},21} \\
  \qquad \vec{M}_{\hat{n},12} = - \vec{M}_{\hat{n},21} \\
\end{cases}
$$

#### Support
The support constraint is a unilateral constraint **todo** *add description*

(classical-mechanics:actions:reactions:contact:friction)=
### Friction
(classical-mechanics:actions:reactions:contact:friction:static)=
#### Static Friction

Static friction is the type of friction that occurs between two bodies when there is no relative motion between them, acting as a tangential force to the contact surface. The simplest model of static friction assumes that the maximum static friction force $F^s_{max}$ that can be exerted between two bodies is proportional to the normal reaction between them, $N$,

$$F^s_{max} = \mu^s \, N \ .$$

The proportionality constant $\mu^s$ is defined as the **coefficient of static friction**. Generally, static friction forces are determined by the equilibrium conditions of the body, if these conditions can be met, and the relation

$$|F^s| \ge F^s_{max} \ .$$

(classical-mechanics:actions:reactions:contact:friction:dynamic)=
#### Dynamic Friction

Dynamic friction occurs between two bodies in contact and in relative motion, acting as a tangential force to the contact surface. The simplest model of dynamic friction assumes that the dynamic friction force is proportional to the normal reaction between the two bodies and directed opposite to the relative velocity,

$$\vec{F}_{12} = - \mu^d N \frac{\vec{v}_{12}}{|\vec{v}_{12}|} \ ,$$

where $\vec{F}_{12}$ is the force acting on body 1 due to body 2, and $\vec{v}_{12} = \vec{v}_1 - \vec{v}_2$ is the velocity of body 1 relative to body 2.

(classical-mechanics:actions:reactions:contact:friction:pure-rolling)=
#### Pure Rolling
**todo** *add description*

