(classical-mechanics:lagrange:ii-type)=
# Lagrange Equations of the Second Kind

Here, the equivalence of analytical mechanics and Newton mechanics is stressed, by means of the derivation of the principle of analytical mechanics starting from the equations of motions derived in Newtonian mechanics, relying on the conservation of mass and the three principles of Newton mechanics. The process is shown in the following sections for [point systems](classical-mechanics:lagrange:point), [systems of points](classical-mechanics:lagrange:points), [extended rigid bodies](classical-mechanics:lagrange:rigid) and follows these steps:
- **strong form of equations.** Starting point is the dynamical equations of Newton mechanics, here also referred as the strong form of equations
- **weak form of equations.** Strong form are recast in weak form, also referred as **D'Alembert approach** or **virtual work formulation**, multiplying strong form of equations for arbitrary test functions
- **Lagrange equations.** A proper choice of test functions as a function of generalized coordinates, and some manipulation, leads to Lagrange equations. While the choice of test functions depends on the nature of the system, their expression always reads

   $$\dfrac{d}{dt}\left( \frac{\partial \mathscr{L}}{\partial \dot{q}^k} \right) - \frac{\partial \mathscr{L}}{\partial q^k} = Q_{q^k} \ ,$$ (eq:lagrange-eq)

   being $q^k(t)$ the generalized coordinates, $\mathscr{L}\left(\dot{q}^k(t), q?k(t), t \right) = K\left(\dot{q}^k(t), q^k(t), t\right) + U(q^k(t), t)$ the Lagrangian function of the system, defined as the sum of the kinetic energy $K$ and the potential function $U = - V$, being $V$ the potential energy - s.t. the conservative vector field reads $\vec{F} = - \nabla V$, and $Q_q$ the generalized force.

- Lagrange equations can be interpreted as a result of a stationary principle of a functional, $S$, defined **action functional**, as it can be shown with the tools of [calculus of variations](https://basics2022.github.io/bbooks-math-miscellanea/ch/calculus-variations/intro.html).

     - **If $Q_{q^{k}} = 0$**, multiplying by $w^k(t)$, integrating over time from $t_0$, $t_1$, and assuming that $w(t_0) = w(t_1) = 0$,

       $$\begin{aligned}
         0 & = \int_{t_0}^{t_1} w^k (t) \left[ \dfrac{d}{dt}\left( \frac{\partial \mathscr{L}}{\partial \dot{q}^k} \right) - \frac{\partial \mathscr{L}}{\partial q} \right] \, dt = \\
           & = w^k(t) \left.\left( \frac{\partial \mathscr{L}}{\partial \dot{q}^k} \right)\right|_{t_0}^{t_1} - \int_{t_0}^{t_1} \left[ \dot{w}^k(t) \, \frac{\partial \mathscr{L}}{\partial \dot{q}^k} + w^k(t) \, \frac{\partial \mathscr{L}}{\partial q^k} \right] \, dt \ . \\
     \end{aligned}$$

       If $w^k(t)$ is equal to zero for $t$ equal to $t_0$ and $t_1$, first term vanishes

       $$\begin{aligned}
           0 & = - \int_{t_0}^{t_1} \left[ \dot{w}^k(t) \, \frac{\partial \mathscr{L}}{\partial \dot{q}^k} + w^k(t) \, \frac{\partial \mathscr{L}}{\partial q^k} \right] \, dt \\
           & = - \frac{1}{\varepsilon} \int_{t_0}^{t_1} \varepsilon \left[ \dot{w}^k(t) \, \frac{\partial \mathscr{L}}{\partial \dot{q}^k}\left(\dot{q}^l(t), q^l(t), t \right) + w^k(t) \, \frac{\partial \mathscr{L}}{\partial q^k}\left(\dot{q}^l(t), q^l(t), t \right) \right] \, dt = \\
           & = - \lim_{\varepsilon \rightarrow 0} \left\{ \frac{1}{\varepsilon} \int_{t_0}^{t_1} \varepsilon \left[ \dot{w}^k(t) \, \frac{\partial \mathscr{L}}{\partial \dot{q}^k}\left(\dot{q}^l(t), q^l(t), t \right) + w^k(t) \, \frac{\partial \mathscr{L}}{\partial q^k}\left(\dot{q}^l(t), q^l(t), t \right) \right] \, dt \right\}= \\
           & = - \lim_{\varepsilon \rightarrow 0} \left\{ \frac{1}{\varepsilon} \int_{t_0}^{t_1} \left[ \mathscr{L}\left(\dot{q}^l(t)+\varepsilon \dot{w}^l(t), q^l(t) + \varepsilon w^l(t), t \right) - \mathscr{L}\left(\dot{q}^l(t), q^l(t), t \right) \right] \, dt + o(\varepsilon) \right\}= \\
           & = - \delta \int_{t_0}^{t_1} \mathscr{L}(\dot{q}^l(t), q^l(t), t) \, dt =: - \delta S[q^k(t)] \ ,
       \end{aligned}$$
    
       i.e. Lagrange equations are equivalent to the stationary condition of the action functional
    
       $$S[q^k(t)]:= \int_{t_0}^{t_1} \mathscr{L}\left(\dot{q}^l(t), q^l(t), t\right) \, dt \ .$$

    - **If $Q_k \ne 0$**, the variational principle becomes

         $$\begin{aligned}
           0 & = \int_{t_0}^{t_1} w^k (t) \left[ \dfrac{d}{dt}\left( \frac{\partial \mathscr{L}}{\partial \dot{q}^k} \right) - \frac{\partial \mathscr{L}}{\partial q^k} - Q_k \right] \, dt = \\
             & = w^k(t) \left.\left( \frac{\partial \mathscr{L}}{\partial \dot{q}^k} \right)\right|_{t_0}^{t_1} - \int_{t_0}^{t_1} \left[ \dot{w}^k(t) \, \frac{\partial \mathscr{L}}{\partial \dot{q}^k} + w^k(t) \, \frac{\partial \mathscr{L}}{\partial q^k} \right] \, dt 
             + \int_{t_0}^{t_1} w^k(t) Q_k \, dt \ . \\
             & = \dots \\
             & = - \delta \int_{t_0}^{t_1} \mathscr{L}\left(\dot{q}^l(t), q^l(t), t\right) \, dt + \int_{t_0}^{t_1} \delta q^k(t) Q_k \, dt \ ,
       \end{aligned}$$

       having written the arbitrary test function as $w^k(t) =: \delta q^k(t)$ to keep in mind that they're used as variations of functions $q^k(t)$.

       The second contribution is usually defined **virtual work** of generalized forces $Q_k$ - that is equal to the virtual work of actions not included in the potential $U\left(q^k(t),t\right)$. For the very nature of variation, it can be thought as the *infinitesimal work done by forces for small displacements compatible with constraints, keeping time constant*.
  

