### Review of S.E 
$$
p = \frac{h}{\lambda} ; E=\hbar\omega
$$
$$
\Psi = \text{complex}
$$
$$
e^{i\omega t}
$$
Has to be continuous and normalize-able 
$$
j \equiv \frac{\hbar}{2mi} \left( \Psi^{*} \frac{d\Psi}{dx}- \frac{\Psi d\Psi^{*}}{dx}\right)
$$
S.E
$$
-\frac{\hbar^{2}}{2m} \frac{d^{2}\Psi}{dx^{2}} + V\Psi = \frac{\hbar}{i} \frac{d\Psi}{pt}
$$
We can express any wavefunction as a sum of pure momentum states

2 ways to calculate momentum 
1. Hard way. math major way. 
Use the wave function to compute $\Phi_{p}(p)$.
2. Easy way. (better way)
Express p as a function of x
Using momentum operator

## Correspondence principle
- Anything calculated from quantum physics in the right limits should correspond to classical physics in the right limits
- We should find a momentum operator that corresponds

Pure momentum state
$$
\psi(x,t) = Ae^{i(px-Et)/\hbar}=Ae^{i(kx-\omega t)}
$$
And using the momentum operator: 
$$
p_\text{op} \Psi = \frac{\hbar}{i}\frac{ \partial \Psi }{ \partial x } = \frac{\hbar}{i} \frac{Aip}{\hbar} e^{i(px-E)/\hbar}
$$
General operator construction


### Solving S.E (time independent)

$$
-\frac{\hbar^{2}}{2m} f(t) \frac{ d ^{2}\psi(x) }{ d x^{2} } + V\psi(x)f(t)   = i\hbar \psi(x)\frac{ d f(t) }{ d t } 
$$
divide everything by 
$$
\psi(x)f(t)
$$
You get
$$
-\frac{i\hbar^{2}}{f} \frac{ d ^{2}\psi(x) }{ d x^{2} } + V(x) = \frac{ib\hbar}{f} \frac{ d f(t) }{ d t }  =E
$$
$$
\frac{i\hbar}{f}\frac{ d f }{ d t }  = E
$$
$$
\frac{df}{f} = \frac{1}{i\hbar} Edt
$$
$$
\frac{\hbar^{2}}{2m} \frac{1}{\psi} \frac{ d ^{2}\psi }{ d x^{2} +v} -V\psi = -E\psi
$$
$$
\frac{\hbar^{2}}{2m} \frac{d^{2}\psi}{dx^{2}} + (E-V) \psi=0
$$
Time independent S.E 
[[Notes/Physics/Quantum Physics/Concepts/Time independent Schrodinger equation]]

TISE

$$
\frac{ d ^{2}\psi }{ d x^{2} } + \frac{2m}{\hbar} (E-V) \psi = 0
$$


