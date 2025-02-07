# Remaining Course Topics
- Potentials and fields
	- Leads into the Lagrangian and Hamiltonian of EM fields, Quantum electrodynamics 
- Relativistic Electrodynamics
# Scalar and Vector potentials
- We are seeking the general solution to [[Maxwell's Laws]] 
- In a vacuum they are: 
$$
\vec{\nabla} \cdot \vec{E}=0
$$
$$
\vec{\nabla} \cdot \vec{B} = 0
$$
$$
\vec{\nabla} \times \vec{E} = -\vec{B}
$$
$$
\vec{\nabla} \times \vec{B} = \mu_{0}\epsilon_{0}\vec{\dot{E}}
$$
- Given Linear dielectrics /magnetic materials, the first three laws remain the same. The last one becomes 
$$
\vec{\nabla} \times \vec{B} = \mu\epsilon \vec{\dot{E}}
$$
- With an electrically conducting material, the amperes law becomes 
$$
\vec{\nabla} \times \vec{B} = \mu \sigma \vec{E} + \mu \epsilon \vec{\dot{E}}
$$
## Maxwell's Equations with electric charge and current
- Faraday's Law always holds
- Maxwell's laws become:
$$
\vec{\nabla} \cdot \vec{E} = \frac{\rho}{\epsilon_{0}}
$$
$$
\vec{\nabla} \cdot \vec{B}=0
$$
$$
\vec{\nabla} \times \vec{E} = -\vec{B}
$$
$$
\vec{\nabla} \times \vec{B} = \mu \vec{j} +\mu\epsilon \vec{\dot{E}}
$$

- Given a charge distribution $\rho(\mathbf{r},t)$ and a current density $\mathbf{J}(\mathbf{r},t)$, what are the electric and magnetic fields at any given point and time?
- Start representing fields as potentials
$$
\mathbf{B}=\nabla \times \mathbf{ A}
$$
and 
$$
\mathbf{E}= - \nabla V - \frac{ \partial \mathbf{A} }{ \partial t } 
$$
Using [[Gauss' Law]] on this: 
$$
\nabla \cdot \left( -\nabla V-\frac{ \partial A }{ \partial t }  \right)=\frac{1}{\epsilon_{0}} \rho
$$
$$
\nabla^{2}V + \frac{ \partial  }{ \partial t })(\nabla \cdot \mathbf{A})=-\frac{1}{\epsilon_{0}}\rho 
$$

Looking at the magnetic field: 
$$
\vec{\nabla} \times \vec{B} = \vec{\nabla} \times \vec{\nabla} \times \vec{A} = \mu_{0} \vec{j} + \mu_{0}\epsilon_{0} \frac{ \partial \vec{E} }{ \partial t }  = \mu_{0}\vec{j}+ \mu_{0}\epsilon_{0} \frac{d}{dt} \left( -\vec{\nabla}V - \frac{ \partial \vec{A} }{ \partial t }  \right)
$$
$$
-\vec{\nabla} ^{2} \vec{A} +\vec{\nabla} (\vec{\nabla} \cdot \vec{A}) = \mu_{0}\vec{j} - \mu_{0} \epsilon_{0}\vec{\nabla} \frac{ \partial V }{ \partial t } - \mu_{0}\epsilon 0-\frac{ \partial^{2} \vec{A} }{ \partial t^{2} } 
$$
$$
-\vec{\nabla} ^{2} \vec{A} + \mu_{0}\epsilon_{0} \frac{ \partial^{2} \vec{A} }{ \partial t^{2} } = \mu_{0}\vec{j} - \vec{\nabla}(\vec{\nabla} \cdot \vec{A}) -\mu_{0}\epsilon_{0}\vec{\nabla} \frac{ \partial V }{ \partial t } 
$$
The RHS can be written as 
$$
\vec{\nabla} \left[ -\vec{\nabla} \cdot \vec{A} - \frac{1}{c^{2}}\frac{ \partial V }{ \partial t }  \right]
$$
And the LHS + the first term of the right hand side is the inhomogenous wave equation (solvable)
We decide the RHS is equal to zero. Because fiskis. 

We are working in the [[Lorentz Gauge]] in opposition to the [[Coulomb Gauge]] used in electrostatics. 


$$
\vec{E} = -\vec{\nabla} V - \frac{ \partial \vec{A} }{ \partial t } 
$$
$$
 \vec{B} = \vec{\nabla} \times \vec{A}
$$
$$
\vec{A}, \ \vec{A}' + \vec{\nabla}\lambda
$$
$$
\vec{B}' = \vec{\nabla} \times \vec{A}' = \vec{\nabla} \times \vec{A} + \cancelto{ 0 }{ \vec{\nabla}\times(\vec{\nabla}\lambda ) }=\vec{B}
$$
$$
\vec{E}'= -\vec{\nabla}V' - \frac{ \partial \vec{A} '' }{ \partial t } =-\vec{\nabla}\left( V-\frac{ \partial \vec{A} }{ \partial t }  \right)-\frac{d}{dt}  (\vec{A}+\vec{\nabla}\lambda)
$$
$$
\vec{E}'= -\vec{\nabla} V - \frac{ \partial \vec{A} }{ \partial t } + \cancelto{ 0 }{ \vec{\nabla} \frac{ \partial \lambda }{ \partial t }-\frac{d}{dt} \vec{\nabla}\lambda }-\vec{E} 
$$
# Lorentz Force 
The Lorentz force is given by 
$$
\vec{F} = \frac{ d \vec{p} }{ d t }  = q(\vec{E} + \vec{v}+\vec{B})
$$$$
\vec{E} = -\vec{\nabla} - \frac{ \partial \vec{A} }{ \partial t } ,  \ \ \vec{B} = \vec{\nabla}\times \vec{A}
$$
$$
\vec{F} = \frac{ d \vec{p} }{ d t } =q\left( -\vec{\nabla}V-\frac{ \partial \vec{A}  }{ \partial t  } + \vec{v}\times(\vec{V}\times \vec{A}) \right) 
$$
Rewrite triple cross product with useful mathematical formula
$$
\vec{F} = \frac{ d \vec{p}  }{ d t }  = q\left( -\vec{\nabla}V - \frac{ \partial \vec{A}  }{ \partial t } + \vec{\nabla} (\vec{v}\cdot \vec{A})-(\vec{v}\vec{\nabla}) \cdot \vec{A}   \right)
$$
$$
\vec{F} = \frac{ d \vec{p} }{ d t } = -q \frac{ d \vec{A} }{ d t } -q\vec{\nabla}(V + \vec{v} \cdot \vec{A})
$$
$$
\implies \frac{d}{dt}  ( \vec{p} + q\vec{A}) = - q\vec{\nabla}(V-\vec{v} \cdot \vec{A})
$$
the $(\vec{p}+q\vec{A})$ is also known as canonical momentum. Used in Lagrangian and Hamiltonian electrodynamics. This is a velocity dependent potential energy. 

In class problems 10.3 and 10.7

