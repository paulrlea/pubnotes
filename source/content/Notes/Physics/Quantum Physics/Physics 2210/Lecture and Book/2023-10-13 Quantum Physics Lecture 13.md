See last class [[2023-10-10 Quantum Physics Lecture 12]]

# Simple Harmonic Oscillator 

Review:
[[Notes/Physics/Quantum Physics/Concepts/Functional Vector Space]]
[[Energy Eigenvalue Equation]]

Examples of different eigenstates that manifest from different V(x):
- [[Notes/Physics/Quantum Physics/Concepts/Infinite square well]]
- [[Notes/Physics/Quantum Physics/Concepts/Finite Square Well]]
- [[Quantum Harmonic Oscillator]]
- Coulombs potential (v=1/r)

Recall: Classical Harmonic Oscillator: 
The model for a classical harmonic oscillator is given by: 
$$
v=\frac{1}{2}k_{0}x^{2} 
$$
Where $k_{0}$ is the spring constant

$$
F=-\frac{dv}{dx} = -k_{0}x = m \frac{dx^{2}}{dt^{2}}
$$
This differential equation yields solutions: 
$$
	e^{i\omega t} \ and \ \omega \equiv \sqrt{ \frac{k_{0}}{m} }
$$
$$
H=\frac{p^{2}}{2m} + V(x)
$$
Where H represents the energy of the system. 

If we extend this to the quantum case, we get 
$$
\hat{H} = \frac{\hat{p}^{2}}{2m} + v(\hat{x}) \implies =\frac{\hbar^{2}}{2m} \frac{d^{2}\varphi(x)}{dx^{2}} + v(x) \varphi(x) = E\varphi(x)
$$
Solving this for the 
