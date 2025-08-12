---
dg-publish: true
---

Superposition 
$$
\psi_{1} + \psi_{2} = ?
$$
Previously, we have defined 
$$
\psi(x) = \int A(k)\sin(kx) \, dk
$$
So, $A(k) = ?$

In general, 
$$
\psi(x) = \sum c_{n}\sin\left( \frac{n\pi x}{L} \right)
$$
The previous portion($\sin\left( \frac{n\pi x}{L} \right)$) of the above formula is also the [[basis]] for our [[Notes/Physics/Quantum Physics/Concepts/Functional Vector Space]]. Wave superposition gives rise through time dependence. 
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
$$
$t=0$ 


This is also the Fourier series expansion

The wave function given above  is a specific example of [[Notes/Physics/Quantum Physics/Concepts/superposition]] that can be generalized to the function given below. 
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
through [[time evolution]]. (adding the $e^{-iE_{n}t/\hbar}$ term)

Setting t=0, we can see the following 
$$
\varphi^{*}_{m}\Psi(x,0) = \sum C_{n}\varphi_{m}^{*}\varphi_{n}(x) 
$$
$$
\int \varphi^{*}_{m} \Psi(x,0)\ dx = \sum C_{n} \int \varphi^{*}_{m}\varphi_{n}(x) \, dx 
$$
>From the integral on the the RHS of the above eq:
$$
\int \varphi_{m}^{*}\varphi_{n} \, dx 
$$
$$
\int \sin\left( \frac{m\pi x}{L} \right) \sin\left( \frac{n\pi x}{L} \right)\, dx 
$$
>This yields a situation where the function is 0 where $m \neq 0$ and 1 where $m=n$. 
>This is known as the [[@Spring2024/Physics/Math Background/Kronecker delta]], and is denoted by
$$
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
