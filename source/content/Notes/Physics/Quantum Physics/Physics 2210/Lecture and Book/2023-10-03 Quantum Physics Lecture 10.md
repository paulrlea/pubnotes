Last class [[2023-09-29 Quantum Physics Lecture 9]]
- Solving [[Notes/Physics/Quantum Physics/Concepts/Time independent Schrodinger equation]] with Separation of variables. 
- [[Notes/Physics/Quantum Physics/Concepts/Infinite square well]] and how to solve for boundry conditions
- Quantization of energy into discrete levels, zero point energy and $\Psi^{*}\Psi$ is time independent

# [[Notes/Physics/Quantum Physics/Concepts/superposition]]
The wave function given in last class is a specific example of [[Notes/Physics/Quantum Physics/Concepts/superposition]] that can be generalized to the function given below. 
$$
\Psi(x)=c_{1}\psi_{1}(x) + c_{2}\psi_{2}(x)
$$
Where $c_{1}$ and $c_{2}$ are complex numbers. We can further generalize this above function to the below function: 
$$
\Psi(x,t) = \sum c_{n} \varphi_{n} (x) e^{-iE_{n}t/\hbar}
$$
where we get 
$$
\varphi (x)e^{-iE_{n}t/\hbar} = \psi_{n}(x)
$$
through time evolution. (adding the $e^{-iE_{n}t/\hbar}$ term)

Setting t=0, we can see the following 
$$
\varphi^{*}_{m}\Psi(x,0) = \sum C_{n}\varphi_{m}^{*}\varphi_{n}(x) 
$$
$$
\int \varphi^{*}_{m} \Psi(x,0)\ dx = \sum C_{n} \int \varphi^{*}_{m}\varphi_{n}(x) \, dx 
$$
>From the integral on the the RHS of the above eq:
>$$
\int \varphi_{m}^{*}\varphi_{n} \, dx 
$$
>$$
\int \sin\left( \frac{m\pi x}{L} \right) \sin\left( \frac{n\pi x}{L} \right)\, dx 
$$
>This yields a situation where the function is 0 where $m \neq 0$ and 1 where $m=n$. 
>This is known as the [[Kronecker delta]], and is denoted by
>$$
\delta_{m,n}
$$
$$
\int \varphi_{m}^{*}\Psi(x,0) \, dx  = \sum C_{n}\delta_{m,n}=C_{m}
$$

This above equation is equivalent to the Fourier coefficient. 

**NB**: $|C_{m}|^{2}\sim$ probability of a particle being in the "nth" state. 

For $t>0$, 
$$
\Psi(x,t) = \sum_{n} c_{n}\varphi_{n}(x)e^{-iE_{n}t/\hbar}
$$
We know that 
$$
\int ^{L} _{0} \Psi^{*}(x,t)\Psi(x,t) \, dt = 1
$$
Because the particle has to be *somewhere*. 
If we substitute in $\sum_{n} c_{n}^{*}\varphi_{n}^{*}(x)$ for $\Psi^{*}(x,t)$ we can derive the formula above to
$$
\sum_{m} |C_{m}|^{2} = 1
$$
where $C_{m}$ is the probability of finding the particle in the "m"th state.

# [[Functional Vector Space]]
Using the following equation, 
$$
\Psi(x,t) = \sum c_{n} \psi_{n} (x)
$$
We can draw an analogy to geometrical vector space $\mathcal{V}$, where we have vectors $\vec{A}, \vec{B}$ that are composed of unit vectors $\hat{i}, \hat{j}\ \& \ \hat{k}$. If we take an analogy to wave-function vector space, we can compose objects (vectors), $\Psi(x,t)$ with unit vectors $\varphi_{n}$ and $\varphi_{m}^{*}$. 
![[Pasted image 20231026222121.png]]'
vs
![[Pasted image 20231026222135.png]]

Applying the above, we can have a basis vector:
$$
\varphi_{n}(x) = \sqrt{ \frac{2}{L} } \sin\left( \frac{n\pi x}{L} \right) 
$$
Represent an [[eigenfunction]] of the Hamiltonian operator $\hat{H}$ in the following equation: 
$$
\left[ -\frac{\hbar^{2}}{2m} \frac{d^{2}}{dx^{2}} + V(x) \right]\varphi(x) = E\varphi(x)
$$
where the Hamiltonian operator $\hat{H}$ is represented in the square brackets. If you solve for appropriate values of E and $\varphi$, you can graph it: 
![[Pasted image 20231026222619.png]]
