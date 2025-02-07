---
dg-publish: true
---
>We look at [[Laplace's equation]] and solving it with separation of variables, example in Figure 2.9, and math behind Fourier series and orthogonality of harmonic functions. 
### General solution of [[Laplace's equation]] in Cartesian coordinates
$$
\vec{\nabla}^{2}V=0
$$
$$
	\frac{ \partial^{2} V(x,y,z) }{ \partial x^{2} } + \frac{ \partial^{2} V(x,y,z) }{ \partial y^{2} } +\frac{ \partial^{2} V(x,y,z) }{ \partial z^{2} } =0
$$
Trial Solution given by
$$
V(x,y,z) = X(x)Y(y)Z(z)
$$
Put this in the differential Equation
$$
YZ \frac{ \partial^{2} X }{ \partial x^{2} }+XZ\frac{ \partial^{2} Y }{ \partial y^{2} } +XY \frac{ \partial^{2} Z }{ \partial z^{2} } = 0
$$
Divide both sides of equation by $XYZ$
$$
\frac{1}{X} \frac{ \partial^{2} X }{ \partial x^{2} } + \frac{1}{Y} \frac{ \partial^{2} Y }{ \partial y^{2} } +\frac{1}{Z} \frac{ \partial^{2} Z }{ \partial z^{2} } =0
$$
For the sum of these terms to be 0, each term has to be constant. We assign $\alpha,\beta$ and $\gamma$ to the terms 
$$
\alpha^{2}+\beta^{2}-\gamma^{2} = 0
$$
$$
\frac{1}{X} \frac{ \partial^{2} X }{ \partial x^{2} }  = \alpha^{2}
$$
$$
\frac{1}{Y} \frac{ \partial^{2} Y }{ \partial Y^{2} } = \beta^{2}
$$
$$
\frac{1}{Z} \frac{ \partial^{2} Z }{ \partial z^{2} } =\gamma^{2}
$$
Now we get 3 separate differential equations
We can use an [[ansatz]] of 
$$
x = e^{-i\alpha x}
$$
to solve these equations for x,y and z respectively, with differing appropriate exponential components. 
$$
\frac{ \partial^{2} X }{ \partial x^{2} } =  (\pm i\alpha)(\pm i\alpha)e^{\pm i\alpha x}
$$
$$
=-\alpha^{2}e^{\pm i\alpha x}
$$
And generalizing this to the other 2 coordinates, 

$$
V(x,y,z) = e^{\pm i\alpha x}e^{\pm i\beta y}e^{\pm i\gamma z}
$$
### Example with Figure 2.9 from the textbook
- See powerpoint for full description 
- Uses a double fourier integral over the top of the box

### Orthogonality of harmonic functions
$$
\int \sin ax\sin bx \, dx \begin{cases}
\frac{\sin(a-b)x}{2(a-b)}-\frac{\sin(a+b)x}{2(a+b)}
\end{cases}
 \text{ if a} \neq \text{b}
$$
Solution of integral
$$
\frac{1}{2}x - \frac{1}{4a}\sin(2ax )
$$

Looking at finite case
$$
\int\limits_{0}^{L} \sin \frac{n\pi x}{L} \sin \frac{m\pi x}{L} \, dx =\frac{\frac{\sin\left( n-\frac{m\pi x}{} \right)}{L}}{2\frac{n-L\pi}{L}} - \frac{\sin\frac{((n-m)\pi x)}{L}}{2 \frac{n+m\pi}{L}} |^{L}_{0}
$$
Evaluated:
$$
\frac{\sin(n-m\pi)}{2 \frac{(n-m)\pi}{L}}-\frac{\frac{\sin(n+m)\pi}{2(n-m)\pi}}{L}-\left[ \frac{\sin0}{2(n-m)\pi/L}-\frac{\sin0}{2(n-m\pi \pi) \frac{\pi}{L}} \right] = 0
$$
The whole integral is 0 if n & m are both 0 or if they are unequal 
$$
\int\limits_{0}^{L} \sin\left( \frac{n\pi x}{L} \right)\sin\left( \frac{m\pi x}{L} \right) \, d = \frac{1}{2x}- \frac{1}{\frac{4n\pi}{L}}\sin\left( \frac{2n\pi}{L} \right)x | ^{L}_{0} 
$$
$$
=\frac{1}{2}L - \frac{1}{\frac{4n\pi}{L}} \sin n2\pi-\left[ 0-\frac{1}{\frac{4n\pi}{L}} \sin0\right]
$$
$$
\int\limits_{0}^{L} \sin\left( \frac{n\pi x}{L}\sin \frac{m\pi x}{L} \right) \, d = \frac{1}{2L}\delta_{n,m} 
$$
The $\delta_{n,m}$ is known as the[[@Spring2024/Physics/Math Background/Kronecker delta]]. Makes life easier. 

$$
\delta_{nm} = \begin{cases}
0 &  n \neq m  \\
1 & n=m
\end{cases}
$$

### [[@Spring2024/Physics/Math Background/Fourier Series]]
Any function $F(x)$ can be represented as an infinite series of sin or cosine functions
$$
F(x) = \sum^{\infty}_{n=1} a_{n}\sin\left( \frac{n\pi x}{L}  \right) | \sin \left( \frac{m\pi x}{L} \right)
$$
$$
F(x)\sin\left( \frac{m\pi x}{L} \right) = \sum^{\infty}_{n=1} a_{n}\sin \frac{n\pi x}{L}\sin \frac{m\pi x}{L}
$$
Integrate both sides from 0 -> L

$$
	\int\limits_{0}^{L} F(x)\sin\left( \frac{m\pi x}{L} \right) \, d = \int\limits_{0}^{L} \sum ^{\infty}_{n=1} a_{n} \sin\left( \frac{n\pi x}{L} \right) \sin\left( \frac{m\pi x}{L} \right) \, dx  
$$
$$
	 = \sum^{\infty}_{ n=1} a_{n} \int\limits_{0}^{L} \sin\left( \frac{n\pi x}{L} \right)\sin\left( \frac{m\pi x}{L} \right)  \, dx 
$$
$$
= \sum^{\infty}_{n=1}a_{n} \frac{1}{2}L\delta_{nm}
$$
Use [[@Spring2024/Physics/Math Background/Kronecker delta]]

The integral from 0 -> L over $F(x)\sin (\frac{m\pi x}{L})$ is equal to 
$$
a_{m} \frac{1}{2}\delta_{n,m}
$$
Know that the Kronecker delta can be used to represent a product of two sines like seen above. 

$$
a_{m} \frac{1}{2}L \implies a_{m} = \frac{2}{L} \int\limits_{0}^{L} F(x)\sin\left( \frac{m\pi x}{L} \right) \, dx 
$$
Use boundary conditions to solve out
Next time: double Fourier series

In class problem 3.15
A rectangular pipe, running parallel to the z-axis (from −∞ to +∞), has three grounded metal sides, at y = 0, y = a, and x = 0. The fourth side, at x = b, is maintained at a specified potential $V_{0}(y)$

(a) Develop a general formula for the potential inside the pipe.
$$
\frac{ \partial^{2} V }{ \partial x^{2} } +\frac{ \partial^{2} V }{ \partial y^{2} } + \frac{ \partial^{2} V }{ \partial z^{2} } =0
$$
Boundary Conditions
$$
\begin{cases}
V = 0 \text{ when } y=0 \\
V = 0 \text{ when } y = a \\
V = 0 \text{ when } x = 0 \\
V = V_{0}(y) \text{ when } x = b \\
\end{cases}
$$
Should be constant along z axis, because the $x=b$ plane runs infinitely long along the z axis
$$
V(x,y,z) = X(x)Y(y)Z(z)
$$
$$
\frac{1}{X} \frac{ \partial^{2} X }{ \partial x^{2} } + \frac{1}{Y} \frac{ \partial^{2} Y }{ \partial y^{2} }  =0
$$
$$
C_{1} + C_{2} = 0 
$$
$$
\frac{1}{X} \frac{ \partial^{2} X }{ \partial x^{2} }  = C_{1}
$$
$$
\frac{1}{Y} \frac{ \partial^{2} Y }{ \partial Y^{2} } = C_{2}
$$
$$
X(x) = Ae^{kx}+Be^{-kx}
$$
$$
Y(y) = C\sin ky+ D \cos ky
$$
$$
V(x,y) = ( Ae^{kx}+Be^{-kx})(C\sin ky+ D \cos ky)
$$
Condition 1 $\implies$ $D =0$
Condition 3 $\implies$ 
(b) Find the potential explicitly, for the case $V_{0}(y) = V_{0}$





