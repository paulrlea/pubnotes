---
dg-publish: true
---
## Electrostatics in a nutshell
- Field lines start on positive, end on negative 
- Divergence of electric field is prop. to charge density
- Electrostatic field is gradient of scalar function (potential)
### General description of electrostatic field and potential
- Vector $\vec{r}'$  points to charge
- Vector $\vec{r}$ points to a test point
#### Boundary conditions
Perpendicular boundary charges are discontinuous. Parallel boundary conditions are continuous. 
- Charged hollow sphere example. 
	- Inside the sphere, $E=0$ 
		- Can be determined with Gauss's law
	- Outside the sphere, similar to point charge sitting at the origin
	- Discontinuity between inside and outside sphere

# Methods of solving [[Laplace's equation]]
Direct integration of the 1-d Laplace and Poisson equations

Hollow Sphere example: 
Given a hollow sphere with total charge $Q$
This gives us $\sigma = \frac{Q}{4\pi R^{2}}$
Find potential by solving [[Laplace's equation]]
$$
\vec{\nabla} ^{2} V = 0
$$
We will use spherical coordinates. 
Need to find Laplacian operator for spherical coordinates from the textbook
$$
\frac{1}{r^{2}} \frac{\partial}{\partial r}\left(  r^{2} \frac{\partial V}{\partial r} \right) + \frac{1}{r^{2} \sin \theta} \frac{\partial}{\partial\theta} \left( \sin\theta  \frac{\partial v}{\partial \theta} \right) + \frac{1}{r^{2}\sin ^{2}\theta} \frac{\partial^{2}V}{\partial \phi^{2}} = 0
$$
Potential is equal around the sphere in both azimuthal and polar angles
$$
\frac{\partial V}{\partial\theta} = 0,  \ \frac{\partial V}{\partial \phi} =0  
$$
$$
\frac{1}{r^{2}} \frac{\partial}{\partial r}\left( r^{2} \frac{\partial V}{\partial r} \right)= 0 
$$
$$
\frac{\partial}{\partial r} \left( r^{2} \frac{\partial V}{\partial r} \right)= 0 \implies r^{2} \frac{\partial V}{\partial r} = c_{1}
$$
$$
\implies \frac{\partial V}{\partial r} = \frac{c_{1}}{r^{2}} \implies V = \int \frac{c_{1}}{r^{2}} \, dr  = -\frac{c_{1}}{r} + c_{2}
$$We have 2 integration constants, $c_{1} \text{ and } c_{2}$. These are given by boundary conditions. 

$$
V_{in} =(r=R) = V_{out} (r=R)
$$
$$
-\frac{c_{1}}{R} + c_{2}= \frac{1}{4\pi\epsilon_{0}} \frac{Q}{R} + c_{2}
$$
$$
c_{2} = 0, V_{in}(t) =\frac{Q}{4\pi\epsilon_{0}R} = \text{ constant}
$$
Inside: 
$$
\vec{E}_{in} = -\vec{\nabla}V = 0 
$$

TLDR: If the problem is reduced to a 1-D problem, it can be solved using direct integration. 

You can check (at least for the hollow sphere) using [[Gauss' Law]].

$$
\vec{E} = -\vec{\nabla}V
$$
If the field $\vec{E}$  is 0, then the potential has to be **constant** (inside of hollow sphere). Can be solved for with: 
$$
V_{in} = const. = \frac{Q}{4\pi \epsilon_{0}R}
$$
The potential outside the hollow sphere is 
$$
V_{out} = \frac{1}{4\pi\epsilon_{0}} \frac{Q}{r}
$$
You can prove this with laplace's equation. They agree!
Boundary conditions is therefore as follows: 
$$
V_{in} = V_{out} ; \ \ r=R
$$
# Methods of solving [[Poisson's Equation]]
Start with general methods of solving for the electric potential: 
$$
V(\vec{r}) = \int _{V'} \frac{\rho(\vec{r})1}{\mathscr{r}} \, dV'
$$
$$
\vec{\nabla}^{2}_{\vec{r}} V(\vec{r}) = -\frac{\rho}{\epsilon_{0}} \implies \nabla^{2}_{r} V(\vec{r}) = \frac{1}{4\pi\epsilon_{0}} \int \rho(\vec{r})\vec{\nabla}^{2} \frac{1}{|\vec{r}- \vec{r}'|} \, dV' 
$$
Recall Homework 1, question 13
$$
-\vec{\nabla} \frac{1}{|\vec{r}-\vec{r}'|} = \frac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^{3}}
$$
$$
\vec{\nabla}_{\vec{r}}\left( \vec{\nabla}_{\vec{r}} \frac{1}{\vec{r} -\vec{r}'} \right)
$$
$$
\vec{\nabla} _{\vec{r}} \left(  - \frac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|} \right)
$$
Use Delta function
$$
4\pi\delta(\vec{r}-\vec{r}')
$$
### General comments on Laplace and Poisson 
Solving the Laplace and Poisson equations is solving a 2nd order diffeq
2nd order diffeq's are elliptic differential equations and are unique
Trust the math
All extrema in Laplace equation occurs at the boundary
This makes it unique

## In class problems 
3.3 
 Find the general solution to Laplace’s equation in spherical coordinates, for the case where V depends only on r. Do the same for cylindrical coordinates, assuming V depends only on s.
Spherical case (see above)
$$
-\frac{c_{1}}{R} + c_{2}
$$
Cylindrical case
$$
\frac{1}{r} \frac{\partial}{\partial r}\left(r \frac{\partial V}{\partial r}\right) + \frac{1}{r^2} \frac{\partial^2 V}{\partial \theta^2} + \frac{\partial^2 V}{\partial z^2} = 0
$$
$$
\frac{d^{2}V}{d\theta^{2}} = 0, \ \frac{d^{2}V}{dz^{2}} =0
$$
$$
\frac{1}{r} \frac{d}{dr}\left( r \frac{dV}{dr} \right) 
$$
$$
r \frac{dV}{dr} = c_{1}
$$
$$
\frac{dV}{dr} = \frac{c_{1}}{r}
$$
$$
dV = \frac{c_{1}}{r}dr
$$
$$
V = \int \frac{c_{1}}{r} \, dr
$$
$$
V = c_{1}\ln(r) + c_{2}
$$
2.53
a. 
[[Poisson's Equation]]
$$
\vec{\nabla}^{2} V = -\frac{\rho}{\epsilon_{0}}
$$
$$
\nabla^2 V = \frac{\partial^2 V}{\partial x^2} + \frac{\partial^2 V}{\partial y^2} + \frac{\partial^2 V}{\partial z^2} = \frac{\rho}{\epsilon_{0}}
$$
$$
-\frac{\rho}{\epsilon_{0}} = \frac{\partial^2 V}{\partial x^2}
$$

b. 
$$
T=qV = \frac{1}{2} mv^{2}
$$
$$
\sqrt{ \frac{2qV(x)}{m}}=v
$$
c. 
$$
I = \rho v
$$
$$
\frac{I}{\rho} = v
$$
d. 
$$
-\frac{\rho}{\epsilon_{0}} = \frac{\partial^2 V}{\partial x^2}
$$
$$
\sqrt{ \frac{2qV(x)}{m}}=v = \frac{aI}{\rho}
$$
$$
\frac{aI\sqrt{ \frac{2qV(x)}{m}}}{v}=\rho
$$
$$
-\frac{aI\sqrt{ \frac{2qV(x)}{m}}}{v\epsilon_{0}} =  \frac{\partial^2 V}{\partial x^2}
$$
$$
\beta \sqrt{ V(x) } = \frac{\partial^2 V}{\partial x^2}
$$
$$
\beta V^{1/2} =\frac{\partial^2 V}{\partial x^2}
$$













