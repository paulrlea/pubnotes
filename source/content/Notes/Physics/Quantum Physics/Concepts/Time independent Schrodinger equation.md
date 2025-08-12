---
dg-publish: true
---
The [[Notes/Physics/Quantum Physics/Concepts/Schrodinger equation]] in a single dimension can be reduced to two ordinary differential equations through separation of variables. This yields one equation that is dependent on time, and one that is time independent. It is also known as the [[Energy Eigenvalue Equation]]. 
$$
-\frac{\hbar^{2}}{2m} \frac{\partial\Psi(x,t)}{\partial x^2} + V(x)\Psi(x,t) = i\hbar  \frac{\partial\Psi(x,t)}{\partial t}
$$
Above is the Schrodinger Equation. It can be solved for a free particle. See  (i.e no potential energy, $V(x)$ term is zero). 

When $V(x)$ is independent of time, we can separate the [[Notes/Physics/Quantum Physics/Concepts/Schrodinger equation]] into 
$$
\frac{df(t)}{dt} = -\frac{iE}{\hbar}f(t)
$$
and
$$
-\frac{\hbar^2}{2m} \frac{\partial\psi(x,t)}{\partial x^2} + V(x)\psi(x) = E\psi(x)
$$
The latter is known as the [[Notes/Physics/Quantum Physics/Concepts/Time independent Schrodinger equation]], while the former can be rather easily solved using an [[ansatz]] of $F(t) =f(0)e^{-iEt/\hbar}$ , or $F(t) =f(0)e^{i\omega}$ where $E = \hbar \omega$ . 

**NB**:
$$
|\Psi(x,t)|^2 = |\Psi(x)|^2
$$
Probability is Independent of time

Using the [[Notes/Physics/Quantum Physics/Concepts/Time independent Schrodinger equation]], and a suitable $V(x)$ we can model a "particle in a box", also known as an [[Notes/Physics/Quantum Physics/Concepts/Infinite square well]]. We can also use the [[Notes/Physics/Quantum Physics/Concepts/Time independent Schrodinger equation]] to model [[Notes/Physics/Quantum Physics/Concepts/Step Potentials]] as seen later on. 


## Three Dimensional Versions
The Three dimensional [[Notes/Physics/Quantum Physics/Concepts/Time independent Schrodinger equation]] is given by 

$$
-\frac{\hbar^{2}}{2m} \left[ \frac{d^{2}\psi}{dx^{2}}+\frac{d^{2}\psi}{dy^{2}} +\frac{d^{2}\psi}{dz^{2}} \right]= (E-V(r))\psi(x,y,z)
$$
in Cartesian coordinates.
NB- This can also be represented with the Laplacian operator $\nabla^{2}$.


The Laplacian in spherical coordinates is given below: $$
-\frac{\hbar^{2}}{2m} \left[ \frac{1}{r^{2}} \frac{d}{dr}\left( r^{2} \frac{d}{dr} \right) + \frac{1}{r^{2}\sin \theta} \frac{d}{d\theta} \left( \sin \theta \frac{ d}{d\theta} \right) + \frac{1}{r^{2} \sin ^{2}\theta} \frac{d^{2}}{d\phi^{2}}  \right] \psi(r,\theta,\phi) = (E-V(r)) \psi(r,\theta,\phi)
$$ This gives rise to the momentum operator in three dimensions: $\mathbf{P}$, as well as the more interesting angular momentum operator $\mathbf{L}_{op}$, which will be covered more in next class. 
$$
	\mathbf{P}^{2} = -\hbar^{2} \nabla^{2} 
$$
$$
\mathbf{L} = -\hbar^{2}\left[ \frac{1}{\sin \theta} \frac{d}{d\theta} \left( \sin \theta \frac{d}{d\theta} \right) + \frac{1}{\sin \theta} \frac{d^{2}}{d\phi^{2}} \right] = \mathbf{r} \times \mathbf{p}
$$
The rotational kinetic energy term in the Hamiltonian (RHS of following) is also equal to the angular momentum over $2mr^{2}$ 
$$
\frac{\mathbf{L}^{2}_{op}}{2mr^{2}} = -\frac{\hbar^{2}}{2m}\left[ \frac{1}{r^{2}\sin \theta} \frac{d}{d\theta} \left( \sin \theta \frac{ d}{d\theta} \right) + \frac{1}{r^{2} \sin ^{2}\theta} \frac{d^{2}}{d\phi^{2}}  \right]
$$
### Separation of Variables in Spherical Coordinates
Replacing the Hamiltonian operator with $\left( \frac{\hat{P}_{r}^{2}}{2m} + \frac{\hat{L}^{2}}{2mr^{2}} \right)$, we get 
$$
\left( \frac{\hat{P}_{r}^{2}}{2m} + \frac{\hat{L}^{2}}{2mr^{2}} \right) \Psi(r,\theta,\phi)=(E-V(r))\Psi(r,\theta,\phi)
$$
Replacing $\Psi$ with $R(r)Y(\theta, \phi)$ 

$$
\implies \left( \frac{\hat{P}_{r}^{2}}{2m} + \frac{\hat{L}^{2}}{2mr^{2}} \right)R(r)Y(\theta,\phi) = (E-V)R(r)Y(\theta,\phi)
$$


