---
dg-publish: true
---
## Image charges
- Useful for modeling electric potentials in situations where it can be simplified to a point/line charge and a conducting plane/sphere
- The boundary condition is the surface of the sphere/plane 
### Solving Poisson's equation with image charges
- This is an empirical approach based on the basic facts of a conductor
	Field lines are perpendicular at the surface of a conductor
	Using an imaginary charge behind the surface of the conductor we can solve for the potential behind the surface
	
- This method requires the potential from a point charge:
	$$
	V=\frac{1}{4\pi\epsilon_{0}} \frac{q}{r}
	$$
	and a line charge

### Uniqueness theorem
- If a function fulfills Poisson's equation, and assume the correct values at the boundaries, then that is the unique solution to the differential equation.


$$
V(x,y,z) = \frac{1}{4\pi\epsilon_{0}} \left[ \frac{9}{[x^{2}+y^{2}+(z-d)^{2}]^{1/2}}-\frac{9}{[x^{2}+y^{2}+(z+d)^{2}]^{1/2}} \right]
$$
$$
V(x,y,z=0) =0
$$
$$
V(x,y,z) \to 0 
$$
Where 
$$
x^{2}+y^{2}+z^{2} \gg d^{2}
$$
The uniqueness theorem allows the method of images to work, because by obeying the same boundary principles the solution to Poisson's equation is valid for both the real case and imaginary case

Example: 
$$
v(\vec{x}) = \frac{1}{4\pi\epsilon_{0}} \left(  \frac{q}{|\vec{x}-\vec{x}'|} - \frac{q'}{|\vec{x}-\vec{x}''|} \right)
$$
$$
\vec{n}' = \frac{\vec{x}'}{x}, \ \vec{n} = \frac{\vec{x}}{x}
$$
$$
\vec{n}'' -\vec{n}', \ \vec{x}'' =\vec{n}'x''
$$
$$
V(\vec{x}) = \frac{1}{4\pi\epsilon_{0}} \left( \frac{q}{|x\vec{n}-\vec{x}'\vec{n}'|} - \frac{q}{|x\vec{n} - x''\vec{n}'} \right)
$$
$$
V(\vec{x} = \frac{1}{4\pi\epsilon_{0}} \left( \frac{1}{x} \frac{q}{|\vec{n} - \frac{\vec{x}}{x}\vec{n}'|}-\frac{q}{x''| \frac{x}{x''}\vec{n} -\vec{n}'|} \right)
$$
$$
V(\mid \vec{x}\mid = R) = 0
$$
$$
\frac{q}{R} = \frac{q'}{x''}
$$
### In class assignment
Problems #'s 3.7, 3.10, 3.11
3.7
$$
\mathbf{F} = q\mathbf{E}
$$
$$
V(z) = \frac{1}{4\pi\epsilon_{0}}\left[ -\frac{q}{3d+z} + \frac{2q}{d+z} -\frac{2q}{z-d} \right]
$$
$$
E = -\nabla V = -k q\left( \frac{2}{(d-z)^{2}}-\frac{2}{(d+z)^{2}}+\frac{1}{(3d+z)^{2}} \right)\hat{\mathbf{z}}
$$
$$
E(3d) = -kq\left( \frac{2}{(d-3d)^{2}} - \frac{2}{(d+3d)^{2}} +\frac{1}{(3d+3d)^{2}} \right)\hat{\mathbf{z}}
$$
$$
E(3d) = -kq\left( \frac{2}{4d^{2}}-\frac{2}{16d^{2}}+\frac{1}{36d^{2}} \right)\hat{\mathbf{z}}
$$
$$
F(3d) =- \frac{q^{2}}{4\pi\epsilon_{0}} \frac{29}{72x^{2}}\hat{\mathbf{z}}
$$
3.10
a. Potential from a line charge mirrored 
$$
V(r)=\frac{\lambda}{2\pi\epsilon_{0}} \ln r
$$
$$
V(x,y,z) = \frac{\lambda}{2\pi\epsilon_{0}} \left[ \ln\left( {\sqrt{ x^{2} + y^{2}  + (z-d) ^{2}}} \right) -\ln\left( {\sqrt{ x^{2}+y^{2}+(z+d)^{2} }} \right) \right]
$$
b. Find the charge density
$$
V(x,y,z) = \frac{\lambda}{2\pi\epsilon_{0}} \ln \left( \frac{\sqrt{ x^{2} + y^{2}  + (z-d) ^{2}}}{\sqrt{ x^{2} + y^{2}  + (z+d) ^{2}}} \right)
$$
$$
\sigma = -\epsilon_{0} \frac{ \partial V }{ \partial z } 
$$
$$
\sigma = -\frac{\lambda}{2\pi} (\dfrac{z-d}{\left(z-d\right)^2+y^2+x^2} - \dfrac{z+d}{\left(z+d\right)^2+y^2+x^2})
$$






