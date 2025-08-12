---
dg-publish: true
---
# Review
- We've touched upon oscillations when doing central force problems, in particular oscillations about an equilibrium position 
- We did this using Taylor expansions 
- We were trying to find a potential as a function of $x$ Taylor-expanded around a position 
$$
u(x) = u(x_{0}) + \frac{ d u }{ d x } |_{x_{0}} (x-x_{0}) + \frac{ d ^{2}u }{ d x^{2} } (x-x_{0})^{2}+\dots
$$
Where $x=x_{0}$ was the equilibrium position. 
- This tells us the potential at a point can be represented by a [[Taylor Series]]
### Forces
We can model the forces acting upon the object with 
$$
F = -\frac{du}{dx}
$$
where 
$$
\frac{ d u }{ d x } = 0 + \cancelto{ 0 }{ \frac{d}{dx}\left[ \frac{du}{dx}|_{x_{0}} (x-x_{0}) \right] } + \frac{d}{dx}\left[ \frac{1}{2!} \frac{d^{2}u}{dx^{2}}|_{x_{0}} (x-x_{0})^{2} \right]+\dots
$$
For oscillations about equilibrium point, the second term always goes to 0 as per above.

$$
F = -\frac{du}{dx} = -\frac{d}{dx} \left[ \frac{1}{2} \frac{d^{2}u}{dx^{2}} | _{x_{0}} (x-x_{0})^{2} \right] = m \ddot{x}
$$
$$
\implies -\frac{d^{2}u}{dx^{2}} |_{x_{0}} (x-x_{0}) = m \ddot{x}
$$
Now onto new material

# Starting with force
Slight difference from above, we start with force instead of potential

$$
F(x)=F(x_{0}) + \frac{dF}{dx}|_{x_{0}} (x-x_{0}) + \frac{1}{2} \frac{d^{2}F}{dx^{2}}|_{x_{0}} (x-x_{0})^{2}+\dots
$$

![[Attachments/Pasted image 20240326083154.png]]

At point $x_{0}$ ,$F(x_{0})=0$. At equilibrium the force vanishes so the particle doesn't leave equilibrium. Then we can ignore order $x^{2}$ in the force Taylor expansion. This would be order $x^{3}$ in the potential expansion. 

We get 
$$
F(x) = \frac{dF}{dx}|_{x_{0}} (x-x_{0}) = -k(x-x_{0})
$$
Where 
$$
\frac{dF}{dx} |x_{0} = -k
$$

This looks like Hooke's law. Gives solutions for oscillations, but only small ones. 
Life is sometimes complicated... 

# Simple Harmonic Oscillator (SHO)

$$
F=m \ddot{x} = -kx
$$
We will define $\omega_{0}^{2}$ as $\frac{k}{m}$

Rearrange: 
$$
\ddot{x} = -\omega_{0}^{2}x
$$
or
$$
\ddot{x} + \omega_{0}^{2}x=0
$$
Solutions to above differential equations take the form of 
$$
x(t) = A\cos(\omega t+\phi)
$$
From this position we can find kinetic and potential energies. 
Lets do that 

Kinetic energy is found by taking the time derivitave of force

$$
T=\frac{1}{2}m\dot{x}^{2} = \frac{1}{2}m[\omega_{0}^{2}A^{2}\sin ^{2}(\omega t-\phi)]
$$
$$
= \frac{1}{2}kA^{2}\sin ^{2}(\omega t-\phi)
$$
Potential energy is calculated from work. 
$$
d\omega = -Fdx = kxdx
$$
Integrate both sides 
$$
\int  \, d\omega = -Fdx = \int kx \, dx
$$
$$
u=\frac{1}{2}kx^{2}
$$
$$
=\frac{1}{2}kA^{2}\cos ^{2}(\omega t-\phi)
$$
$$
E=T+U = \frac{1}{2}kA^{2}
$$
Where $A$ and $k$ are time independent.

Energy conservation !!

