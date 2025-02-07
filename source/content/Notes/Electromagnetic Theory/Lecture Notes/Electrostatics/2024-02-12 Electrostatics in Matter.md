---
dg-publish: true
---
## Review of Electrostatics in Vacuum
$$
\nabla \cdot \vec{E} = \frac{\rho}{\epsilon_{0}}
$$
$$
\nabla \times \vec{E}=0
$$
$$
\vec{E}=-\nabla V
$$
- Three primary equations for dealing with electrostatics in vacuum. 
- Different methods to solve [[Laplace's equation]] and [[Poisson's Equation]]
	- Multi-pole expansion
	- Direct integration 
	- Method of images
	- Differential Equation
	- Legendre Polynomials

## Electrostatic fields in matter
Compared to a conductor, the electric field on the inside does not necessarily have to be 0 on the inside for a dielectric.

Atoms can be polarized by a strong electric field, puling the protons to one side and electrons to another. The strength of the dipole is given by the equation below:
$$
\vec{p}=\alpha \vec{E}
$$
Where $\alpha$ is a material dependent scalar value. 

> Very strong lasers are also used to polarize atoms. See 2018 Nobel Prize winners. 

>See also: Development of intense laser light sources graph in PowerPoint slides. Very cool diagram of the evolution of lasers over time.

The behavior of [[electric dipoles]] in an electric field is interesting. The electric field applies a force to align the dipoles together, but this is contrary to the thermal energy which will attempt to disorganize it. [[Electric polarization]], $\mathbf{P}$ ,is the average dipole moment divided over the volume. The field of atoms being aligned by an electric field is the opposite to the electric field. 



Continuing from atomic polarizability, we can also calculate molecular polarizability using the following equation: 
$$
\vec{p} = \{\alpha\} \vec{E}
$$
The electric field vector and dipole vectors are not necessarily parallel in this situation. 

### Calculating the electric field of a polarized object
- Use the n=1 term of the multi-pole expansion to calculate potential at distance from a small dipole object

Example of calculating potential from polarized object
$$
v(\vec{r} ) = \frac{1}{4\pi\epsilon_{0}} \frac{\vec{p}(\vec{r}-\vec{r}')}{|\vec{r}-\vec{r}'|^{2}} \tag{1}
$$
$$
\vec{P}  = \frac{\left< \vec{P}_{i}  \right>}{V} \tag{2}
$$
$$
\vec{P} = \int \vec{P}(\vec{r}') \, dV' \tag{3}
$$
You can plug equation 3 into 1:
$$
V(\vec{r}) = \int _{V'} \frac{\vec{P}(\vec{r}')(\vec{r}-\vec{r}')}{|\vec{r}-\vec{r}'|^{2}}\, dV'
$$
We can use this cool math trick to simplify:
$$
\vec{\nabla}_{\vec{r}} \frac{1}{|\vec{r}-\vec{r}'|}= \frac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}|^{2}}
$$
$$
	v(\vec{r})=\frac{1}{4\pi\epsilon_{0}} \int _{v'} \vec{P}'\cdot\left( \vec{\nabla}_{\vec{r}'} \frac{1}{|\vec{r}-\vec{r}'|^{2}} \right)\, dV'
$$
Equation 5 from the book 
$$
\vec{\nabla} \cdot (F\vec{A}) = F \cdot \vec{\nabla} \cdot \vec{A} + \vec{A}\vec{\nabla}F
$$
$$
\vec{A}(\vec{\nabla}F)=\vec{\nabla} \cdot(F\vec{A}) - F\cdot \vec{\nabla}\vec{A}
$$
Use this to simplify further
$$
V(\vec{r}) = \left[  \int _{v'}\vec{\nabla}_{\vec{r}} \left( \frac{\vec{P}}{|\vec{r}-\vec{r}'|^{2}} \right) \, dV' - \int _{v'} \frac{1}{|\vec{r}-\vec{r}'|}(\vec{\nabla}_{\vec{r}}\cdot \vec{P}) \, dV'  \right]
$$
The divergence of A over the volume is the same as the flux through the volume around the volume via [[Divergence Theorem]]
$$
v(r) = \frac{1}{4\pi\epsilon_{0}} \int_{A'(v)} \frac{1}{|\vec{r}-\vec{r}'|}\vec{P} \cdot d\vec{A} -\frac{1}{4\pi\epsilon_{0}} \int _{v'} \frac{1}{|\vec{r}-\vec{r}'|} (\vec{\nabla}_{\vec{r}}\vec{P}) \, dV' 
$$

## In class questions: 
A sphere of radius $R$ carries a polarization $\mathbf{P}(\mathbf{r})=k\mathbf{r}$
	Where k is a constant and $\mathbf{r}$ is the vector from the center to the sphere.
$$
\mathbf{P}= k\mathbf{r}
$$
$$
\sigma_{b} = \mathbf{P} \cdot \mathbf{\hat{n}}
$$
$$
\sigma_{b} = k\mathbf{r} \cdot \mathbf{\hat{n}}
$$
$$
\sigma_{b} = kR
$$
$$
\rho_{b} = -\nabla \cdot \mathbf{P}
$$
$$
\mathbf{P}= k\mathbf{r}\hat{r}
$$
$$
\rho_{b} = \nabla \cdot \mathbf{P} = k\left( \frac{1}{r^2}\frac{\partial}{\partial r}(r^2P_r) + \frac{1}{r\sin\theta}\frac{\partial}{\partial \theta}(\sin\theta P_\theta) + \frac{1}{r\sin\theta}\frac{\partial P_\phi}{\partial \phi} \right)
$$
$$
\rho_{b} = k\left( \frac{1}{r^{2}}\frac{ \partial  }{ \partial r } (r^{2}P_{r}) \right)
$$
$$
\rho_{b} =k\left(  \frac{1}{r^{2}} \frac{ \partial  }{ \partial r }  (r^{3}) \right)
$$
$$
\rho_{b} = k\frac{3}{\cancel{ r^{2} }} \cancel{ (r^{2}) }
$$
$$
\rho_{b} = -3k
$$
$$
Q_{enc} = \frac{4}{3} \pi R^{3} 3k + k 4\pi R^{3}
$$
$$
\int E \cdot d\vec{A} = \frac{-\frac{4}{3} \pi R^{3} 3k + k 4\pi R^{3}}{\epsilon_{0}}
$$
$$
E= \frac{-\frac{4}{3} \pi R^{3} 3k + k 4\pi R^{3}}{\epsilon_{0}4\pi R^{2}}
$$
$$
E = \frac{-\frac{1}{3} R^{2}3k + k R^{2}}{\epsilon_{0}}
$$
$$
E_{\text{outside}} = \frac{0}{\epsilon_{0}}
$$
$$
E_\text{outside}=0
$$
How to find electric field inside? 


4.11










