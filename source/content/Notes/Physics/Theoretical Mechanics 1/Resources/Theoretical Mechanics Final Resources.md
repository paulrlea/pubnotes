---
dg-publish: true
---
> "Once more unto the breach"

# Topics
The two topics that *will* be on the final exam are coupled oscillations and vibrations. It may or may not include any other topics. 
- See section below on Final Exam Information 

[[2024-03-26 Oscillations]]

[[2024-03-29 Coupled Oscillations]]

[[2024-04-05 General Coupled Oscillations]]

# Equations
## General Mathematical Relations
1. Taylor Series 
$$
(x + h) = (x) + '(x)h + ''(x) \frac{h^{2}}{2!} + \dots
$$
2. Small Angle Approximation 
$$
\tan\theta \approx\sin\theta \approx \theta
$$
$$
 \cos\theta \approx 1 
$$
3. Harmonic Oscillator diffeq
$$
\ddot{ \theta} = -\omega^{2}\theta
$$
## From exam 1 topics: 
Equations: 
1. . Kinetic energy formulas
$$
T_\text{rolling}=\frac{1}{2} I \omega^{2}
$$
$$
T_\text{linear}=\frac{1}{2}mv^{2}
$$
2. Potential Energy formulas
$$
U_\text{ gravity} = mgh \text{  (depends on coordinate system)}
$$
$$
U_\text{spring}= \frac{1}{2}k\Delta x^{2} \text{  (hookian spring)}
$$
3. Lagrangian
$$
L=T-U
$$
4. Euler-Lagrange Equation 
$$
\frac{d}{dt} \frac{ \partial L }{ \partial \dot{q}_{i} } -\frac{ \partial L }{ \partial q_{i} }=0
$$
## Exam 2 Equations on final 
 1. Modified Lagrangian (optional, can use substitution)
$$
\tilde{L}  =L - \lambda f
$$
$$
f = \text{ force }
$$

2. Centrifugal Potential

$$
U_{cf} = \frac{l}{2\mu r^{2}}
$$
4. Effective Potential
$$
U_{eff} = U + U_{cf}
$$
5. Continuous Inertia Tensor 
$$
	I_{ij} = \int _{v} p(\vec{r}) \left( \delta_{ij}\sum_{k} x_{ k}^{2}-x_{ i} x_{ j} \right) \, dV
$$
7. Eigenvalue and Eigenvector Relation
$$
(\mathbf{A}-\lambda \mathbf{I})\cdot \mathbf{\vec{v}}=0
$$
and
$$
\det(\mathbf{A}-\lambda \mathbf{I})=0
$$

## Final-Exclusive Topics (Study these)
1. $A_{jk}$ Matrices
2. Continuous systems 





# Final Exam information
6 problems 
- Non-Relativistic Newtonian Mechanics Problem 1
	- $F=MA$
	- Free body diagrams 
	- Generating newtons second law
	- Rearrange and solve integrals 
	- Position and velocity as function of time
	- Drag forces?
- Central Force Problem Problem 2 
	- Starting with from Lagrangian 
		- See homework 7 problem 3
	- Coordinate transformation to uncouple differential equations
	- Reduced mass equation !!
- Lagrangian w/ constraints Problem 3
	- Not going to be forced to do Lagrange multiplier. Can if you want.
- Moment of inertia problem Problem 4
	- Continuous distribution 
$$
I_{ij} = \int \rho \left( \delta_{ij} \sum_{k} x^{2}_{\alpha k} -x_{\alpha i}x_{\alpha j } \right) \, dV
$$
	- In Cartesian coordinates
- Coupled Oscillations Problem 5
	- Finding $A_{jk}$ matrices
	- Find determinants to find $\omega$
	- Hw 10
- Continuous Systems: Waves Problem 6
	- Hw 11
	- Plucked and struck strings
	- Maybe its a struck, plucked string
	- Lots of integrals

No Relativity, No Hamiltonian, No Non-inertial reference frame, No scattering


# Final Equations list to review
Lagrangian and Euler-Lagrange Equation
$$
L = T-U
$$
$$
\frac{d}{dt} \frac{ \partial L }{ \partial \dot{q}_{i} } - \frac{ \partial L }{ \partial q_{i} } =0 
$$
Reduced Mass Equation 
$$
\frac{m_{1}m_{2}}{m_{1}+m_{2}} = \mu 
$$
Centrifugal Potential
$$
U_{cf} = \frac{l}{2\mu r^{2}}
$$
Effective Potential 
$$
U_{eff} = U + U_{cf}
$$
Continuous Distribution Inertia Tensor 
$$
I_{ij} = \int \rho \left( \delta_{ij} \sum_{k} x^{2}_{\alpha k} -x_{\alpha i}x_{\alpha j } \right) \, dV
$$
$A_{jk}$ matrices 
$$
A_{jk} = \frac{ \partial^{2} u }{ \partial q_{j}\partial q_{k} } 
$$
Eigenfrequency and Eigenvector relations
$$
\det[\bar{A}-\omega^{2}\bar{m}] = 0
$$
$$
[\bar{A}-\omega^{2}\bar{m}] \cdot \vec{v} = 0
$$
$\mu_{r}$ formula
$$
\mu_{r}  = \frac{2}{L}\int\limits_{0}^{L} q(x,0) \sin\left( \frac{r\pi x}{L} \right) \, dx 
$$
$\nu_{r}$ formula
$$
\nu_{r} = -\frac{2}{\omega_{r}L} \int\limits_{0}^{L} \dot{q}(x,0)\sin\left( \frac{r\pi x}{L} \right) \, dx 
$$
position of strings formula 
$$
q(x,t) = \sum_{r=1}^{\infty}  \sin\left( \frac{r\pi x}{L} \right) (\mu_{r} \cos(\omega_{r}t)-\nu_{r}\sin(\omega_{r}t))
$$



