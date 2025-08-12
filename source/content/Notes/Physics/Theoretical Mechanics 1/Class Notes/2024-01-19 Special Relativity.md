---
dg-publish: true
---
## Special Relativity 
Velocity addition 
$$
v' = \frac{u-v}{1-\frac{uv}{^{2}}}
$$

u=c example shows c is constant 
If c is constant, scalar product of the 4-vector with itself is invariant under Lorentz transform
$$
\vec{x}' \cdot \vec{x}' = \vec{x} \cdot \vec{x}
$$
$$
\vec{x} \cdot \vec{x} = x_{1}^{2} + x_{2}^{2}+ x_{3}^{2}-c^{2}t^{2}
$$
Tensors are matrices
Minkowski Tensor
$$
\mu_{\nu}=\begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & -1
\end{pmatrix}
$$

$$
\vec{x} \cdot \vec{x} = x \mu_{\nu} x^{\nu}
$$
Test: 
$$
x_{1}'=\gamma x_{1}-\gamma\beta ct
$$
$$
x_{2}' = x_{2}
$$
$$
x_{3}'=x_{3}
$$
$$
ct'-\gamma\beta x_{1}+\gamma ct
$$
$$
x_{1}'^{2}=(\gamma x_{1}-\gamma\beta ct)^{2} = \gamma^{2}x_{1}^{2}+\gamma^{2}\beta^{2}c^{2}t^{2}-2\gamma^{2}\beta x_{1}ct
$$
$$
x_{2}'^{2} = x_{2}^{2}
$$
$$
x_{3}'^{2}=x_{3}
$$
$$
c^{2}t^{2} = (-\gamma\beta x_{1} + \gamma ct)^{2}=\gamma^{2}\beta^{2} x_{1}^{2} + \gamma^{2}c^{2}t^{2}-2\gamma^{2}\beta x_{1}ct
$$
$$
\vec{x}' \cdot \vec{x}' = x_{1}'^{2} + x_{2}'^{2} + x_{3}'^{2} - c^{2}t^{2}
$$
$$
=\gamma^{2}x_{1}^{2}+\gamma^{2}\beta^{2}c^{2}t^{2} - 2\gamma^{2}\beta x_{1}ct+x_{2}^{2}+x_{3}^{2}-\gamma^{2}\beta^{2}x_{1}^{2}-\gamma^{2}c^{2}t^{2}+2\gamma^{2}\beta x_{2}ct
$$
$$
=\gamma^{2}x_{1}^{2}(1-\beta^{2})+x_{2}^{2}+x_{3}^{2}-\gamma^{2}c^{2}t^{2}(1-\beta^{2})
$$
$$
\to =x_{1}^{2} + x_{2}^{2} + x_{3}^{2}-c^{2}t^{2} = \vec{x} \cdot \vec{x}
$$
Invariant!
## Relativistic Mechanics
### Newtons laws of motions
#### 1st law of motion:
Object at rest stays at rest
Object in motion stays in motion
If no net external forces
$\vec{F} = 0$, $\vec{v} = \text{constant}$.
- Also valid in relativity
#### 2nd law of motion
$\vec{F} =m\vec{a} = \frac{d}{dt}\vec{p}$
If constant $\vec{F}$ then constant $\vec{a}$
$v = at \to \infty$
as $t\to \infty$
**This is not allowed!** 
$v \leq c$ must be true

Requires momentum modification:
$$
p=mv \to p=\gamma mv
$$
This is relativistic momentum.
Mass is function of velocity now:
$$
m(v) = \frac{m}{\sqrt{ 1-\frac{v^{2}}{c^{2}} }}
$$
	$m(v=0)$ is the "rest mass " of the object

As speed increases, mass functionally increases
As it approaches the speed of light, mass reaches infinity
	 if you were able to accelerate at $9.8 \frac{m}{s^{2}}$ in perpetuity, youd reach c in about a year

$$
\vec{F} = \frac{d\vec{p}}{dt} = m \frac{d}{dt}  \frac{\vec{v}}{\sqrt{ 1-\frac{v^{2}}{c^{2}} }}
$$

