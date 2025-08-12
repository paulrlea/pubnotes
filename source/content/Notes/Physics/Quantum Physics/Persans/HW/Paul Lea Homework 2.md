Problem 9
![[Pasted image 20240125170256.png]]
$$
-\frac{\hbar}{2m} \frac{\partial^{2}(A\cos(kx-\omega t))}{\partial x^{2}} = i\hbar \frac{\partial (A\cos(kx-\omega t))}{\partial t}
$$
$$
-\frac{\hbar}{2m} (-Ak^{2}\cos(kx-\omega t)) = i\hbar (A\omega\sin(kx-\omega t))
$$
$$
\frac{k^{2}\cos(kx-\omega t)}{2m} \neq i\omega \sin(kx-\omega t)
$$
Therefore this is not a solution to the [[Notes/Physics/Quantum Physics/Concepts/Schrodinger equation]] for a free particle
$$
-\frac{\hbar}{2m} \frac{\partial^{2}(A\sin(kx-\omega t))}{\partial x^{2}} = i\hbar \frac{\partial (A\sin(kx-\omega t))}{\partial t}
$$
$$
-\frac{\hbar}{2m} (-Ak^{2}\sin(kx-\omega t)) = i\hbar (-A\omega\cos(kx-\omega t))
$$
$$
\frac{k^{2}\sin(kx-\omega t)}{2m} \neq -i\omega \cos(kx-\omega t)
$$
Therefore this is not a solution to the [[Notes/Physics/Quantum Physics/Concepts/Schrodinger equation]] for a free particle

Problem 10
![[Pasted image 20240125170304.png]]

$$
-\frac{\hbar^{2}}{2m} \frac{ \partial (c_{1}\psi_{1}+c_{2}\psi_{2}) }{ \partial x } =i\hbar \frac{ \partial (c_{1}\psi_{1}+c_{2}\psi_{2}) }{ \partial t } 
$$
$$
-\frac{\hbar^{2}}{2m}\left( \frac{ \partial c_{1}\psi_{1} }{ \partial x } + \frac{ \partial c_{2}\psi_{2} }{ \partial x }   \right) = i\hbar (\frac{ \partial c_{1}\psi_{1} }{ \partial t } +\frac{ \partial c_{2}\psi_{2} }{ \partial t }) 
$$
$$
c_{1}\psi_{1} \propto \psi_{1} ; \ \ c_{2}\psi_{2}\propto \psi_{2}
$$
$$
-\frac{\hbar^{2}}{2m} \frac{ \partial \psi_{1} }{ \partial x } -\frac{\hbar^{2}}{2m} \frac{ \partial \psi_{2} }{ \partial x } = i\hbar \frac{ \partial \psi_{1} }{ \partial t } +i\hbar \frac{ \partial \psi_{2} }{ \partial t } 
$$
$$
-\frac{\hbar^{2}}{2m} \frac{ \partial \psi_{1} }{ \partial x }  = i\hbar \frac{ \partial \psi_{1} }{ \partial t } 
$$
$$
-\frac{\hbar^{2}}{2m} \frac{ \partial \psi_{2} }{ \partial x }  = i\hbar \frac{ \partial \psi_{2} }{ \partial t } 
$$
$$
\therefore -\frac{\hbar^{2}}{2m}\frac{ \partial \psi_{1} }{ \partial x } + \left( -\frac{\hbar^{2}}{2m} \frac{ \partial \psi_{2} }{ \partial x }  \right) = i\hbar \frac{ \partial \psi_{1} }{ \partial t }  + i\hbar \frac{ \partial \psi_{2} }{ \partial t } 
$$
Problem 11
![[Pasted image 20240125170314.png]]
$$
((Ae^{-ikx}+Be^{ikx})(Aike^{ikx}-Bike^{-ikx})-(Ae^{ikx}+Be^{-ikx})(-Aike^{-ikx}+Bike^{ikx}))
$$
Expanded and simplified with wolfram
$$
2ik(A^{2}-B^{2})
$$
$$
j_{x} = \frac{\hbar}{2mi} (2ik(A^{2}-B^{2}))
$$
$$
j_{x} = \frac{\hbar}{m} k(A^{2}-B^{2})
$$
Problem 12
![[Pasted image 20240125170324.png]]
$$
1=\int\limits_{0}^{L} Nx^{2}(L-x) \, dx 
$$
$$
\frac{1}{N} = \int\limits_{0}^{L} x^{2}(L-x) \, dx 
$$
Computed with wolfram
$$
\frac{1}{N} = \frac{L^{4}}{12}
$$
$$
N = \frac{12}{L^{4}}
$$
Finding expectation value for x
$$
\langle x \rangle = \int \psi^* x\psi\, dx 
$$
$$
\int\limits_{0}^{L} (\frac{12}{L^{4}}x^{2}(L-x))^{2}x \, dx 
$$
$$
\frac{12}{L^{4}}\int\limits_{0}^{L} (x^{2}(L-x^{2}))^{2}x \, dx 
$$
Computed with wolfram 
$$
\frac{12}{L^{4}}(\dfrac{L^8\cdot\left(6L^2-15L+10\right)}{60})
$$
$$
\langle x \rangle = \dfrac{L^4\cdot\left(6L^2-15L+10\right)}{5}
$$
Problem 13

![[Pasted image 20240125170335.png]]
$$
\langle p_{x} \rangle = \int\limits_{-\infty}^{\infty} \Psi^{*} \frac{\hbar}{i} \frac{\partial}{\partial x}(\Psi)\, dx 
$$
$$
\int\limits_{-\infty}^{\infty} e^{-ikx}\psi^{*}(x) \frac{\hbar}{i} ike^{ikx}\psi(x) \, dx 
$$
$$
	\int\limits_{-\infty}^{\infty}e^{-ikx}\psi(x) \frac{\hbar}{i}ike^{ikx}\psi(x)  \, dx 