However, this is very idealized. Not everything is so nice in real life

We however can find some useful info from this, such as the 
period of oscillation (time to return to starting point)

$$
x(t) = A\cos(\omega t-\phi)
$$
Assuming $\phi=0$
$$
\to A\cos(\omega t)
$$
@ $t=0$ and $x=A$

This happens when $\omega \tau = 2\pi$
Period is given by:
$$
 \tau = \frac{2\pi}{\omega} = 2\pi \sqrt{ \frac{m}{k} }
$$
$\sqrt{ \frac{k}{m} }=\omega$ = angular frequency

And frequency is given by: 
$$
f= \frac{1}{\tau}
$$
Both period and frequency are functions of mass and the spring constant. They are independent of amplitude. 

> This is how they measure how heavy things are in space. they put astronauts in the astronaut oscillator. 

This is assuming small oscillations tho... so at larger amplitudes it densest quite work. 

So far we assumed an ideal system (no friction or slowing force)

This means oscillations should continue forever. This isn't super realistic, since it doesn't account for damping forces which stop the oscillator. 

#### yapping interlude 
yapping......... i wish people would wait for the professor to call on them................

more yapping.........

*larrrggeee very massive bodies* 
*yeah im talki-*
*what im saying is-*
*but anyway but-*

> cool sidenote on the fabric of spacetime from Dr. Martin

> *i think the way you explained it is a little odd*
> our favorite math major to Dr Martin

> *uhhh... are talking about hawking radiation or something else*
> (has absolutely nothing to do with hawking radiation)

> *sorry i love digging down physics rabbit holes... lets move on*


# Damped SHO
Assume the damping force is a function of the velocity and not position of the oscillator. 
To do this, add a term to our differential equation. 

$$
F=-kx
$$
Add damping 
$$
\vec{F}_{\alpha} = \alpha \vec{v} \to F=-b\dot{x}
$$
where $b>0$
This is the differential equation for damping
$$
m\ddot{x} + b\dot{x} + kx=0
$$
or 
$$
\ddot{x} + 2\beta \dot{x} + \omega_{0}^{2}x=0
$$
Where $\beta$ is known as the damping parameter 
$$
\beta = \frac{b}{2m}
$$
$$
\omega_{0}=\sqrt{ \frac{k}{m} }
$$

The roots of the damping differential equation are the following: 
$$
v_{1} = -\beta + \sqrt{ \beta^{2}-\omega_{0}^{2} }
$$
$$
v_{2}=-\beta - -\sqrt{ \beta^{2}-\omega_{0} }
$$
Solutions to the differential equation are: 
$$
x(t) = e^{-\beta t}[A_{1} e^{t\sqrt{ \beta^{2}-\omega_{0}^{2} }}+A_{2}e^{ -t\sqrt{ \beta^{2}-\omega_{0}^{2} }}]
$$

### 3 Interesting cases
> figure 2 

In the figure above, A is the over-damped case, B is the critically damped case, and C is the under-damped case

#### Under damping ($\omega_{0} > \beta^{2}$)
Condition for underdamping is given by:
$$
\omega_{1}^{2} - \omega_{0}^{2} -\beta^{2} >0
$$
Exponentials have imaginary exponents
$$
x(t) = e^{-\beta t}[A_{1}e^{i\omega_{1}t}+A_{2}e^{-i\omega_{1}t}]
$$
This can be rewritten as: 
$$
=Ae^{-\beta t} \cos(\omega_{1}t-\delta)
$$
Where the first segment $(Ae^{-\beta t})$ is known as the "envelope" and the second segment $\cos(\omega_{1}t-\delta)$ is the oscillations

NB: $\omega_{1}\neq\omega_{0}$ unless $\beta=0$

Different angular frequency means different periods/frequency 

Period is longer for damped then un-damped oscillations. 
#### Critical Damping ($\omega_{0}^{2} = \beta^{2}$)
Critical damping occurs when 
$$
\omega^{2} = \beta^{2}
$$
$$
x(t) = (A+Bt)e^{-\beta t}
$$
This approaches 0 more quickly then the other 2 cases.  [[Brachistachrone Problem]]?
Useful for some physical setups. e.g galvanometer.