In the limit of $v \ll c$, should get $F=ma$
Denominator goes to $\approx 1$, so you get $\vec{F}=m\vec{v}\frac{d}{dt}$  which is equivalant to 
$$
\vec{F} = m\vec{a}
$$
#### Newtons 3nd law
Third law pairs
Equal and opposite forces
This is valid for contact forces
	Friction, impact etc etc
This is not valid for non-contact forces at a distance
	Gravity 
The force of gravity doesn't travel faster then the speed of light
If something moves at a significant portion of the speed of light, its gravitational potentials may move slow enough to cause discrepancies
- Takes time for things to propagate and update and space is big


## Relativistic Kinetic Energy
$$
T=mc^{2}(\gamma-1) = mc^{2}\gamma-mc^{2}
$$
Derived from work-energy theorem using relativistic momentum $p=\gamma mv$
Rest Energy: 
$$
E_{0} = mc^{2}
$$
Total energy of the system:
$$
E=\gamma mc^{2}
$$
$$
E=T+mc^{2} = mc^{2}\gamma-mc^{2}+mc^{2}
$$
Multiply both sides of relativistic by c and square
$$
c^{2}p^{2} = \gamma^{2}m^{2}v^{2}c^{2} = \gamma^{2}m^{2}c^{4} \frac{v^{2}}{c^{2}}
$$
$$
g^{2} = \frac{1}{1-\frac{v^{2}}{c^{2}}}
$$
$$
\frac{v^{2}}{c^{2}} = 1- \frac{1}{\gamma^{2}}
$$
$$
c^{2}p^{2} = g^{2}m^{2}c^{4} \left( 1-\frac{1}{\gamma^{2}} \right)
$$
$$
=\gamma^{2}m^{2}c^{4} - m^{2}c^{4}
$$
$$
c^{2}p^{2} = E^{2}-E_{0}^{2}
$$
$$
E^{2} = c^{2}p^{2} + E_{0}^{2}
$$
For a mass-less particle: 
$$
E = cp
$$
$$
E=h\nu = \frac{hc}{\lambda}
$$
$$
\frac{h}{\lambda}= p
$$
This agrees with quantum physics!

For case of non-relativistic speeds $(v\ll c)$, then relativistic kinetic energy should reduce to 
$$
\frac{1}{2} mv^{2}
$$
$$
T=mc^{2}(\gamma-1)
$$
$$
\gamma = \frac{1}{\sqrt{ 1-\frac{v^{2}}{c^{2}} }}
$$
Taylor expansion of $\gamma$
$$
\gamma = \frac{1}{\sqrt{ 1-\frac{v^{2}}{c^{2}} }} \approx \frac{1}{ (1-x)^{1/2}}
$$
First equation turns into
$$
=1+\frac{1}{2} \frac{v^{2}}{c^{2}} + 0 \left( \frac{v^{4}}{c^{4}} \right)
$$
Ignoring higher orders
$$
T=mc^{2}\left( 1+\frac{1}{2} \frac{v^{2}}{c^{2}} \dots  \right)
$$
$$
T=\frac{1}{2}mv^{2}
$$
Work energy theorem to get kinetic energy
$$
\Delta T  = w = \int F \, dx 
$$
$$
F = \frac{dp}{dt} \cdot \frac{dx}{dx}
$$
$$
F_{dx} = dpv
$$
$$
p =\gamma mv = \frac{mv}{\sqrt{ 1-\frac{v^{2}}{c^{2}} }}
$$
$$
dp =\frac{mdv}{\sqrt{ 1-\frac{v^{2}}{c^{2}} }} + \frac{mv\left( -\frac{1}{2} \right)\left( -2 \frac{v}{c^{2}}dv \right)}{\left( 1-\frac{v^{2}}{c^{2}} \right)^{3/2}}
$$
$$
dp = \gamma mdv + \frac{mv^{2}}{c^{2}}
$$
$$
=\gamma mdv\left( 1+\gamma^{2} \frac{v^{2}}{c^{2}} \right)
$$
$$
=\gamma mdv \gamma^{2}
$$
$$
\gamma^{2} = \frac{1}{1-\frac{v^{2}}{c^{2}}}
$$
$$
\gamma^{2} \frac{v^{2}}{c^{2}} = \frac{v^{2}}{\left( 1-\frac{v^{2}}{c^{2}} \right)c^{2}}
$$
$$
=\frac{v^{2}}{c^{2}-v^{2}}
$$
$$
1+ \gamma^{2} \frac{v^{2}}{c^{2}} = 1 + \frac{v^{2}}{c^{2}-v^{2}}=\frac{c^{2}-v^{2}}{c^{2}-v^{2}} + \frac{v^{2}}{c^{2}-v^{2}}
$$
$$
=\frac{c^{2}}{c^{2}-v^{2}} \frac{\frac{1}{c^{2}}}{\frac{1}{c^{2}}} = \frac{1}{1-\frac{v^{2}}{c^{2}}} = \gamma^{2}
$$
$$
dp = \gamma^{3} mdv
$$
$$
\Delta T = \int v \, dp = \int m\gamma^{3}v \, dv 
$$
$$
=m\int \frac{v}{\left( 1-\frac{v^{2}}{c^{2}} \right)^{3/2}} \, dv 
$$
$$
\to \frac{c^{2}}{\sqrt{ 1-\frac{v^{2}}{c^{2}} }}
$$
Integrate from 0 to T and from 0 to v
$$
m\left[ \frac{c^{2}}{\sqrt{ 1-\frac{v^{2}}{c^{2}} }} - \frac{c^{2}}{1} \right ] 
$$
$$
T=mc^{2}(\gamma-1)
$$
### Lorentz Transformation Derivation
If a light pulse is emitted from a flashbulb from a common origin of $k$ and $k'$ when they are coincident then from postulate 2 (c is constant value in all frames) the wavefronts in each system is described by the following

