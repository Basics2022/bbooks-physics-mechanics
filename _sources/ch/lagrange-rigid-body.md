(classical-mechanics:lagrange:rigid)=
# Rigid Body

**Newton dynamical equations - strong form.** Dynamical equations governing the motion of a rigid body, referred to its center of mass $G$ read

$$\begin{cases}
  \dot{\vec{Q}} = \vec{R}^{e} \\
  \dot{\vec{\Gamma}}_G = \vec{M}^e_G \ ,
\end{cases}$$

with momentum $\vec{Q} = m \vec{v}_G$ and angular momentum $\vec{\Gamma}_G = \mathbb{I}_G \cdot \vec{\omega}$.

**Weak form.** Weak form of dynamical equations is derived with scalar multiplication of the strong form by an arbitrary test functions $\vec{w}_t$, $\vec{w}_r$

$$\vec{0} = \vec{w}_t \cdot \left( m \dot{\vec{v}} - \vec{R}^e\right) + \vec{w}_r \cdot ( \dot{\vec{\Gamma}}_G - \vec{M}^e_G ) \qquad \forall \vec{w}$$ (eq:lagrange:rigid:weak)

**Lagrange equations.**
