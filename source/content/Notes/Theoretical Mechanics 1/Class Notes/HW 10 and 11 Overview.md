
> Goal: To find the normal modes of a generalized coupled oscillating system and understand what they mean. I will attempt to do this by breaking down the HW problems 

# HW 10 
[[Physics/Theoretical Mechanics 1/HW/HW#10 2024.pdf|HW#10 2024]]
## Problem 1 

> The potential U is given for a three oscillator system. We are asked to find the eigenfrequencies and the physical interpretation of the system. 

Steps: 
- Find $A_{jk}$ matrix. 
$$
A_{jk} = \frac{ \partial^{2} U }{ \partial q_{j} \partial q_{k} } |_{0} 
$$
- When finding the $A_{jk}$ matrix, you index over the number of oscillators in the system. In this case it's 3, so we will have a 3x3 **Symmetric** matrix. Keep this in mind because it simplifies calculations 
- The order of differentiation shouldn't matter (symmetric matrix), we take a double partial derivative, first w.r.t the first index's generalized coordinate ($x_{i}$) , and then w.r.t the second indices' generalized coordinate $(x_{2})$. 
- After finding $A_{jk}$ matrix, the next step is to do some fun linear algebra. We have to find the square root of the eigenvalues for the system, because these are the eigenfrequencies
$$
\omega^{2} = \lambda
$$

Oh also there is a mass matrix. In the case where the masses are the same, its given simply by 
$$
\begin{matrix}
m & 0 & 0 \\
0 & m & 0 \\
0 & 0 & m
\end{matrix}
$$

Putting this together, we want to solve the following
$$
\det[\bar{A} - \omega^{2} \bar{m}] = 0
$$
Solving this for $\omega$ is... hairy but trivial. Remember your 3x3 determinant rules, and keep your numbers straight. 

We should get 3 eigenfrequencies from this, and we are asked the interpretation of the $\omega=0$ solution. Under this solution, there is no frequency, and therefore no oscillation. The physical interpretation of this means that the system is either moving linearly with constant velocity or is stopped. 

## Problem 2 

> Two equal masses, one on y-axis and one on the x-axis, with 3 springs connecting them. We are looking for the eigenfrequencies, eigenvectors and a verbal description of the system's normal modes. 

- Drawing a diagram is most helpful for this problem. I will steal Dr. Martin's and put it below

![[Pasted image 20240427181000.png]]

The procedure for this problem is similar to the first problem, with the caveat that we have to find the potential of the system. This is annoying but doable with a few math tricks, or sufficient time and determination. 

Starting with 
$$
U = \frac{1}{2}k(x^{2}+y^{2}) + \frac{1}{2}k_{12} z^{2}
$$
Where we define a coordinate "z" that describes the deflection of the $k_{12}$ spring. The derivation of this, and the subsequent simplification is left as an exercise to the reader (its annoying and probably maybe won't be on the final methinks)

Here is the potential energy: 
$$
U = \frac{1}{2} \left( k+\frac{k_{12}}{2} \right)x^{2} + \frac{1}{2}\left( k+\frac{k_{12}}{2} \right)y^{2} + \frac{1}{2}kxy
$$
We are now going to find our $A_{jk}$ matrix. This is the same procedure as gone over above, but with only 2 oscillators we will only have 2 eigenfrequencies. 

$$
\det[\bar{A} - \omega^{2}\bar{m}] = 0
$$
- Using the quadratic formula we find the two eigenvalues. 

Finding the eigenvectors is the second step of this problem. We use more linear algebra stuff to do this. 

$$
(\bar{A} - \omega^{2}\bar{m}) \bar{x} = 0
$$
Finding x for both eigenvalues/frequencies will yield the two eigenvectors. The physical interpretation of this is that one normal mode (w/ eigenfrequency 1) is that one mass is compressed in while one is stretched. Or vice versa. The second mode, with eigenfrequency 2, occurs when both masses are compressed or stretched with the same magnitude. 

## Problem 3

> 3 oscillators with equal weight and springs between them

This is an extension of the previous ideas. You should get a 3x3 $A_{jk}$ matrix, and 3 eigenvalues and eigenvectors. 

# HW 11: Continuous Systems

- Two primary types of string problems, plucked and struck strings. 
	- Plucked strings have position as the initial condition, while struck strings use velocity for the initial condition 

## Problem 1: The Struck String

> We are given a string struck at the point $\frac{L}{4}$ with a velocity $v_{0}$ and decreases linearly to at $x=0$ and $x=\frac{L}{2}$. Determine the motion of the string and what harmonics are absent. 

First step: define initial conditions:
$$
\dot{q}(x) = \begin{cases}
 xv_{0} \frac{4}{L}  & 0<x< \frac{L}{4} \\
-v_{0} \frac{4}{L} \left( \frac{L}{2}-x \right)&  \frac{L}{4}<x< \frac{L}{2} \\
0 &  \frac{L}{2} < x < L 
\end{cases}
$$
These are defined in terms of velocity, as denoted by the $\dot{q}$. Since we have 0 initial positioning, the $\mu_{r}$ term will go to 0

$$
\mu_{r} = \frac{2}{n+1} \sum_{j} q_{j}(0) \sin\left( j \frac{r\pi}{n+1} \right)
$$
The $q_{j}(0)$ term will be zero for any j 

This means we have to find $\nu_{r}$

The formula for $\nu_{r}$ is given by the following 

$$
\nu_{r} = -\frac{2}{\omega_{r}(n+1)} \sum_{j} \dot{q}_{j}(0) \sin\left( j \frac{r\pi}{n+1} \right)
$$
However, this is... hairy. We can use the properties of the [[@Spring2024/Physics/Math Background/Kronecker delta]] to rewrite this as the following: 

$$
\nu_{r} = -\frac{2}{\omega_{r}L} \int\limits_{0}^{L} \dot{q}(x,0)\sin\left( \frac{r\pi x}{L} \right) \, dx 
$$
Now, to solve this equation. This problem will be a 3 piece integral, over regions defined in the initial conditions. After solving for this, we can use the following definition to find the position of the string as a function of time and position: 

$$
q_{j}(t) = \sum_{r} \sin\left( j \frac{r\pi}{n+1} \right)(\mu_{r}\cos(\omega_{r}t) -\nu_{r}\sin(\omega_{r}t))
$$
There is no $\mu$ term, and we want $q$ as a function of $x,t$. So we rewrite the equation as follows

$$
q(x,t) = -\sum_{r} \sin\left( \frac{r\pi x}{L} \right) \nu_{r}\sin(\omega_{r}t)
$$

**NB: Remember the following for the exam** 
$$
q(x,t) = \sum_{r=1}^{\infty}  \sin\left( \frac{r\pi x}{L} \right) (\mu_{r} \cos(\omega_{r}t)-\nu_{r}\sin(\omega_{r}t))
$$

We plug in our value for $\nu_{r}$, simplify, and observe for which values of $r$ does $q(x,t)$ go to 0. These are the missing harmonics. 


## Problem 2: The plucked string

> As opposed to the previous question, this question gives us position as initial conditions. 

A string is pulled a distance $h$ at $3L/7$, and pulled in equal magnitude in the opposite direction at $3L / 7$ at the other end. 

Initial Conditions:

$$
q(x) = \begin{cases}
\frac{7}{3L} h x  &  0<x< \frac{3L}{7} \\ 
\left( \frac{L}{2}-x \right) \frac{14h}{L} & \frac{3L}{7}<0< \frac{4L}{7} \\
-\frac{7}{3L}h (L-x)  &  \frac{4L}{7}<0<L
\end{cases}
$$
With these initial conditions, we next have to find $\mu_{r}$

$$
\mu_{r}  = \frac{2}{L}\int\limits_{0}^{L} q(x,0) \sin\left( \frac{r\pi x}{L} \right) \, dx 
$$

- Do the 3 piece integral to find $\mu$

To find position, we need to then use the following relation 
$$
q(x,t) = \sum_{r=1}^{\infty}  \sin\left( \frac{r\pi x}{L} \right) (\mu_{r} \cos(\omega_{r}t)-\nu_{r}\sin(\omega_{r}t))
$$

Plugging in $\mu$ and 0 for $\nu$ we can solve for the position of the string at any point, and find the missing harmonics. 


# Equations to memorize
## Coupled Oscillations
$A_{jk}$ matrix components
$$
A_{jk} = \frac{ \partial^{2} u }{ \partial q_{j}\partial q_{k} } 
$$
$A_{jk}$ matrix eigenfrequencies
$$
\det[\bar{A}-\omega^{2}\bar{m}] = 0
$$
$A_{jk}$ matrix eigenvectors 
$$
[\bar{A}-\omega^{2}\bar{m}] \cdot \vec{v} = 0
$$
NB: The $\bar{m}$ matrix is determined from the kinetic energy, usually is equal to $m \mathbf{I}$ though. 

Keep in mind the spring potential energy is given by 
$$
U = \frac{1}{2}kx^{2}
$$
## Continuous Systems

Important things to keep in mind for continuous systems are to pay close attention to initial conditions and make sure that you set your bounds of integration correctly. 

Formula for $\mu_{r}$ (initial position based)
$$
\mu_{r}  = \frac{2}{L}\int\limits_{0}^{L} q(x,0) \sin\left( \frac{r\pi x}{L} \right) \, dx 
$$
Formula for $\nu_{r}$ (initial velocity based)
$$
\nu_{r} = -\frac{2}{\omega_{r}L} \int\limits_{0}^{L} \dot{q}(x,0)\sin\left( \frac{r\pi x}{L} \right) \, dx 
$$
General form of position equation
$$
q(x,t) = \sum_{r=1}^{\infty}  \sin\left( \frac{r\pi x}{L} \right) (\mu_{r} \cos(\omega_{r}t)-\nu_{r}\sin(\omega_{r}t))
$$







