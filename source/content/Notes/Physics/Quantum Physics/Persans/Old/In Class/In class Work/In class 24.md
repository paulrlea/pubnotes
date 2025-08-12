# 24.1
An electron with mass $m_{0}$ is confined in a spherical shell with radius R. Determine eigenvalues and eigenfunctions of system in a magnetic field $\mathbf{B} = B_{0}\mathbf{\hat{z}}$. Recall that Hamiltonian of system without external magnetic field is $\frac{L^{2}}{2m_{0}R^{2}}$

Write down [[Notes/Physics/Quantum Physics/Concepts/Time independent Schrodinger equation]]
write down potential component?
magnetic potential?
use Lz instead of big L
someone said the eigenfunctions and i missed it
eigenfunctions (wave functions) corresponding to eigenvalues (energy levels)


$$
R(r)_{n,l} = r^{l} F_{n} (r) e^{-\sqrt{ 2m_{0}E/\hbar^{2}}r}
$$
![[Pasted image 20231121141102.png]]
# 24.2
Electron with mass $m_{0}$ confined to move in a circle in the x-y plane with radius R. System is in magnetic field given by $\mathbf{B} = B_{0}\mathbf{\hat{z}}$. Ignore kinetic energy, only magnetic interaction energy.

At t=0, wave function has form $\psi(\phi)=A\cos \phi$

Determine what A is: 
$$
1=\int _{0} ^{2\pi} (A\cos \phi)^{2} \, d\phi 
$$
$$
\frac{1}{A^{2}} = \int ^{2\pi}_{0} \cos ^{2}\phi \, d\phi
$$
$$
\frac{1}{A^{2}} = \pi
$$
$$
A = \sqrt{ \frac{1}{\pi} }
$$
![[Pasted image 20231121141113.png]]
# 24.3
Electron with mass $m_{0}$ confined to move in x-y plane with radius r. System is placed in a magnetic field $\mathbf{B}=B_{0}\mathbf{\hat{z}}$. Consider only magnetic interaction energy. 

The wavefunction is given by 
$$
\Psi(\phi, t)= \frac{1}{\sqrt{ 2 }} [\varphi_{1}e^{-iE_{1}t/\hbar} + \varphi_{2}e^{iE_{2}t/\hbar}] 
$$
Where
$$
\varphi_{1}=\frac{1}{\sqrt{ 2\pi }}e^{i\phi} \ \ \& \ \ \varphi_{2}=\frac{1}{\sqrt{ 2\pi  }}e^{ -i\phi }
$$
a. Determine matrix of energy operator: 
b. Determine expectation of the energy 
![[Pasted image 20231121141159.png]]
![[Pasted image 20231121141206.png]]
# 24.4
Determine the energy spectrum of a H-atom placed in a magnetic field 
$$
B=B_{0}\mathbf{\hat{z}}
$$
Consider only $n=2, l=1$ state. 

$$
H=H_{0}-\frac{e}{2m_{0}}\mathbf{L}\cdot \mathbf{B} = H_{0} + \frac{e}{2m_{0}} B_{0}L_{z}
$$
$$
H_{0} = -\frac{\hbar^{2}}{2m_{0}}\nabla^{2} +V(r)
$$

![[Pasted image 20231121141213.png]]