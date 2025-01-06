---
dg-publish: true
---
## Central forces and the Hamiltonian
$$
H = T + u
$$
$$
H = \sum_{i} \dot{q}_{i} \frac{ \partial L }{ \partial \dot{q}_{i} } -L
$$
$$
L = T-u
$$
$$
\frac{ \partial L }{ \partial \dot{q}_{i} } =P_{i}
$$
$$
L = \frac{1}{2}m\dot{x}^{2} - u 
$$
$$
\frac{ \partial L }{ \partial \dot{x} } = m\dot{x}= P
$$
$$
\dot{x} = \frac{P}{m}
$$
$$
H = \dot{x}m\dot{x} = \frac{1}{2}m\dot{x}^{2}+u
$$
$$
=\frac{1}{2}m\dot{x}^{2}+u
$$
$$
= \frac{P^{2}}{2m} + u
$$
Hamiltonian form: 
$$
H(q,P,t)
$$
$$
\frac{ \partial H }{ \partial q_{i}  }  =  - P_{i}
$$
$$
\frac{ d H }{ d P_{i} }= \dot{q}
$$
$$
L = \frac{1}{2} \frac{m_{1}m_{2}}{m_{1}+m_{2}} - u(|\vec{r}|) = \frac{1}{2}\mu  \dot{\vec{r}}^{2}  - u(|\vec{r})
$$
$$
\frac{dL}{dt} = 0
$$
Energy is conserved, $E\equiv \text{Constant}$

Spherical symmetry of the problem implies that angular momentum $\vec{L}$ is conserved

$$
\vec{L}=\text{constant}
$$
Therefore $\vec{r}$, $\vec{p}$ are in the same plane

[[Central Forces]] -> motion in a plane

Using [[Polar Coordinates]] example
$$
x = r\cos\theta , \ \ \dot{x} = -r\dot{\theta}\sin\theta + \dot{r}\cos\theta
$$
$$
y = r\sin\theta, \ \ \dot{y} = r\dot{\theta}\sin\theta + \dot{r}\sin\theta
$$
$$
\dot{\vec{r}}^{2} = (\dot{x}^{2} + \dot{y}^{2})= \dot{r}^{2} + r^{2}+r^{2}\dot{\theta}^{2}
$$
$$
L = \frac{1}{2 } \mu (\dot{r}^{2} + r^{2}\dot{\theta}^{2}) - u(r)
$$
Do [[Euler-Lagrange Equation]]

$$
\frac{d}{dt} \frac{ \partial L }{ \partial   \dot{r} }- \frac{ \partial L }{ \partial r }  = 0 
$$
$$
\frac{d}{dt} \frac{ \partial L }{ \partial   \dot{r} }  = \mu \ddot{r}
$$
$$
\frac{ \partial L }{ \partial r } = \mu r\dot{\theta}^{2} + \frac{ \partial u }{ \partial r  } 
$$
$$
\mu  \ddot{r}- \mu r\dot{\theta}^{2}+ \frac{ \partial u }{ \partial r } =0 \tag{1}
$$
$$
\frac{d}{dt} (\mu r^{2}\dot{\theta}) =0 \tag{2}
$$
Combining these two
$$
2\mu r \dot{r}\dot{\theta} + \mu r^{2} \ddot{\theta} =0
$$
This yields us 2 coupled differential equations for $r(t)$ and $\theta(t)$. We want to divorce these equations

