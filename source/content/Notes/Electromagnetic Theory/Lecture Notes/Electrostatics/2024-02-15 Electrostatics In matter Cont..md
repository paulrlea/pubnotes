---
dg-publish: true
---
## Logistics: 
- No class next Tuesday
- Midterm next Thursday
	- Covers classes 2-10
	- Exam format will be pen and paper
	- Resources provided will be "Very Useful Mathematical Formulas" and "Legendre Polynomials and Their Important Properties"
	- 4 problems
	- 60 Percent is easily earned, 20-30% intermediate, 10% difficult
	- No self provided crib sheets
	- Back exams will be posted
[[2024-02-12 Electrostatics in Matter]] review
- Dialectics and polarization

## Describing [[linear dielectrics]]
- We can use electric displacement $\mathbf{D}$ and properties of [[electric susceptibility]] $\chi_{e}$ and [[electric permittivity]] $\epsilon$

Previously: 
$$
\vec{p} = \alpha_{1} \vec{E} \implies \vec{P} = \frac{\left< \vec{p}_{i} \right> }{V}
$$
Alternatively:
$$
\vec{P} = \epsilon_{0}\chi_{e}\vec{E}
$$
An isotropic dielectric has a scalar value for [[electric susceptibility]]. This means that the susceptibility is independent from the crystal structure of the material and is not dependent on the polarization. 

An anisotrpoic dielectric is dependent on polarization

A linear dielectric denotes a material in which $\chi_{e}$ is independent of the $\vec{E}$ 

A nonlinear dielectric has changing electric properties based on applied external electric fields .

Displacement is given by the following:
$$
\vec{D} = \epsilon_{0}\vec{E} + \vec{P} = \epsilon_{0}\vec{E} + \epsilon_{0}\chi_{e}\vec{E}
$$
Factoring out $\epsilon_{0}$ we get 
$$
\vec{D} = \epsilon_{0}\vec{E}(1+\chi_{e})
$$
Where $1+\chi_{e}$ is known as the relative dielectric constant and denoted by $\epsilon _r$
$$
\vec{D} = \epsilon_{0}\epsilon_{r}\vec{E}
$$
$$
\epsilon_{0} \approx 8.85\times 10^{-12} \frac{As}{Vm}
$$
## Boundary Conditions for Dielectric Interfaces

If the dielectric has a surface charge, the perpendicular element of electric field is discontinuous
$$
E_{\perp}^{o} - E^{i}_{\perp} = \frac{\sigma}{\epsilon_{0}}
$$
We can have electric field inside the material in a dielectric so the parallel component of the electric field is continuous
$$
E_{\parallel}^{o}=E_{\parallel}^{i}
$$
## Super and Ultra [[Capacitors]]
- The energy storage of a capacitor is proportional to it's capacitance, which is based on the materials and geometry of the capacitor. 
- Capacitance:
$$
C = \frac{\epsilon_{r}\epsilon_{0}A}{d}
$$
- Energy storage: 
$$
U_{e} =\frac{1}{2}CV^{2}
$$

![[Pasted image 20240215144654.png]]

a. Find the electric displacement in each slab
$$
\vec{D} = \epsilon_{0}\vec{E}(1+\chi_{e})
$$
$$
\vec{D} = \epsilon_{0}\epsilon_{r}\vec{E}
$$
$$
\vec{E}_{1} = \frac{\sigma}{\epsilon_{1}\epsilon_{0}}
$$
$$
\vec{D}_{1} = \epsilon_{0}\epsilon_{1} \frac{\sigma}{\epsilon_{1}\epsilon_{0}}
$$
$$
\vec{D}_{1} \text{ and } \vec{D}_{2}=\sigma
$$
b. Find the electric field: 
$$
\vec{E}_{1}=\frac{\sigma}{\epsilon_{1}\epsilon_{0}}
$$
$$
\vec{E}_{2}=\frac{\sigma}{\epsilon_{2}\epsilon_{0}}
$$
c. Find the polarization in each slab
 $$
\vec{P} = \epsilon_{0}\chi_{e}\vec{E}
$$
$$
\vec{P} = \vec{D}-\epsilon_{0}\vec{E}
$$
$$
\vec{P}_{1}= \sigma - \frac{\epsilon_{0}\sigma}{\epsilon_{0}\epsilon_{1}}
$$
$$
\vec{P}_{2}= \sigma - \frac{\epsilon_{0}\sigma}{\epsilon_{0}\epsilon_{2}}
$$
d. 
$$
V = E_{1}a + E_{2}a
$$
$$
\frac{\sigma}{\epsilon_{1}\epsilon_{0}} a + \frac{\sigma}{\epsilon_{2}\epsilon_{0}}
$$
$$
V=
\frac{7\sigma a}{6\epsilon_{0}}
$$
e. 

