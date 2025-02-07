---
dg-publish: true
---
### Derivation of EM wave equation 
$$
\vec{\nabla}\times \vec{\nabla} \times \vec{E} = - \vec{\nabla} \times  \dot{\vec{B}} =-\mu_{0}\epsilon_{0} \ddot{\vec{E}}
$$
$$
\vec{\nabla} \times \vec{\nabla} \times \vec{B} = \mu_{0}\epsilon_{0} \vec{\nabla} \times \ddot{\vec{E}}
$$
With 
$$
\mu_{0}\epsilon_{0} = \frac{1}{c^{2}}
$$

### General solution to EM wave equation
The general solution to EM wave equation is plain monochromatic waves given in the form of 
$$
\vec{E} (z,t) = \vec{E}_{0} e ^{i(kz-\omega t)}
$$
$$
\vec{B}(z,t) = \vec{B}_{0} e^{ikz-\omega t}
$$
Monochromatic means that the wave oscillates at a certain single frequency. The magnetic field vector and electric field vector are perpendicular to each-other. 

You can prove this by taking the time derivative of the solution and plugging it into the above differential equation. 

A transverse wave means that the oscillation is perpendicular to the direction of propagation. The fact that EM waves are transverse follows from the fact that the divergence of $\vec{E}$ and $\vec{B}$ are both 0 

$$
\vec{E} = E_{0}\cos(kz-\omega t) \hat{x} + E_{0}\cos(kz-\omega t) \hat{y}
$$
And  
$$
\vec{\nabla}\vec{E} = \frac{ \partial E_{x} }{ \partial x } + \frac{ \partial E_{y} }{ \partial y }  + \frac{ \partial E_{z} }{ \partial z } =0
$$
$E_{x}$ and $E_{y}$ are both independent of $z$

This is in agreement with Faraday's law 

$$
\vec{\nabla} \times \vec{E} = -\vec{B} 
$$
or 
$$
\vec{B}_{0} = \frac{k}{\omega} (\hat{z} \times \vec{E}_{0})
$$
I.E if the B-field is in the y direction, and the E-field is in the x direction, the direction of propagation is in the $z$ direction.
$$
\vec{\nabla} \times \vec{E} = \frac{ \partial E_{x} }{ \partial z } \hat{y} = - \frac{d}{dt} \vec{B}
$$
The change over space of the electric field is directly related to the change over time of the magnetic field, relating this directly to [[@SchoolFall 2023/School/Physics/Physics 1250/Concepts/Faraday's law]].

further generalized EM wave equation

$\vec{n}$ is the vector in the direction of $\vec{E}$
$\vec{k}$ is the vector in the direction of propagation
$\vec{k} \times \vec{n}$ : the vector perpendicular to $\vec{n}$ and $\vec{k}$

General description of EM wave:
$$
\vec{E}(\vec{r}, t) = E_{0} e ^{i(\vec{k} \cdot \vec{r} - \omega t)}\hat{n}
$$
$$
\vec{B}(\vec{r},t) = \frac{1}{c} E_{0} e^{ i(\vec{k} \cdot \vec{r} -\omega t)} (\hat{k} \times \hat{n}) = \frac{1}{c} \hat{k} \times \vec{E}
$$
with $\hat{n} \cdot \hat{k} = 0$

### Polarization of EM waves

The electromagnetic wave has two components (E & B) that are perpendicular to the direction of propagation. There may exist a phase difference between these two components denoted by $\phi$. This phase difference is determined by the polarization of the electromagnet wave. 

$$
\vec{E} = \vec{E} _{x}  + \vec{E}_{y} = E_{0} \cos (kz-\omega t +\phi) \hat{x} + E_{0}\cos(kz - \omega t)\hat{y}
$$
If $\phi=0$, there is linear polarization. 
If $\phi = \frac{\pi}{4}$ there is circular polarization. 

Any other value of phi results in elliptical polarization 

The direction of the electric field is always perpendicular to the magnetic field. In the case of vertically polarized light, the electric field vector exists only in the y axis, and therefore the magnetic in the x axis. 

Un-polarized light has many incoherent components oscillating in many separate directions simultaneously, and has no time-independent phase difference. 

> is this how lasers work?

Polarizers can be used to linearize light.

### Momentum of EM waves

We can use the content learned last class to calculate the energy density of electromagnetic waves. The EM energy density is equal to the following
$$
\frac{1}{2} \left( \epsilon_{0} E^{2} + \frac{1}{\mu_{0}}B^{2} \right)
$$
For the monochromatic plane wave
$$
B^{2} = \frac{1}{c^{2}} E^{2} = \mu_{0} \epsilon_{0}E^{2}
$$

Energy flux density using [[Poynting vector]]
$$
\vec{s}  = \frac{1}{\mu_{0}} (\vec{E} \times \vec{B})
$$
$$
\vec{s} = c\epsilon_{0}E^{2}\cos(kz - \omega +\delta) \hat{z} = c ? z
$$


See also : quantum description of light. [[Photoelectric experiment]] 
in which energy is given by 
$$
E= h \cdot \nu
$$
Momentum: 
$$
\vec{p} = \frac{h}{2\pi} \vec{k} = \hbar \vec{k}
$$
Angular momentum: 
$$
\vec{l}= \vec{r} \times \vec{p}
$$
In class questions: 9.9, 9.13














