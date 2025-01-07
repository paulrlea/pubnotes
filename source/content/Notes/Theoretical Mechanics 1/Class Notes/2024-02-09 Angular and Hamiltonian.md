---
dg-publish: true
---
## Exam Logistics
- Tuesday 2/13 form 8-9:50
- 4 problems, each problem should be ~ half hour
- Concepts covered
	- [[2024-01-03 Classical  Review]]
	- [[2024-01-19 Special Relativity]]
		- Have numbers in it, will be simple numbers
		- Boost Equations
		- Length contraction/time dilation equations
		- Velocity transformations
	- [[2024-01-23 Lagrangian Mechanics]]
		- **Not** doing forces of constraint
	- 2 problems on Lagrangian Mechanics, 1 on classical review, one on special relativity. 
	- No calculators, no crib sheet
	- Any non-standard integral will be given
	- Use problems in the book for review
## Conservation of Angular Momentum
Continued from [[2024-02-06 Hamilton and Conservation]]

- Lagrangian is invariant under rotation 
- For some vector $\vec{r}$
![[Pasted image 20240209084639.png]]

$$
L(\vec{r} + \delta \vec{r} ) = L(\vec{r})
$$
$$
\delta \vec{r}=\delta\vec{\theta} \times \vec{r}
$$
Then 
$$
\delta   \dot{\vec{r}} = \delta\vec{\theta} {\times}\dot{\vec{r}}
$$
$$
L(\vec{r} + \delta \vec{r})-L(\vec{r})=\delta L
$$
$$
\delta L = \sum_{i}\frac{ \partial L }{ \partial x_{i} } \delta x_{i} + \sum_{i} \frac{ \partial L }{ \partial \dot{x}_{i} } \delta \dot{x}_{i} \tag{0}
$$
$$
\frac{ d L }{ d \dot{x}_{i} } = P_{i}  \tag{1}
$$
$$
\frac{ d L }{ d x_{i} }  = \dot{P}_{i}\tag{2}
$$
Plug eqs 1 and 2 into 0
$$
\delta L = \sum_{i} \dot{P}_{i} \delta x_{i} + P_{i}\delta \dot{x}_{i} 
$$
We can use the [[dot product]] to simplify this into the following: 
$$
\delta L = \dot{\vec{P}} \cdot \delta \vec{r} + \vec{P} \cdot \delta   \dot{\vec{r}}
$$
Simplify with chain rule
$$
= \vec{\dot{P}}\cdot(\delta\vec{\theta}\times \vec{r}) + \vec{P} \cdot(\delta\vec{\theta} \times  \dot{\vec{r}})
$$
$$
=\delta\vec{\theta} \cdot ( \vec{r} \times    \vec{\dot{P}}) + \delta\vec{\theta} \cdot(\dot{\vec{r}} \times \vec{P})
$$
$$
\delta L=\delta \vec{\theta} \frac{d}{dt} (\vec{r}\times \vec{P})
$$
[[Angular Momentum]] formulas

Angular momentum is conserved if L is invariant under rotation. If a system is symmetric about an axis, then angular momentum in that direction (of axis ) is conserved. 

Examples with uniform circular motion

in x-y plane
- Symmetry about z-axis, so $L_{z}$ is conserved
Cylindrical symmetry $L_{z}$ conserved. 
Spherical symmetry $\vec{L}=$ constant

goddamn

## Hamilton Dynamics
Canonical (inherent) equations of motion. For example, the canonical equation of motion for Lagrangian mechanics is the [[Euler-Lagrange Equation]]

Aside:
	Hamiltonian mechanics and dynamics are very useful for things that are not classical. They are, however, very useful for quantum physics. It produces first order differential equations, which was very useful hundreds of years ago when computers didn't exist. 

