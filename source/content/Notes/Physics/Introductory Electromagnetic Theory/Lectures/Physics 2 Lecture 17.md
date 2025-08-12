# Transient Circuits
- We have seen several different circuit components (capacitors, inductors, resistors)
$$
EMF_{L} =-L \frac{di}{dt} = -L \frac{d^{2}q}{dt^{2}}
$$
$$
EMF_{R} = ir = R \frac{dq}{dt}
$$
$$
EMF_{C} = \frac{I}{C}\int i \, dt = \frac{q}{c} 
$$
The three formulas above give us the EMF for [[inductor]]s, [[resistor]]s and [[capacitor]]s
respectively. The relation between potential and current give us 




Inductance is based on [[Lenz's Law]]. 

# [[RC Circuit]]
The RC circuit is composed of a resistor, a switch and a capacitor. The switch controls flow from the battery to the resistor and capacitor that are wired in series. 
![[Attachments/Pasted image 20231026101652.png]]

1). Turn circuit "on" by switching S to the "a" position. 
2). Write potential for each element
3). Write loop rule paying attention to signs. 



$$
EMF_{R} = ir = R \frac{dq}{dt}
$$

$$
EMF_{C} = \frac{I}{C}\int i \, dt = \frac{q}{c} 
$$
Using the above two we can use the loop rule, as depicted by the purple rectangle in the figure above. This yields the below equation. 

$$
\mathcal{E} - iR - \frac{q}{c} = 0
$$
> "so a couple questions..."

>"\*cutting off prof\* so it alternates from positive to negative"

Rewriting the above equation in terms of charge instead of current yields the below: 
$$
\mathcal{E} - r \frac{dq}{dt} - \frac{q}{c} = 0
$$
Then we can integrate: 
$$
\int ^{Q_{f}}_{Q} \frac{dq}{\mathcal{E}_{c} - q} \, = \int ^{tf}_{ti} \frac{dt}{RC} \,
$$
Letting $u=\mathcal{E}_{c}-q$ so $dq=-du$

$$
-\int ^{\mathcal{E}c-Qf} _{\mathcal{E}_{c}-Qi} \, \frac{du}{u} = -\ln(-\frac{\mathcal{E}_{c}-Q_{f}}{\mathcal{E}_{c}-Q_{i}}) = \frac{t_{f} -t_{i}}{RC} +-\frac{\mathcal{E}_{c}-Q_{f}}{\mathcal{E}_{c}-Q_{i}} =  e^{-(t_{f}-t_{i})/RC}
$$

>"can we use stuff we learned in DiffEq to solve these problems?"

>"i draw arrows okay?"


Initial conditions: Uncharged capacitor at $t=0$ 
$$
\frac{\mathcal{E}_{c} -Q_{f}}{\mathcal{E}_{c}} = e^{-t/RC}
  $$
  $$
\implies Q(t) = \mathcal{E}C(1-e^{-t/RC}) 
$$

All of the above was about turning the circuit "on". Now what if we turn the circuit "off"?

We can redo the [[loop rule]] again with the switch in the B position after the capacitor is charged: 

$$
-ir - \frac{q}{c} = 0
$$
or 
$$
\frac{dq}{dt} R + \frac{q}{c} = 0 
$$
$$
\frac{dq}{q}=-\frac{I}{RC} dt
$$
$$
\implies \ln(Q(t)-\ln (Q(0))) = -\frac{t}{RC}
$$
$$
Q(t) = Q(0)e^{-t/RC}
$$
Our capacitor is fully charged at $t=0$ in this case. 


 







# [[RL Circuit]]
- An [[inductor]] is a device that only has a potential across it when there is a change in current. An inductor generates a magnetic field if you have a change in current. With a constant current, the inductor does nothing. No potential difference $\equiv$ no change in current and vise versa
- See last lab, we applied triangle wave across inductor, when current increased potential was negative across inductor. 
- 
- 
- The sign of the potential drop is in such a way as to oppose the change. The inductor attempts to "maintain" the current as it was previously. 
	- Increasing current => negative potential and vise versa


