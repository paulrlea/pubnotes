---
dg-publish: true
---
HW Problem 3 Review
$$
I = \frac{2}{5}MR^{2} \cdot \mathbf{I}
$$
$$
=\frac{2}{5}MR^{2} \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0  \\
0 & 0 & 1
\end{bmatrix}
$$
$$
I_{ij}=J_{ij}-M(\delta_{ij}a^{2}-a_{i}a_{j})
$$
$$
I_{ij} = \int  \rho \left( \delta_{ij} \sum_{k} x^{2}_{\alpha k}-x_{\alpha i}x_{\alpha j} \right)\, dx  
$$
$$
T = \frac{1}{2 } \vec{\omega}\{\mathbf{I}\} \vec{\omega}
$$
$$
(\omega_{1}, \ \omega_{2}, \ \omega_{3}) \begin{pmatrix}
I_{11} & I_{12} & I_{13} \\
I_{21} & I_{22} & I_{23} \\
I_{31} & I_{32} & I_{33}
\end{pmatrix}\cdot \begin{pmatrix}
\omega_{1} \\
\omega_{2} \\
\omega_{3}
\end{pmatrix}
$$
This simplified is
$$
\frac{1}{2}[I_{11}\omega_{1}^{2}+I_{12}\omega_{1}\omega_{2}+I_{12}\omega_{1}\omega_{3}+I_{21}\omega_{2}\omega_{1}+I_{22}\omega_{2}^{2}+I_{23}\omega_{2}\omega_{3}+I_{31}\omega_{3}\omega_{1} +I_{32}\omega_{3}\omega_{2}+I_{33}\omega_{3}^{2}]
$$

NB: Need to memorize the parallel axis theorem, discrete and continuous inertia tensor thing. 

# E X A M topics

Homeworks 5-9: 
- HW 5: Lagrange Multiplier Method ***
- HW 6: Hamiltonian Mechanics
- HW 7: Central Force Problems
- ~~HW 8: Scattering &  Non-Inertial frames ~~(not on exam)
- HW 9: Inertia Tensors 

4 problems on exam
- One on Lagrange multipliers
- One on Hamiltonian
- One on Central forces 
- One on inertia tensor

 Hamiltonian Review: 
 $$
H=\sum\dot{q}_{j} \frac{ \partial L }{ \partial \dot{q}_{j} } -L
$$
Also might be 
$$
T+U 
$$
Central forces
Review centrifugal potential energy 
$$
U_{cf} = \frac{l^{2}}{2\mu r^{2}}
$$

Inertia Tensors 
Discrete, continuous, how to diagonal matrices using eigenvalues 

Dont memorize how to solve individual problems, review homework. 

Non-lambda method?

How to generate Hamiltonian 
Generalized Momentum 
Central Forces
Oscillating (Taylor series)

$$
\tilde{L}=L+\lambda f
$$

Review gravity and spring potentials

Force of constraint F is equal to "something"...
Central forces, know the oscillations, taylor series. 
Inertia tensors
should be about 8 equations 

The two topics that *will* be on the final exam are coupled oscillations and vibrations

# Coupled Oscillations

In general, this is a complex motion that can always be described using a system of normal coordinates (each oscillates with a single, well defined frequency)

**Normal Modes**- Making use of initial conditions, motion can be constrained so only 1 normal coordinate varies with time. 

For a system of "n" oscillators, there will be "n" normal modes, which may be degenerate. 

> figure 1 

$$
T = \frac{1}{2}m_{1} \dot{x}_{1}^{2} + \frac{1}{2}m_{2}\dot{x}_{2}^{2}
$$
$$
U=\frac{1}{2} \kappa x_{1}^{2} + \frac{1}{2}\kappa x_{2}^{2} + \frac{1}{2}\kappa_{12} (x_{1}-x_{2})^{2}
$$
$$
L=T-U
$$
$$
L = \frac{1}{2}m_{1} \dot{x}_{1}^{2} + \frac{1}{2}m_{2}\dot{x}_{2}^{2}-\frac{1}{2} \kappa x_{1}^{2} + \frac{1}{2}\kappa x_{2}^{2} + \frac{1}{2}\kappa_{12} (x_{1}-x_{2})^{2}
$$
First [[Euler-Lagrange Equation]]
$$
\frac{d}{dt} \frac{ \partial L }{ \partial \dot{x}_{1} } -\frac{ \partial L }{ \partial x_{1} }=0 
$$
$$
M\ddot{x}_{1} + \kappa x_{1}+\kappa_{12}(x_{1}-x_{2})=0
$$
$$
\frac{d}{dt}  \frac{ \partial L }{ \partial \dot{x}_{2} } -\frac{ \partial L }{ \partial x_{2 } }=0
$$
$$
M\ddot{x}_{1}+(\kappa+\kappa_{12})x_{1} - \kappa_{12}x_{2}=0
$$
$$
M\ddot{x}_{2} + (\kappa+\kappa_{12})x_{2}-\kappa_{12}x_{1}=0
$$
These are coupled equations 

