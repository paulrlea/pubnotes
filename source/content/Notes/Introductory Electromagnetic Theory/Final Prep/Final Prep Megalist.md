# Lecture 1
Coulombs Law
$$
\vec{F}_{1 \ on \ 2} = \frac{1}{4\pi\epsilon_{0}} \frac{q_{1}q_{2}}{r_{12}} ^{2} \hat{r}_{12}
$$
- Relates Force from 2 point charges that are at rest in a vacuum. 
- Force is inversely proportional to distance between charges squared

Vector Review
- The direction of any force can be modeled with a a vector, you can add vectors by adding their components. 
Electric Field
- The electric field is defined as
$$
\vec{E} = \frac{\vec{F}}{q_{0}}
$$
- The direction of the electric field is the direction of the force applied to a positive particle within it. 
- The electric field at a point caused by a point charge is given by
$$
\vec{E}_{1} = k \frac{q_{1}}{r^{2}} \hat{r}_{12}
$$
- Electric field is useful because given the electric field at a region in space, we will know what happens to any particle placed within that region. 
Electric Field Lines: The Faraday Representation
- Electric field lines show direction of electric field at any point
- Line length is proportional to field strength
- Lines go from positive to negative
Charge Transfer
- Charge on insulator remains in position
- Charges on conductor move around to make field 0 within conductor
- A neutral conductor will always be attracted to sources of field

## Lecture 2
Lecture 2: $$\rho = dq/dv$$ Charge density where dq is the distribution of the charge over volume dv Distribution in a thin sheet: $$dq(x,y) = \sigma(x,y)dxdy$$ where $$\sigma$$ is the surface charge distribution Distribution along a thin line: $$\lambda(x)=\int \int\rho(x,y,z) , dy , dz \implies dq(x)=\lambda(x)dx $$ where $$\lambda$$ is the line charge distribution

# Lecture 3
Gauss' Law
- Qualitatively, Gauss' law gives us the electric field in a region from its source. This is very useful. 
- For us to understand Gauss' law, we must first define Flux. 
	- Flux is the integral of the field over a surface, pointing in the direction of the vector normal to the surface. Normal == Perpendicular. 
	- In simpler terms, its how much field is passing through a surface. 
	- For an example, the flux of a vector field $\vec{E}$ over a surface $s$ with normal vector $\hat{n}$ is given by 
$$
\Phi= \int _{s}\vec{E} \cdot \, d\vec{a} = \int \vec{E} \cdot \hat{n}da  
$$
- Now that we've defined flux, we can define Gauss' law as the following. 
$$
\oint \vec{E} \cdot d\vec{a} = \frac{q_{enc}}{\epsilon_{0}} = \frac{1}{\epsilon_{0}} \int _{v} \rho dv
$$
- In simpler terms, this states that the total flux through any closed surface is equal to the charge enclosed by this surface, which is in turn equal to the integral of the charge density through the volume enclosed by the surface.
# Lecture 4
$$ \Delta U_{elec}=-q_{0}\int_{A}^B E\cdot dl , dx $$Motion of charge q_0 in a field, the electric potential is the work per unit charge done in moving a charge from point A to B

$$
U = \frac{q_{1}q_{2}}{4\pi\epsilon_{0}r_{12}}+\frac{q_{2}q_{3}}{4\pi\epsilon_{0}r_{23}}\frac{q_{1}q_{3}}{4\pi\epsilon_{0}r_{13}} 
$$ $$ \Delta V=\frac{\Delta U}{q_{0}}=-\int _{i}^f E\cdot dl, dx $$Change of electric potential between two points defined as change of PE of a charge when moved between two points The gradient 
$$ \nabla = \left( \frac{\hat{i}\partial}{\partial x}+\hat{\frac{j\partial}{\partial y}}+\hat{\frac{k\partial}{\partial z}} \right) $$ $$ E = -\left( \hat{i}\frac{\partial V}{\partial x}+\frac{\hat{j}\partial}{\partial y} +\hat{k} \frac{\partial V}{\partial z} \right) $$

# Lecture 5
- Vector Calculus
- There are 4 major operators that are covered in this class
- The gradient:
	- This was covered above, but as a refresher, 
