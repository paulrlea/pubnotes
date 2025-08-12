---
dg-publish: true
---
# What is a hermitian operator
- Hermitian operators have real expectation values. 
$$
\therefore \left< A \right> =\left< A \right> ^{*}
$$
- Observational (physically measurable) operators are hermitian. 
$\hat{Q}$ is hermitian if for any two physically possible state functions 
$$
\int \Psi_{1}^{*} \hat{Q} \Psi_{2} \, dx  = \int (\hat{Q}^{*}\Psi_{1}^{*}) \Psi_{2} \, dx 
$$
# Why do I care

- All operators with measurable quantities are hermitian, which is why they have real expecation values/eigenvalues
- Any real function of a hermitian operator is also hermitian.
- The product of two hermitian operators is also hermitian, given that the two operators follow .[[Notes/Physics/Quantum Physics/Concepts/Commutation Relations]]
- The eigenvalues of a hermitian operator are the only observable measurements of that observable. Think about that for a second. This leads to the quantization of energy, momentum, etc etc 
- And last but not least, the [[eigenfunction]]s of a hermitian operator are [[orthogonal]], constitute a complete set and satisfy closure. Linear algebra bullshit. 

## Completeness
More linear algebra bullshit regarding the properties of hermiticity...
- In general, the completeness of a set of eigenfunctions generally usually means that any function of the variables on which the eigenvalues depend can be represented through the following
$$
f=\sum_{q} c_{q}\psi_{q}
$$
> This is kinda related to [[@Spring2024/Physics/Math Background/Fourier Series]]... if you read [[Lecture 17 - Quantum Mechanics]] then you'll see why this is kinda cool. This fourier guy was pretty neat. 

- In normal-non-math-major speak, this means that if you have a function, any function, that depends on variables $x,y$ and $z$, we can represent this thing through a bunch of other functions added together. Completeness just means that any function dependent on these variables can be represented by a sum of eigenfunctions

#### Finding coefficents
- this is the mathy stuff that you probably actually will be doing 
$$
\int \psi^{*}_{q} f \, dx = \int  \psi^{*}_{q'}\sum c_{q} \psi_{q} \, dx = \sum c_{q} \int \psi^{*}_{q'} \psi_{q} \, dx  = c_{q'} 
$$
This can be more formally proved and is gone into more depth later on. See EM theory notes for similar work. 

In layman's terms, this is how we find how "much" of $\psi^{*}_{q}$ is in $f$

Summary: 
If an operator has
 1. Real Eigenvalues
 2. Orthogonal Eigenfunctions and distinct Eigenvalues for these Eigenfunctions,
 3. Eigenfunctions that form a complete set: i.e can express any function as a superposition of its constituent eigenfunctions. 
 Then the operator is known as a hermitian operator.



Example with dagger notation... might be wrong
$$
\int ^{\infty}_{-\infty} \varphi^*(A\Psi)\, dx = \int ^{\infty}_{-\infty} (A\varphi)^{*} \Psi \, dx =\int ^{\infty}_{-\infty} \varphi^{*} A^{\dagger} \Psi  \, dx 
$$
