The RC circuit is composed of a resistor, a switch and a capacitor. The switch controls flow from the battery to the resistor and capacitor that are wired in series. 
![[Pasted image 20231026101652 1.png]]

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

Initial conditions: Uncharged capacitor at $t=0$ 
$$
\frac{\mathcal{E}_{c} -Q_{f}}{\mathcal{E}_{c}} = e^{-t/RC}
  $$
  $$
\implies Q(t) = \mathcal{E}C(1-e^{-t/RC}) 
$$

All of the above was about turning the circuit "on". Now what if we turn the circuit "off"?

We can redo the loop rule again with the switch in the B position after the capacitor is charged: 

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