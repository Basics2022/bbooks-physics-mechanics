(classical-mechanics:kinematics:rotations:tensor)=
# Tensor formalism for rotations

This section deals with the tensor formalism to represent rotations, its increment and angular velocity, and composition. First the expression of the rotation tensor rotating a Cartesian basis $\{ \hat{e}_i^0\}_i$ into another Cartesian basis $\{ \hat{e}^1_j\}_j$ is given, then angular velocity and angular acceleration are defined and their role in the description of the motion of rigid bodies is discussed.
Then successive rotations are discussed: a rotation can be represented as the composition of many rotations, via dot tensor product of the rotation tensors, while the corresponding angular velocity can be written as the sum of the angular velocity of the successive relative rotations.

(classical-mechanics:kinematics:rotations:tensor:components)=
## Rotation tensor

Given 2 right-handed Cartesian bases $\{ \hat{e}^0_i \}_{i=1:3}$, $\{ \hat{e}^1_j \}_{j=1:3}$, a rotation transforming the first basis $\{ \hat{e}^0_i \}_i$ into the second basis $\{ \hat{e}^1_j \}_j$ exists, and can be represented by unitary tensor with unit determinant, the rotation tensor $\mathbb{R}$.
Given that for Cartesian bases (**todo** add link to Math:Vector Algebra)[^vector-algebra:basis-transformation]

[^vector-algebra:basis-transformation]: In general, basis transformation rely on the reciprocal basis,
  $\mathbf{b}^j$, defined as those set of vectors $\mathbf{b}^j \cdot \mathbf{b}_i = \delta_i^j$. A vector $\mathbf{w}$ can be written using two different bases $\{ \mathbf{u}_i \}_i$ and $\{ \mathbf{v}_j \}_j$, as $\mathbf{w} = u^i \mathbf{u}_i = v^j \mathbf{v}_j$. The vectors of a basis can be written as a linear combinations of the vectors of the other basis, namely $\mathbf{v}_j = T^i_j \mathbf{u}_i$, or $\mathbf{u}_i = \tilde{T}^{j}_i \mathbf{v}_j$, using the inverse transformation $T^{-1} := \tilde{T}$, defined as $\tilde{T}^k_i T^i_j = \delta^k_j$. Exploiting the definition of the reciprocal basis, it should be not hard to prove that $T^i_j = \mathbf{v}_j \cdot \mathbf{u}^i$ and $\tilde{T}^j_i = \mathbf{v}^j \cdot \mathbf{u}_i$. As the reciprocal basis of a Cartesian basis is the basis itself ($\mathbf{e}^j = g^{ij} \mathbf{e}_i$, with $g_{ij} = g^{ij} = \delta_{ij}$), the components of the transformation between two Cartesian bases read $T_j^i = \mathbf{u}_i \cdot \mathbf{v}_j$, while the inverse transform involves the transpose, $\tilde{T} = T^T$: $\mathbf{v}_j = T_j^i \mathbf{u}_i = \left( \mathbf{v}_j \cdot \mathbf{u}_i \right) \mathbf{u}_i$, or $\mathbf{u}_i = T_i^j \mathbf{v}_j = \left( \mathbf{u}_i \cdot \mathbf{v}_j \right) \mathbf{v}_j$.

$$\hat{e}_k^1 = \left( \hat{e}_k^1 \cdot \hat{e}^0_i \right) \hat{e}^0_i \ ,$$

this expression can be recast using tensor formalism and introducing rotation tensor

$$\begin{aligned}
  \hat{e}_k^1
  & = \left( \hat{e}_k^1 \cdot \hat{e}^0_i \right) \hat{e}^0_i = \\
  & = \left( \hat{e}_j^1 \cdot \hat{e}^0_i \right) \hat{e}^0_i \delta_{jk} = \\
  & = \left( \hat{e}_j^1 \cdot \hat{e}^0_i \right) \hat{e}^0_i \otimes \hat{e}^0_j \cdot \hat{e}^0_k = \\
  & = \mathbb{R}^{0 \rightarrow 1} \cdot \hat{e}^0_k \ ,
\end{aligned}$$

