# 23.1 Determine the most probable r in the ground state H-atom.
Probability density and unknown R, solve for R
Take the derivative, set to 0
$$
P(r)=r^{2}\left[ 2\left( \frac{1}{a_{0}} \right)^{3/2}e^{-r/a_{0}} \right] \left[ 2\left( \frac{1}{a_{0}} \right)^{3/2}e^{-r/a_{0}} \right]
$$
$$
\frac{d}{dr}P(r)=\dfrac{8r\mathrm{e}^{-\frac{2r}{a_0}}}{a_0^3}-\dfrac{8r^2\mathrm{e}^{-\frac{2r}{a_0}}}{a_0^4}
$$
with zeros at $r=0, a_{0}$. Therefore the most probable R is $a_{0}$

# 23.2 What is the expectation value < r > for the ground state of H-atom?
$$
R_{1,0} (r) = 2( \frac{1}{a_{0}})^{3/2}e^{-r/a_{0}}
$$
$$
<r> \ = 4\left( \frac{1}{a_{0}} \right)^{2} \int r^{3}e^{(-2/a_{0})r} \ \, dr  =\left[ -\frac{a_{0}}{2}r^{3} e^{-2r/a_{0}} +\frac{3a_{0}}{2}e^{-2r/a_{0}} \left( -\frac{a_{0}r^{2}}{2} - \frac{a_{0}^{2}r}{2}-\frac{a_{0}^{3}}{4} \right)\right]^{\infty}_{0}
$$
$$
4\left( \frac{1}{a_{0}} \right)^{3}\left[ \frac{3a_{0}^{4}}{8} \right]
$$
$$
\frac{3}{2}a_{0}
$$
# 23.3  At t=0 a hydrogen atom is in a mixed state given 
$$
\Psi(r,\theta,\phi,t=0) = \frac{1}{\sqrt{ 2 }}\Psi_{1,0,0} + \frac{1}{\sqrt{ 2 }}\Psi_{(2,1,1)}
$$
(a) Determine the wave function at t later. 
$$
\Psi(r,\theta,\phi,t) = \frac{1}{\sqrt{ 2 }}\Psi_{1,0,0}e^{-iE_{n}t/\hbar} + \frac{1}{\sqrt{ 2 }}\Psi_{(2,1,1)}e^{-iE_{n}t/\hbar}
$$
(b) Determine expectation value of energy < 𝐸 >.
$$
	<E> = \int ( \frac{1}{\sqrt{ 2 }}\Psi_{1,0,0}e^{-iE_{n}t/\hbar} + \frac{1}{\sqrt{ 2 }}\Psi_{(2,1,1)}e^{-iE_{n}t/\hbar}) \hat{H} ( \frac{1}{\sqrt{ 2 }}\Psi_{1,0,0}e^{-iE_{n}t/\hbar} + \frac{1}{\sqrt{ 2 }}\Psi_{(2,1,1)}e^{-iE_{n}t/\hbar})
$$
$$
\frac{E_{1}+E_{2}}{2}
$$
# 23.4 At t=0 a hydrogen atom is in a mixed state given: 
$$
\Psi(r,\theta,\phi,t) = \frac{1}{\sqrt{ 2 }}\Psi_{1,0,0}e^{-iE_{n}t/\hbar} + \frac{1}{\sqrt{ 2 }}\Psi_{(2,1,1)}e^{-iE_{n}t/\hbar}
$$
$$
L^{2}=L_{x}^{2} + L_{y}^{2} + L_{z}^{2} \ , \ L_{z} = xP_{y} -yP_{x}
$$
$$
\Psi(r,\theta,\varphi,t) = \frac{1}{\sqrt{ 2 }} e^{-iE_{1}t/\hbar} \psi_{(1,0,0)} + \frac{1}{\sqrt{ 2 }}e^{-iE_{1}t/\hbar} \psi_{(2,1,1)}
$$
$$
< L ^{2}>  \ = \frac{1}{2} \cdot 0\hbar^{2} + \frac{1}{2}(2\hbar^{2})=\hbar^{2}
$$
$$
< L _{z}> = \frac{1}{2}(0\hbar) + \frac{1}{2}(\hbar ) = \frac{\hbar}{2}
$$


 