Because we expect oscillatory behavior

Solutions should be of an oscillatory form...

$$
x_{1}(t)= B_{1}e^{i\omega t}
$$
$$
x_{2}(t)=B_{2}e^{i\omega t}
$$

Aside: 
$$
\ddot{x}=-\omega^{2}x
$$

$$
x=Ae^{i\omega t}
$$
$$
\dot{x}=i\omega Ae^{i\omega t}
$$
$$
\ddot{x} =-A\omega^{2}e^{i\omega t}
$$
$$
=\omega^{2}x
$$
Plugging this back into coupled equation to cancel $e^{i\omega t}$

$$
-MB_{1}\omega^{2}+(\kappa+\kappa_{12})B_{1}-\kappa_{12}B_{2}=0
$$
$$
-MB_{2}\omega^{2}+(\kappa+\kappa_{12})B_{2}-\kappa_{12}B_{1}=0
$$
Reorganize
$$
(\kappa + \kappa_{12}-M\omega^{2})B_{1}-\kappa_{12}B_{2}=0
$$
$$
-\kappa_{12} B_{1}+(\kappa+\kappa_{12}-M\omega^{2})B_{2}=0
$$
Finding solutions:
Trivial solution $B_{1}$ and $B_{2}$ are zero. No movement.

For a nontrivial solution determinant of $B_{1}$ and $B_{2}$ coefficient matrix must be 0 
$$
\det \begin{bmatrix}
\kappa + \kappa_{12}- M\omega^{2} & -\kappa_{12} \\
-\kappa_{12}  & \kappa+\kappa_{12}-M\omega^{2} 
\end{bmatrix}
$$
$$
(\kappa+\kappa_{12}-M\omega^{2})^{2}-\kappa_{12}^{2}=0
$$
$$
\kappa+\kappa_{12}-M\omega^{2} = \pm\kappa_{12}
$$
$$
\omega = \pm \sqrt{ \frac{\kappa+\kappa_{12} \pm \kappa_{12}}{M}}
$$
$$
\omega_{1} = \pm \sqrt{ \frac{\kappa+2\kappa_{12}}{M} }
$$
$$
\omega_{2}= \pm \sqrt{ \frac{\kappa}{M} }
$$
General Solutions
$$
x_{1}(t) = B_{1}^{+}e^{i\omega_{1}t}+B_{1}^{-}e^{-i\omega t}+B_{2}^{+}e^{i\omega_{2}t}+B_{2}^{-}e^{-i\omega_{2}t}
$$
$$
x_{2}(t) = -B_{1}^{+}e^{i\omega_{1}t}-B_{1}^{-}e^{-i\omega t}+B_{2}^{+}e^{i\omega_{2}t}+B_{2}^{-}e^{-i\omega_{2}t}
$$
define coordinates 
$$
\eta_{1} = x_{1}-x_{2}
$$
$$
\eta_{2} = x_{1}+x_{2}
$$
$$
x_{1} = \frac{1}{2}(\eta_{2}+\eta_{1})
$$
$$
x_{2}=\frac{1}{2}(\eta_{2}-\eta_{1})
$$
Our EL equations
$$
M(\ddot{\eta}_{2}+\ddot{\eta}_{1})+(\kappa+\kappa_{12})(\eta_{2}+\eta_{1}) - \kappa_{12}(\eta_{2}-\eta_{1})=0
$$
$$
M(\ddot{\eta}_{2}-\ddot{\eta}_{1})+(\kappa+\kappa_{12})(\eta_{2}-\eta_{1}) - \kappa_{12}(\eta_{2}+\eta_{1})=0
$$
Rewrite
$$
M(\ddot{\eta}_{2}+\ddot{\eta}_{1})+(\kappa+2\kappa_{12})\eta_{1}+\kappa \eta_{2}=0
$$
$$
M(\ddot{\eta}_{2}-\ddot{\eta}_{1})-(\kappa+2\kappa_{12})\eta_{1}+\kappa \eta_{2}=0
$$
Add/subtract equations 

Subtract: 
$$
M \ddot{\eta}_{1} + (\kappa +2\kappa_{12})\eta_{1}=0
$$
Add: 
$$
M \ddot{\eta}_{2} + 2\kappa \eta_{1}=0
$$


