---
dg-publish: true
---
The ordering of [[Notes/Physics/Quantum Physics/Concepts/Hermitian Operator]]s is important, and therefore they are not commutative. The commutator of two operators is defined as $[\hat{A},\hat{b}] = \hat{A}\hat{B}-\hat{B}\hat{A}$. 

For example, (class example 1)
A free particle with $H=\frac{p^{2}}{2m}$, determine $[\hat{p}, \hat{H}]$:
$$
\hat{p} = \frac{\hbar}{i} \frac{d}{dx}
$$
$$
\hat{H} = -\frac{\hbar}{2m} \frac{\partial^{2}}{\partial x^{2}}
$$
$$
[\hat{p}, \hat{H}]=\frac{1}{2m}[\hat{p},\hat{p}^{2}]=0
$$
A simple harmonic oscillator with $H=\dots$
$$
[\hat{p}, \hat{H}] = \left[ \hat{p}, \frac{\hat{p}^{2}}{2m} +\frac{1}{2} k_{0}\hat{x}_{2}\right]  = \frac{1}{2}k_{0}[\hat{p}, \hat{x}^{2}]
$$
$$
[\hat{p}, \hat{H}] = -i\hbar k_{0}x
$$
Why are commutation relations important? 
- We need hermitian operators to have the same eigenfunctions.
- Commuting operators have the same eigenfunctions
- Non commuting operations have uncertainty. 


In class assignment 2

Given $\frac{d<A>}{dt}=\frac{i}{\hbar}\int dx[(\bar{H}\Psi)^*\hat{A}\psi-\Psi^*\hat{A}\hat{H}\Psi]$ show that $\frac{d<A>}{dt} = \frac{i}{\hbar}\int \Psi^*[\hat{H}, \hat{A}]\Psi dx \equiv \frac{i}{\hbar}<[\hat{H},\hat{A}]> \, dx$
(use hermitian property of $\hat{H}$)
$$
H^{\dagger}=H
$$
$$
\frac{d<A>}{dt}=\frac{i}{\hbar}\int dx[(\bar{H}\Psi)^*\hat{A}\psi-\Psi^*\hat{A}\hat{H}\Psi]
$$
$$
 \frac{i}{\hbar}\int (\hat{H}\Psi)^*(\hat{A}\Psi)-\Psi^*\hat{A}\hat{H}\Psi \, dx = \frac{i}{\hbar}\int  \,  [\Psi^*H^{\dagger}\hat{A}\Psi-\Psi^*\hat{A}\hat{H}\Psi] dx
$$
$$
	=\frac{i}{\hbar}\int [\Psi^*\hat{H}(\hat{A}\Psi)-\Psi^*\hat{A}\hat{H}\Psi] \, dx 
$$
$$
=\frac{i}{\hbar}\int \Psi^*[\hat{H},\hat{A}]\Psi \, dx = \frac{i}{\hbar} <[\hat{H}, \hat{A}]>
$$
In class assignment 3
For Hamiltonian $H=\frac{p^{2}}{2m} + V_{x}$ show that $\frac{d<p>}{dt}= <-\frac{\partial V}{\partial x}>$

$$
\frac{d<A>}{dt} = \frac{i}{\hbar}<[\hat{H},\hat{A}]>
$$
$$
\frac{d<\hat{p}>}{dt} = \frac{i}{\hbar} <[\hat{H}, \hat{p}]>
$$
$$
=\frac{i}{\hbar} < \frac{\hat{p}^{2}}{2m}+V(x),\hat{p}> = \frac{i}{\hbar}<[V(x),\hat{p}]>
$$
$$
[V(x),\hat{p}]\varphi(x) = \frac{\hbar}{i}\left[ V(x) \frac{\partial \varphi}{\partial x}-\frac{\partial}{\partial x}V(x)\varphi(x)
\right]
$$
$$
=\frac{\hbar}{i}\left[ \frac{V(x)\partial \varphi}{\partial x} - \varphi(x) \frac{\partial V(x)}{\partial x}-V(x) \frac{\partial \varphi}{\partial x} \right]= -\frac{\hbar}{i} \frac{\partial V(x)}{\partial x} \varphi(x)
$$
$$
\frac{d<p>}{dt}=\frac{i}{\hbar}<-\frac{i}{\hbar}< -\frac{\hbar}{i} \frac{\partial V(x)}{\partial x} > = < -\frac{\partial V(x)}{\partial x}>
$$
$$
\frac{dp}{dt}=-\frac{\partial V(x)}{\partial x} = F
$$



In class assignment 4
For Hamiltonian $H=\frac{p^{2}}{2m} + V_{x}$ show that $\frac{d<x>}{dt}= \frac{<p>}{m}$
$$
\frac{d<x>}{dt} = \frac{i}{\hbar}<[\hat{H},\hat{x}]\geq\frac{d<x>}{dt} 
$$
$$
= \frac{i}{\hbar} <\left[  \frac{p^{2}}{2m}+V(x), \hat{x} \right]> =\frac{i}{2m\hbar} < [ \hat{p}^{2},\hat{x}]> = -\frac{i}{2mh} < [\hat{x},\hat{p}^{2}]>  
$$
$$
[\hat{x},\hat{p}^{2}]\varphi = \left[ x\left( \frac{\hbar}{i} \frac{\partial}{\partial x} \right)^{2} - \left( \frac{\hbar}{i} \frac{\partial}{\partial x} \right)x^{2}\right]\varphi = -\hbar^{2} \left[ x \frac{\partial^{2}}{\partial x^{2}}\varphi-\frac{\partial^{2}}{\partial x^{2}}(x\varphi) \right]
$$
$$
=-\hbar^{2}\left[ x \frac{\partial^{2}}{\partial x^{2}}\varphi - x\frac{\partial^{2}}{\partial x^{2}}\varphi-\frac{\partial}{\partial x}\varphi - \frac{\partial}{\partial x}\varphi \right] = 2\hbar^{2} \frac{\partial}{\partial x} \varphi = 2i\hbar \hat{p}\varphi
$$
$$
\frac{d<x>}{dt} = -\frac{i}{2mh}<2i\hbar \hat{p}> = \frac{<\hat{p}>}{m}
$$
