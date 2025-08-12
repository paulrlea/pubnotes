---
dg-publish: true
---
# Topics today: 
- Storage of energy in magnetic and electric fields 
- Linear and Angular momentum
- Energy and momentum of electromagnetic fields within the framework of maxwell's equations
	- Energy density of EM field 
	- Poynting Vector 
	- Maxwell stress/strain tensors
	- Force $\vec{F}=q\vec{E} + q\vec{v}\times \vec{B}$, known as the [[Lorentz Force]].
## Phys 2 review : 

- Electric charge is quantized in electrons
	- All electric charges is stored as integer multiples of the electron
- It is globally conserved


## Charge conservation in EM theory 
- Continuity equation states there the change in charge is equal to the flux through a surface around the change in charge 
$$
\frac{ d \rho }{ d t }  + \vec{\nabla} \cdot \vec{j}=0
$$
$$
	\implies \frac{d}{dt}  \int  \rho \, dV = - \int \vec{\nabla} \cdot \vec{j} \, dV 
$$
$$
\frac{ d  Q_\text{in Vol} }{ d t }  = -\int  \vec{j} \cdot \, d\vec{a} 
$$
Via [[Divergence Theorem]]

The Coulomb and Lorentz forces work over distance in a vacuum. This is interesting and unique. 

The energy density of electric and magnetic fields can be easily seen in capacitors. 
Ex: Parallel plate capacitor
$$
C = \epsilon_{0} \frac{A}{d}
$$
$$
U _{E} = \frac{1}{2}\epsilon_{0} \frac{A}{d}E^{2}d^{2}
$$

Inductors as well!

Conservation of electromagnetic field energy: 
$$
\frac{d}{dt}  E_{1mech} + \frac{d}{dt} \int \frac{1}{2} \vec{E} \cdot \vec{D}+\vec{B} + \vec{h} \, dV + \int\limits_{a(v)}^{} \vec{s} \ \cdot \, d\vec{a} 
$$
The last term of this is also known as the [[Poynting vector]]
In laymans terms, the above equation states that the energy lost or gained electromagnetically in the system has to be in the form of a poynting vector

Flashback to Phys 1:

Mechanical power is from the change in mechanical energy


Using the lorentz force equation 
$$
\vec{F}  = q\vec{E} + \vec{q} \times \vec{B}
$$
The mechanical power is :
$$
F\cdot \vec{v} = q\vec{v} \cdot \vec{E} + q\vec{v} \cancelto{ 0 }{ \cdot ( \vec{v} \times \vec{B} )K }
$$
Therefore the electrical power is given by 
$$
\vec{F} \cdot \vec{v} = q\vec{v} \cdot \vec{E}
$$
Electrical Power density is given by 
$$
\frac{q\vec{v} \cdot \vec{E} }{\text{volume}}  \to \vec{j} \cdot E
$$
And current density is given by 
$$
\vec{j} = \frac{q\vec{v}}{\text{ volume}}
$$
Electrical power is given by 
$$
\int _{V} \vec{j} \cdot \vec{E}  \, dV = \frac{dE_{mech}}{dE}
$$
Example of the utility of these fields
$$
\vec{j} = \vec{\nabla}\times \vec{H} - \dot{\vec{D}}
$$
$$
\vec{\nabla}\cdot (\vec{E} \times \vec{H} ) = \vec{H} \cdot(\vec{\nabla} \times \vec{E} ) - \vec{E} \cdot ( \vec{\nabla} \times \vec{H})
$$
$$
\vec{\nabla} \times \vec{E} = - \dot{\vec{B}}
$$
$$
\vec{E} ( \vec{\nabla} \times \vec{H} ) = -\vec{H} \cdot \vec{B} - \nabla \cdot ( \vec{E} \times \vec{H})
$$
$$
	\int \vec{j} \cdot \vec{E} \, dV = \int_{V} \vec{E} \cdot (\vec{\nabla} \times \vec{H})-\vec{\dot{D}} \, dV 
	
$$
$$
=\int _{V} (-\vec{H} \cdot  \vec{\dot{B}-\vec{\nabla} \cdot (\vec{E}\times \vec{H}-\vec{E} \cdot \dot{D}\vec{})}) \, dV
$$
$$
=\int_{V} (-\mu \vec{H} \dot{\vec{H}} - \epsilon \vec{E} \dot{\vec{E}}-\vec{\nabla} \cdot(\vec{E} \times \vec{H})) \, dV
$$

Change in time of $E_{mech}$ is 
$$
\frac{dE_\text{mech}}{dt} = \int \vec{j} \cdot \vec{E}  \, dV = - \frac{d}{dt}  \int _{V} \frac{1}{2 }\epsilon \vec{E}^{2} \frac{1}{2}\mu \vec{H}^{2} \, dV - \int \vec{E} \times \vec{H} \, da
$$

Energy Flux Density term is given by the poynting vector $\int \vec{S} \cdot \, d\vec{a}$