having defined the rotation tensor $\mathbb{R}^{0 \rightarrow 1}$ transforming the vectors of basis $\{ \hat{e}^0_i \}_i$ into vectors of basis $\{ \hat{e}^1_j \}_j$ as

$$\mathbb{R}^{0 \rightarrow 1}
 = R_{ij}^{0 \rightarrow 1} \hat{e}^0_i \otimes \hat{e}^0_j 
 = \left( \hat{e}^0_i \cdot \hat{e}^1_j \right) \hat{e}^0_i \otimes \hat{e}^0_j
$$

having defined the components of the rotation from $0$ to $1$ w.r.t. basis $0$ as $R^{0 \rightarrow 1}_{ij} = \hat{e}^0_i \cdot \hat{e}^1_j$.

````{admonition} Rotation tensor is unitary with unit determinant: component relation
:class: tip

As $\mathbb{R} \cdot \mathbb{R}^T = \mathbb{R}^T \cdot  \mathbb{R} =  \mathbb{I}$, it follows

$$R_{ij} R_{kj} = R_{ji} R_{jk} = \delta_{ik} \ .$$


```{dropdown} Proof
Let's prove the first relation, explicitly writing rotation tensor using basis $\{ \hat{e}^0_i \}_i$,

$$\begin{aligned}
  \delta_{ik} \hat{e}^0_i \otimes \hat{e}^0_k = \mathbb{I} 
  & = \mathbb{R} \cdot \mathbb{R}^T = \\
  & = \left( R_{ij}^{0 \rightarrow 1} \hat{e}^0_i \otimes \hat{e}^0_j  \right) \cdot \left( R_{lk}^{0 \rightarrow 1} \hat{e}^0_l \otimes \hat{e}^0_k \right)^T = \\
  & = \left( R_{ij}^{0 \rightarrow 1} \hat{e}^0_i \otimes \hat{e}^0_j  \right) \cdot \left( R_{kl}^{0 \rightarrow 1} \hat{e}^0_l \otimes \hat{e}^0_k \right) = \\
  & = R_{ij}^{0 \rightarrow 1} \, R_{kl}^{0 \rightarrow 1} \, \hat{e}^0_i \otimes \underbrace{\hat{e}^0_j  \cdot  \hat{e}^0_l}_{\delta_{jl}} \otimes \hat{e}^0_k  = \\
  & = R_{ij}^{0 \rightarrow 1} \, R_{kj}^{0 \rightarrow 1} \, \hat{e}^0_i \otimes \hat{e}^0_k \ ,
\end{aligned}$$

and thus $\delta_{ik} = R_{ij}^{0 \rightarrow 1} \, R_{kj}^{0 \rightarrow 1} $.

**todo** *Show that $\mathbb{I}$ has the same components in all the (Cartesian?) reference frames. Show the rule of transformation of Ricci tensor also.*


```
````

```{admonition} Components of a rotation tensor are the same in the original and transformed basis
:class: tip

Components of the rotation tensor are the same if referred to the original or to the rotated basis.

$$\begin{aligned}
  \mathbb{R}^{0 \rightarrow 1} 
  & = R^{0 \rightarrow 1, 00}_{ij} \hat{e}^0_i \otimes \hat{e}^0_j = \\
  & = \underbrace{ R^{0 \rightarrow 1, 00}_{ij}  \left( R^{0 \rightarrow 1, 00 }_{ik}\right.}_{= \delta_{jk}} \left. \hat{e}^1_k \right) \otimes \left( R^{0 \rightarrow 1, 00}_{jl} \hat{e}^1_l \right) = \\
  & = R^{0 \rightarrow 1, 00}_{kl} \hat{e}^1_k \otimes \hat{e}^1_{l} \ ,
\end{aligned}$$

and thus the components w.r.t. basis $1$ equal the component w.r.t. basis $0$, $R^{0 \rightarrow 1, 11} = R^{0\rightarrow 1, 00}$.
Transforming only one set of vectors of the rank-2 tensor, the rotation tensor can be further written as

$$\mathbb{R}^{0 \rightarrow 1} = \delta_{jk} \hat{e}^1_k \otimes \hat{e}^0_j \ .$$

It's immediate to show the correctness of the last expression, showing the effect of tensor rotation on the vectors of the basis $0$,

$$\mathbb{R}^{0 \rightarrow 1} \cdot \hat{e}^0_i = \left( \delta_{jk} \, \hat{e}^1_k \otimes \hat{e}^0_j \right) \cdot \hat{e}^0_i = \hat{e}^1_k \, \delta_{jk} \, \delta_{ji} = \hat{e}^1_i \ .$$

```

