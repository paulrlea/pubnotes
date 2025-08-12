---
dg-publish: true
---
#incomplete 
Review [[Notes/Physics/Quantum Physics/Concepts/Step Potentials]] and scattering

![[Pasted image 20231024100907.png]]
Using probability flux $j$
$$
 j_{A} = \frac{\hbar k}{m} AA^*
$$
Negative $\hbar k$ term for B. 
Applications of Quantum Tunneling
- Scanning tunneling microscopy
- Field emission scanning electron microscopy
- Alpha decay
- Dielectric breakdown
- Ivar Giaever (Nobel Prize winner for quantum tunneling)
![[Pasted image 20231024101117.png]]
Also recall photoelectric effect: 
![[Pasted image 20231024101307.png]]
Note figure on right utilizing quantum tunneling

In class assignment 1: 
From boundary conditions at x=0 and L, determine the four algebraic equations that relate A,B,C,D,E,F and G
$$
Ae^{ikx} + Be^{-ikx} =Ge^{\kappa x} +  Fe^{-\kappa x}
$$
At x=0
$$
A+B = F+G
$$
$$
ik(A-B) = \kappa(-F+G)
$$
At x=L
$$
  Ge^{\kappa x} + Fe^{-\kappa x} = Ce^{ikx}
$$
$$
-\kappa Fe^{-\kappa L} + \kappa Ge^{\kappa L} = ikCe^{ikx}
$$
Now considering a finite barrier as a scattering problem with a wave coming from the left.
$$
@x<0: Ae^{ikx} + Be^{-ikx}
$$
$$
@0<x<L: Fe^{\kappa x} + Ge^{-\kappa x}
$$
$$
@ x>L: Ce^{ikx}
$$
In class Assignment 2:
$$
\left( \frac{4k\kappa}{k^{2}+\kappa^{2}} \right)^{2} = 16 \frac{E}{V_{0} } \left( 1-\frac{E}{V_{0}} \right)
$$
Consider a barrier with an arbitrary shape: 
![[Pasted image 20231024112017.png]]
With transmission coeff. 
$$
 T \approx Ce^{-2\sum \kappa_{i}dx} \approx Ce^{-2
\int_{a}^{b} \, dx \sqrt{ 2m(V_{0}-E)/\hbar }}
$$

There are many situations where we need to consider a barrier that is not rectangular:
![[Pasted image 20231024112607.png]]
![[Pasted image 20231024112616.png]]
Recall: [[@SchoolFall 2023/School/Physics/Physics 1250/Concepts/Electric field]], $E_{0}$ w/t $V = qE_{0}x$ 
Now, 
$$
E = W + E -eE_{0}x_{0}
$$
$$
0 = W - eE_{0}x_{0}
$$
$$
x_{0} = \frac{w}{eE_{0}}
$$
$$
\therefore T \approx Ce^{-2\int_{0}^{x_{0}} \, dx\sqrt{ 2m/\hbar (W-eE_{0}x) } }
$$
This is known as the [[Fowler-Nordheim]] Relationship