- An RL circuit is a circuit with a resistor and an inductor in series. Same as above RC circuit, but replacing the capacitor with an inductor. 
- ![[/Attachments/Pasted image 20231026104605.png]]
- We "start" this system the same way as the last system, by flipping the switch to the "A position".
- We can once again use the [[loop rule]], as denoted by the purple rectangle in the figure above. We are going from the negative to the positive terminal on the battery. 
Loop Rule for this: 
$$
\mathcal{E} - iR -L \frac{di}{dt} = 0 
$$
$$
\int ^{If} _{Ii} \frac{di}{-i+\frac{\mathcal{E}}{R}} =  \int ^{Tf} _{Ti} \ \frac{R}{L }dt
$$
Change of variable $u=i-\frac{\mathcal{E}}{R}$ 
Then integrate: 
$$
\int ^{If-\mathcal{E}/R} _{Ii-\mathcal{E}/R} \frac{du}{u} = \frac{t_{f} - t_{i}}{\frac{L}{R}} = \ln\left( \frac{I_{f}-\frac{\mathcal{E}}{R}}{I_{i}-\frac{\mathcal{E}}{R}} \right)
$$
$$
\frac{I_{f}-\frac{\mathcal{E}}{R}}{I_{i}-\frac{\mathcal{E}}{R}}  = e ^{-(t_{f}-t_{i})/\frac{L}{R})}
$$
For initial conditions $I =0$ and $t = 0$
$$
\frac{I(t)-\frac{\mathcal{E}}{R}}{\frac{-\mathcal{E}}{R}} = e^{-t/\frac{L}{R}}
$$
$$
\mathcal{E}_{L} = -L \frac{dI(t)}{dt} = \mathcal{E}e^{-t/\frac{L}{R}}
$$
![[/Attachments/Pasted image 20231026105708.png]]



# [[LC Circuit]]
LC Circuit consists of a charged capacitor and an inductor in series
![[/Attachments/Pasted image 20231026110012.png]]
We will once again be using the loop rule for this system:
$$
-L \frac{di}{dt} - \frac{q}{c} = 0 \implies L \frac{d^{2}q}{dt^{2}} + \frac{q}{c} = 0
$$
$$
q(t) = Q_{max} \cos(\omega t = \phi)
$$
where $\omega =\frac{1}{\sqrt{ LC }}$
This is similar to mass on a spring harmonic oscillations, but the energy storage is all electric and is being transformed into magnetic energy. Cool stuff. 

Electric field => Spring (potential) energy
Magnetic field => Magnetic (kinetic) energy

>It is very interesting to see how themes play out throughout physics. The same harmonic oscillation problems also come up in QP1, and I am sure they will appear in IQM and Theoretical Mech. 

For our electric system:
$$
U_{E} = \frac{q^{2}}{2C} = \frac{Q^{2}}{2C}\cos ^{2}(\omega t+ \phi)
$$
$$
U_{B} = \frac{1}{2} L^{2} = \frac{1}{2} LI^{2}\sin ^{2}(\omega t + \phi)
$$
$$
U_{E} + U_{B} = constant
$$
> "im assuming that if you had all three in a circuit youd get some time of exponential time oscillation"

# Useful Summary 
$$
\mathcal{E}_{L} = -L \frac{di}{dt} = L \frac{d^{2}q}{dt^{2}}
 $$
 $$
\mathcal{E}_{R} = iR = R \frac{dq}{dt}
$$
$$
\mathcal{E}_{C} = \frac{1}{C} \int idt = \frac{q_{c}}{C} 
$$
$$
V_{c}(t) = v_{0}e^{-t/\tau_{RC}} 
$$
Discharging with $\tau = RC$
 
 $$
I_{L}(t) = I_{0}e^{-t/\tau_{LR}} 
$$
Decay with $\tau_{LR} = \frac{L}{R}$ and $I_{0}=\frac{V_{0}}{R}$
$$
V_{LC} (t) = V_{0}\cos (\omega t +\phi)
$$
with $\omega = \frac{1}{\sqrt{ LC }}$

Energy in capacitor
$$
U=\frac{1}{2}\frac{q^{2}}{C}
$$
Energy in inductor
$$
U=\frac{1}{2}Li^{2}
$$
- The maximum energy stored in the inductor is equal to the maximum energy stored in the capacitor. The maxima are $90\deg$ out of phase with each other. 

> "im such a man i have a big truck"

>"some people are just less intelligent then other people"