### Rotation of a vector
...

### Rotation of basis, and change of components of given vectors and tensors
...

## Angular velocity and acceleration

**Angular velocity.** Taken time derivative of the unitary relation **todo** *add ref*, the definition of angular velocity naturally arises. As the identity tensor is constant,

$$\mathbb{0} = \dot{\mathbb{R}} \cdot \mathbb{R}^T + \mathbb{R} \cdot \dot{\mathbb{R}}^T \ ,$$

and thus tensor $\dot{\mathbb{R}} \cdot \mathbb{R}^T$ is anti-symmetric, 

$$\dot{\mathbb{R}} \cdot \mathbb{R}^T = - \mathbb{R} \cdot \dot{\mathbb{R}}^T = - \left( \dot{\mathbb{R}} \cdot \mathbb{R}^T \right)^T \ ,$$

and thus it can be written as the *cross* (**todo** *check the def*) of a vector,

$$\vec{\omega}_{\times} = \dot{\mathbb{R}} \cdot \mathbb{R}^T \ ,$$

defined angular velocity.

As it will be clear in the [section about successive rotations](classical-mechanics:kinematics:rotations:tensor:successive), the angular velocity $\vec{\omega}^{1/0}$ of a reference frame $1$ w.r.t. a reference frame $0$ is defined by the relation

$$\vec{\omega}^{1/0}_{\times} := \mathbb{\Omega}^{1/0} = \dfrac{{}^0 d }{d t}\mathbb{R}^{0\rightarrow 1} \cdot \mathbb{R}^{1 \rightarrow 0} \ ,$$

having replaced the trasponse tensor with the tensor of the inverse rotation $1 \rightarrow 0$.

Using the properties of Dirac's delta and Ricci's tensor, it's possible to retrive the angular velocity vector $\vec{\omega}$,

$$\omega^0_l = \frac{1}{2} \varepsilon^0_{ilk} \dot{R}_{ij} R_{kj} = - \frac{1}{2} \varepsilon_{lik} \dot{R}_{ij} R_{kj} = -\frac{1}{2} \varepsilon_{lij} \Omega_{ij}$$

**todo**
- $$\omega^1_k = \dots$$
- *Explicitly discuss the two common uses of rotation tensors: 1. rotate a given vector into a new vector; 2. write components of a given vector w.r.t. 2 different Cartesian bases.*

```{dropdown} Proof

Using index notation

$$\varepsilon_{ijk} \omega^0_j \hat{e}^0_i \hat{e}^0_k = \dot{R}_{ij} R_{kj} \hat{e}^0_i \hat{e}^0_j \ ,$$

and the identities

$$\begin{aligned}
  \varepsilon_{ijk} \varepsilon_{lmk} & = \delta_{il} \delta_{jm} - \delta_{jl} \delta_{im} \\
  \varepsilon_{ijk} \varepsilon_{ljk} & = \delta_{il} \delta_{jj} - \delta_{ij} \delta_{jl} = 3 \delta_{il} - \delta_{il} = 2 \delta_{il}
\end{aligned}$$

it follows

$$\begin{aligned}
  \varepsilon_{ilk} \varepsilon_{ijk} \omega^0_j & = \varepsilon_{ilk} \dot{R}_{ij} R_{kj} \\
  2 \delta_{lj} \omega^0_j & = \varepsilon_{ilk} \dot{R}_{ij} R_{kj}
\end{aligned}$$

and eventually

$$\omega^0_l = \frac{1}{2} \varepsilon_{ilk} \dot{R}_{ij} R_{kj} = - \frac{1}{2} \varepsilon_{lik} \dot{R}_{ij} R_{kj} = -\frac{1}{2} \varepsilon_{lij} \Omega_{ij} \ .$$


```

**Angular acceleration.** Angular acceleration, $\vec{\alpha}$, is the time derivative of angular velocity, $\vec{\omega}$,

