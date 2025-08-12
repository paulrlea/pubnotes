# Problem 1:
![[Attachments/Pasted image 20240428161358.png]]
## Part a: Calculate $F(x)$
We know that 
$$
F=MA = M \frac{dv}{dt}
$$
So we need to take the time derivative of the velocity, to find acceleration, to find force. 
We have velocity as a function of x, which can be expressed as a function of time. 
$$
V(x(t)) = \frac{\alpha}{x}
$$
We're gonna do some "funny math" to take the time derivative of velocity
$$
\frac{dv}{dt} = \frac{dv}{dt} \frac{dx}{dx}
$$
Multiply by "1" ($\frac{dx}{dx}$)
$$
\frac{dv}{dt} = \frac{dv}{dx} \frac{dx}{dt}
$$
We know the time derivative of position is velocity
$$
\frac{dv}{dt} = \frac{dv}{dx} v
$$
Now we just have to take the position derivative of velocity
$$
\frac{dv}{dt} = -\frac{\alpha}{x^{2}} v
$$
Subbing in $\frac{dv}{dt}$ for a, and $v$ for $v$
$$
a = -\frac{\alpha}{x^{2}} \frac{\alpha}{x}
$$
Plug into newtons second law 
$$
F(x) = m \left[ -\frac{\alpha^{2}}{x^{3}} \right]
$$
## Part B: Calculate X(t)
We can solve this by treating it like a separable differential equation
$$
\frac{dx}{dt} = \frac{\alpha}{x}
$$
Separate
$$
xdx = \alpha dt
$$
Integrate 
$$
\int x \, dx  = \int \alpha \, dt
$$
$$
\frac{x^{2}}{2} = \alpha t
$$
Solve for x
$$
x(t) = \sqrt{ 2\alpha t }
$$
The rest of this problem is pretty trivial. 
![[Attachments/Pasted image 20240428161510.png]]
# Problem 2: 

![[Attachments/Pasted image 20240428161544.png]]
## For part a: Finding the Lagrange Equations of Motion 
We need to define the degrees of freedom for this problem, there exists 2. 
$\theta$: angular position of mass $m$ on the table 
$r$: radial position of mass m on table, and coupled to mass M below table 

Now, we need to find our equations for kinetic and potential energy 
$$
T = \frac{1}{2}m( r\dot{\theta} )^{2} + \frac{1}{2}m \dot{r}^{2} + \frac{1}{2}M\dot{r}^{2}
$$
$$
U = Mg(l-r)
$$
$$
L = T - U
$$
$$
L = \frac{1}{2}m( r\dot{\theta} )^{2} + \frac{1}{2}m \dot{r}^{2} + \frac{1}{2}M\dot{r}^{2} - Mg(l-r)
$$
Use E-L equations
Solving for $\theta$
$$
\frac{d}{dt}  \frac{ \partial L }{ \partial \dot{\theta} }  - \frac{ \partial L }{ \partial \theta }  = 0
$$
$$
\frac{d}{dt} \left( 2 \frac{1}{2} m r^{2} \dot{\theta} \right) - 0 = 0 
$$
Product Rule
$$
2m\dot{r}\dot{\theta} + m r^{2} \ddot{\theta} = 0
$$
Simplify
$$
2\dot{r}\dot{\theta} + r \ddot{\theta}
$$

Solving for $r$
$$
\frac{d}{dt} \frac{ \partial L  }{ \partial \dot{r} } - \frac{ \partial L }{ \partial  r }  = 0
$$
$$
\frac{d}{dt} \left( \frac{1}{2} 2 m\dot{r} + \frac{1}{2}2 M\dot{r}\right) - \left[ \frac{1}{2}2 mr\dot{\theta}^{2} + Mgr\right] = 0
$$
$$
(m+M) \ddot{r} - mr \dot{\theta}^{2} + Mg=0
$$

## Part B: Solving for equilibrium separation

When $\dot{r}$ and $\ddot{r}$ is 0, the radius is constant

Setting $\ddot{r}$ to 0: 
$$
-mr\dot{\theta}^{2} + Mg = 0
$$
$$
Mg = mr\dot{\theta}^{2}
$$
$$
\frac{Mg}{m\dot{\theta}^{2}} = r_{0} 
$$







# Problem 3: 
![[Attachments/Pasted image 20240428161653.png]]


# Problem 4:
![[Attachments/Pasted image 20240428162046.png]]

(this will be in Cartesian coordinates tho so don't worry too much)

# Problem 5: 
![[Attachments/Pasted image 20240428162145.png]]

# Problem 6: 
Will likely be a plucked, struck string...  I couldn't find a good example, so just go through HW 11