$$
\theta(t)
$$
$$
\frac{d}{dt} (\mu r^{2}\dot{\theta}) = 0
$$
$$
\therefore \mu r^{2}\dot{\theta} = \text{const}
$$
$$
\frac{ \partial L }{ \partial \theta } =0 = \frac{d}{dt} \frac{ \partial L }{ \partial \dot{\theta} } = \frac{d}{dt} P_{\theta}  \to \frac{ \partial L }{ \partial \dot{\theta} } =P_{\theta}
$$
$$
\dot{\theta}= \frac{l}{\mu r^{2}} \tag{3}
$$
$$
\frac{ d \theta }{ d t }  = \frac{l}{\mu r^{2}} \implies \theta = \theta_{0} + \int \frac{l}{\mu r(t)^{2}} \, dt 
$$
Referencing equation 1 above, we can plug equation 3 into that
$$
\mu \ddot{r} - \frac{l^{2}}{\mu r^{3}} + \frac{ \partial u }{ \partial r }  = 0
$$
$$
\mu  \ddot{r} = \frac{l^{2}}{\mu r^{3}}-\frac{ \partial u }{ \partial  r} 
$$
Multiply by 1 ($\frac{\dot{r}}{\dot{r}}$)
$$
u \dot{r} \ddot{r} = \left( \frac{l^{2}}{\mu l^{3}} - \frac{ \partial u }{ \partial r }  \right) \dot{r} \tag{4}
$$
Analyzing LHS
$$
\mu  \dot{r}\ddot{r} = \frac{d}{dt} \left( \frac{1}{2} \dot{\mu}r^{2} \right)
$$
Analyzing RHS
$$
\frac{ d g(r) }{ d t } = \frac{ \partial g }{ \partial r }  \frac{ \partial r }{ \partial t } 
$$
Using these two, we can look at the equation 4 from above and use the chain rule example from above
$$
\left( \frac{l^{2}}{\mu r^{3}}-\frac{ \partial u }{ \partial r }  \right) \dot{r} = -\frac{d}{dt} \left( \frac{1}{2 } \frac{l^{2}}{\mu r^{2}} + u \right)
$$$$
\mu  \dot{r}\ddot{r}  = \left( \frac{l^{2}}{\mu r^{3}} - \frac{ \partial u }{ \partial r }  \right) \dot{r}
$$
$$
\frac{d}{dt}\left( \frac{1}{2}\mu  \dot{r}^{2} \right) = -\frac{d}{dt} \left( \frac{1}{2} \frac{l^{2}}{\mu r^{2}}+u \right)
$$
$$
\frac{d}{dt} \left( \frac{1}{2} \mu   \dot{r}^{2} + \frac{1}{2} \frac{l^{2}}{\mu r^{2}}+u \right) =0
$$
$E=$ constant
Compare to original E-L equation
$$
E=T+ u = \frac{1}{2}\mu(\dot{r^{2} + r^{2} \dot{\theta}^{2}})+u(r) = \frac{1}{2} \mu  \dot{r}^{2} + \frac{1}{2} \frac{l^{2}}{\mu^{2} r^{2} }+ u(r)
$$
Solve for $\dot{r}$
$$
\dot{r} = \pm \sqrt{ \frac{2}{\mu} \left( E-u-\frac{l^{2}}{2\mu r^{2}} \right) } = \frac{dr}{dt}
$$
$$
t = \int\limits_{r_{0}}^{r}  \frac{1}{\pm \sqrt{ E-u-\frac{l^{2}}{2\mu r^{2}} }} \, dr 
$$
Rearrange and integrate -> $r(t)$

Can find $\theta(r)$
$$
\dot{\theta}=\frac{ d \theta }{ d t } = \frac{l}{\mu r^{2}}
$$
$$
\frac{d\theta}{dr} = \frac{ d \theta }{ d t } \frac{ d t }{ d r } = \frac{\dot{\theta}}{\dot{r}}
$$
$$
d\theta = \frac{\dot{\theta}}{\dot{r}}dr
$$
$$
	\theta = \int  \frac{l}{\mu r^{2}}\left[ \frac{2}{\mu}\left( E-u-\frac{l^{2}}{2\mu r^{2}} \right) \right]^{-1/2} \, dr
$$
This will again depend on the potential for $u\propto r ^{n+1}$, $F(r) \propto r ^{n}$
for $n=1,2,3$

Solutions will be oscillating (sin & cos)

Orbits: ($r(\theta)$) 
Go back $r(t)$
$$
\mu \ddot{r} - \mu r \dot{\theta}^{2} + \frac{ \partial u }{ \partial r } =0
$$
$$
u \ddot{r} - \frac{l^{2}}{\mu r^{3}} = - \frac{ \partial u }{ \partial r } = F(r)
$$
$$
\frac{\mu d^{2}}{dt^{2}} r - \frac{l^{2}}{\mu r^{3}} = F(r)
$$
Aside time: 
$$
\frac{d\theta}{dt}=\frac{l}{\mu r^{2}}
$$
$$
\mu r^{2}d\theta = ldt
$$
	**or**

$$
\frac{d}{dt} = \frac{l}{\mu r^{2}} \frac{d}{d\theta}
$$
$$
\frac{d^{2}}{dt^{2}} = \frac{l}{\mu r^{2}}\frac{d}{dt} \left( \frac{l}{\mu r^{2}} \frac{d}{d\theta} \right)
$$
Putting this back in: 
$$
\mu  \frac{l}{ur^{2}} \frac{d}{d\theta}\left( \frac{l}{\mu r^{2}} \frac{ d r }{ d \theta }  \right) - \frac{l^{2}}{\mu r^{3} } = F(r)
$$
If we know the orbit $r(\theta)$ then we can express the force or vice versa: 
Solving for $r(\theta)$

