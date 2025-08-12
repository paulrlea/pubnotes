Last time: [[@Spring2024/Physics/Theoretical Mechanics 1/Class Notes/Concepts/Expectation values]] and [[Gaussian distributions]], as well as [[Heisenberg Uncertainty Principle ]]
#qp1 #phys #lecture 



## Superposition of waves and time evolution

Recall [[Notes/Physics/Quantum Physics/Concepts/superposition]] of waves. 
$$
\psi_{1} + \psi_{2} = ?
$$
In previous lectures we have defined 
$$
\psi(x) = \int A(k)\sin(kx) \, dk
$$
So, $A(k) = ?$

In general, 
$$
\psi(x) = \sum c_{n}\sin\left( \frac{n\pi x}{L} \right)
$$
The previous portion($\sin\left( \frac{n\pi x}{L} \right)$) of the above formula is also the [[basis]] for our [[Notes/Physics/Quantum Physics/Concepts/Functional Vector Space]]? Wave superposition gives rise through time dependence. 
Example:
$$
\Psi(x,t) = \frac{1}{\sqrt{ 2 }}\Psi_{1}(x,t) + \frac{1}{\sqrt{ 2 }}\Psi_{2}(x,t)
$$

Solving this by including the appropriate factor of $e^{-iE_{n}t/\hbar}$ we get. 
$$
e^{-iE_{n}t/\hbar}\left[ \frac{1}{\sqrt{ 2 }}\psi_{1} + \frac{e^{-iE_{n}t/\hbar}}{\sqrt{ 2 }} \right]
$$
And the probability density is therefore given by
$$
|\Psi(x,t)|^2 = \Psi^*\Psi = \frac{1}{2}\psi^2_{1} \frac{1}{2}\psi^2_{2} + \psi_{2}\psi_{1}\cos(E_{2}-E_{1})t/\hbar
$$
Recall: 
$$
\Psi_{n}(x,t)=\sum c_{n}\varphi_{n}(x)e^{-iE_{n}t/\hbar}
$$$ @ $t=0$ 


This is also the Fourier series expansion? 
Need to talk to him in office hours about the rest of this section. I don't understand wtf is a Fourier coefficient. 



