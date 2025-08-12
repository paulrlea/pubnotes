Problems 6.2, 6.5, 6.6, 6.7, 6.11, 6.17

## 6.2 
$$
-\frac{\hbar^{2}}{2m}\left( \frac{d^{2}}{dx^{2}} + \frac{d^{2}}{dy^{2}} +\frac{d^{2}}{dz^{2}} \right)\psi(x,y,z) + \frac{1}{2}m\omega^{2}(x^{2}+y^{2}+z^{2}) = E\psi(x,y,z)
$$
assuming [[eigenfunctions]] $\psi_{n}(x)$ with **one-dimensional** energy eigenvalues $E_{n} = (n +\frac{1}{2})\hbar \omega$
First excited state is given by $E_{1} = (\frac{3}{2})\hbar \omega$.
The Hamiltonian is given by: 
$$
H=\frac{\hat{p}^{2}}{2m} + \frac{1}{2}m\omega^{2}(x^{2}+y^{2}+z^{2})
$$
Expanding this, we get: 
$$
H = \frac{\hat{p}^{2}}{2m} + \frac{1}{2}m\omega^{2}x^{2} + \frac{1}{2}m\omega^{2}y^{2} + \frac{1}{2}m\omega^{2}z^{2}
$$
Separating the [[Momentum Operator]] into its 1-D components, we get: 
$$
H = \frac{\hat{p_{x}}^{2}}{2m}+ \frac{1}{2}m\omega^{2}x^{2}+\frac{\hat{p_{y}}^{2}}{2m} + \frac{1}{2}m\omega^{2}y^{2}+\frac{\hat{p_{z}}^{2}}{2m} + \frac{1}{2}m\omega^{2}z^{2}
$$
And if we take 
$$
H_{n} = \frac{\hat{p}_{n}^{2}}{2m} + \frac{1}{2}m\omega^{2}n^{2} 
$$
for any variable $n$, then we can rewrite the [[Hamiltonian]] as the following: 
$$
H = H_{x} + H_{y}+ H_{z}
$$
which means that the energy level is the sum of 
$$
(n_{x} + n_{y} + n_{z})
$$
Plugging in the energy level into the energy equation we get: 
$$
E_{n} = (n_{x}+\frac{1}{2})\hbar \omega_{x} + (n_{y}+\frac{1}{2})\hbar \omega_{y} + (n_{z}+\frac{1}{2})\hbar \omega_{z}
$$
$$
	E_{n}= \left( n_{x} +n_{y}+n_{z} + \frac{3}{2} \right)\hbar \omega 
$$
Looking at this function, there is a 6-fold [[degeneracy]], because for x,y and z, one could be 2 and the rest 0, or there could be two 1's and one zero. That's 2 possibilities per coordinate, and there's three coordinates yielding a 6-fold [[degeneracy]].

## 6.5 
Prove that the operator $L_{zop} = \frac{\hbar}{i} \frac{d}{d\phi}$ is a [[Hermitian Operators]]. Wave function must be single valued. 