$$
\sum^{3}_{i=i} x^{2}_{i} -c^{2}t^{2} = 0
$$
These are eq1
$$
\sum^{3}_{i=1} x_{i}'^{2}-c^{2}t^{2} = 0
$$
This comes from the invariance. The rate of the pulse is $ct$
(dot product of 4-vector using the +++- conversion )

	*insert picture here*

Recall from Galileo transforms 
$$
x_{1}' = x_{1}-vt
$$
$$
x_{2}' = x_{2}
$$
$$
x_{3}' = x_{3}
$$
$$
t'=t
$$
and that using eq.1 in accordance with the postulates of relativity can not be reconciled

Einstein's contribution was that Galileo transformation was *approximately* correct

We confined movement to the positive x direction for the k' system meaning y'=y and z'=z

At t=t'=0 the flashbulb goes off, the position of the 0' origin (of k' system) is measured to be $x=vt$ (w.r.t the k system), or $x-vt = 0$

In the k' system the origin 0' is at x'=0

So at t=t'=0 set them equal 
$$
x' = x-vt
$$

But we know that the Galileo transform is incorrect
So we can add a coefficient to the transform. We could call it gamma...
It would depend on v and is independent of x,x',t,t'

$$
x' = \gamma(x-vt) 
$$
Eq. 2

We can describe motion in k with origin o in terms of k'

Postulate I demands that the laws of physics be the same in both reference frames
$$
\gamma = \gamma'
$$

Relativistic Meter stick problem:
How long is the meterstick?
At a 45 degree angle

### Continued on 1-23

$$
x'=\gamma(x-vt)
$$
$$
x=\gamma(x'+vt')
$$
Sub top equation into above equation and solve for t
$$
x=\gamma[\gamma(x-vt)+vt']
$$
$$
x=\gamma^{2}(x-vt)+\gamma vt'
$$
$$
x=\gamma^{2}(x-vt)+\gamma vt'
$$
$$
x=\gamma^{2}x-\gamma^{2}vt+\gamma vt'
$$
$$
\gamma vt' = x-\gamma^{2}x + \gamma^{2}vt
$$
$$
t' = \gamma t + \frac{x}{\gamma v}(1-\gamma^{2})
$$
The speed of light is the same in both frames

Position of flashbulb pulse:
$$
x=ct
$$
$$
x'=ct'
$$
Now solve for $\gamma$ using substitutions

$$
\gamma = \frac{1}{\sqrt{ \left( 1-\frac{v^{2}}{c^{2}} \right) }}
$$
Also:
$$
t'=\gamma\left( t-\frac{xv}{c^{2}} \right)
$$
Time dilation
$$
\Delta t = \gamma \Delta t'
$$
Length contraction
$$
\Delta x = \frac{\Delta x'}{\gamma}
$$


