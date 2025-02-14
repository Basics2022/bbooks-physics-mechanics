(classical-mechanics:exercise:dynamics)=
# Dynamics

<!-- Exercise -->
```{exercise}
**todo** Add description of the problem and image

Find:
- the pure equations of motion (solution methods: dynamical equilibria, Lagrange II,...) **done**
- constraint reactions (solution methods: dynamical equilibria, Lagrange I,...) **todo**
- equilibria and their stability **todo**
- evolution of the linear(ized) dynamics of the system around stable equilibria **todo**

```

```{dropdown} Solution.

**Kinematics.** Using $x$, $\theta$ as generalized coordinates,

$$\begin{cases}
  \vec{r}_A = x \hat{x} \\
  \vec{r}_B = ( x + \ell \sin \theta ) \hat{x} + \ell \cos \theta \hat{y} \\
\end{cases}$$

$$\begin{cases}
  \vec{v}_A = \dot{x} \hat{x} \\
  \vec{v}_B = ( \dot{x} + \ell \dot{\theta} \cos \theta ) \hat{x} - \ell \dot{\theta} \sin \theta \hat{y} \\
\end{cases}$$

**Lagrangian function.**

$$\mathscr{L} = K + U$$

$$\begin{aligned}
  K & = \frac{1}{2} m_A |\vec{v}_A|^2 + \frac{1}{2} m_B |\vec{v}_B|^2 = \\
    & = \frac{1}{2} m_A \dot{x}^2 + \frac{1}{2} m_B \left( \dot{x}^2 + \ell^2 \dot{\theta}^2 + 2 \ell \dot{x} \dot{\theta} \cos \theta  \right) 
\end{aligned}$$
$$\begin{aligned}
  U & = - \frac{1}{2} k x_A^2 + m_B g y_B = \\
    & = - \frac{1}{2} k x^2 + m_B g \ell \cos \theta  
\end{aligned}$$

**Lagrange equations (II type)** RHS of Lagrange equations read

$$\begin{aligned}
  \dfrac{d}{dt}\left( \frac{\partial \mathscr{L}}{\partial \dot{x}} \right) & = \dfrac{d}{dt} \left( m_A \dot{x} + m_B \dot{x} + m_B \ell \dot{\theta} \cos \theta \right) = \left( m_A + m_B \right) \ddot{x} + m_B \ell \ddot{\theta} \cos \theta - m_B \ell \dot{\theta}^2 \sin \theta \\
                      \frac{\partial \mathscr{L}}{\partial      x }         & = -k x \\
\end{aligned}$$

$$\begin{aligned}
  \dfrac{d}{dt}\left( \frac{\partial \mathscr{L}}{\partial \dot{\theta}} \right) & = \dfrac{d}{dt} \left( m_B \ell^2 \dot{\theta} + m_B \ell \dot{x} \cos \theta \right) = m_B \ell^2 \ddot{\theta} + m_B \ell \ddot{x} \cos \theta - m_B \ell \dot{x} \dot{\theta} \sin \theta  \\
                      \frac{\partial \mathscr{L}}{\partial      \theta }         & = - m_B \ell \dot{x} \dot{\theta} \sin \theta - m_B g \ell \sin \theta  \\
\end{aligned}$$

Generalized forces read

$$Q_x = F$$
$$Q_\theta = C$$

so that the pure equations of motion follows from Lagrange equations $\frac{d}{dt} \left( \frac{\partial \mathscr{L}}{\partial \dot{q}} \right) - \frac{\partial \mathscr{L}}{\partial q} = Q_q$ 

$$\begin{cases}
  \left( m_A + m_B \right) \ddot{x} + m_B \ell \ddot{\theta} \cos \theta - m_B \ell \dot{\theta}^2 \sin \theta + k x = F \\ 
  m_B \ell^2 \ddot{\theta} + m_B \ell \ddot{x} \cos \theta - m_B \ell \dot{x} \dot{\theta} \sin \theta + m_B \ell \dot{x} \dot{\theta} \sin \theta + m_B g \ell \sin \theta = C \\ 
\end{cases}$$

and after the simplifications

$$\begin{cases}
  \left( m_A + m_B \right) \ddot{x} + m_B \ell \ddot{\theta} \cos \theta - m_B \ell \dot{\theta}^2 \sin \theta + k x = F \\ 
  m_B \ell \ddot{x} \cos \theta + m_B \ell^2 \ddot{\theta} + m_B g \ell \sin \theta = C \\ 
\end{cases}$$

**Obs.** The first equation is the $x$-component of the momentum equation of the whole system. The second equation is the angular momentum equation of the rod around the hinge in $A$.

```

