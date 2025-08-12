#phys #qp1 
Review [[2023-10-24 Quantum Physics Lecture 16]]
- [[Notes/Physics/Quantum Physics/Concepts/Quantum Tunneling]]
- [[Notes/Physics/Quantum Physics/Concepts/Step Potentials]] and [[Scattering]]
- [[Bound States]] including [[Notes/Physics/Quantum Physics/Concepts/Infinite square well]], [[Notes/Physics/Quantum Physics/Concepts/Finite Square Well]] and [[Quantum Harmonic Oscillator]].
- Solving the [[Notes/Physics/Quantum Physics/Concepts/Time independent Schrodinger equation]] for $\hat{H}$
## Quantum Postulates
1. Every measurable quantity "a" is associated with an operator $\hat{A}$, that is also called an "observable", that is related through: $$
\hat{A}\varphi(x) = a \varphi(x)
$$
2. Any _measurement_ of $A$ gives a corresponding eigenvalue $a$ and a matching eigenstates $\varphi_{n}$
3. $\Psi_{(x,t)}$ contains all the information of the system
	1. $|\Psi|^{2}$ is the probability density, and $<A> = \int \Psi ^* \hat{A} \Psi \, dx$ gives the expectation value of $A$.
4. Time dependent $\Psi(x,t)$ obeys S.E: $$
\frac{\hat{p}^{2}}{2m} \Psi_{(x,t)} + V(x) \Psi_{x,t} = i\hbar \frac{d}{dt}\Psi_{x,t}
$$

## [[Notes/Physics/Quantum Physics/Concepts/Hermitian Operator]]
If an operator has
 1. Real Eigenvalues
 2. Orthogonal Eigenfunctions and distinct Eigenvalues for these Eigenfunctions,
 3. Eigenfunctions that form a complete set: i.e can express any function as a superposition of its constituent eigenfunctions. 
 Then the operator is known as a hermitian operator.
N.B: Observational operators are hermitian. 

Example: 
$$
\int ^{\infty}_{-\infty} \varphi^*(A\Psi)\, dx = \int ^{\infty}_{-\infty} (A\varphi)^{*} \Psi \, dx =\int ^{\infty}_{-\infty} \varphi^{*} A^{\dagger} \Psi  \, dx 
$$

## Matrix Mechanics and Representation