Transforming the [[Lagrangian]] into the [[Hamiltonian]]
The Lagrangian is a function of position, velocity and time
$$
L(q,\dot{q},t) \to H(q,p,t)
$$
$$
H = \sum_{j} \dot{q}_{j} \frac{ \partial L }{ \partial \dot{q}_{j} } -L
$$
$$
=\sum_{j} P_{j}\dot{q}_{j}- L(q_{k},\dot{q}_{k},t)
$$
$$
\dot{q}_{j} = \dot{q}_{J}(q_{k},p_{k},t)
$$
$$
dH = \sum_{k} \left[ \frac{ \partial H }{ \partial q_{k} } dq_{k}+ \frac{ \partial H }{ \partial P_{k} } dp_{k} \right]+\frac{ \partial H }{ \partial t } dt
$$
$$
\frac{ \partial H }{ \partial q_{k} } = P_{k}\frac{ \partial \dot{q}_{k} }{ \partial q_{k} } -\frac{ \partial L }{ \partial q_{k} } -\frac{ \partial L }{ \partial \dot{q}_{k} } \frac{ \partial \dot{q}_{k} }{ \partial q_{k} } 
$$
$$
\frac{ \partial H }{ \partial q_{k} } = - \frac{ \partial L }{ \partial q_{k} } = -\dot{p}_{k}
$$
$$
\frac{ \partial H }{ \partial p_{k} } = \dot{q}_{k}+P_{k} \frac{ \partial \dot{q}_{k} }{ \partial p_{k} } - \frac{ \partial L }{ \partial \dot{q}_{k} }\frac{ \partial \dot{q}_{k} }{ \partial p_{k} } =\dot{q}_{k}
$$
$$
dH = \sum_{k} [-\dot{p}_{k}dq_{k} + \dot{q}_{k}dp_{k}]-\frac{ \partial L }{ \partial t } dt 
$$
Hamiltonian equations of motion:
$$
\frac{ \partial H }{ \partial q_{k} }  = -\dot{P}_{k}
$$
$$
\frac{ \partial H }{ \partial P_{k} }  = \dot{q}_{k}
$$
$$
\frac{ \partial H }{ \partial t } =  - \frac{ \partial L }{ \partial t } 
$$
if 
$$
\frac{ d H }{ d q_{k} } = 0 \therefore P_{k} \text{ = constant}
$$
if
$$
\frac{ d H }{ d P_{k} }  =0 \therefore q_{k} \text{=constan}
$$

Example: Free particle of mass m in 1 dimension
$$
x=q
$$
$$
L =T > q? > 0 = \frac{1}{2}m\dot{q}^{2}
$$
Need generalized momentum. Ignore weird part above, i couldnt really read his handwriting.

$$
H = \dot{q} \frac{ \partial L }{ \partial \dot{q} } -L
$$
$$
\frac{ \partial L }{ \partial \dot{q} }  = m\dot{q} = P
$$
$$
\dot{q} = \frac{P}{m}
$$
$$
=\dot{q} \cdot m\dot{q} - \frac{1}{2}m\dot{q}^{2} = \frac{1}{2}m\dot{q}^{2}
$$
This is not correct! no velocity allowed
$$
H= H(q,p,t)
$$
$$
H = \frac{1}{2} \frac{P^{2}}{m}
$$
$$
\frac{ \partial H }{ \partial p }  =\frac{p}{m} 
$$
$$
\frac{ \partial H }{ \partial p } = \frac{p}{m} = \dot{q}
$$
$$
\frac{ \partial H }{ \partial q  }= 0 = -\dot{p}
$$
$$
\frac{dp}{dt} = 0 \text{ and } p= \text{ constant}
$$

$$
\frac{ d q }{ d t } = \frac{p}{m}
$$
$$
\int  \, dq = \int \frac{p}{m} \, dt 
$$
$$ 
q = \frac{p}{m}t + c_{1}
$$
Which is equiv. to
$$
x = v_{0}t + x_{0}
$$
 