```{dropdown} Generalized forces on rigid bodies
:open:

Following the derivation of the [Lagrange equations for rigid bodies](classical-mechanics:lagrange:rigid), generalized forces are

$$Q_q = \frac{\partial \vec{r}_G}{\partial q} \cdot \vec{R}^e + \frac{\partial \vec{\theta}}{\partial q} \cdot \vec{M}_G^e$$

With the definition of $\theta_{\delta}$ in the increment of the rigid body motion

$$d \vec{r}_A = d \vec{r}_B + \theta_{\delta} \times (A - B) \ ,$$

and writing the resultant of forces and moments as

$$\begin{aligned}
  \vec{R}^e   & = \sum_i \vec{F}_i \\
  \vec{M}^e_G & = \sum_i \left( \vec{r}_G - \vec{r}_i \right) \times \vec{F}_i + \sum_i \vec{C}_i \\
\end{aligned}$$

the generalized force can be recast as

$$\begin{aligned}
  Q_q 
  & = \frac{\partial \vec{r}_G}{\partial q} \cdot \vec{R}^e + \frac{\partial \vec{\theta}}{\partial q} \cdot \vec{M}_G^e = \\
  & = \frac{\partial \vec{r}_G}{\partial q} \cdot \sum_i \vec{F}_i + \frac{\partial \vec{\theta}}{\partial q} \cdot \left[ \sum_i \left( \vec{r}_G - \vec{r}_i \right) \times \vec{F}_i + \sum_i \vec{C}_i  \right] = \\
  & = \sum_i \left[ \frac{\partial \vec{r}_G}{\partial q} + \frac{\partial \vec{\theta}}{\partial q} \times \left( \vec{r}_G - \vec{r}_i \right) \right] \cdot \vec{F}_i + \sum_i \frac{\partial \vec{\theta}}{\partial q} \cdot \vec{C}_i = \\
  & = \sum_i \frac{\partial \vec{r}_i}{\partial q} \cdot \vec{F}_i + \sum_i \frac{\partial \vec{\theta}}{\partial q} \cdot \vec{C}_i \ ,
\end{aligned}$$

i.e. as the contribution of the single forces $\vec{F}_i$ acting on different points $\vec{r}_i$ the rigid body and the overall contribution of the couples of forces $\vec{C}_i$.

With $\vec{r}_C\left(q(t),t \right)$ and $\mathbb{R}\left(q(t), t \right)$,

$$\vec{r}_i(q(t), t) - \vec{r}_C(q(t), t) = \mathbb{R}(q(t), t) \cdot \left( \vec{r}_i^0 - \vec{r}_C^0 \right)$$

Time derivative becomes

$$\begin{aligned}
\vec{v}_i - \vec{v}_C
 & = \left[ \dot{q}(t) \, \frac{\partial \mathbb{R}}{\partial q} + \frac{\partial \mathbb{R}}{\partial t} \right] \cdot \left( \vec{r}_i^0 - \vec{r}_C^0 \right) = \\
 & =  \left[ \dot{q}(t) \, \frac{\partial \mathbb{R}}{\partial q} + \frac{\partial \mathbb{R}}{\partial t} \right] \cdot \mathbb{R}^T \cdot \underbrace{\mathbb{R} \cdot \left( \vec{r}_i^0 - \vec{r}_C^0 \right)}_{\vec{r}_i - \vec{r}_C}
\end{aligned}$$

$$\begin{aligned}
  \vec{\omega}_\times & = \dot{\mathbb{R}} \cdot \mathbb{R}^T \\
  \delta \vec{\theta}_{\times} & = \delta \mathbb{R} \cdot \mathbb{R}^T \\
  \frac{\partial \vec{\theta}_{\times}}{\partial q} & = \dfrac{\partial \mathbb{R}}{\partial q} \cdot \mathbb{R}^T
\end{aligned}$$


```

