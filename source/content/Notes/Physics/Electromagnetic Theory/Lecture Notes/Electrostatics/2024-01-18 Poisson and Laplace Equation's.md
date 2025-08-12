---
dg-publish: true
---
# Poisson’s Equation and Laplace’s Equation
- Electric field can be written as the gradient of a scalar potential
$$
\mathbf{E} = -\nabla V
$$
- What about divergence and curl look like for V?
- The divergence of $\mathbf{E}$ is the Laplacian of $V$. Gauss's law states:
$$
\nabla^{2}V = -\frac{\rho}{\epsilon_{0}}
$$
- This is [[Poisson's Equation]]
- Where $\rho=0$ this reduces to [[Laplace's equation]]
$$
\nabla^{2}V= 0
$$
# The Potential of a Localized Charge Distribution
- We found $V$ in terms of $\mathbf{E}$, now find $\mathbf{E}$ from $V$
- Invert Poisson's Equation!
- For a point charge 
$$
V(r) = \frac{1}{4\pi\epsilon_{0}} \frac{q}{\mathscr{r}}
$$
- For a continuous distribution
$$
V(r) = \frac{1}{4\pi\epsilon_{0}} \int \frac{1}{\mathscr{r}} \, dq
$$
- For a volume charge
$$
V(\mathbf{r}) = \frac{1}{4\pi\epsilon_{0}} \int \frac{\rho(\mathbf{r}')}{\mathscr{r}} \, d\tau' 
$$
- Note this has no unit vector
- Line charge 
$$
	V = \frac{1}{4\pi\epsilon_{0}}\int \frac{\lambda(\mathbf{r'})}{\mathscr{r}} \, dl'
$$
- Surface charge
$$
V = \frac{1}{4\pi\epsilon 0} \int \frac{\sigma(\mathbf{r'})}{\mathscr{r}} \, da'
$$
# Boundary conditions
- Typically you have a source charge distribution, and have to calculate $\mathbf{E}$ from it
- Without symmetry, you have to calculate potential first
- Three fundamental quantities of electrostatics
	- $\rho$, volume charge density 
	- $\mathbf{E}$, electric charge 
	- $V$, potential
- Gauss's Law for a pillbox
$$
\oint_{\mathcal{S}} \mathbf{E}\cdot da =\frac{1}{\epsilon_{0}}Q_{enc} = \frac{1}{\epsilon_{0}}\sigma A
$$
- Where A is the surface area of the pillbox lid
![[Attachments/Pasted image 20240117204455.png]]
Cool diagram of how things interact 


# Lecture on Electric Potential
### Useful math
- The curl of the gradient of the scalar function is 0
$$
\vec{\nabla} \times (\vec{\nabla}F)=0
$$
- The cross product of the electric field is 0 for electrostatics 
$$
\vec{\nabla} \times \vec{E} = 0
$$
- [[Divergence Theorem]]
$$
\int (\vec{\nabla} \times \vec{E}) \, d\vec{A} = \oint\vec{E} \cdot d\vec{s}
$$



### Electric potential
- Electric potential function 
$$
\vec{E}(\vec{r}) = -\vec{\nabla}V(\vec{r})
$$
- Electric field is a physical concept, while potential is a mathematical one. 
- The electric potential function fulfills the electrostatic field condition
$$
\vec{\nabla} \times \vec{E} = \vec{\nabla}\times(-\vec{\nabla}V(\vec{r}))=0
$$
- Used for electrodynamics and magnetic
- We can use this to derive differential equations in electrodynamics!
$$
-\vec{\nabla}_{\vec{r}} \frac{1}{\vec{\mathscr{r}}} = \frac{\mathscr{r}}{\mathscr{r}^{3}}
$$
$$
\vec{E}(\vec{r}) = \frac{1}{4\pi \epsilon_{0}}\int\limits_{v'}^{} \frac{\rho \vec{r}'(\vec{\mathscr{r}})}{\vec{\mathscr{r}}^{3}} \, dV'
$$
$$
\vec{E}(\vec{r}) = \frac{1}{4\pi\epsilon_{0}} \int\limits_{V'} \rho(\vec{r}')\left( -\vec{\nabla}_{\vec{r}} \frac{1}{\vec{\mathscr{r}}} \right)  \, dV'
$$
$$
\vec{E}(\vec{r}) =-\vec{\nabla}_{\vec{r}}\left[ \frac{1}{4\pi\epsilon_{0}}\int\limits_{V'}^{} \frac{\rho(\vec{r}')}{\vec{\mathscr{r}}} \, dV'  \right]=-\vec{\nabla}F(\vec{r})
$$
General description of potential from electric charge density at r'
$$
V(\vec{r}) = \frac{1}{4\pi\epsilon_{0}} \int\limits_{V'}^{} \frac{\rho \vec{r}'}{\vec{\mathscr{r}}} \, dV' 
$$
- See cool triangle diagram above! This shows up there
Definition of electric potential from electric field
$$
\vec{\nabla} \times \vec{E} = 0 \therefore \oint \vec{E} \cdot d\vec{s} = 0 \to \int\limits_{\vec{r}_{a}}^{\vec{r}_{a}} \vec{E}\cdot d\vec{s} 
$$
$$
V(\vec{r}) = - \int\limits_{\vec{r}a}^{\vec{r}_{b}} \vec{E} \cdot  \, d\vec{s} = -[v(\vec{r}_{b})- v(\vec{r}_{a})]
$$
Electrostatic potential **energy** (not potential). These are different things!
$$
U=-\int\limits_{\vec{r}_{a}}^{\vec{r}_{b}} \vec{F}_{c} \, d\vec{s} = -\int\limits_{\vec{r}_{a}}^{\vec{r}_{b}} q\vec{E}\cdot \, d\vec{s} =  -q[v(\vec{r}_{b}-v(\vec{r}_{a}))] 
$$
To get potential energy, integrate over the electric fields

### Boundary Conditions
- Between materials with different electric properties
	- Ex. Plastic and metal, air and water
- Interface of materials with different electric properties
- Start with boundary between metal and vacuum

EX. Spherical Shell with surface charge density $\sigma = \frac{Q}{4\pi R^{2}}$
$$
\oint \vec{E} \cdot d\vec{A} = \frac{Q_{enc}}{\epsilon_{0}}
$$
$$
E(r) =  0 \ : \ r < R
$$
Electric field inside shell is 0 
$$
E(r) = \frac{1}{4\pi\epsilon_{0}} \frac{Q}{r^{2}} \ : \ r \geq R
$$
See graph of this: 
description: Electric field is 0 until point R, where it jumps to a maximum value and decays quadratically?

$$
E(r=R) - \frac{1}{4\pi\epsilon_{0}} \frac{Q}{R^{2}} = \frac{4\pi R^{2}\sigma}{4\pi\epsilon_{0}R^{2}} = \frac{\sigma}{\epsilon_{0}}
$$
For a metal surface (conducting surface) 
- the electric field at surface is always perpendicular to surface 
$$
E_{\perp} = \frac{\sigma}{\epsilon_{0}}
$$
On a sphere, the electric field is perpendicular to the surface at any point. The parallel component is 0
$$
E_{\parallel} = 0
$$
$$
E(r) =\frac{1}{4\pi\epsilon_{0}} \frac{Q}{r^{2}} = \frac{\sigma R^{2}}{\epsilon_{0}r^{2}}
$$
The electric potential inside the sphere is a constant
$$
\vec{E} = -\vec{\nabla}V \therefore V = \text{constant}
$$
$$
V=\frac{1}{4\pi\epsilon_{0}} \frac{Q}{r}
$$
Plot for electric potential: 
- inside the sphere it is constant, outside sphere decays at rate $\frac{1}{r}$
$$
V_{inside} = V_{outside} \ : \ R=r
$$
$$
\vec{\nabla}V = - \vec{E}
$$
The plot of the gradient of V
0 until the sphere boarder, then jumps up and decays 


#### Boundary conditions at electrically charged surfaces
Discontinuous:
$$
E_{\perp \text{outside}} - E_{\perp \text{inside}} = \frac{\sigma}{\epsilon_{0}} 
$$
$$
\vec{\nabla}V_{\text{outside}} - \vec{\nabla}V_{inside} \implies \frac{\sigma}{\epsilon_{0}}
$$
Continuous: 
see ppt 

#### Poisson's law and Laplace's equations for electric potential
$$
\vec{\nabla} \times \vec{E}  = 0 
$$
$$
\vec{\nabla} \cdot \vec{E} = \frac{\rho}{\epsilon_{0}}
$$
$$
\vec{E} = - \vec{\nabla}V
$$
$$
\vec{\nabla} \cdot \vec{E} = (\vec{\nabla} \cdot(-\vec{\nabla}V)) = -\vec{\nabla}^{2}V=\frac{\rho}{\epsilon_{0}}
$$
$$
\vec{\nabla}^{2}=\vec{\nabla} \cdot \vec{\nabla} = \frac{\partial^{2}}{\partial x^{2}}+\frac{\partial^{2}}{\partial y^{2}} + \frac{\partial^{2}}{\partial z^{2}}
$$
[[Poisson's Equation]]
[[Laplace's equation]]




### In class activities
Required Equations
2.30
$$
V(\mathbf{r}) = \frac{1}{4\pi\epsilon_{0}} \int \frac{\sigma}{\mathscr{r}} \, da' 
$$
2.26
$$
V(\mathbf{r}) = \frac{1}{4\pi\epsilon_{0}} \frac{q}{\mathscr{r}}
$$
For part a. (2 point charges)
$$
\mathscr{r}=\sqrt{ \left( \frac{d}{2} \right)^{2}+z^{2} }
$$
$$
V_{1} = \frac{1}{4\pi\epsilon_{0}} \frac{q}{\sqrt{ \left( \frac{d}{2} \right)^{2}+z^{2} }}
$$
$$
V_{\text{total}} = V_{1} + V_{2}
$$
$$
V_{\text{total}} = \frac{1}{4\pi\epsilon_{0}} \frac{2q}{\mathscr{r}}
$$
Taking the derivative wrt x cancels out, and wrt y gives the same result in Ex 2.1
For part b. 
$$
V(\mathbf{r}) = \frac{1}{4\pi\epsilon_{0}} \int \frac{1}{\mathscr{r}} \, dq 
$$
$$
V(\mathbf{r}) = k \int\limits_{-L}^{L} \frac{\lambda}{\sqrt{ \left( L\right)^{2}+z^{2} }} dL
$$
$$
V(r) = \lambda \ \text{arcsinh}\left( \frac{L}{z} \right)
$$
the derivative of this is equivalent to the result in Ex 2.2

For part c. Uniform surface charge
$$
V(\mathbf{r}) = k \int \frac{\sigma}{\mathscr{r}} \, da'
$$
$$
V(\mathbf{r})=k \int\limits ^{2\pi}_{0}\int\limits_{0}^{R} \frac{\sigma}{\sqrt{ r^{2} +z^{2}}} \, r dr d\theta \,
$$
$$
V(r) = k \int\limits_{0}^{2\pi} {\sigma}\left(\sqrt{z^2+R^2}-z\right) \, d\theta 
$$
$$
V(r)=k(2{\pi}{\sigma}\cdot\left(\sqrt{z^2+R^2}-z\right))
$$
$$
V(r) = \frac{2{\pi}{\sigma}\cdot\left(\sqrt{z^2+R^2}-z\right)}{4\pi\epsilon_{0}}
$$