Example Harmonic oscillator
$$
L = \frac{1}{2}m\dot{x}^{2} - \frac{1}{2}kx^{2}
$$
$$
\omega^{2} = \frac{k}{m} ; \ k = m\omega^{2}
$$
$$
\frac{ \partial L }{ \partial \dot{x} } = m\dot{x} = P_{x} \implies \dot{x}=\frac{P_{x}}{m}
$$
$$
H = \dot{x} \frac{ \partial L }{ \partial \dot{x}  } - L = m\dot{x}^{2} - \left( \frac{1}{2}m\dot{x}^{2} - \frac{1}{2}kx^{2} \right)
$$
$$
=\frac{1}{2}m\dot{x}^{2} + \frac{1}{2}kx^{2}
$$
This is not the Hamiltonian! Has velocity, not momentum 
$$
= \frac{1}{2} \frac{P_{x}^{2}}{m} + \frac{1}{2}kx^{2}
$$
$$
\frac{ d H }{ d x }  = kx = -\dot{P}_{x}
$$
$$
\frac{ d H }{ d P_{x} }  = \frac{P_{x}}{m}=\dot{x}
$$
$$
-\dot{P} = kx = m\omega^{2}x
$$
$$
P = m\dot{x} = m\dot{x}
$$
$$
\frac{i}{m\omega}\cdot(-\dot{P}) = m\omega^{2}x \cdot \frac{i}{m\omega}
$$
$$
-\frac{i\dot{P}}{m\omega} = i \omega x
$$
$$
-\frac{i\dot{P}}{m\omega} + \frac{P}{m} = i\omega x + \dot{x}
$$
$$
\dot{x} + \frac{i\dot{p}}{m\omega} = \frac{p}{m} - i\omega x = -i\omega \left(  x+\frac{ip}{m\omega} \right)
$$
$$
z=x + \frac{ip}{m\omega}
$$
$$
\dot{z} = \dot{x} + \frac{i\dot{p}}{m\omega}
$$
$$
\dot{z} = -i\omega z
$$
$$
z = z_{0}e^{-i\omega t}
$$
Alternative: 
$$
H = \frac{p^{2}}{2m} + \frac{k}{2}x^{2}
$$
Choose coordinates such that H is cyclic 
$$
\left( \frac{ d H }{ d q_{0} }  \right) =0
$$
$$
P_{1}x \to P_{1}Q
$$
$$
P = \sqrt{ 2m\omega P} \cos Q
$$
$$
x = \frac{\sqrt{ 2m\omega P }}{m\omega}\sin Q
$$
What the fuck is this. 
$$
H = \frac{1}{2m} 2m\omega P\cos ^{2}Q + \frac{m\omega^{2}}{2} \frac{2m\omega P}{m^{2}\omega^{2}}
$$
$$
H = \omega P
$$
$$
\frac{ \partial H }{ \partial Q  }  = 0 = -\dot{P} 
$$
$$
P = \text{constant} = \frac{H}{\omega} = \frac{E}{\omega}
$$
$$
\frac{ \partial H }{ \partial P } = \omega = \dot{Q}
$$
$$
\dot{Q} = \omega t + \phi
$$Go back?
$$
p=\sqrt{ 2mE } \cos(\omega t+\phi)
$$
$$
x = \sqrt{ \frac{2E}{m\omega^{2}} } \sin(\omega t+\phi)
$$
### Conservation Laws
- For a given variable, q, p or t, to see if that quantity is conserved we should check the total time derivative. 
 - $F(q,p,t)$ general function of $q_{i},P_{i}$ and $t$
 $$
\frac{ d F }{ d t }  = \frac{ d F }{ d t } + \sum_{i} \left( \frac{ d F }{ d q_{i} } \dot{q}_{i} + \frac{ d F }{ d P_{i} }\dot{P}_{i}  \right)
$$
$$
\frac{dF}{dt} = \frac{ d F }{ d t } + \sum_{i}\left[ \frac{ \partial F }{ \partial q_{i} } \frac{ \partial H }{ \partial P_{i} }-\frac{ \partial F }{ \partial P_{i} }\frac{ \partial H }{ \partial q_{i} }    \right]
$$

The bracket can be expressed compactly as a [[Poisson bracket]]
$$
\left[ \frac{ \partial F }{ \partial q_{i} } \frac{ \partial H }{ \partial P_{i} }-\frac{ \partial F }{ \partial P_{i} }\frac{ \partial H }{ \partial q_{i} }    \right] \equiv \{H,F\}
$$
F is conserved if $\frac{dF}{dt}=0$
Implies $\frac{ d F }{ d t }=0 \to \{H,F\}=0$

This is especially useful when we transition from classical to quantum mechanics.
For a problem
1. Determine the classical Hamiltonian
2. Transition by replacing q and p by their operators
$$
\{H,q\}=[\hat{H}\hat{Q}-\hat{Q}\hat{H}]
$$
$$
q \to \hat{Q}
$$
$$
p \to \hat{P}
$$
$$
p_{x} = i\hbar \frac{d}{dx}
$$
Next topic is [[Central Forces]]







