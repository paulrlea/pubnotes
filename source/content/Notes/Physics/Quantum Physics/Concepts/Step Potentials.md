---
dg-publish: true
---
#incomplete 
[[Notes/Physics/Quantum Physics/Concepts/Finite Square Well]]

$$
x > \frac{L}{2}; e^{-\kappa x}
$$
$$
\kappa = \frac{\sqrt{ 2m(v_{0}-E) }}{\hbar }
$$
$$
x < -\frac{L}{2} ; e^{\kappa x}
$$
Solutions for E from:
$$
\tan \xi = \frac{\sqrt{ \xi^2 _{0} - \xi^2}}{\xi}
$$
$$
\xi = \frac{\sqrt{ 2mE }}{\hbar}; \xi_{0} = \frac{L}{\hbar}\sqrt{ \frac{mv_{0}}{2} }
$$
What happens if $E > V_0$?
(energy is greater then potential)

![[Pasted image 20231020132325.png]]
We can take the [[Notes/Physics/Quantum Physics/Concepts/Time independent Schrodinger equation]]

$$
-\frac{\hbar^2}{2m} \frac{d^2\varphi(x)}{dx^2} + v(x)\varphi = E\varphi(x)
$$
$$
\frac{d^2\varphi(x)}{dx^2} = -\frac{2m}{\hbar^2}(E-V)\varphi (x) = -k_{0}^2 \varphi(x)
$$
Where 
$$
k_{0} = \frac{\sqrt{ 2m(E-V_{0}) }}{\hbar} , k = \frac{\sqrt{ 2mE }}{\hbar}
$$

![[Pasted image 20231020132340.png]]
Now Consider Regions 1 and 2
Region 1: For $x<0$ ; $E>(V=0)$ 
$$
k = \frac{\sqrt{ 2mE }}{\hbar} > 0
$$
Solutions: 
$$
Ae^{ikx} + Be^{ikx}
$$
Region 2: For $x>0$, $E<V_0$
$$
k_{0} = \frac{\sqrt{ 2m(E-V_{0}) }}{\hbar} = \frac{i\sqrt{ 2m(v_{0} -E)}}{\hbar} 
$$
$$
\xi \kappa \equiv \frac{\sqrt{ 2m(v_{0}-E)}}{\hbar}
$$
$$
\therefore \varphi= Ce^{ik_{0}x} + De^{-ik_{0} }x
$$
$$
\varphi= Ce^{ik_{0}x} + 0e^{-ik_{0} }x
$$
![[Pasted image 20231020133306.png]]

What happens if E > V everywhere? 
![[Pasted image 20231020133341.png]]
Region I: $x<0; k=\frac{\sqrt{ 2mE }}{\hbar}$
with solution:
$$
\varphi \sim Ae^{ikx} + Be^{-ikx} 
$$
Region II: $x>0; E>V_0,k_{0}=\frac{\sqrt{2m(E-V_{0}) }}{\hbar}$

with solution: 
$$
\varphi \sim Ce^{ik_{0}x} + De^{-ik_{0}x}
$$
Consider incident [[traveling wave]] from the left: 
![[Pasted image 20231020134136.png]]
In the above diagram: 

## Region 1
$e^{ikx}$ Represents flux coming from the left
and
$e^{-ikx}$ Represents the flux reflected from the potential

$\therefore$ for $x<0$ $\varphi(x)=Ae^{ikx} + b^{-ikx};k=\sqrt{ \frac{2mE}{\hbar} }$ 
and for $x>0 \varphi(x) = Ce^{ik_{0}x} + De^{-ik_{0}x}; k_{0} = \frac{\sqrt{ 2m(E-V_{0}) }}{\hbar}$

**no wave incident from $x = \infty$ 
![[Pasted image 20231020155000.png]]

There is reflection and transmission:
Lets use the [[Notes/Physics/Quantum Physics/Concepts/probability current]] to quantify this: 
Recall: 
$$
j_{x} = \frac{\hbar}{2mi} \left( \varphi^* \frac{d\varphi}{dx}-\varphi\frac{ d\varphi^*}{dx} \right)
$$
Now, $$
R\equiv\frac{j_{ref}}{j_{inc}} ; T \equiv \frac{j_{trans}}{j_{inc}}
$$

![[Pasted image 20231020155432.png]]

Recall also: 
$$
\phi_{(x,t)} = \int A(k)e^{i(kx-\omega t)} \, dx 
$$

