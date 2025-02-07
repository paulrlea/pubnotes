---
dg-publish: true
---
## Review
Introductory physics introduced the following:
- Sources of magnetic field (current)
- Magnetic/Lorentz force $\mathbf{F} = q \mathbf{v}\times \mathbf{B}$
- Ampere's law in integral form
- Biot-Savart law for line currents

Useful Relations: 
Straight line segment magnetic field
$$
B = \frac{\mu_{0}I}{2\pi r}
$$
At the center of a circular loop of radius R:
$$
B = \frac{\mu_{0}I}{2R}
$$
## New material: 
- Magnetostatic Maxwell Equations in differential form
- Biot Savart law in general form 
- Magnetic vector potentials

### Differential form of Magnetostatic equations
$$
	\nabla \cdot \mathbf{B} =0
$$
$$
\nabla \times \mathbf{B }= \mu_{0}\mathbf{J}
$$
- Looking at Maxwell's equations in integral form we can derive the above equations using [[Divergence Theorem]] and [[Stokes Theorem]], similarly to electrostatics.

The derivations are below: 
$$
\oint \vec{B} \cdot d\vec{A} = \int (\vec{\nabla} \cdot \vec{B}) \, dV \to \vec{\nabla} \cdot \vec{B} = 0 
$$
$$
\oint \vec{B} \cdot d\vec{s} = \int (\vec{\nabla} \times \vec{B}) \cdot\, d\vec{A} =  \mu_{0}i_\text{enc} = \mu_{0} \int \vec{j} \cdot \, d\vec{A} 
$$
$$
	\int (\vec{\nabla} \times \vec{B} - \mu_{0} \vec{j}) \, d\vec{A} = 0 \to \vec{\nabla} \times \vec{B} = \mu_{0}\vec{j}
$$
### Continuity Equation
Describes the behavior of current flowing through a volume. 
$$
\vec{\nabla} \cdot \vec{j} = - \frac{ \partial s }{ \partial t } 
$$
### General Biot-Savart Law
$$
\vec{\mathbf{B}} (\vec{r}) = \frac{\mu_{0}}{4\pi} \int \frac{\vec{j}(\vec{r}')\times|\vec{r}-\vec{r}'}{|\vec{r} - \vec{r}'|^{2}} \, dV' 
$$
### Electric Current Densities
Total current is integral of current density integrated over surface
$$
	\vec{j} \implies I =\int \vec{j} \cdot \, d\vec{A}
$$

### Magnetic Vector Potential
The magnetic field can always be obtained as the curl of a vector function that we call the magnetic vector potential
$$
\mathbf{\vec{B}} = \vec{\nabla} \times \vec{A} 
$$
Where $\vec{A}$ is the magnetic vector potential

$$
\vec{\nabla} \cdot \vec{B}=0  \implies \vec{\nabla} \cdot ( \vec{\nabla} \times \vec{A} ) = 0
$$
The divergence of the curl of a vector is 0 as per the book. 

$$
\vec{\nabla}  \times \vec{B} = \mu_{0}\vec{j} \implies \vec{\nabla}\times \vec{\nabla} \times \vec{A} = \vec{\nabla}  (\vec{\nabla} \cdot \vec{A}) - \vec{\nabla}^{2}\vec{A} = \mu_{0}\vec{j}
$$
$$
 \vec{\nabla}  \cdot \vec{A} = 0
$$
The above equation is also known as the coulomb gauge

### General Field Theory
$$
\vec{\nabla} = -\vec{\nabla} \phi + \vec{\nabla} \times \vec{A} 
$$
$$
\vec{\nabla} \cdot \vec{V} = - \vec{\nabla}^{2} \phi + \vec{\nabla} \cdot( \vec{\nabla} \times \vec{A})
$$
Plugging in potential 
$$
= - \vec{\nabla} ^{2}_{\vec{r}} \phi  = \frac{1}{4\pi} \int _{\vec{V}}  S(\vec{r}') \vec{\nabla}^{2}_{\vec{r}} \frac{1}{|\vec{r}-\vec{r}'|} \, dV'
$$
$$
= - \frac{1}{4\pi} \int  S(\vec{r}')(-4\pi \delta(\vec{r}-\vec{r}')) \, dV'
$$
Curl
$$
\vec{\nabla} = -\vec{\nabla}\phi + \vec{\nabla} \times \vec{A}
$$
$$
\vec{\nabla}\times \vec{\nabla} = \vec{\nabla} \times (-\vec{\nabla}\phi) + \vec{\nabla} \times \vec{\nabla} \times \vec{A} 
$$
$$
= \vec{\nabla}(\vec{\nabla} \cdot \vec{A}) - \vec{\nabla}^{2}_{\vec{r}} \left( \frac{1}{4\pi} \int \frac{\vec{c}(\vec{r}')}{|\vec{r} - \vec{r}'|} \, dV'  \right)
$$
$$
\vec{\nabla} \times \vec{V} = \vec{\nabla} (\vec{\nabla} \cdot \vec{A} ) + \vec{C} (\vec{r}) = \vec{C}(\vec{r})\implies \vec{\nabla} \cdot \vec{A} =0
$$

Solution to DiffEq
$$
-\vec{\nabla} \vec{A} = \mu_{0}\vec{j}
$$
$$
\vec{A} = \frac{\mu_{0}}{4\pi} \int  \frac{\vec{j} (\vec{r}')}{|\vec{r}_{0}\vec{r}'|} \, dV' 
$$
$$
\vec{B} = \vec{\nabla} \times \vec{A}
$$

## In class problems
![[Pasted image 20240226151038.png]]
a. 
$$
K = \frac{I}{2\pi a}
$$
b. 
$$
J(s) =  \frac{k}{s} = \frac{I}{2\pi as}
$$
![[Pasted image 20240226151926.png]]
a. 
$$
\oint B \cdot dl = \mu_{0}I
$$
$$
Br = \mu_{0}I \to B_\text{r>a}= \frac{\mu_{0}I}{r}
$$
$$
B_{a>r} = \mu_{0}Ir
$$











