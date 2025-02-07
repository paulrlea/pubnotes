---
dg-publish: true
---
The solution to [[Legendre Differential Equations]]
$$
R(t) = A_{n} t^{n} + B_{n}t^{-n-1}
$$
Integrating the product of 2 Legendre polynomials yields the following: 
$$
\int\limits_{-1}^{1} P_{n}(x)P_{m}(x)  \, dx  = \frac{2}{2n+1} \delta_{mn} 
$$
$$
\delta_{mn}\begin{cases}
0 & m\neq n \\
1 & m=n
\end{cases}
$$
$$
F(x) = \sum^{\infty}_{n=p} A_{n}P_{n}(x) | P_{m}(x) = 
$$
$$
\int\limits_{-1}^{1} F(x)P_{m}(x)dx  = \sum^{\infty}_{n=0} A_{n} \frac{2}{2n+1} \delta_{mn}  = A_{m} \frac{2}{2m+1}
$$
$$
A_{m} = \frac{2m+1}{2}\int\limits_{-1}^{1} F(x)P_{m}(x) \, dx 
$$
