---
dg-publish: true
---
# Quantum Physics v. Quantum Mechanics 

- [[Quantum Physics]] is the study of the behavior of matter and energy at very small scales. There are a variety of fields of Quantum physics, just as there is a variety of fields of classical physics 
- Quantum Mechanics, or QM, is the underlying fundamental theory at subatomic scales. Quantum Mechanics form the foundation of quantum physics. The experiments covered previously are quantum physics, the mathematical framework behind them is quantum mechanics. 

# Quantum Mechanics: A Brief Introduction

## Measurement and Operators
- Systems can exist as a superposition of multiple eigenstates. Like the ingredients in a cake, they come together to form a complete system, but can change independently. 
- When measuring a system, we take a measurement of one eigenvalue. Examples include energy, momentum, position, etc. etc. The act of measurement confines the entire system into the state corresponding to that eigenvalue, known as an eigenstate. 
- This is known as "collapsing" the system 

### Operators and Eigenvalues

- The concept of an operator is a cornerstone of quantum mechanics. Every observable has a corresponding operator. Examples include: 
	- Energy operator: (Hamiltonian), used in the [[Notes/Physics/Quantum Physics/Concepts/Time independent Schrodinger equation]]
	$$
    \hat{H} = -\frac{\hbar^{2}}{2m} \frac{ \partial^{2}  }{ \partial x^{2} } +V(x)
    $$
    - The linear momentum operator: 
    $$
    \hat{p}_{x} = \frac{\hbar}{i} \frac{ \partial  }{ \partial x } 
    $$
    - The parity operator: 
    $$
    \hat{\Pi} \psi(x) = \psi(-x)
    $$

These are just a few of many operators. Others include the [[Angular Momentum]] operator. 
Some rules for operators to keep in mind: 
- Operators must act on a function $(\psi)$
- Operators act to the right (see also: [[Dirac Notation]])
- Multiple operators implies successive operations on the function, starting from the right
	- Not always commutative. Order matters

#### The eigenvalue equation
- The eigenvalue equation is given by 
$$
\hat{A}\psi_{a} =a\psi
$$
	with operator $\hat{A}$ and eigenvalue $a$
- All possible values of $a$ is called the spectrum of the operator. 
- !!! **WHILE IN AN EIGENSTATE, THE UNCERTAINTY IN THE OBSERVABLE IS 0!!!**
- The eigenstate of one observable may or may not be an eigenstate of another observable
- This leads us nicely into the topic of [[Notes/Physics/Quantum Physics/Concepts/Hermitian Operator]]s. I cover Hermitian operators on their own page, therefore they are omitted from this lecture notes :). 

## Linearity and Superposition
### Linearity

- Given 2 distinct state functions $(\psi)$ of a system with energy level H, the linear combination of these two $\psi$ will also satisfy the [[Notes/Physics/Quantum Physics/Concepts/Time independent Schrodinger equation]] with arbitrary constants $c_{1}$ and $c_{2}$. This is known as a [[Notes/Physics/Quantum Physics/Concepts/superposition]] of two quantum states. 

$$
\hat{H}(c_{1}\psi_{1} + c_{2}\psi_{2} ) = \hat{E}(c_{1}\psi_{1} + c_{2}\psi_{2} )
$$
$$
\implies (c_{1}(\hat{H}-\hat{E})\psi_{1} + c_{2}(\hat{H}-\hat{E})\psi_{2})=0
$$
- Any given linear combination represents a [[Quantum state]] of a system
- If you think about it, its conceptually similar to a Fourier series. Hmmm.....


## Parity Operator
The parity operator was teased earlier in the notes. It is defined as the following: 
$$
\hat{\Pi} \psi(x) = \psi(-x)
$$