$$\vec{\alpha} = \dot{\vec{\omega}} \ .$$

(classical-mechanics:kinematics:rotations:tensor:successive)=
## Sequence of rotations

A rotation may be represented as the composition of successive rotations. The vectors of a Cartesian basis $\{ \vec{e}_i^0 \}_i$ can be transformed into the vectors of the Cartesian basis $\{ \vec{e}_k^2 \}_k$, first rotating $0$ into an intermediate basis $1$, and then rotating $1$ into $2$. 

  $$\mathbb{R}^{0 \rightarrow 2} = \mathbb{R}^{1 \rightarrow 2} \cdot \mathbb{R}^{0 \rightarrow 1}$$ (eq:rot:sequence:rot)

Angular velocity of the reference frame $2$ w.r.t. $0$ can be written as the sum of the relative angular velocity of the intermediate rotations,

  $$\vec{\omega}^{2/0} = \vec{\omega}^{2/1} + \vec{\omega}^{1/0}$$ (eq:rot:sequence:vel)

The same relation holds for angular acceleration

  $$\vec{\alpha}^{2/0} = \vec{\alpha}^{2/1} + \vec{\alpha}^{1/0}$$ (eq:rot:sequence:acc)

```{dropdown} Orientation

Given 3 Cartesian bases $\{ \hat{e}^0_i \}_{i=1:3}$, $\{ \hat{e}^1_j \}_{j=1:3}$, $\{ \hat{e}^2_k \}_{k=1:3}$,

$$\begin{aligned}
 \hat{e}^2_i 
  & = \mathbb{R}^{1 \rightarrow 2} \cdot \hat{e}^1_i = \\ 
  & = \mathbb{R}^{1 \rightarrow 2} \cdot \mathbb{R}^{0 \rightarrow 1} \cdot\hat{e}^0_i 
\end{aligned} \ , $$

i.e composition of rotations holds

$$\mathbb{R}^{0 \rightarrow 2} = \mathbb{R}^{1 \rightarrow 2} \cdot \mathbb{R}^{0 \rightarrow 1} \ .$$

```

```{dropdown} Angular velocity

Indicating with the apex a time derivative performed keeping constant the vectors of the basis, the following relations hold for vectors and tensors

$$\dfrac{d}{dt}{\vec{a}} = \dfrac{d }{d t} \left( a^1_i \hat{e}^1_i  \right) = \dot{a}^1_i \hat{e}^1_i + a^1_i \vec{\omega}^{1/0} \times \hat{e}^1_i = \dfrac{{}^1 d}{d t} \vec{a} + \vec{\omega}^{1/0} \times \vec{a} $$

$$\begin{aligned}
\dfrac{d}{dt} \mathbb{R}^{1 \rightarrow 2} 
  & = \frac{d}{dt} \left[ R^{1 \rightarrow 2}_{ik} \hat{e}^1_i \otimes \hat{e}^1_k \right] = \\
  & = \dot{R}^{1\rightarrow 2}_{ik} \hat{e}^1_i \otimes \hat{e}^1_k + \mathbb{\Omega}^{1/0} \cdot  \mathbb{R}^{1 \rightarrow 2} - \mathbb{R}^{1 \rightarrow 2} \cdot \mathbb{\Omega}^{1/0} = \\
  & = \dfrac{{}^1 d}{dt} \mathbb{R}^{1 \rightarrow 2} + \mathbb{\Omega}^{1/0} \cdot  \mathbb{R}^{1 \rightarrow 2} - \mathbb{R}^{1 \rightarrow 2} \cdot \mathbb{\Omega}^{1/0} \ .
\end{aligned}$$

**todo** *Show details of the evaluation of the last term, exploiting index notation and properties permutation properties of indices of Ricci's symbols, related to properties of vector product.*

Using the latter relation, it's possible to prove the angular velocity of a composite rotation is the sum of the relatvie angularvelocities of the intermediate rotations.

$$\begin{aligned}
 \mathbb{\Omega}^{2/0}
 & = \dot{\mathbb{R}}^{0 \rightarrow 2} \cdot \mathbb{R}^{2 \rightarrow 0} = \\
 & = \frac{d}{dt} \left( \mathbb{R}^{1 \rightarrow 2} \cdot \mathbb{R}^{0 \rightarrow 1} \right) \cdot \mathbb{R}^{2 \rightarrow 0} = \\
 & = \left\{ \left[ \dfrac{{}^1 d}{dt} \mathbb{R}^{1 \rightarrow 2} + \mathbb{\Omega}^{1/0} \cdot  \mathbb{R}^{1 \rightarrow 2} - \mathbb{R}^{1 \rightarrow 2} \cdot \mathbb{\Omega}^{1/0} \right] \cdot \mathbb{R}^{0 \rightarrow 1} + \mathbb{R}^{1 \rightarrow 2} \cdot \dot{\mathbb{R}}^{0 \rightarrow 1}  \right\} \cdot \mathbb{R}^{1 \rightarrow 0} \cdot \mathbb{R}^{2 \rightarrow 1} = \\
 & =\left[ \dfrac{{}^1 d}{dt} \mathbb{R}^{1 \rightarrow 2} + \mathbb{\Omega}^{1/0} \cdot  \mathbb{R}^{1 \rightarrow 2} - \mathbb{R}^{1 \rightarrow 2} \cdot \mathbb{\Omega}^{1/0} \right] \cdot \mathbb{R}^{2 \rightarrow 1} + \mathbb{R}^{1 \rightarrow 2} \cdot \mathbb{\Omega}^{1 / 0} \cdot \mathbb{R}^{2 \rightarrow 1} = \\
 & =  \dfrac{{}^1 d}{dt} \mathbb{R}^{1 \rightarrow 2} \cdot \mathbb{R}^{2 \rightarrow 1} + \mathbb{\Omega}^{1/0} = \\
 & = \mathbb{\Omega}^{2/1} + \mathbb{\Omega}^{1/0} \ .
\end{aligned}$$

so that addition of relative angular velocity holds

$$\mathbb{\Omega}^{20} = \mathbb{\Omega}^{21} + \mathbb{\Omega}^{10} \qquad , \qquad \vec{\omega}_{2/0} = \vec{\omega}_{2/1} + \vec{\omega}_{1/0} \ .$$
```