## Momentum
Momentum of the electromagnetic field
Lorentz force
$$
\vec{F} = q(\vec{E} + \vec{v} \times \vec{B}) = \frac{d\vec{p}m}{dt} \tag{1}
$$
When we introduce rho and cancel $\vec{j}$, equation 1 is conserved and converted to 
$$
\frac{d\vec{p}m}{dt} = \int _{v} (\rho \vec{E} + \vec{j}\times \vec{B}) \, dV 
$$
From maxwells eqs. 
$$
\rho =  \vec{\nabla}  \cdot \vec{D}, \ \ \rho =  \vec{\nabla} \cdot \vec{D}, \ \ \vec{j} = \vec{\nabla} \times \vec{H} - \dot{\vec{D}}
$$
The converted eq 1 becomes 
$$
	\int _{V} (\vec{E}(\vec{\nabla} \cdot \vec{D})+(\vec{\nabla} \times \vec{H} - \dot{\vec{D}})\times \vec{B})  \, dV
$$
$$
\frac{d}{dt}  ( \vec{D} \times \vec{B} ) = \vec{D} \times \vec{B} + \vec{D} \times   \dot{\vec{B}}
$$
$$
= \frac{d}{dt} (\vec{D} \times \vec{B} ) - \vec{D} \times(-\vec{\nabla} \times \vec{E})
$$

$$
\frac{d\vec{p}m}{dt} = \int _{v} \vec{E} ( \vec{\nabla} \cdot \vec{D} ) - \vec{D} \times (\vec{\nabla} \times \vec{E} ) + (\vec{\nabla}\times \vec{H}) \times \vec{B} - \frac{d}{dt} (\vec{D} \times \vec{B}) \, dV 
$$

There is a lot of components in this integral that correspond to real quantities. Not the first term though Adding "0"
$$
0 = \vec{H} \cdot (\vec{\nabla} \cdot \vec{B})
$$
$$
\frac{d\vec{p}m}{dt} = \int _{v} \vec{E} ( \vec{\nabla} \cdot \vec{D} ) - \vec{D} \times (\vec{\nabla} \times \vec{E} ) + (\vec{\nabla}\times \vec{H}) \times \vec{B} - \frac{d}{dt} (\vec{D} \times \vec{B})+\vec{H} \cdot (\vec{\nabla} \cdot \vec{B}) \, dV 
$$
Which yields the following: 
$$
\frac{d\vec{p}m}{dt} = \int _{v} \vec{E} ( \vec{\nabla} \cdot \vec{D} ) - \vec{D} \times (\vec{\nabla} \times \vec{E} ) + (\vec{\nabla}\times \vec{H}) \times \vec{B} - \frac{d}{dt} (\vec{D} \times \vec{B})+\vec{H} \cdot (\vec{\nabla} \cdot \vec{B}) \, dV 
$$
$$
	\frac{d\vec{p}m}{dt} = \int _{v} (\vec{E}(\vec{\nabla}\cdot\vec{D})-\vec{D} \times \vec{\nabla} \times \vec{E} + (\vec{\nabla} \times \vec{H} )\times \vec{B} - \frac{d}{dt} (\vec{d} \times \vec{B}) + \vec{H}(\vec{\nabla} \cdot \vec{B}))\, dV 
$$
This yields us the final result: 

The change of momentum with time is 
$$
\frac{d\vec{p}m}{dt} + \frac{d}{dt} \int _{V} \vec{D} \times \vec{B} \, dV 
$$
$$
 = \int _{V} [\vec{E} (\vec{\nabla} \cdot \vec{D} - \vec{D} \times (\vec{\nabla}\times \vec{E})+ \vec{H}(\vec{\nabla} \cdot \vec{B}) - \vec{B}\times(\vec{\nabla}\times \vec{H}))] \, dV
$$
Where $\vec{D} \times \vec{B}$ is the electromagnetic momentum density

and 
$$
(\vec{E} (\vec{\nabla} \cdot \vec{D})-\vec{D} \times (\vec{\nabla} \times \vec{E})+\vec{H}(\vec{\nabla}\cdot \vec{B} ) - \vec{B} \times (\vec{\nabla} \times \vec{H}))
$$
This  is known as the Maxwell stress-strain tensor:

$$
T_{ij} = D_{i} E_{j} - \frac{1}{2} \delta_{ij} (\vec{D} \cdot \vec{E}) + B_{i} H_{j} - \frac{1}{2} \delta_{ij} (\vec{B} \cdot \vec{H})
$$



## Angular Momentum 
Defined in mechanics as
$$
\vec{l} = \vec{t} \times \vec{p} 
$$
For the angular momentum density of the electromagnetic field we can use 
$$
\vec{l} = \vec{t} \times (\vec{D} \times \vec{B})
$$
This is analogous to classical/mechanical angular momentum. 

Electromagnetic waves have $\vec{E}$ and $\vec{B}$ fields, current topic of research is generating EM waves with a specific angular momenta. 

In class problems  8.1 and 8.7




