# Announcements: 
- HW 10 returned 
- Do course evaluations

# Continuous Systems 

## Loaded String Solutions 
$$
q_{j} = \sum_{r}\beta_{r} \sin \left( j \frac{r\pi}{n+1} \right) e^{i\omega t}
$$
Where 
$$
\begin{matrix}
n = \text{number of masses} \\
r= \text{mode index}
\end{matrix}
$$
Frequencies given by: 
$$
\omega_{r} = 2 \sqrt{ \frac{\tau}{m\alpha}  } \sin \left( \frac{r\pi}{2(n+1)} \right)
$$
$$
q_{j} (t) = \sum _{r } \eta_{r} (t) \sin \left(  j \frac{r\pi}{n+1} i \eta_{r} \right) = \beta _{r} e^{i\omega t}
$$
Where $\beta_{r}=\mu_{r}+i \nu_{r}$
$$
\mu_{r} = \frac{2}{n+1} \sum_{j} q_{j} (0) \sin\left( j \frac{r\pi}{n+1} \right)
$$
Using initial position to solve for mu
$$
\nu_{r} = -\frac{2}{\omega_{r}(n+1)} \sum \dot{q}_{j} (0) \sin\left( j \frac{r\pi}{n+1} \right)
$$
Using initial velocity to solve for nu

R goes up to number of masses. With 10 particles, there is 10 frequencies, and 10 sets of coefficients. 

Using this discussion, we examine the consequence of allowing the number of particles on the string to be infinite, while maintaining a constant linear mass density. 

As the number of string "particles" increases, the distance between them decreases

We need to make sure we don't have infinite mass. Therefore
$$
\rho = \frac{m}{d} = \text{constant}
$$
Continuous String: 
$$
j \frac{r\pi}{n+1} \cdot \frac{d}{d} = r \pi  \frac{x}{L}
$$
$$
jd =x
$$
We need this to be a function of $x$ and $t$, as follows: 
$$
q(x,t) = \sum_{r} \eta_{r}(t) \sin\left( r\pi      \frac{x}{L} \right) = \sum_{r} \beta _{r} e^{i\omega_{r}t} \sin\left( \frac{r\pi x}{L} \right)
$$
There are infinite frequencies from infinite particles

Keeping only real terms (expanded $\eta_{r}$) and apply initial conditions

We get: 
$$
q(x,0) =  \sum_{r} \mu_{r} \sin(\frac{r\pi x}{L})
$$
$$
\dot{q} (x,0) = -\sum_{r} \omega_{r} \nu_{r} \sin\left( \frac{r\pi x}{L} \right)
$$
Multiply both sides by sin term, integrate from 0 -> L. Using [[@Spring2024/Physics/Math Background/Kronecker delta]], we get:
$$
\frac{L}{2} \delta_{r,s} = \sin \frac{r\pi x}{L} \sin \frac{s\pi x}{L}
$$
$$
\mu_{r} =\frac{2}{L}\int\limits_{0}^{L}  q(x,0) \sin\left( \frac{r\pi x}{L} \right) \, dx
$$
$$
\nu_{r} = -\frac{2}{\omega_{r} L } \int\limits_{0}^{L} \dot{q}(x,0) \sin\left( \frac{r\pi x}{L} \right) \, dx 
$$
$$
\omega_{r} = 2\sqrt{ \frac{\tau}{md}  }\sin\left( \frac{r\pi}{2(n+1)} \right)
$$
$$
\frac{2}{d} \sqrt{  \frac{\tau}{\rho} } \sin\left( \frac{r\pi d}{2L} \right)
$$
As d goes to zero and particles go to infinity, we can use the small angle approx: 
$$
\frac{2}{d} \sqrt{ \frac{\tau}{\rho} } \frac{r\pi d}{2L}
$$
$$
\omega_{r}= \frac{r\pi}{L} \sqrt{ \frac{\tau}{\rho} }
$$
Tension over density, the second term, is the velocity of the wave on the string. 

## Plucked String: 
at $\frac{L}{3}$
> figure here

String, plucked to height h at l/3

In the space $x< \frac{L}{3}$

Slope 
$$
\frac{\Delta y}{\Delta x} = \frac{3h}{L}
$$
$$
y = ax + b = \frac{3h}{L} x + b
$$
$$
q(x,0) = \frac{3h}{L} x ; \ \ \ \  0 \leq x \leq \frac{L}{3}
$$
$$
0 = \frac{3h}{L}(0) + b \implies b=0
$$
In the space $\frac{x>L}{3}$
Slope given by: 
$$
-\frac{3h}{2L}
$$
$$
y = -\frac{3h}{2L} x + b
$$
$$
0 = -\frac{3h}{2L}(L)+b  \implies b=\frac{3h}{2}
$$
$$
q(x,0) = \frac{3h}{2L} (L-x);  \\ \ \ \\ \frac{L}{3} \leq x \leq L
$$

![[Pasted image 20240419101626.png]]
![[Pasted image 20240419101631.png]]
![[Pasted image 20240419101639.png]]
![[Pasted image 20240419101644.png]]
![[Pasted image 20240419101648.png]]