$$ 
\nabla = \left( \frac{\hat{i}\partial}{\partial x}+\hat{\frac{j\partial}{\partial y}}+\hat{\frac{k\partial}{\partial z}} \right)
$$
- The divergence
$$
\vec{\nabla} \cdot \vec{E} = \frac{\partial E_{x}}{\partial x} + \frac{\partial E_{y}}{\partial y}+ \frac{\partial E_{z}}{\partial z}
$$
- The Laplacian
$$
\vec{\nabla} \cdot \vec{\nabla}V = \frac{\partial^{2}V}{\partial x^{2}}  +\frac{\partial^{2}V}{\partial y^{2}}+\frac{\partial^{2}V}{\partial z^{2}}
$$
- The Curl
$$
\vec{\nabla} \times \vec{E} = (\frac{\partial E_{z}}{\partial y} -  \frac{\partial E_{y}}{\partial z})\hat{i} + (\frac{\partial E_{x}}{\partial z} -  \frac{\partial E_{z}}{\partial x})\hat{j} + (\frac{\partial E_{y}}{\partial x} -  \frac{\partial E_{x}}{\partial y})\hat{k}
$$

- Divergence at a point $p$ of the field $\vec{E}$ is the flux outwards through the surfaces that enclose p. 
- Using this, we can solve Gauss' law in a differential form 
$$
\vec{\nabla} \cdot \vec{E} = - \frac{\rho}{\epsilon_{0}}
$$

# Lecture 6
Step 1: Find an easier problem with same BCs Place an imaginary charge -q a distance h Step 2: Calculate potential $$ V=\frac{kq}{(x^2+y^2+(z-h)^2)^{1/2}}-\frac{kq}{(x^2+y^2+(z+h)^2)^{1/2}} $$ Step 3: Find the field using the gradient $$ E = -\nabla V = -\partial \frac{V}{\partial x}\hat{i}-\partial \frac{V}{\partial y}\hat{j}-\partial \frac{V}{\partial z}\hat{k} $$ $$ E_{x}=-\frac{kqx}{(x^2+y^2+(z-h)^2)^{3/2}}+\frac{kqx}{(x^2+y^2+(z+h)^2)^{3/2}} $$ $$ E_{z}=-\frac{kq(z-h)}{(x^2+y^2+(z-h)^2)^{3/2}}+\frac{kq(z+h)}{(x^2+y^2+(z+h)^2)^{3/2}} $$ Step 4: Calculate the surface charge at $z = 0, E_x = E_y = 0$, the field is perpendicular to the equipotential surface 
$$ E_{z} | _{z=0} = -\frac{-qh}{(x^2+y^2+(-h)^2)^{3/2}}+\frac{qh}{(x^2+y^2+h^2)^{3/2}} = \frac{2qh}{(x^2+y^2+h^2)^{3/2}} = \frac{\sigma}{\epsilon_{0}} $$

# Lecture 7

- A Capacitor is a device that stores charge when a potential is applied. Capacitance is the measure of how much charge an object can store, defined below
$$
Q=C\Delta V
$$
- In the above, charge is denoted as Q, C is the capacitance (unit of farads), and $\Delta V$ is the difference in potential across the plates. C and $\Delta V$ are magnitudes ($\geq 0$)
- One Farad is $1 \frac{C}{V}$ very large capacitance, most lab capacitors are in the micro-farad range. 
- Capacitance can be described as the ratio of charge to potential
How to Calculate Capacitance?
- Find electric field between plates and charge Q
- Use electric field to find potential using
$$
\Delta V = V_{+} - V_{-} = \int ^{+}_{-} \vec{E} \cdot \, d\vec{l} 
$$
- Use capacitor formula
$$
C = \frac{Q}{\Delta V}
$$
Relevant Example- Parallel Plate Capacitor
Given 2 plates with spacing $d$ and area $A$, find capacitance. 
- First step is to find electric field between the plates using [[Gauss's law]]. 
$$
\oint \vec{E} \cdot d\vec{a} = \frac{Q_{enc}}{\epsilon_{0}}
$$
$$
\implies EA = \frac{Q}{\epsilon_{0}} \therefore E = \frac{\sigma}{\epsilon_{0}}
$$
Now to find the potential between the two plates
$$
\Delta V = \frac{Qd}{\epsilon A}
$$
Now we know potential and charge, we can calculate capacitance
$$
C=\frac{Q}{\Delta v} = \frac{\epsilon_{0}A}{d}
$$
As you see, capacitance only depends on geometry. 

Example 2: Spherical capacitor


