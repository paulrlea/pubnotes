---
dg-publish: true
---
-  A cycloid curve is a curve that is the path traced by a circle rolling. 
- 3Blue1Brown video on this is good 
## Derivation of cycloid curve from calculus of variations and [[Euler-Lagrange Equation]]


The speed of the particle 
$$
V = \frac{ds}{dt} \to dt=\frac{ds}{V}
$$
The total time is the integral over $dt$
$$
\tau = \int\limits_{A}^{B} \frac{ds}{V} 
$$
What is $ds$
$$
ds = \sqrt{ dx^{2} + dy^{2} } = dx\sqrt{ 1 + \left( \frac{dy}{dx} \right)^{2}} =dx\sqrt{ 1+y'^{2} }
$$
$$
V  \to T =\frac{1}{2mv^{2}}
$$
$$
u =- mgx
$$
> $T+U$ is conserved because gravity is conservative

$$
\frac{1}{2}mV^{2}-mgx = \text{constant} = 0
$$
$$
\frac{1}{2}mV^{2} =mgx \implies \frac{1}{2v^{2}}= gx
$$
$$
V = \sqrt{ 2gx }
$$
$$
\tau  = \int\limits_{A}^{B} \frac{ds}{V} = \int\limits_{0}^{x_{B}} \frac{\sqrt{ 1 +y'^{2} }dx}{\sqrt{ 2gx }} \, dx  
$$
Compare to $J=\int F(y(x,y'(x),x)) \, dx$
$$
F = \sqrt{ \frac{1+y'^{2}}{2gx} }
$$
Use [[Euler-Lagrange Equation]]
$$
\frac{d}{dx}\frac{ \partial F }{ \partial y' } -\frac{ \partial F }{ \partial y }  = 0
$$
$$
\frac{ \partial F }{ \partial y }  = 0 ; \ \ \frac{d}{dx}\frac{ \partial F }{ \partial y' }  = 0
$$
$$
\frac{ \partial F }{ \partial y' }  \text{ must be constant}
$$
$$
\frac{ \partial F }{ \partial y' } = \frac{d}{dy'}\left( \frac{1+y'^{2}}{2gx} \right)=\frac{1}{\sqrt{ 2g } } \frac{d}{dy'} \left( \frac{1+y'^{2}}{x} \right)^{1/2} 
$$
$$
= \frac{1}{2}\left( \frac{1+y'^{2}}{x} \right)^{-1/2}\left( \frac{2y'}{x} \right)
$$
$$
=\left( \frac{x}{1+y'^{2}} \right)^{1/2}\left( \frac{y'}{x} \right) = \text{constant}
$$
Square both sides
$$
\frac{x}{1+y'^{2}} \frac{y'^{2}}{x^{2}} = \text{constant}^{2} = \frac{1}{2a}
$$
$$
2ay'^{2} = (1+y'^{2})x = x+xy^{2}
$$$$
2ay'^{2}-xy'^{2} = x
$$
$$
y^{2}(2a-x) = x 
$$
$$
y'^{2} = \frac{x}{2a-x} \left( \frac{x}{x} \right) = \frac{x^{2}}{2ax-x^{2}}
$$
$$
\frac{dy}{dx} = \frac{x}{\sqrt{ 2ax-x^{2} }}
$$
$$
	\int  \, dy  = \int \frac{x}{\sqrt{ 2ax-x^{2} }} \, dx 
$$
$$
x = a(1-\cos(\theta)) ; \ dx = a\sin \theta d\theta
$$
$$
	y (x) = \int \frac{a(1-\cos \theta)a\sin\theta}{\sqrt{ 2a^{2}(1-\cos\theta)-a^{2}(1-\cos\theta)^{2} }} \, d\theta
$$
Denominator becomes
$$
2a^{2} - 2a^{2}\cos\theta -a^{2} + 2a^{2}\cos\theta-a^{2}\cos ^{2}\theta 
$$
$$
a^{2} - a^{2}\cos ^{2}\theta 
$$
$$
y(x) = \int \frac{a^{2}\sin\theta(1-\cos\theta)}{\sqrt{ a^{2}-a^{2}\cos \theta }} \, d\theta= \int a(1-\cos(\theta)) \, d\theta
$$
$$
= y(x) = a(\theta-\sin\theta)+ \text{constant}
$$
$$
x=a(1-\cos(\theta))
$$
>This is the path of a cycloid curve!