$$
\frac{1}{r^{2}} \frac{ d r }{ d \theta }  = - \frac{ d  }{ d \theta } \frac{1}{r} 
$$
$$
\frac{l^{2}}{\mu}\left[ \frac{1}{r^{2}} \frac{d}{d\theta}\left( -\frac{d}{d\theta} \left( \frac{1}{r} \right) \right)-\frac{1}{r^{3}} \right] = F(r)
$$
$$
\frac{l^{2}}{\mu r^{2}} \left[ \frac{d^{2}}{d\theta^{2}} \left( \frac{1}{r} \right) +\frac{1}{r} \right] = -F(r)
$$
Centrifugal energy and the effective potential
$$
E-u - \frac{l^{2}}{2\mu r^{2}}
$$
Define potential energy $u_{e} = \frac{l^{2}}{2\mu r^{2}}$

$$
F_{e} = -\frac{ \partial u }{ \partial r }  = \frac{l^{2}}{\mu r^{3}}=\mu r\theta^{2}
$$
Effective potential
$$
v=u + \frac{l^{2}}{2\mu r^{2}}
$$
$$
F(r) = -\frac{k}{r^{2}}
$$
$$
V(r) = -\frac{k}{r} + \frac{l^{2}}{2\mu r^{2}}
$$
## Dynamics of systems of particles

Motion of the system = Motion of the center of mass of the system + the motion of particles relative to the center of mass

For $n$ particles of mass $m_{i}$ at positions $\vec{r}_{i}$ 
$$
\vec{R}_{cm} = \frac{\sum^{n}_{l=1} m_{i}\vec{r}_{i}}{\sum^{n}_{i=1} m_{i}}
$$
$$
=\frac{1}{M_{tot}} \sum^{N}_{i=1} m_{i}\vec{r}_{i}
$$
If instead we have a continuous distribution
$$
\vec{R}_{cm} = \frac{\int \vec{r}dm}{\int  \, dm } 
$$
$$
\rho = \frac{m}{v}
$$
$$
dm = \rho dV
$$
$$
=\frac{\int \vec{r}\rho \, dv }{\int \rho \, dv }
$$
For a variable mass density 
$$
\rho=\rho(r)
$$
Total linear momentum of a system
$$
\vec{P}_{tot} = \sum^{N}_{i=1} \vec{P}_{i}  = \sum^{N}_{i=1} m_{i} \vec{v}_{i}
$$
N particles of $\vec{P}_{i}$ momentum

Conservation of linear momentum
$$
\frac{d\vec{P}_\text{tot}}{dt}=0
$$
if $\vec{F}_\text{tot}=0$
and internal forces obey newtons 3rd law 
i.e $F_{ij}=-F_{ji}$

Velocity of center of mass
$$
\vec{V}_{com} = \frac{d\vec{R}_{com}}{dt} = \frac{1}{M_{tot}} \sum^{N}_{i=1} m_{i} \frac{d\vec{r}_{i}}{dt}= \frac{1}{m_{tot}} \sum^{N}_{i=1} m_{i}\vec{v}_{i}
$$
$$
=\frac{\vec{P}_{tot}}{M_{tot}}
$$
$$
\vec{P}_\text{tot} = M_\text{tot} \vec{V}_{com}
$$
Taking time derivatives of both sides to give external forces and acceleration via newtons second law

$$
\vec{P}_{tot} = M_{tot}\vec{V}_{com}
$$
$$
\frac{ d \vec{P}_{tot} }{ d t } = \vec{F}_\text{ext} = \frac{d}{dt} (M_\text{tot}\vec{V}_\text{com}) = M_\text{tot} \frac{d\vec{V}_\text{com}}{dt}
$$
$$
\frac{d\vec{V}_\text{cm}}{dt}=\vec{A}_\text{com} 
$$
Center of mass acceleration
External forces act on the center of mass
If there is rotation of the system then we must consider the total angular momentum of the system
$$
\vec{L}_\text{tot} = \vec{R}_\text{com} \times \vec{P}_\text{tot} + \sum^{N}_{i=1} \vec{r}_{i}' \times \vec{P}'_{i}
$$
The first term $\vec{R}_\text{com}\times \vec{P}_\text{tot}$ is angular momentum of the center of mass about the origin
The second term $\sum^{N}_{i=1} \vec{r}'_{i} \times \vec{P}_{i}'$ is the angular momentum of particles about the center of mass