```{prf:example} Explicit form of time derivative of rotation tensor

$$\begin{aligned}
 \dot{\mathbb{R}}^{1 \rightarrow 2} 
 & = \dfrac{{}^1 d}{dt} \mathbb{R}^{1 \rightarrow 2} + \mathbb{\Omega}^{1/0} \cdot  \mathbb{R}^{1 \rightarrow 2} - \mathbb{R}^{1 \rightarrow 2} \cdot \mathbb{\Omega}^{1/0} = & (1) \\
 & = \left[ \mathbb{\Omega}^{2/1} + \mathbb{\Omega}^{1/0} \right] \cdot  \mathbb{R}^{1 \rightarrow 2} - \mathbb{R}^{1 \rightarrow 2} \cdot \mathbb{\Omega}^{1/0} \ .
\end{aligned}$$

having used $(1)$ $\mathbb{\Omega}^{2/1} = \frac{{}^1 d}{dt} \mathbb{R}^{1 \rightarrow 2} \cdot \mathbb{R}^{2 \rightarrow 1}$

```

```{prf:example} Sequence of three rotations

**todo**

```


```{dropdown} Angular acceleration

Time derivative of angular velocity composition provides the addition of relative angular accelerations

$$\dfrac{{}^0 d}{dt} \vec{\omega}_{2/0} = \dfrac{{}^0 d}{dt} \vec{\omega}_{2/1} + \dfrac{{}^0 d}{dt} \vec{\omega}_{1/0} \ ,$$

or

$$\vec{\alpha}_{2/0} = \vec{\alpha}_{2/1} + \vec{\alpha}_{1/0} \ .$$
```


## Linearization of rotations

**todo** Take care of components. Here referred to $0$ reference frame
- explicitly write components in the original and rotated reference frame
- deal with intermediate rotations: does increment of $\mathbb{R}^{i \rightarrow j}$ have simple expression with "relative variation", keeping constant the vectors of the original basis $i$, something like ${}^i \delta \vec{\theta}_\times = {}^i \delta \mathbb{R} \cdot \mathbb{R}$ General expression?

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
