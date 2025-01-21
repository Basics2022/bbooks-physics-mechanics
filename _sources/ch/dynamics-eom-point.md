(classical-mechanics:dynamics:eom:point)=
# Equations of motion of a point mass

**Dynamic quantities.**

$$\begin{aligned}
  \vec{Q}_P & := m_P \vec{v}_P \\
  \vec{L}_{P,H} & := (\vec{r}_P - \vec{r}_H) \times \vec{Q} = m_P (\vec{r}_P - \vec{r}_H) \times \vec{v}_P \\
  K & := \frac{1}{2} m_P \vec{v}_P \cdot \vec{v}_P = \frac{1}{2} m_P |\vec{v}_P|^2
\end{aligned}$$

**Momentum balance equation.** The balance equation of momentum of a point $P$ with mass $m$, $\vec{Q}_P = m \vec{v}_P$ readily follows the second principle of dynamics,

$$\dot{\vec{Q}}_P = \vec{R}^e_P$$

**Angular momentum balance equation.** Time derivative of the angular momentum is evaluated with the rule of derivative of product,

$$\begin{aligned}
\dot{\vec{L}}_{P,H} & = \dfrac{d}{dt} \left[ m_P (\vec{r}_P - \vec{r}_H) \times \vec{v}_P \right] = \\
& = m \left[ ( \dot{\vec{r}}_P - \dot{\vec{r}}_H ) \times \vec{v}_P + m_P (\vec{r}_P - \vec{r}_H) \times \dot{\vec{v}}_P \right] = \\
& = - m_P \dot{\vec{r}}_H \times \vec{v}_P + m_P (\vec{r}_P - \vec{r}_H) \times \dot{\vec{v}}_P = \\
& = - \dot{\vec{r}}_H \times \vec{Q} + \vec{M}_H^{ext} \ .
\end{aligned}$$

**Kinetic energy blanace equation.**

$$\begin{aligned}
\dot{K}_{P} & = \dfrac{d}{dt} \left( \frac{1}{2} m_P \vec{v}_P \cdot \vec{v}_P \right) = \\
            & = m_P \dot{\vec{v}}_P \cdot \vec{v}_P = \\
            & = \vec{R}^e \cdot \vec{v}_P = P^e = P^{tot} \\
\end{aligned}$$

being the power of external actions $P^e$ equal to the total power acting on the system, assuming there is no internal action in the point system, or at least they have zero net power.