<!-- Exercise -->
```{exercise}
**todo** Add description of the problem and image

Find:
- the pure equations of motion (solution methods: dynamical equilibria, Lagrange II, Kinetic energy theorem - energy conservation - since the problem has 1 dof,...) **done**
- constraint reactions (solution methods: dynamical equilibria, Lagrange I,...) **todo**
- equilibria and their stability **todo**
- evolution of the linear(ized) dynamics of the system around stable equilibria **todo**

```
```{dropdown} Solution
**Geometry.**

$$\begin{aligned}
  R & = d \sin \alpha \\
  b & = d \cos^2 \alpha \\
\end{aligned}$$

so that $\frac{b}{R} = \frac{\cos^2 \alpha}{\sin \alpha}$.

**Kinematics.**

Position of the center of mass, $C$

$$\begin{aligned}
  \vec{r}_C & = b \cos \theta \hat{x} + b \sin \theta \hat{y} - h \hat{z} \\
  \vec{v}_C & = -b \dot{\theta} \sin \theta \hat{x} + b \dot{\theta} \cos \theta \hat{y} = b \dot{\theta} \hat{y}_1 \\
\end{aligned}$$

Angular velocity $\vec{\omega}$ of the rigid body

$$\vec{\omega} = \dot{\theta} \hat{z} + \dot{\varphi} \hat{x}_1$$

Velocity of point contact point $A$ is zero, $\vec{v}_A = \vec{0}$ for **pure rolling** constraint. Being $(A-C) = R \hat{z}_1$, the general expression of $\vec{v}_A$ as function of $\theta$ and $\varphi$ reads

$$\begin{aligned}
 \vec{v}_A
 & = \vec{v}_C + \vec{\omega} \times \left( A - C \right) = \\
 & = \hat{y}_1 b \dot{\theta} + \left( \dot{\theta} \hat{z} + \dot{\varphi} \hat{x}_1 \right) \times R \hat{z}_1 = \\
 & = \hat{y}_1 \left( b \dot{\theta} + R \dot{\theta} \sin \alpha - R \dot{\varphi} \right) = \\
\end{aligned}$$

so that the kinetatic constraint (integrable, with arbitrary initial condition) between $\theta$ and $\varphi$ is

$$R \varphi = \left( R \sin \alpha + b \right) \, \theta \ .$$

**Lagrangian function.**

With

$$\mathbb{I}_C = I_{x} \hat{x}_1 \hat{x}_1 + I_{y} \hat{y}_1 \hat{y}_1 + I_{z} \hat{z}_1 \hat{z}_1 \ ,$$
$$\vec{\omega} = \dot{\theta} \hat{z} + \dot{\varphi} \hat{x}_1 = \left( \dot{\varphi} - \dot{\theta} \sin \alpha  \right) \hat{x}_1 + \dot{\theta} \cos \alpha \hat{z}_1 $$

and using

$$\dot{\varphi} - \dot{\theta} \sin \alpha = \frac{b}{R} \dot{\theta} \ ,$$

the Lagrangian function becomes

$$\begin{aligned}
  \mathscr{L} & = K + U = \\
  & =\frac{1}{2} m |\vec{v}_C|^2 + \frac{1}{2} \vec{\omega} \cdot \mathbb{I}_C \cdot \vec{\omega} + m g x_C = \\
  & =\frac{1}{2} m b^2 \dot{\theta}^2 + \frac{1}{2} \left[ I_x \left( \dot{\varphi} - \dot{\theta} \sin \alpha \right)^2 + I_z \dot{\theta}^2 \cos^2 \alpha \right] + m g b \cos \theta = \\
  & =\frac{1}{2} m b^2 \dot{\theta}^2 + \frac{1}{2} \left[ I_x \left( \frac{b}{R} \right)^2 + I_z \cos^2 \alpha \right] \dot{\theta}^2 + m g b \cos \theta = \\
  & =\frac{1}{2} \widetilde{I} \dot{\theta}^2 + m g b \cos \theta  \ ,
\end{aligned}$$

with the equivalent inertia

$$\widetilde{I} = m b^2 + I_x \left( \frac{b}{R} \right)^2 + I_z \cos^2 \alpha \ .$$


**Method 1. Lagrange equation (II).** Legrange equation gives a pure equation of motion

$$\begin{aligned}
  0 & = \dfrac{d}{dt}\left( \frac{\partial \mathscr{L}}{\partial \dot{\theta}} \right) - \frac{\partial \mathscr{L}}{\partial \theta} = \widetilde{I} \ddot{\theta} + m g b \sin \theta \ . \\
\end{aligned}$$


**Method 2. Kinetic energy theorem - or energy conservation**

```
<!-- Exercise -->
```{exercise} Inverted pendulum
```
```{dropdown} Solution
```
<!-- Exercise -->
```{exercise} 
```
```{dropdown} Solution
```



