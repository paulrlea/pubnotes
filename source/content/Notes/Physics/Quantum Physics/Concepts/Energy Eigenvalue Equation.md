---
dg-publish: true
---
Another name for the [[Notes/Physics/Quantum Physics/Concepts/Time independent Schrodinger equation|Time independent Schrodinger equation]]

$$
\hat{H}\varphi(x) = E \varphi(x)
$$
The energy operator is given by $\hat{H}$, our eigenfunctions are given by $\varphi(x)$, and our eigenvalue is given by $E$. 

This can be extended to a general form where
$$
\hat{A}\varphi_{a} = a\varphi_{a}
$$
Where $\hat{A}$ can be any operator. 

Example: 
$$
\hat{p}\left( \sqrt{ \frac{2}{L} }\left( \frac{n\hbar x}{L} \right) \right) = \frac{\hbar}{i} \frac{d}{dx}\left( \sqrt{ \frac{2}{L} } \sin\left( \frac{n\hbar x}{L} \right) \right)
$$
$$
	=\frac{\hbar}{i} \sqrt{ \frac{2}{L} } \frac{n\hbar}{L}\cos\left( \frac{n \hbar x}{L} \right)
$$
$$
\neq constant\ x  \ \sin\left( \frac{n\hbar x}{L} \right)
$$
Therefore, $\sin\left( \frac{n\hbar x}{L} \right)$ is not an eigenfunction of $\hat{p}$

The operator $\hat{H}$ is interesting because it is a linear operator
Consider: 
$$
\psi(x) = c_{1}\varphi(x) + c_{2}\varphi_{2}(x)
$$
Now if $\hat{H}\varphi_{n}(x)=E_{n}\varphi_{n}(x)$, then 
$$
\hat{H}\Psi_{n}(x) = \hat{H}[c_{1}\varphi_{1}(x)=c_{2}\varphi_{2}(x)]
$$
$$
= c_{1}E_{1}\varphi_{1}(x) + c_{2}E_{2}\varphi_{2}(x) \neq E[c_{1}\varphi_{1}(x) + c_{2}\varphi_{2}(x)]
$$
In general, unless $E_{1} = E_{2}$