To determine if an operator is Hermitian, we have to see if $L_{zop}^{\dagger} = L_{zop}$
Functionally, this means proving that
$$
\int ^{\infty}_{-\infty} \varphi^*(L\Psi)\, d\phi = \int ^{\infty}_{-\infty} (L\varphi)^{*} \Psi \, d\phi
$$
$$
\int ^{\infty}_{-\infty} \varphi^*\left( \frac{\hbar}{i} \frac{d}{d \phi}\Psi \right)\, d\phi = \int ^{\infty}_{-\infty} (\frac{\hbar}{i} \frac{d}{d \phi}\varphi)^{*} \Psi \, d\phi
$$
$$
\int ^{\infty}_{-\infty} \varphi^* \frac{\hbar}{i} \frac{d}{d \phi}\Psi \, d\phi = -\int^{\infty}_{-\infty} \left( \frac{d\phi}{dx} \right)^{*} \psi\, d\phi +\frac{\hbar}{i} \phi^{*}\psi |^{\infty}_{-\infty} = \int ^{\infty}_{-\infty} (\frac{\hbar}{i} \frac{d}{d \phi}\varphi)^{*} \Psi \, d\phi
$$
Therefore, $L_{zop}$ is Hermitian. 
## 6.6 
Suppose that 
$$
\Psi(\phi) = \sqrt{ \frac{1}{3\pi} } +  \sqrt{\frac{1}{6\pi}} e^{i\phi}
$$
Show that $\Psi(x)$ is properly normalized. What are possible results of a measurement of $L_{z}$ for a particle with wave function $\Psi(\phi)$, and what are the probabilities of these results. 
$$
\int ^{2\pi}_{0} \Psi(\phi)^{*}\Psi(\phi) \, d\phi = \int ^{2\pi}_{0} \left( \sqrt{ \frac{1}{3\pi} } +  \sqrt{\frac{1}{6\pi}} e^{-i\phi} \right)\left( \sqrt{ \frac{1}{3\pi} } +  \sqrt{\frac{1}{6\pi}} e^{i\phi} \right) \, d\phi= 
$$
$$
\int ^{2\pi}_{0} \frac{2\sqrt{2}\cos(\phi)}{6\pi} + \frac{3}{6\pi} \, d\phi = \int ^{2\pi}_{0} \frac{2\sqrt{2}}{6\pi}\cos(\phi) \ d\phi + \int ^{2\pi}_{0}\frac{3}{6\pi} \, d\phi 
$$
$$
\frac{\sqrt{2}}{3\pi}\int ^{2\pi}_{0} \cos(\phi) \ d\phi + \int ^{2\pi}_{0}\frac{1}{2\pi} \, d\phi = \frac{\sqrt{2}}{3\pi}[\sin \phi]|^{2\pi}_{0} + \left[ \frac{1}{2\pi} \phi \right]|^{2\pi}_{0}
$$
First term goes to 0, second term yields
$$
\frac{1}{2\pi} 2\pi - 0 = 1
$$
Therefore the wave-function is normalized. 

To find the possible measurement results of $L_{z}$, we can apply the operator to the wave function:
$$
L_{z} = \frac{\hbar}{i} \frac{d}{d\phi} (\sqrt{ \frac{1}{3\pi} } +  \sqrt{\frac{1}{6\pi}} e^{i\phi})
$$
$$
(\hbar \phi \sqrt{ \frac{1}{6\pi} }e^{i\phi}) =  \alpha (\Psi)
$$
There exists no constant $\alpha$ to make this happen, therefore the wave function is not an eigenfunction. This means it has to be a superposition of the normalized eigenfunctions of $L_{z}$. Looking at the form of the given wave function, we can determine that there are two possible states, either $m_{1} = 0$ or $1$, yielding two wave functions based on the normalized eigenfunction of the $L_{z}$ operator $\psi_{m}=\frac{1}{\sqrt{ 2\pi }}e^{im\phi}$
$$1
\psi_{1} = \sqrt{ \frac{1}{3} }e^{i\phi}
$$
and
$$
\psi_{0} = \sqrt{ \frac{2}{3} }
$$
Applying the rotational momentum operator to both of these wave functions yields our momentum eigenvalues:
$$
L_{z}(\psi_{1})=\alpha\psi_{1} \ \& \ L_{z}(\psi_{0}) = \alpha \psi_{0}
$$
Where $\alpha = \hbar,0$ respectively. These have respective probability amplitudes given by the square of their coefficients, $\frac{1}{3}$ and $\frac{2}{3}$ respectively. 


## 6.7 
Verify that $$Y_{2,2}(\theta,\phi)=\sqrt{ \frac{15}{32\pi}}\sin ^{2}\theta e^{2i\phi}$$ is an eigenfunction of $\mathbf{L}^{2}$ and $L_{z}$ with appropriate eigenvalues

The operator $L_{z}$ is given by the following: $$\frac{\hbar}{i} \frac{d}{d\phi}$$
Finding the eigenvalues: 
$$
L_{z}Y_{2,2} = \lambda  Y_{2,2}
$$
where eigenvalues are denoted by  $\lambda$  

