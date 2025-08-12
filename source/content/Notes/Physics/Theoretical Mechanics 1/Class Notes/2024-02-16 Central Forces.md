---
dg-publish: true
---
## Fields and forces
- Fields are a useful concept we use to describe action at a distance
- Examples include electricity, magnetism and gravitation. 
- There is a time dependent component to field that requires a certain amount of time for the field to "update" at a point 

## Gravitational Potential
- Gravitational potential $\neq$ Gravitational potential energy 
$$
\vec{g}  = -\vec{\nabla}\phi
$$
$$
-\frac{d\phi}{dr} = -\frac{GM}{r^{2}} \implies \phi=\frac{-GM}{r}
$$
- Force and Gravitational potential energy on one side, Fields and potentials on the other side. 
- This dichotomy divides between physical quantities and mathematical concepts.

> What is phi?
> Phi is gravitational potential. 

$$
\vec{F} = -\vec{\nabla}u
$$
$$
\vec{g} = -\vec{\nabla} \phi
$$
$$
\therefore u = m\phi
$$
For an extended object, the force of gravity is defined as below 
$$
\vec{F}_{g} = -Gm \int \frac{\rho(\vec{r})}{r^{2}}\hat{e}_{r} \, dV 
$$
How to get little g?
$$
\vec{g} = -G\int\limits_{V}^{} \frac{\rho(\vec{r})}{r^{2}}\hat{e}_{r} \, dV  
$$

![[Attachments/Pasted image 20240216101853.png]]
$$
\phi =  -\frac{Gm_{1}}{r_{1}}- \frac{Gm_{2}}{r_{2}}
$$
$$
-Gm\left( \frac{1}{r_{1}}+\frac{1}{r_{2}} \right)
$$
Want to generalize to all possible locations of $p$. 
$$
r_{1}= \sqrt{ (x-a)^{2}+y^{2} }
$$
$$
r^{2} = \sqrt{ (x+a)^{2}+y^{2} }
$$
$$
\phi= -Gm\left[ \frac{1}{\sqrt{V(x-a)^{2}  }}+ \frac{1}{\sqrt{(x+a)^{2}+y^{2}}} \right]
$$
$$
\vec{g} = -\vec{\nabla} = -\frac{ \partial \phi }{ \partial x } \hat{e}_{x} -\frac{ \partial \phi }{ \partial y } \hat{e}_{y}
$$
$$
g_{x} = -\frac{ \partial \phi }{ \partial x } = \frac{d}{dx} (-Gm[((x-a)^{2}+y^{2})^{-1/2}+((x+a)^{2}+y^{2})^{-1/2}])
$$
$$
\frac{ d \phi }{ d x } =-Gm\left[ -\frac{1}{2}((x-a)^{2}+y^{2})^{-3/2} \cdot(2(x-a)) - ((x+a)^{2}+y^{2})^{-3/2} \cdot(\cancel{ 2 }(x+a)) \right]
$$
$$
-\frac{ \partial \phi }{ \partial x } =-Gm\left[ \frac{x-a}{((x-a)^{2}+y^{2})^{3/2}}+ \frac{x+a}{((x+a)^{2}+y^{2})^{3/2}} \right] = g_{y}
$$

![[Attachments/Pasted image 20240216101913.png]]
## Example 1
Gravitational field produced by a thin layer of material spread over an infinite plane

![[Attachments/Pasted image 20240216101930.png]]
Where $\sigma$ is mass/unit area

We have divided the plane into a series of rings of radius R and thickness dR

Area ring $2\pi RdR$
Mass ring
$$
dm=\sigma 2\pi RdR
$$
Potential @ point P
$$
d\phi = -\frac{Gdm}{r}=-\frac{G\sigma 2\pi RdR}{(z^{2}+r^{2})^{1/2}}
$$
$$
\phi = \int  \, d\phi = - G\sigma_{2}p \int\limits_{0}^{\infty} \frac{R}{(z^{2}+R^{2})^{1/2}} \, dR
$$
Do u-sub
$$
u = z^{2}+ R^{2}
$$
$$
du = 2RdR
$$
$$
	\frac{1}{2} \int \frac{du}{u^{1/2}} = \cancel{ \frac{1}{2 }2 }u^{1/2} = u^{1/2}
$$