$$
$$
\hbar k\int\limits_{-\infty}^{\infty} \psi^{2}(x) \, dx 
$$
$$
\int\limits_{-\infty}^{\infty} \psi^{2}(x) \, dx =1
$$
$$
\langle p_{x} \rangle = \hbar k
$$

Problem 14
![[Pasted image 20240125135405.png]]
$$
A(k)=\left( \frac{2}{\pi} \right)^{1/4}\sqrt{ \sigma }e^{-\sigma^{2}}(k-k_{0})^{2}
$$
$$
\Psi(x) = \frac{1}{\sqrt{ 2\pi }}\int\limits_{-\infty}^{\infty} A(k)e^{ikx} \, dk
$$
$$
\Psi(x) = \frac{1}{\sqrt{ 2\pi }}\int\limits_{-\infty}^{\infty} \left( \frac{2}{\pi} \right)^{1/4}\sqrt{ \sigma }e^{-\sigma^{2}(k-k_{0})^{2}}e^{ikx} \, dk
$$

$$
\int\limits_{-\infty}^{\infty}e^{-a(k-k_{0})^{2}x}e^{ikx}  \, dx 
$$
Multiply by 
$$
e^{ik_{0}x}e^{-ik_{0}x}
$$
You get 
$$
e^{ik_{0}x} \int\limits_{-\infty}^{\infty} e^{-a(k-k_{0})^{2}}e^{ikx}e^{-ik_{0}x} \, dk
$$
$$
e^{ik_{0}x} \int\limits_{-\infty}^{\infty} e^{-a(k-k_{0})^{2}}e^{i(k-k_{0})x} \, dk
$$
$$
e^{ik_{0}x} \int\limits_{-\infty}^{\infty} e^{-ak'^{2}}e^{ik'x} \, dk'
$$
$$
e^{ik_{0}x} \int\limits_{-\infty}^{\infty} e^{-ak'^{2}+{ik'x}} \, dk'
$$
$$
(bk' + c) ^{2} = b^{2}k'^{2} +2c b k' + c^{2}
$$
$$
b^{2}k'^{2} + 2c b k' = (bk'+c)^{2}-c^{2}
$$
$$
ak'^{2}+ik'x
$$
$$
b^{2} = a 
$$
$$
ak'^{2} + ik'x = \left( \sqrt{ ak' }  + \frac{ix}{2\sqrt{ a }} \right) - -\frac{x^{2}}{4a}
$$
$$
2bc = ix
$$
$$
c=\frac{ix}{2\sqrt{a}}
$$
rewrite int as
$$
e^{ik_{0}x} \int e^{-(\sqrt{ a }k' + (ix)/2\sqrt{ a })^{2}}e^{-x^{2}/4a} \, dx 
$$
$$
e^{ik_{0}x} \int e^{-u^{2}} e^{-x^{2}/4a} \, dx 
$$
$$
e^{ik_{0}x} e^{-x^{2}/4\sigma}\int\limits_{-\infty}^{\infty} e^{-u^{2}} \, du = \sqrt{ \pi }
$$
$$
u = -(\sqrt{ a }k' + (ix)/2\sqrt{ a })^{2} ; \ \ du= \frac{a}{2} (x-2ik)
$$
We can drop the constants
$$
\propto e^{ik_{0}x} e^{-x^{2}/4\sigma}
$$
Ta-da

Problem 15
![[Pasted image 20240125130750.png]]
Normalize Wave functions
$$
\int\limits_{-\infty}^{\infty} \psi^{*}\psi \, dx  =1
$$
$$
1 = \int\limits_{-\infty}^{0} A^{2}e^{2\kappa x} \, dx + \int\limits_{0}^{\infty} A^{2}e^{-2\kappa x} \, dx  
$$
$$
\frac{1}{A^{2}} =  \int\limits_{-\infty}^{0} e^{2\kappa x} \, dx + \int\limits_{0}^{\infty} e^{-2\kappa x} \, dx  
$$
$$
\frac{1}{A^{2}} = \frac{1}{2\kappa} + \frac{1}{2\kappa}
$$
$$
\frac{1}{A^{2}} = \frac{1}{\kappa}
$$
$$
A^{2} = \kappa \therefore A = \sqrt{ \kappa }
$$
Finding $\langle x \rangle$
$$
\int\limits_{-\infty}^{0} x\kappa e^{2\kappa x} \, dx +\int\limits_{0}^{\infty} x\kappa e^{-2\kappa x} \, dx 
$$
Integration by parts (wolfram)
$$
-\dfrac{1}{4{\kappa}} + \frac{1}{4\kappa}
$$
$$
\langle x \rangle = 0
$$
This corresponds to the graphical observation!
![[Pasted image 20240125134700.png]]

$$
\int\limits_{-\infty}^{0} x^{2}\kappa e^{2\kappa x} \, dx +\int\limits_{0}^{\infty} x^{2}\kappa e^{-2\kappa x} \, dx 
$$
Use integration by parts (wolfram alpha)
$$
\frac{1}{4\kappa^{2}} + \frac{1}{4\kappa^{2}}
$$
$$
\frac{2}{4\kappa^{2}} = \frac{1}{2\kappa^{2}}
$$

$$
\frac{1}{2\kappa^{2}}
$$
$$
\Delta x = \sqrt{ \frac{1}{2\kappa^{2}} + 0^{2} } = 0 
$$
$$
\Delta x =\frac{1}{\kappa} \sqrt{ \frac{1}{2} }
$$





