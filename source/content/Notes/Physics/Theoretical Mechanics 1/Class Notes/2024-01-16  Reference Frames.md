---
dg-publish: true
---

# Inertial Reference Frames

- Reference frames are used to describe the motion and position of...

... fill in later...



- Given a point $p$ @ $\vec{r} = \vec{r}(x,y,z)$, this same point can be described by $\vec{r}' = \vec{r}'=(x',y',z')$. 
- We can *transform* between these two coordinate systems using the vector $\vec{R}$, the vector between the two origins
- Time is the same in all frames for Galilean systems (absolute)
	- $t=t'$
- To find velocity, take time derivative
$$
\frac{d}{dt} (\vec{r}) = \frac{d}{dt} (\vec{r}'+\vec{R} ')
$$
$$
\frac{d\vec{r}}{dt}=\vec{v} = \frac{d\vec{r}'}{dt} + \frac{d\vec{R}'}{dt}
$$
$$
v =\vec{v}' + \vec{V}
$$
- Where $\vec{V}$ is the rate of change (velocity) of the distance between the two origins. 
- For acceleration
$$
\frac{d}{dt} (\vec{v}) = \frac{d}{dt}(\vec{v}' + \vec{V}')
$$
$$
\frac{d\vec{v}}{dt} = \vec{a}=\frac{d\vec{v}'}{dt} + \frac{d\vec{V}}{dt}
$$
$$
\vec{a} = \vec{a}' + \vec{A}
$$
- Acceleration in unprimed coordinate system is equal to acceleration in primed reference frame + $\vec{A}$
- An inertial reference frame is one in which the reference frame is **not** acceleration relative to another. $\vec{A}=0$

If Newtons laws of motions are invariant, (not changing) under a coordinate transform, then the frames are inertial. 
$$
\vec{F}'=\vec{F}
$$
Starting in unprimed frame
$$
\vec{F} = m\vec{a}
$$
Transformation 
$$
\vec{F} = m(\vec{a}'+\vec{A}')
$$
$$
=m\vec{a}' + m\vec{A}
$$
$$
\vec{F} = \vec{F}' + m\vec{A}
$$
$$
m\vec{a}=m\vec{a}' \text{ if} \ \vec{A}=0
$$
These frames can still move relative to one another as long as velocity is **constant**. 


# Special Relativity
- We must use relativistic mechanics when the velocities involved are significant fractions of $c$
- The speed of light is a universal constant, the same in all reference frames
	- $c=299,792,458 \frac{m}{s}$
	- Fine to use $3E8$
- This important fact means that our rule for velocity addition in different frames is incorrect
- The Galileo transformation violates $c=\text{constant}$ 
	- $c' \neq \vec{v} + c$
- Time is relative $t\neq t'$
- Our original rules are still valid for an approximation for $v\ll c$
- New set of coordinate transformations are needed which are in agreement with Einstein's insight that light moves at constant speed
## Lorentz Transformation 
$$
x' = \frac{x-vt}{\sqrt{ 1-\frac{v^{2}}{c^{2}} }}
$$

rOtAtIoN MatRiX

$$
y' = y
$$
$$
z'=z
$$
$$
t' = \frac{t- \frac{vx}{c^{2}}}{\sqrt{ 1-\frac{v^{2}}{c^{2}} }}
$$
also sometimes written with $\beta = \frac{v}{c}$
$$
t' = \gamma t - g \frac{vx}{c^{2}}
$$
- v is the relative speed of the two reference frames.
Reference frames cannot be traveling faster then the speed of light to each other. 

1. Classical mechanics take place in 3 dimensional space (euclidean space) with a separate time $t$
2. For special relativity we use 4-dimensional Minkowsky spacetime (4D spacetime)
		$x_{1} = x_{1}, \ x_{2}=y_{1}, \ x_{3}=z_{1}, \ x_{4}=ct$
		4 vectors: 
		
$$
\vec{x}=\begin{pmatrix}
x_{1} \\
x_{2} \\
x_{3} \\
x_{4}
\end{pmatrix} = \begin{pmatrix}
x \\
y \\
z \\
ct \\
\end{pmatrix}
$$
- Mathematically, 1 and 2 are equivalent
## The Lorentz Transformation
- Expressed as a 4x4 matrix, represented by $\Lambda$ such that $\vec{x}' = \Lambda \vec{x}$, with $\Lambda$ represented as
$$
\Lambda = \begin{bmatrix}
\gamma , 0 , 0 , -\beta\gamma \\
0,1,0,0 \\
0,0,1,0 \\
-\beta\gamma,0,0,\gamma
\end{bmatrix}
$$
- "Standard-boost" movement along x-axis
- So transforming position from the 4-vector gives 
$$
\vec{x}' = \Lambda \vec{x} = \begin{bmatrix}
\gamma,0,0,-\beta\gamma \\
0,1,0,0 \\
0,0,1,0 \\
-\beta\gamma,0,0,\gamma
\end{bmatrix}
\begin{bmatrix}
x \\
y \\
z \\
ct
\end{bmatrix} = \begin{bmatrix}
\gamma x + 0y +0z-\beta\gamma ct \\
0x+1y+0z+0ct \\
0x +0y+1z+0ct \\
-\beta\gamma x + 0y + 0z + \gamma ct
\end{bmatrix}=\begin{bmatrix}
\gamma x-\beta ct \\
y \\
z \\
-\beta\gamma x + \gamma ct
\end{bmatrix}
$$
$$
=\begin{bmatrix}
x' \\
y' \\
z' \\
ct' \\
\end{bmatrix}
$$

$$
x' = \gamma x-\gamma vt
$$
$$
y'=y
$$
$$
z'=z
$$
$$
ct' =-\frac{\gamma vx}{c} + \gamma ct
$$
We can also transform the velocities
The v in the equations above represents the speed between reference frames
$$
v'=\frac{dx'}{dt'}
$$
use primed position and time
$$
dx'=\frac{\partial x'}{\partial x}dx + \frac{\partial x'}{\partial t}dt
$$
$$
dt'=\frac{\partial t'}{\partial x}dx + \frac{\partial t'}{\partial t}dt
$$
Access partials
$$
\frac{\partial x'}{dx} = \gamma 
$$
$$
\frac{\partial x'}{\partial t} = -\gamma v
$$
$$
\frac{\partial t'}{dx} = -\frac{\gamma v}{c^{2}}
$$
$$
\frac{\partial t'}{\partial t} = \gamma
$$
$$
dx' = \gamma dx + (-\gamma v)dt
$$
$$
dt'=\left( -\frac{\gamma v}{c^{2}} \right)dx + \gamma dt
$$
$$
v' = \frac{dx'}{dt'} = \frac{dx-vdt}{-\frac{v}{c^{2}}dx + dt}
$$
$$
v' = \frac{\frac{dx}{dt}-c}{-\frac{v}{c^{2}} \frac{dx}{dt}+1} = \frac{\frac{dx}{dt}-v}{1-\frac{vdx}{c^{2}dt}}
$$


V is the speed of the x,y,z frame compared to x',y',z'

$$
\frac{dx}{dt} = u
$$
Where u is speed measured in x,y,z, frame with t clock

$$
v' = \frac{u-v}{1-\frac{uv}{c^{2}}}
$$
This is the velocity transformation!

