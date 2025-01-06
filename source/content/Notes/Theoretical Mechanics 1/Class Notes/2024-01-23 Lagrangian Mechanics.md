---
dg-publish: true
---
## Newtonian Mechanics:
- Based on force
- Newtons 3 laws
$$
\vec{F}_\text{net} =\frac{ d \vec{p} }{ d t }  , \ m\ddot{x} = F_\text{net}
$$
## Lagrangian Mechanics
- Energy based
- Practical problems with Newtonian mechanics led to development of Lagrangian mechanics
![[Pasted image 20240129103214.png]]
Example of problem that would be nearly impossible to solve with newtonian mechanics

The [[Lagrangian]] is defined as:
$$
L = T-U
$$
$$
L = L(x,\dot{x},t)
$$
It is a function of position, velocity and time 

#### Lagrange's equation of motion 
aka [[Euler-Lagrange Equation]]
$$
\frac{d}{dt} \frac{ \partial L }{ \partial \dot{x} } - \frac{ \partial L }{ \partial x }  = 0
$$
5 simple steps to Lagrangian mechanics 
1. Find the kinetic energy (T)
	$T = \frac{1}{2}mv^{2}$
2. Find the potential energy 
	$U=mgh$ for gravity
3. Calculate [[Lagrangian]]
	$L = T-U$
4. Calculate [[Euler-Lagrange Equation]]
	$\frac{d}{dt} \frac{ \partial L }{ \partial \dot{x} }-\frac{ \partial L }{ \partial x }=0$
5. Solve Diff. eq (optional)

#### Free particle example
Kinetic Energy: 
$$
T = \frac{1}{2} mv^{2} 
$$
Potential energy $= 0$ or $u_{0}$
$$
L = \frac{1}{2}m\dot{x}^{2} - u_{0}
$$
Take derivatives 
$$
\frac{ \partial L }{ \partial \dot{x} }  = m\dot{x}
$$
$$
\frac{ \partial L }{ \partial x }  = 0
$$
$$
\frac{d}{dt}  \frac{ \partial L }{ \partial \dot{x} }   = \frac{d}{dt} (m\dot{x}) = m\ddot{x}
$$
Apply Euler-Lagrange
$$
\frac{d}{dt} \frac{ \partial L }{ \partial \dot{x} } - \frac{ \partial L }{ \partial x } = 0 
$$
$$
m\ddot{x}-0=0 \implies m\ddot{x} = 0 \ \& \ \ddot{x}=0
$$
Same approach
$$
\ddot{x} = 0
$$
$$
\frac{dv}{dt} = 0 \to v= \text{constant} = v_{0}
$$
$$
v=\frac{ d x }{ d t } =v_{0} \to x= v_{0}t+x_{0}
$$

 