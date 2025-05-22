(classical-mechanics:kinematics:rotations)=
# Rotations

A rotation is a transformation preserving length, angles and orientation of space[^reflection].

[^reflection]: A reflection is a transformation preserving length and angles but reversing orientation of space. A reflection can be represented by a unitary tensor $\mathbb{R}$, with determinant $|\mathbb{R}| = -1$.

A rotation in 3-dimensional spaces can be represented by a **rotation tensor**, $\mathbb{R}$. A rotation tensor has some mathematical properties: it's a **unitary tensor**, $\mathbb{R}^T \cdot \mathbb{R} = \mathbb{R} \cdot \mathbb{R}^T = \mathbb{I}$, and unit determinant, $|\mathbb{R}| = 1$.
From these properties, it immediately follows the definition of **angular velocity**, and angular acceleration. A rotation can be represented as **compositions of successive rotations**, $\mathbb{R}^{0\rightarrow 2} = \mathbb{R}^{1\rightarrow 2} \cdot \mathbb{R}^{0\rightarrow 1}$, while summation of relative angular velocity (and acceleration) of successive rotations holds, $\vec{\omega}^{0 \rightarrow 2} = \vec{\omega}^{1 \rightarrow 2} + \vec{\omega}^{0 \rightarrow 1}$. For small rotations, **linearization** provides a small-amplitude approximation: in the linearization limit, composition of rotations reduces to summation, while incremental rotation in a small time interval reduces to the definition of angular velocity.

This section of kinematic deals with rotations in details, first in absolute tensor notation, and then introducing parametrizations to describe rotations like axis and angle $(\hat{n}, \theta)$, Euler's angles $(\phi, \theta, \psi)$ for successive simple rotations, and unitary quaternions $q = q_0 + \vec{q}$, with $1 = q_0^2 + |\vec{q}|^2$.

[**Tensors**](classical-mechanics:kinematics:rotations:tensor).

[**Parametrizations: axis and angle**](classical-mechanics:kinematics:rotations:axis-angle).

[**Parametrizations: Euler's equations**](classical-mechanics:kinematics:rotations:euler).

[**Parametrizations: quaternions**](classical-mechanics:kinematics:rotations:quaternions).