$$
\phi = -G\sigma 2\pi(z^{2}+R^{2})^{1/2}|^{\infty}_{0}
$$
$$
=-G\sigma_{2}\pi \infty + G\sigma 2\pi z
$$
$$
\phi = G\sigma 2\pi(z-\infty)
$$
However, we don't care about the potential. We are only interested in the potential difference

$$
\vec{g} = -\vec{\nabla}\phi
$$
relative to the plane 
$$
\phi=G\sigma{2}\pi(z-\infty) + G\sigma2\pi \infty
$$
This is the process of re-normalizing
$$
\phi = G\sigma 2\pi z
$$
$$
\vec{g} = -\vec{\nabla} \phi
$$
$$
\vec{g} = -2G\sigma \pi
$$
$$
=-2\pi G\sigma
$$
above and below the plane

![[Attachments/Pasted image 20240216101942.png]]

## Example 2 
2- body central force problem (using [[Lagrangian Mechanics]])

![[Attachments/Pasted image 20240216101952.png]]
$$
L = T-U = \frac{1}{2}m_{1}\vec{r}_{1}^{2}  +\frac{1}{2}m_{2}\vec{r}_{2}^{2} - u(\vec{r} _{2} - \vec{r}_{1})
$$

> What is a central force, really?

Generalized coordinates $\vec{R}$ and $\vec{r}$

$$
\vec{R} = \frac{m_{1}\vec{r}_{1} + m_{2}\vec{r}_{2}}{m_{1}+m_{2}} \text{ (C.O.M)}
$$
$$
\vec{r} = \vec{r}_{2} + \vec{r}_{1}
$$
$$
\vec{r} = \vec{R} - \frac{m_{2}}{M}\vec{r} , \ \ \vec{r}_{2} = \vec{R} + \frac{m_{1}}{M}\vec{r}
$$
with  $M = m_{1}+m_{2}$

$$
\vec{\dot{r}}_{1} = \vec{\dot{R}}  - \frac{m_{2}}{m} \vec{\dot{r}}, \ \ \ \vec{\dot{r}}_{2} =\vec{\dot{R}} + \frac{m_{1}}{m}\vec{\dot{r}}
$$
$$
\vec{\dot{r}}_{1}^{2} = \vec{\dot{R}}^{2} + \frac{m_{2}^{2}}{m_{2}} \vec{\dot{r}}^{2} - 2 \frac{m_{2}}{m}\vec{\dot{R}} 
$$
etc etc for $\dot{\vec{r}}_{2}$
$$
L = \frac{m_{1} + m_{2}}{2}\dot{\vec{R}}^{2} + \frac{1}{2} \frac{m_{1}m_{2}}{m_{1}+m_{2}} \dot{\vec{r}}^{2}-u(|\vec{r}|)
$$
Inspect second element
$$
\frac{1}{2} m_{1} \frac{m_{2}^{2}}{m_{2}} \dot{\vec{r}}^{2} + \frac{\frac{1}{2 }m_{2}m_{1}^{2}}{m_{2}}\dot{\vec{r}}^{2}
$$
$$
=\frac{1}{2} \frac{\dot{\vec{r}}^{2}}{m^{2}} (m_{1}m_{2}^{2}+m_{1}^{2}m_{2})
$$
$$
 = \frac{1}{2} \frac{m_{1}m_{2}}{M^{2}}\dot{\vec{r}}^{2} (m_{2}+m_{1}) = \frac{1}{2} \frac{m_{1}m_{2}}{M} \dot{\vec{r}}^{2}
$$
$$
\frac{m_{1}m_{2}}{M} = \mu \text{ Reduced mass}
$$
Equations of motion 
for $\vec{R}$
$$
\frac{ \partial L }{ \partial \dot{R} }  = 0
$$
This means that R is a [[cyclic coordinate]]. Aka, the Lagrangian is invariant under translation of R.
$$
\vec{P} = M \dot{\vec{R}}
$$
$$
\frac{d}{dt} \frac{ \partial L }{ \partial \vec{R} }  = 0
$$
Motion of COM moves at constant velocity

This permits the reduction of the two body system (central force problem) to a one body problem by dropping the $\frac{1}{2}(m_{1}+m_{2})\dot{\vec{R}}^{2}$ term. 