$$
2\hbar  \sqrt{ \frac{15}{32\pi} }\sin ^{2}\theta e^{2i\phi} =\lambda\sqrt{ \frac{15}{32\pi}}\sin ^{2}\theta e^{2i\phi}
$$
Thus yielding a value of $2\hbar$ for the eigenvalue and proving that this function is an eigenfunction of $L_{z}$ 

Now for the $\mathbf{L}^{2}$ operator:
$$
\mathbf{L}^{2} = -\hbar^{2}\left[ \frac{1}{\sin \theta} \frac{d}{d\theta} \left( \sin \theta\frac{d}{d\theta} \right) +\frac{1}{\sin ^{2}\theta} \frac{d^{2}}{d\phi^{2}} \right]
$$
$$
\mathbf{L}^{2}Y_{2,2} = \lambda Y_{2,2}
$$
$$
\mathbf{L}^{2}\sqrt{ \frac{15}{32\pi}}\sin ^{2}\theta e^{2i\phi} = \lambda\sqrt{ \frac{15}{32\pi}}\sin ^{2}\theta e^{2i\phi}
$$
$$
-\hbar^{2}\left[ \frac{1}{\sin \theta} \frac{d}{d\theta}\left( \sin \theta   \frac{d\Theta}{d\theta} \right)- \frac{4}{\sin ^{2}\theta} \Theta \right] = \lambda \hbar^{2}\Theta
$$
Where 
$$
Y(\theta,\phi) = \Theta(\theta )e^{i m_{1}\phi} 
$$
and 
$$
\Theta(\theta) = \sqrt{\frac{15}{32\pi}}\sin ^{2}\theta
$$
$$
-\hbar\left[ \frac{1}{\sin \theta} \frac{d}{d\theta}\left( \sin \theta  \dfrac{\sqrt{15}\cos\left({\theta}\right)\sin\left({\theta}\right)}{2^\frac{3}{2}\sqrt{{\pi}}} \right)-\frac{4}{\sin ^{2}\theta} \sqrt{\frac{15}{32\pi}}\sin ^{2}\theta\right]
$$
$$
-\hbar\left[ \frac{1}{\sin \theta}-\dfrac{\sqrt{15}\sin\left({\theta}\right)\left(\sin^2\left({\theta}\right)-2\cos^2\left({\theta}\right)\right)}{2^\frac{3}{2}\sqrt{{\pi}}}-\frac{4}{\sin ^{2}\theta} \sqrt{\frac{15}{32\pi}}\sin ^{2}\theta\right]
$$
...
$$
2(2+1)\hbar^{2}\sqrt{ \frac{15}{32\pi}}\sin ^{2}\theta e^{2i\phi}
$$
For a spherical harmonic $Y_{l,m_{1}}$ we can assume it satisfies the following:  
$$
	\mathbf{L}^{2} Y_{l,m_{1}}(\theta,\phi) = l(l+1)\hbar^{2}Y_{l,m_{1}}(\theta,\phi)
$$
Therefore the eigenvalue is given by $6\hbar$ and it is an eigenfunction. 


## 6.11 
Normalized angular wave function for rigid rotator given by: 
$$
	\psi(\theta,\phi) = \sqrt{ \frac{3}{8\pi} } (-\sin \theta \cos \phi + i\cos\theta)
$$
Show that this wave function is an eigenfunction of: 
$$
L_{y} = \frac{\hbar}{i}\left( \cos \phi  \frac{d}{d\theta}-\cot \theta \sin \phi   \frac{d}{d\phi}\right)
$$
What is the eigenvalue?
$$
	\frac{d\psi}{d\theta} = \sqrt{ \frac{3}{8\pi} }(-\cos \theta \cos \phi-i\sin \theta)
