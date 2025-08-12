---
dg-publish: true
---
See: [[Notes/Physics/Quantum Physics/Concepts/Time independent Schrodinger equation]]
**Typically when we refer to the [[Notes/Physics/Quantum Physics/Concepts/Schrodinger equation]] we are talking about the time independent one**
The Schrödinger equation is a fundamental equation in quantum mechanics that describes how the wave function of a physical system evolves over time. It is named after the Austrian physicist Erwin Schrödinger, who formulated it in 1925.

The time-dependent Schrödinger equation for a non-relativistic particle (i.e., a particle not moving close to the speed of light) is given by:

$$i\hbar \frac{\partial}{\partial t} \Psi(\mathbf{r}, t) = \hat{H} \Psi(\mathbf{r}, t)$$

Here's what the terms in the equation represent:

- $i$ is the imaginary unit $i^2 = -1$.
- $\hbar$ is the reduced Planck's constant, which is a fundamental constant in quantum mechanics.
- $\frac{\partial}{\partial t}$denotes the partial derivative with respect to time \(t\).
- $\Psi(\mathbf{r}, t)$ is the wave function, which is a mathematical function that contains all the information about a quantum system. It depends on the spatial coordinates $r$ and time $t$.
- $\hat{H}$ is the Hamiltonian operator, which represents the total energy operator of the system.

The time-independent Schrödinger equation, which is a special case for systems with constant energy (i.e., systems not subject to time-dependent external forces), is given by:

$$\hat{H} \psi(\mathbf{r}) = E \psi(\mathbf{r})$$

Here, $\psi(r)$ is the spatial part of the wave function, which depends only on the spatial coordinates $\mathbf{r}$, and $E$ represents the energy of the system.

Solving the Schrödinger equation allows us to determine the allowed energy levels and corresponding wave functions for a given quantum system. The wave function provides a complete description of the system's quantum state, and from it, we can calculate various observables, such as position, momentum, and energy.

It's important to note that the Schrödinger equation is a cornerstone of non-relativistic quantum mechanics, applicable to systems that do not involve speeds approaching the speed of light. For relativistic particles, a different equation, the Dirac equation, is used.

## Bullet Notes
- Clever guess by Schrodinger
$$
-\frac{\hbar^{2}}{2m} \frac{d^{2}\psi(x,t)}{dx^{2}} + V(x)\psi(x,t) = i\hbar \frac{d\psi(x)(x,t)}{dt}
$$
- First term is kinetic energy , second is potential, right hand is total 
- Hamiltonian is right hand side
- Momentum Operator is given by 
$$
\frac{\hbar}{i} \frac{d\psi}{dx}
$$
- Typical guess for particle in free space (no potential)
$$
\psi(x,t)=e^{i(kx-\omega t)}
$$
- Normalization
$$
\int |\psi^{*}\psi| \, dx = 1 
$$
- Classically you can track the position of things, quantum mechanically $\psi(x,t)$ yields the probability that is at a given location 
- If you have an uncertainty of position you cant follow the trajectory 
- Psi encodes the information about the object
- Probability Density is 
$$
|\psi(x,t)|^{2}
$$
- Depicts how probability changes over space. Can be used to find most probable location for particle.
- Probability Density times infinitesimal distance is probability
$$
\left[ \frac{|\psi(x,t)|^{2}}{dist} \right] \cdot \Delta x = prob
$$
- Integrating free space guess over all space
$$
\psi(x,t)=e^{i(kx-\omega t)}; \ \ \int \psi(x,t) \, dx  =0 \ or \ DNE
$$
- Integrating 1 over all space is infinity, using a wave packet prevents this
![[Pasted image 20231205103939.png]]
- Group vs Phase velocity 
-   Wave function
![[Pasted image 20231205103956.png]]
- Gaussian-Like distribution
- Oscillations at edges are wrong for Gaussian 
