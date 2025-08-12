---
dg-publish: true
---
## A.k.a Particle in a box
![[Pasted image 20231021162902.png]]


To produce an effective model, we start by solving the [[Notes/Physics/Quantum Physics/Concepts/Time independent Schrodinger equation]] for 0 < x < L. Starting by setting V=0, we get 
$$
-\frac{\hbar^{2}}{2m} \frac{\partial\Psi(x)}{\partial x^2} = E\psi(x)
$$
Then, using $E = \frac{P^2}{2m}=\frac{(\hbar k)^{2}}{2m}$ we get $K^2=\frac{2mE}{\hbar^2}$ , which allows us to rearrange the above equation as
$$
\frac{d^2\psi}{dx^{2}} = k^{2}\psi 
$$
for 0 < x < L, or whenever the particle is in the well. The $V$, or potential of the particle outside of this is infinite, so attempting to solve the Schrodinger equation is pointless. 

It is also worth noting that the above equation is similar in form to the classical equation of motion of a mass on a spring, $\frac{d^2y}{dt^{2}} = \frac{k}{m}y$ a motif that repeats throughout wave mechanics. 

Using an [[ansatz]] of $\psi(x) \sim e^{ikx}$ we can solve the above differential equation. 
The worked solution is more then I want to type into latex, but it is *theoretically* in activity 9.1, and yields: 
$$
\psi_{n}(x) = \sqrt{ \frac{2}{L} } \sin\left( \frac{n\pi x}{L} \right)
$$
for 0 < x < L, where $n=1,2,3\dots$ 
And 
$$
E =  \frac{\hbar k^2}{2m} = 
\frac{n^{2}\pi^{2}\hbar^{2}}{2mL^{2}}$$
This reveals a few interesting things: 
1. E, or energy is quantized. It has specific levels, and cannot exist between these levels. 
2. $E_{n}$ is always greater then 0, even at the ground state where n=1. The energy when n=0 is known as the *zero point energy* 

 ![[Pasted image 20231024160814.png]]
 The above figure demonstrates the quantization of energy within our infinite potential well.

We can graphically demonstrate these energy levels through graphing as well. 
![[Pasted image 20231024161422.png]]

Classically, the *amplitude* of the oscillation would determine the energy of the, but for the particle in the box the energy increases as nodes increase. The higher the wave functions *spatial frequency* is, the more energy the particle has. The energy of the particle is not related to amplitude, which is set to 1 via normalization. 

These results also correspond to the relation given to us by the [[Heisenberg Uncertainty Principle]]. If $\Delta p_{x}=0$, then $\Delta x=\infty$, but we know this cannot be possible due to the particle not being able to exist outside the box. Therefore, it logically follows that the particle must have a nonzero momentum and thus a nonzero energy. Further, if the box is smaller, the minimum energy must be larger because $\Delta p$ and $\Delta x$ are inversely related. This also corresponds to our earlier findings, as 
$$
E=\frac{n^{2}\pi^{2}\hbar^{2}}{2mL^{2}}$$
is larger when L is smaller. 

Another item of interest is that the probability density is stationary, unlike classical models, its not bouncing around. Rather, the particle does not exist in any one location, but rather a spectrum of potential locations. For $\psi_{2}$ and higher energy levels, the particle has a "split personality" where is is equally likely to exist on either half but not in the middle. 