screen doors....



#### Over Damping ($\omega_{0}^{2} < \beta^{2}$)
The condition for an overdamped system is 
$$
\omega_{0}^{2}<\beta^{2}
$$
$$
x(t) = e^{-\beta t}[A_{1}e^{t\sqrt{ \beta^{2}-\omega_{0}^{2} }}+A_{2}e^{-t\sqrt{ \beta^{2}-\omega_{0}^{2} }}]
$$
$$
\omega_{2} = \sqrt{ \beta^{2}-\omega_{0}^{2} }
$$
This $\omega_{2}$ is not angular frequency

no oscillations in this case.



# Driven, Damped SHO
We are going to use a sinusoidal function as our applied force. 
Our driving force given by $F_{0}\cos(\omega t)$

Putting this into SHO equation
$$
F = -kx -b \dot{x} + F_{0}\cos(\omega t)
$$
Rewritten
$$
m\ddot{x} + b\dot{x} + kx = F_{0}\cos(\omega t)
$$
$$
A = \frac{F_{0}}{m}
$$
$$
\ddot{x} + 2\beta \dot{x} \omega_{0}^{2}x= A\cos(@wt)
$$
Where $\omega$ is the angular frequency of the driving force 

Solutions to this have a complimentary function
$$
x_{c}(t)
$$
by setting the right to 0

Same as before 
$$
x_{c}(t) = e^{-\beta t} [A_{1}e^{t\sqrt{ \beta^{2}-\omega_{0}^{2} }}+A_{2}e^{-t\sqrt{ \beta^{2}-\omega_{0}^{2} }}]
$$

There is also a particular solution
$$
x_{p}(t) = D\cos(\omega t - \delta)
$$
Plugging this into the diffeq above: 
$$
[A-D[(\omega_{0}^{2}-\omega^{2})\cos\delta+2\omega\beta \sin\delta]] \cos(\omega t)
$$
$$
-D[(\omega_{0}^{2}-\omega^{2})\sin\delta-2\omega\beta \cos\delta] \sin(\omega t)=0
$$
Have orthogonal functions (sin and cos)

coefficients have to vanish to be true 

from $\sin(\omega t)$ term
$$
\tan\delta = \frac{2\omega \beta}{\omega_{0}^{2}-\omega^{2}}
$$
This can be rewritten using trig identities: 
>fig 3


$$
\sin\delta=\frac{2\omega\beta}{\sqrt{ (\omega_{0}^{2}-\omega^{2})+4\omega^{2}\beta^{2} }}
$$
$$
\cos\delta = \frac{\omega_{0}^{2}-\omega^{2}}{\sqrt{ (\omega_{0}^{2}-\omega^{2})+ 4\omega^{2}\beta^{2} }}
$$
From $\cos(\omega t)$
$$
D= \frac{A}{(\omega_{0}^{2}-\omega^{2})\cos\delta+2\omega\beta \sin\delta}
$$
$$
=\frac{A}{\sqrt{ (\omega_{0}^{2}-\omega^{2})^{2} +4\omega^{2}\beta}}
$$
so:
$$
x_{1}(t) = \frac{A}{\sqrt{ (\omega_{0}^{2}-\omega^{2})^{2}+4\omega^{2}\beta^{2} }} \cos(\omega t-\delta)
$$
Where 
$$
\delta = \arctan\left( \frac{2\omega\beta}{\omega_{0}^{2}-\omega^{2}} \right)
$$
$$
x(t) = x_{c}(t)+x_{p}(t)
$$
$x_{c}$ gets damped out
$x_{p}$ is the steady state term

$$
t \gg \frac{1}{\beta}
$$
$$
x(t) = x_{p}(t)
$$

See LC circuit SHO and LRC circut as damped oscillator
