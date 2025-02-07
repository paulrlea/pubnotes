---
dg-publish: true
---
# Coulomb's Law
- The force on a point charge $Q$ from another point charge $q$ at *rest* at a distance $\mathcal{r}$ away is given by [[Coulomb's Law]]
$$
F= \frac{1}{4\pi \epsilon_{0}} \frac{qQ}{r^{2}}\hat{r}
$$
- $e_{0}$ is the permittivity of free space, $\epsilon_{0}=8.85E-12$
# The Electric Field
- Given several point charges the total force on another point charge is the summation of forces from the individual point charges
$$
\mathbf{F} = \mathbf{F}_{1} + \mathbf{F}_{2} + \dots =\frac{1}{4\pi\epsilon_{0}}\left( \frac{q_{1}Q}{r^{2}_{1}}\hat{r_{1}} +  \frac{q_{1}Q}{r^{2}_{2}}\hat{r_{2}}  + \dots\right)
$$
- This sucks. Lets use the electric field instead. 
- We define the electric field as:
$$
\mathbf{E(r)} = \frac{1}{4\pi\epsilon_{0}} \sum_{i=1}^{n} \frac{q_{i}}{r^{2}_{i}} \hat{r}_{i}
$$
- And the force from the electric field on a point charge Q is given by 
$$
\mathbf{F} = Q \mathbf{E}
$$
- The electric field is a function of position. 
- It is a vector quantity. 
# Continuous Charge Distributions
- Generalizing electric field to a continuous distribution over a region
$$
\mathbf{E(r)}=\frac{1}{4\pi\epsilon_{0}}\int \frac{1}{r^{2}}dq 
$$
- Common forms include line charges, surfaces charges, and volume charges
- Volume charge distribution is also sometimes referred to as Coulomb's law. 
$$
\mathbf{E(r)} = \frac{1}{4\pi\epsilon_{0}} \int\frac{\rho(\mathbf{r^{\prime}})}{r^{2}}\hat{r} \, d\tau^{\prime} 
$$
# The Divergence of $\mathbf{E}$
- Calculating the divergence of $\mathbf{E}$ from $\mathbf{E(r)} = \frac{1}{4\pi\epsilon_{0}} \int\frac{\rho(\mathbf{r^{\prime}})}{r^{2}}\hat{r} \, d\tau^{\prime}$ gives us the following
$$
\mathbf{\nabla \cdot E} = \frac{1}{4\pi\epsilon_{0}} \int \nabla \cdot \left( \frac{\hat{r}}{r^{2}} \right) \rho(r ^{\prime}) d\tau^{\prime} 
$$
- The generic solution of a vector field is given by
$$
\nabla \cdot\left( \frac{\hat{r}}{r^{2}} \right) = 4\pi\delta^{3}(r)
$$
- Where $\delta$ is the delta function which is 0 everywhere except for 0, where its $\infty$
- This can derive the differential form of Gauss's law
$$
\nabla \cdot \mathbf{E} = \frac{1}{\epsilon_{0}}\rho(r)
$$
- To convert from the differential form to the integral form we can use the following
$$
	\int _{v}\nabla \cdot \mathbf{E} d\tau = \oint_{\mathcal{S}} \mathbf{E} \cdot d\mathbf{a} = \frac{1}{\epsilon_{0}} \int_{\mathcal{S}} \rho d\tau = \frac{1}{\epsilon_{0}}Q_{enc}
$$
# The Curl of E 
- The integral around a closed path is zero
$$
\oint \mathbf{E} \cdot d \mathbf{l} = 0
$$

- Applying Stoke's theorem 
$$
\nabla \times \mathbf{E} = 0
$$
- These two equations hold true for any static charge distribution whatever.  

# Lecture 1/11 Electrostatic fields
- Maxwell's equations in differential/integral forms
	- Maxwells Equations in Integral form
		- [[Gauss' Law]]
		- [[Gauss' Law for magnetic field ]]
		- [[@SchoolFall 2023/School/Physics/Physics 1250/Concepts/Faraday's law]]
		- [[Ampere-Maxwell Law]]
- Fundamental definitions of [[Electrostatic Fields]]
- Generalized description of electric field of point charges and charge distributions
- Useful math 

#### Why do we bother with differential forms?
- Derivatives are easy
- Integrals are hard
- Makes some computations possible 

### Vector Calculus: 
- [[Divergence Theorem]]
- [[Stokes Theorem]] aka Curl Theorem
- These have been proven correct. 

#### Maxwell Equations converted from Integral to Differential Form
$$
\oint \vec{E} \cdot d\vec{A} = \frac{Q_{enc}}{\epsilon_{0}} = \frac{1}{\epsilon_{0}}\int \rho \, dV
$$
Use Divergence Theory to convert Surface integral to a volume integral over the divergence:
$$
\int \vec{\nabla} \cdot \vec{E} \, dV =\frac{1}{\epsilon_{0}}\int \rho \, dv
$$
$$
\int \left[ \vec{\nabla} \cdot \vec{E} - \frac{\rho}{\epsilon_{0}} \right] \, dV = 0
$$
Therefore, to make the R.H.S = 0, the divergence of the electric field has to be equal to $\frac{\rho}{\epsilon_{0}}$
$$
\vec{\nabla} \cdot \vec{E} - \frac{\rho}{\epsilon_{0}} = 0  \implies \vec{\nabla}\cdot \vec{E}  = \frac{\rho}{\epsilon_{0}}
$$
For the Magnetic Gauss law
$$
\oint \vec{B} \cdot d\vec{A}=0=\int (\vec{\nabla} \cdot \vec{B}) \ dV \implies \vec{\nabla} \cdot \vec{B} = 0 
$$
For Faraday's Law using [[Stokes Theorem]]
$$
\oint \vec{E} \cdot d\vec{s} = -\frac{d\Phi_{B}}{dt} = \frac{d}{dt}\int \vec{B} \cdot d\vec{A} 
$$
$$
\oint \vec{E} \cdot d\vec{s} = \int (\vec{\nabla} \times \vec{E} )\cdot d\vec{A} = -\frac{d}{dt} \int \vec{B} \cdot d\vec{A}  
$$
$$
\int (\vec{\nabla} \times \vec{E} + \frac{d\vec{B}}{dt} )\, d\vec{A} =0
$$
$$
\therefore \vec{\nabla} \times \vec{E} = -\frac{\partial\vec{B}}{\partial t}
$$
For Ampere-Maxwell Law using [[Stokes Theorem]]
$$
\oint \vec{B} \cdot d\vec{s}=\int (\vec{\nabla} \times \vec{B}) \cdot\, d\vec{A} =  \mu_{0}\int \vec{j} \ d\vec{A} + \mu_{0}\epsilon_{0} \frac{d}{dt} \int \vec{E} \cdot \, d\vec{A}
$$
$$
\int \left( \vec{\nabla} \times \vec{B} - \mu_{0}\vec{j}-\mu_{0}\epsilon_{0} \frac{d\vec{E}}{dt}  \right) \, d\vec{A} = 0 
$$
$$
\therefore \vec{\nabla} \times \vec{B}  =  \mu_{0}\vec{j} + \mu_{0}\epsilon_{0} \frac{d\vec{E}}{dt}
$$



### Electrodynamics vs Electrostatics and Magnetostatics
- Electrodynamics
	- Utilizes coupled differential equations
- Electrostatics and Magnetostatics
	- Nothing depends on time. (static)
	- The time derivative is 0
	$$
			  \nabla \times \mathbf{E} = 0
			  $$
	- Definition of electrostatic fields and potentials
	- Gauss' law and Faraday's law for static electric fields in differential form are the mathematical description of electric field lines
Gauss's Law in Differential form
$$
\vec{\nabla} \cdot \vec{E} = \frac{\rho}{\epsilon_{0}}=constant
$$
- Field lines go outwards for positive charge, inwards for negative
- In an electrostatic field, 
$$
\vec{\nabla} \times \vec{E}=0 
$$
- Electrostatic fields do not form closed loop field lines
- The curl of the magnetic field  $\neq$ 0
- An electrodynamic field does not follow this rule

### Notes on charge, force and field 
- Coulomb force attracts opposite forces and separates like charges
	- This is also one of the fundamental forces of nature
- Why use electric field?
	- Dont have to work with many particles
	- Given by $\vec{F} = q\vec{E}$

### General and Special cases for point charge electric field
Special case where the point charge is the origin
$$
\vec{E}(\vec{r}) = \frac{1}{4\pi\epsilon_{0}} \frac{q}{r^{2}}\hat{r} = \frac{1}{4\pi\epsilon_{0}} \frac{q}{r^{3}} \hat{r}
 $$
 General case for all points
 $$
\vec{E}(\vec{r})= \frac{1}{4\pi\epsilon_{0}} \frac{q}{|\vec{r} - \vec{r}'|^{2} } = \frac{q}{4\pi\epsilon_{0}} \vec{r} - \frac{\mathrm{\vec{R}^{\prime}}}{\vec{r}}
$$
...

### Electric Charge Distribution
- Use electric charge density to make the Gauss' integral solvable

## Useful Math Tricks
$$
\frac{\vec{r} - \vec{r} ^{\prime}}{|\vec{r}-\vec{r}^{^{prime}}|} = -\nabla
$$

DELTA FUNCTION 
0 for all values where x $\neq$ 0
$\infty$ for x=0
$$
\frac{dF}{dx} =0 
$$
because the slope has no slope
Aka Derivative of step function


### Example with divergence
$$
\vec{\nabla} \cdot \vec{E} (\vec{r})
$$
$$
\vec{\nabla})_{\vec{r}} \vec{E} = \vec{\nabla}_{\vec{r}}\left( \frac{1}{4\pi\epsilon_{0}}\int  (\rho(\vec{F})) \frac{\vec{\tau}-\vec{\tau}^{\prime}}{|\vec{\tau}-\vec{\tau}^{\prime}|^{3}} dV^{\prime}\right)
$$
$$
k=\frac{1}{4\pi\epsilon_{0}}
$$
$$
k \int_{V^{\prime}} \rho(F^{\prime})(\nabla)
$$
finish later 

### Example with Curl
$$
\vec{E}(\vec{\tau}) = k\int _{v^{\prime}}\rho(F^{\prime}) \frac{\vec{\tau}^{\prime}-\vec{\tau}^{\prime}}{|\vec{\tau}^{\prime}-\vec{\tau}^{\prime}|^{3}} \, dv^{\prime}
$$
$$
\vec{E}(\vec{\tau}) = k \int \rho(\vec{\tau}^{\prime}) \left[ -\vec{\nabla}_{F} \frac{1}{|\vec{r}-\vec{r}^{\prime}|} \right] \, dv^{\prime}
$$
$$
\vec{\nabla}_{F} \times \vec{E}(\vec{r})  = k \int \rho(\vec{r}^{\prime}) \left[ \vec{\nabla}_{F} \times\left( -\vec{\nabla}_{\vec{r}} \frac{1}{|\vec{r} - \vec{r}^{\prime}|} \right) \right] \, dv =0 
$$
#### Self-Worked Problems
Find the electric field a distance z above the center of a circular loop of radius r (Fig. 2.9) that carries a uniform line charge λ.
- We can find the electric field in the z direction from many infinitesimal segments of the loop. 
$$
d = \sqrt{ z^{2} + r^{2} } 
$$
$$
\mathbf{E(r)}=\frac{1}{4\pi\epsilon_{0}}\int _{0} ^{2\pi} \frac{\lambda r}{\left[ z^{2} + \frac{d^{2}}{4} \right]^{3/2}}d\theta
$$
$$
E = \frac{16\pi q\lambda r}{[d^{2} + 4z^{2}]^{3/2}}
$$

