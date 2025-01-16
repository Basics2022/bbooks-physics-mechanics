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

### Successive rotations

Given 3 Cartesian bases $\{ \hat{e}^0_i \}_{i=1:3}$, $\{ \hat{e}^1_j \}_{j=1:3}$, $\{ \hat{e}^2_k \}_{k=1:3}$,

$$\begin{aligned}
 \hat{e}^2_i 
  & = \mathbb{R}^{1 \rightarrow 2} \cdot \hat{e}^1_i = \\ 
  & = \mathbb{R}^{1 \rightarrow 2} \cdot \mathbb{R}^{0 \rightarrow 1} \cdot\hat{e}^0_i 
\end{aligned}$$

Time derivative w.r.t. reference frame 0 is indicated as the standard time derivative

$$\dot{a} = \dfrac{d a}{d t} = \dfrac{{}^0 d a}{d t} \ ,$$



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

### Linearization of rotations

$$\mathbb{I} = \mathbb{R} \cdot \mathbb{R}^T$$

Increment

$$\mathbb{0} = \delta \mathbb{R} \cdot \mathbb{R}^T + \mathbb{R} \cdot \delta \mathbb{R}^T$$

and thus the antisymmetric tensor can be written as

$$\delta \theta_{\times} := \delta \mathbb{R} \cdot \mathbb{R}^T$$

so that

$$\delta \theta_l = -\frac{1}{2} \varepsilon_{lij} \delta R_{ik} \, R_{jk}$$

## Quaternions
