---
dg-publish: true
---
### Uniform Circular motion
- You can use either Cartesian (x,y) or polar $(r,\theta)$coordinates
- Motion in x and y dependent on each other, 1 general coordinate
- Coordinate transform
$$
x=r\cos\theta
$$
$$
y=r\sin\theta
$$
[[forces of constraint]]
$$
r^{2}=x^{2}+y^{2}
$$
Particle confined to circle of radius $r$


- 2 Coordinates describe the position of the ball
- 1 force of constraint
- Therefore, 1 degree of freedom
- A suitable generalized coordinate is the polar coordinate $\theta$

Solving the Lagrangian

$$
L = \frac{1}{2}mv^{2}
$$
$$
v = \dot{x}^{2} + \dot{y}^{2}
$$
$$
\dot{x} = -r \dot{\theta}\sin\theta
$$
$$
\dot{y} = r \dot{\theta}\cos\theta
$$
$$
L  = \frac{1}{2} m(r^{2} \dot{\theta}^{2}\sin ^{2}\theta+ r^{2}\dot{\theta}^{2}\cos ^{2}\theta)
$$
$$
L = \frac{1}{2}mr^{2}\dot{\theta}^{2}
$$
$$
\frac{ \partial L }{ \partial \theta } =0
$$
$$
\frac{d}{dt} \frac{ \partial L }{ \partial \dot{\theta} } =mr^{2}\ddot{\theta}
$$
$$ 
mr^{2}\ddot{\theta}= 0 \therefore \ddot{\theta} =0
$$
>Solving for init. conditions
$$
\dot{\theta} = \text{ constant} = c_{1}
$$
$$
\theta = c_{1}t+c_{2}
$$
Given: 
$$
\theta(t=0) = \theta_{0}
$$
$$
\dot{\theta}(t=0) = \omega_{0}
$$
$$
\theta(t) = \omega_{0}t + \theta_{0}
$$

Another example!
Consider a ball of mass m on a uniformly rotating bar in 
a force-free space (no gravity, no friction). Bar is confined to rotate in the x-y plane

Physics: Ball will move radially outward due to centripetal acceleration. 

Constraint: ball can only move on the bar $r(t)$

$$
L = \frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2})
$$
$$
x = r\cos(\omega t); \ \ \dot{x} = -r\omega \sin(\omega t)+\dot{r}\cos(\omega t)
$$
$$
y = r\sin(\omega t); \ \ \dot{y} = r\omega \cos(\omega t)+ \dot{r}\sin (\omega t)
$$
$$
L = \frac{1}{2}m[r^{2}\omega^{2}\sin ^{2}(\omega t)+\dot{r^{2}}\cos ^{2}(\omega t)-2r \dot{r}\sin(\omega t)\cos(\omega t)+r^{2}\omega^{2}\cos ^{2}(\omega t)\dots
$$
$$
+ \dot{r^{2}}\sin ^{2}(\omega t)+2r \dot{r} \omega \sin(\omega t)\cos(\omega t)
$$
$$
L = \frac{1}{2}m[\dot{r}^{2}+r^{2}\omega]
$$
>Generalized Coordinate is r, so only 1 [[Euler-Lagrange Equation]]
$$
\frac{d}{dt} \frac{ \partial L }{ \partial   \dot{r}  } = m \ddot{r} 
$$
$$
\frac{ \partial L }{ \partial r }  = mr\omega^{2}
$$
$$
m \ddot{r} - mr\omega^{2}=0
$$
$$
m \ddot{r} = mr\omega^{2}
$$
>This is force=centripetal acceleration
$$
\omega=\frac{v}{r} \to \omega^{2} = \frac{v^{2}}{r^{2}}
$$
>Time to solve diffeq
$$
r \propto e^{\omega t}
$$

$$
\dot{r} \approx \omega e^{\omega t}
$$
$$
\ddot{r} \approx \omega^{2}e^{\omega t} - \omega^{2}r
$$
$$
r(t) = Ae^{\omega t} + Be^{-\omega t}
$$
$$
r(t=0) = r_{0}
$$
$$
\dot{r}(t=0)= 0
$$
$$
\dot{r} (t) = A\omega e^{\omega t}-B\omega e^{-\omega t}
$$
$$
\ddot{r}(t) = A\omega^{2} e^{\omega t} + B\omega^{2}e^{-\omega t}
$$
$$
\omega^{2}r(t)
$$
$$
r(t=0)=Ae^{0} + Be^{0}=r_{0}
$$
$$
\dot{r}(t=0)=A\omega e^{0}-B\omega e^{0} = A\omega - B\omega = 0 \therefore A - B =0 
$$
$$
A = B = \frac{r_{0}}{2}
$$

#### Example: Rolling without slipping
Linear vs. rotational variables
$$
v_{t} = R\dot{\theta}
$$
$$
ds = Rd\theta
$$
$$
v = \frac{ds}{dt} = R \frac{d\theta}{dt} = R \dot{\theta}
$$
$$
a_{t} = R_{\alpha}
$$
Rolling without slipping implies that we can describe the system as the motion of the center of mass and the rotation about the center of mass. 
Rolling = translational + rotational

The object is doing 2 things. 

Rolling without slipping $v_{com} = R\dot{\theta} = V_{t}$

Example: 
Consider a disk rolling down an inclined plane. Constraint of rolling without slipping, and $\phi$ is constant. ($\phi$ is the slope of the inclined plane). 

Constraint is integrable!

$$
\dot{x} = R\dot{\theta} = x = R\theta
$$
Equation of constraint
$$
x-R\theta= 0
$$
Kinetic energy: 
$$
T=\frac{1}{2}m\dot{x}^{2} + \frac{1}{2}I\dot{\theta}^{2}
$$
Potential energy: 
$$
u = -Mgx\sin(\phi)
$$
$$
u=Mg(l-x)\sin \phi
$$
$$
L = T- u = \frac{1}{2}M\dot{x}^{2} + \frac{1}{2}I\dot{\theta}^{2} - (g(l-x))\sin \phi
$$
1. We can substitute $\dot{\theta}=\frac{\dot{x}}{R}$ or $\dot{x} = R\dot{\theta}$
2. Use method of [[Lagrange Multipliers]] (cooler method) to change L to 
$$
\tilde{L} = \frac{1}{2} M\dot{x}^{2} + \frac{1}{2}I\dot{\theta}^{2} -Mg(l-x)\sin\theta + \lambda(x-R\theta)
$$
We can go through this expression and come up with two equations of motion. There will be a $\lambda$ term in each of the equations of motion. We can use the constraint and $\lambda$ to solve and work through this problem. Use the constraints to destroy the constraints. $\lambda$ will be "something" that has meaning. yippee