$$
$$
\frac{d\psi}{d\phi}=\sqrt{ \frac{3}{8\pi} }(\sin \theta \sin \phi)
$$
$$
L_{yop} \psi = \frac{\hbar}{i}(\cos \phi)[\sqrt{ \frac{3}{8\pi} }(-\cos \theta \cos \phi-i\sin \theta)]-\cot \theta \sin \phi\sqrt{ \frac{3}{8\pi} }(\sin \theta \sin \phi)
$$
$$
\implies \sqrt{ \frac{3}{8\pi} } \frac{\hbar}{i}(-\cos \theta-i\sin \theta \cos \phi)
$$
$$
\implies \hbar \sqrt{ \frac{3}{8\pi} } (i\cos \theta-\sin \theta \cos \phi)
$$
$$
L_{yop} \psi = \hbar \sqrt{ \frac{3}{8\pi} }\psi
$$
$$
\therefore \lambda  = \hbar \sqrt{ \frac{3}{8\pi} }
$$
$\psi$ is an eigenfunction with eigenfunctions given by $\lambda$ above. 

## 6.17
The energy for a rigid rotator constrained in the x-y plane is given by 
$$
E = \frac{L^{2}_{z}}{2I}
$$
Where the moment of inertia is constant. 

a. What is the Hamiltonian? What are the allowed energies and normalized energy eigenfunctions? 

$$
\hat{H} = \frac{L_{z}^{2}}{2I} =\frac{-\hbar^{2}}{2I}\frac{d^{2}}{d^{2}\phi}
$$
$$
[\hat{H}, \hat{L}_{z}] = \frac{1}{2I}[L_{z}^{2},L_{z}]= \frac{1}{2I}0 = 0
$$
Therefore these two operators commute
$$
\hat{H}\psi = E\psi \implies \frac{d^{2}\psi}{d\phi^{2}} + \left( \frac{2IE}{t^{2}} \right)\psi = 0
$$
$$
\implies \psi(\phi) = Ae^{i\omega \phi}
$$
The allowed energies are given by:
$$
e^{i\omega_{2}\pi}= 1 \implies \omega=n \implies \omega^{2}=n^{2}
$$
$$
E_{n}=\frac{n^{2}\hbar^{2}}{2I}
$$
Normalized eigenfunctions are given by
$$
\psi_{n}(\phi)=\frac{1}{\sqrt{ 2\pi  }}e^{in\phi}
$$
b. What values of $L_{z}$ would be obtained if a measurement of $L_{z}$ were carried out on
$$
\psi(\phi)=\sqrt{ \frac{4}{3\pi} }\sin ^{2} \frac{\phi}{2}=\sqrt{ \frac{4}{3\pi} } \left(  \frac{1-\cos \phi}{2} \right) = \frac{1}{\sqrt{ 3\pi }}\left[ 1-\frac{1}{2}e^{i\phi}-\frac{1}{2}e^{-i\phi} \right]
$$
What are their probabilities?

| Lz | n=0 | n=1 | n=2 |
|----|-----|-----|-----|
| P  | 1/3 | 1/6 | 1/6 | 


c. Time evolution of $\psi$
$$
\psi(\phi,t)=\sqrt{ \frac{4}{3\pi} } \left(  \frac{1-\cos \phi}{2} \right)e^{-it/2I\hbar}
$$
d.
$$
P(n=1) = \frac{1}{2}
$$
e. 
$$
<E> \ =\  <H> \ = \int ^{2\pi}_{0}\psi^{*} \hat{H} \psi  \, d\phi = -\frac{1}{3\pi} \int ^{2\pi}_{0} (1-\cos \phi e^{it/2I\hbar}) \frac{\hbar^{2}}{2I} (1-\cos \phi e^{-it/2I\hbar})\, d\phi
$$
$$
=- \frac{\hbar^{2}}{6\pi I} (-\pi) = \frac{\hbar^{2}}{6I}
$$

$$
< E^{2} > \ = \ < H^{2} > = \left( \frac{\hbar}{2I} \right)^{2} \frac{1}{3\pi}\pi = \frac{4\hbar}{12I^{2}}
$$
$$
\Delta E \sqrt{ <E^{2}> - < E > ^{2} } = \frac{\hbar^{2}\sqrt{ 2 }}{6I}
$$



$$

$$















