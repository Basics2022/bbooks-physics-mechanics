(classical-mechanics:kinematics:rotations)=
# Rotations

## Rotation tensor

Given 2 Cartesian bases $\{ \hat{e}^0_i \}_{i=1:3}$, $\{ \hat{e}^1_j \}_{j=1:3}$, the rotation tensor providing the transformation

$$\hat{e}^1_i = \mathbb{R}^{0 \rightarrow 1} \cdot \hat{e}^0_i \ ,$$

is

$$\mathbb{R}^{0 \rightarrow 1}
 = R_{ij}^{0 \rightarrow 1} \hat{e}^0_i \otimes \hat{e}^0_j  
 = R_{ij}^{0 \rightarrow 1} \hat{e}^1_i \otimes \hat{e}^1_j 
$$

with $R^{0 \rightarrow 1}_{ij} = \hat{e}^0_i \cdot \hat{e}^1_j$.

**Angular velocity.**

$$\vec{\omega}^{01}_{\times} = \mathbb{\Omega}^{01} = \dot{\mathbb{R}}^{01} \cdot \mathbb{R}^{01,T}$$

Using index notation

$$\varepsilon_{ijk} \omega_j = \dot{R}_{ij} R_{kj}$$

and the identities

$$\varepsilon_{ijk} \varepsilon_{lmk} = \delta_{il} \delta_{jm} - \delta_{jl} \delta_{im}$$
$$\varepsilon_{ijk} \varepsilon_{ljk} = \delta_{il} \delta_{jj} - \delta_{ij} \delta_{jl} = 3 \delta_{il} - \delta_{il} = 2 \delta_{il}$$

it follows

$$\varepsilon_{ilk} \varepsilon_{ijk} \omega_j = \varepsilon_{ilk} \dot{R}_{ij} R_{kj}$$
$$2 \delta_{lj} \omega_j = \varepsilon_{ilk} \dot{R}_{ij} R_{kj}$$
$$\omega_l = \frac{1}{2} \varepsilon_{ilk} \dot{R}_{ij} R_{kj} = - \frac{1}{2} \varepsilon_{lik} \dot{R}_{ij} R_{kj} = -\frac{1}{2} \varepsilon_{lij} \Omega_{ij}$$

**Angular acceleration.** Angular acceleration, $\vec{\alpha}$, is the time derivative of angular velocity, $\vec{\omega}$,

$$\vec{\alpha} = \dot{\vec{\omega}} \ .$$

## Successive rotations

**Orientation.** Given 3 Cartesian bases $\{ \hat{e}^0_i \}_{i=1:3}$, $\{ \hat{e}^1_j \}_{j=1:3}$, $\{ \hat{e}^2_k \}_{k=1:3}$,

$$\begin{aligned}
 \hat{e}^2_i 
  & = \mathbb{R}^{1 \rightarrow 2} \cdot \hat{e}^1_i = \\ 
  & = \mathbb{R}^{1 \rightarrow 2} \cdot \mathbb{R}^{0 \rightarrow 1} \cdot\hat{e}^0_i 
\end{aligned} \ , $$

i.e composition of rotations holds

$$\mathbb{R}^{0 \rightarrow 2} = \mathbb{R}^{1 \rightarrow 2} \cdot \mathbb{R}^{0 \rightarrow 1} \ .$$

**Angular velocity.** Time derivative w.r.t. reference frame 0 is indicated as the standard time derivative

$$\dot{a} = \dfrac{d a}{d t} = \dfrac{{}^0 d a}{d t} = \dfrac{{}^1 d}{dt} + \vec{\omega}_{1/0} \times \ ,$$

$$\begin{aligned}
\dfrac{d}{dt} \mathbb{R}^{21} 
  & = \frac{d}{dt} \left[ R^{21}_{ik} \hat{e}^1_i \otimes \hat{e}^1_k \right] = \\
  & = \dot{R}^{21}_{ik} \hat{e}^1_i \otimes \hat{e}^1_k + \mathbb{\Omega}^{10} \cdot  \mathbb{R}^{21} - \mathbb{R}^{21} \cdot \mathbb{\Omega}^{10} = \\
  & = \dfrac{{}^1 d}{dt} \mathbb{R}^{21} + \mathbb{\Omega}^{10} \cdot  \mathbb{R}^{21} - \mathbb{R}^{21} \cdot \mathbb{\Omega}^{10} = \\
\end{aligned}$$

$$\begin{aligned}
 \mathbb{\Omega}^{20}
 & = \dot{\mathbb{R}}^{20} \cdot \mathbb{R}^{20, T} = \\
 & = \frac{d}{dt} \left( \mathbb{R}^{21} \cdot \mathbb{R}^{10} \right) \cdot \mathbb{R}^{20, T} = \\
 & = \left\{ \left[ \dfrac{{}^1 d}{dt} \mathbb{R}^{21} + \mathbb{\Omega}^{10} \cdot  \mathbb{R}^{21} - \mathbb{R}^{21} \cdot \mathbb{\Omega}^{10} \right] \cdot \mathbb{R}^{10} + \mathbb{R}^{21} \cdot \dot{\mathbb{R}}^{10}  \right\} \cdot \mathbb{R}^{01} \cdot \mathbb{R}^{12} = \\
 & =  \dfrac{{}^1 d}{dt} \mathbb{R}^{21} \cdot \mathbb{R}^{12} + \mathbb{\Omega}^{10} = \\
 & = \mathbb{\Omega}^{21} + \mathbb{\Omega}^{10} \ .
\end{aligned}$$

so that addition of relative angular velocity holds

$$\mathbb{\Omega}^{20} = \mathbb{\Omega}^{21} + \mathbb{\Omega}^{10} \qquad , \qquad \vec{\omega}_{2/0} = \vec{\omega}_{2/1} + \vec{\omega}_{1/0} \ .$$

**Angular acceleration.** Time derivative of angular velocity composition provides the addition of relative angular accelerations

$$\dfrac{{}^0 d}{dt} \vec{\omega}_{2/0} = \dfrac{{}^0 d}{dt} \vec{\omega}_{2/1} + \dfrac{{}^0 d}{dt} \vec{\omega}_{1/0} \ ,$$

or

$$\vec{\alpha}_{2/0} = \vec{\alpha}_{2/1} + \vec{\alpha}_{1/0} \ .$$

## Linearization of rotations

$$\mathbb{I} = \mathbb{R} \cdot \mathbb{R}^T$$

Increment

$$\mathbb{0} = \delta \mathbb{R} \cdot \mathbb{R}^T + \mathbb{R} \cdot \delta \mathbb{R}^T$$

and thus the antisymmetric tensor can be written as

$$\delta \theta_{\times} := \delta \mathbb{R} \cdot \mathbb{R}^T = \delta \mathbb{\Theta} \ ,$$

so that

$$\delta \theta_l = -\frac{1}{2} \varepsilon_{lij} \delta R_{ik} \, R_{jk} = - \frac{1}{2} \varepsilon_{lij} \delta \Theta_{ij}$$

(classical-mechanics:kinematics:rotations:param)=
## Parametrizations
Minimal sets of parameters to represent rotations have 3 parameters. However these sets of parameters are not regular over all the possible rotations, and the transformation becomes singular somewhere. [Quaternions](classical-mechanics:kinematics:rotations:param:quaternions) provide a set of 4 parameters for a regular parametrization of rotations

(classical-mechanics:kinematics:rotations:param:euler)=
### Euler angles
(classical-mechanics:kinematics:rotations:param:axis)=
### Axis and rotation angle

(classical-mechanics:kinematics:rotations:param:quaternions)=
### Quaternions
