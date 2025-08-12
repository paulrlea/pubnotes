An RL circuit is a circuit with a resistor and an inductor in series. Same as above RC circuit, but replacing the capacitor with an inductor. 
- ![[Pasted image 20231026104605 1.png]]
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
![[Pasted image 20231026105708 1.png]]
