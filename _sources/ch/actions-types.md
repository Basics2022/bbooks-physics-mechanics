(physics-hs:mechanics:actions:def)=
# Force, Moment of a Force, Distributed Actions

## Concentrated Force

A (concentrated) force is a vector quantity with physical dimensions,

$$[\text{force}] = \frac{\text{[mass]}\text{[length]}}{\text{[time]}^2}$$

which can be measured using a dynamometer, and whose effect can alter the equilibrium or motion conditions of a physical system.

In addition to the typical information of a vector quantity - magnitude, direction, and sense - contained in the force vector $\vec{F}$, it is often necessary to know the **point of application** or the line of application of the force.

## Moment of a Concentrated Force
The moment of a force $\vec{F}$ applied at point $P$, or with a line of application passing through $P$, relative to point $H$ is defined as the vector product,

$$\vec{M}_H = (P - H) \times \vec{F}$$

## System of Forces, Resultant of Actions, and Equivalent Loads
Given a system of $N$ forces $\left\{ \vec{F}_n \right\}_{n=1:N}$, applied at points $P_n$, we define:
- **resultant** of the system of forces: the sum of the forces,

  $$\vec{R} = \sum_{n=1}^{N} \vec{F}_n \ ,$$

- resultant of the moments with respect to a point $H$: the sum of the moments

  $$\vec{M}_H = \sum_{n=1}^{N} (P_n - H) \times \vec{F}_n \ ,$$

- an **equivalent load**: a system of forces that has the same resultant of forces and moments; for a system of forces, an equivalent load can be defined as a single force, the resultant of the forces $\vec{R}$ applied at point $Q$ derived from the equivalence of moments

  $$\begin{aligned}
    \vec{R} & = \sum_{n=1}^{N} \vec{F}_n \\
    (Q - H) \times \vec{R} & = \sum_{n=1}^{N} (P_n - H) \times \vec{F}_n \\
  \end{aligned}$$

## Couple of Forces
A couple of forces is an equivalent load to two forces of equal magnitude and opposite sense, $\vec{F}_2 = - \vec{F}_1$, applied at two points $P_1$, $P_2$ not aligned along the line of application of the forces to have non-zero effects.

**todo** *image*

The resultant of the forces is zero,

$$\vec{R} = \vec{F}_1 + \vec{F}_2 = \vec{F}_1 - \vec{F}_1 = \vec{0} \ ,$$

while the resultant of the moments does not depend on the moment pole,

$$\begin{aligned}
  \vec{M}_H & = (P_1 - H) \times \vec{F}_1 + (P_2 - H) \times \vec{F}_2 = \\
  & = (P_1 - H) \times \vec{F}_1 - (P_2 - H) \times \vec{F}_1 = \\
  & = (P_1 - P_2) \times \vec{F}_1 =: \vec{C} \ .
\end{aligned}$$

## Force Fields
**todo**

## Distributed Actions
**todo**

