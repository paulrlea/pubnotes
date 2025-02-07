# Exponential Analysis of [[AC circuits ]]
## Root mean square
- Square instantaneous current/voltage
- Take the average and square root
Given by: 
$$
i(t) - I \cos(\omega t)
$$
$$
\implies I_{r m s } = \sqrt{ (i^{2})_{avg} } = \sqrt{ \frac{1}{T}\int ^{T}_{0}i^{2}(t) \, dt  }
$$
$$
\dots
$$
$$
I_{r m s } = \frac{I}{\sqrt{ 2 }} ;V_{rms} = \frac{V}{\sqrt{ 2 }}
$$
## Power in AC circuit 
$$
 P(t) = i(t) v(t)
$$
### [[Resistor]]
$$
P_{r}(t) = i_{R}v_{R} = \frac{V_{r}^{2}}{R}\sin(\omega t)
$$
$$
P_{Ravg} = \frac{1}{2} \frac{V_{R}^{2}}{R}=\frac{V^{2}_{rms}}{R}
$$
### [[capacitor]]s
$$
P_{c}(t) = i_{c}v_{c}=V_{c}^{2}\omega t\sin(\omega t)\cos(\omega t)
$$
$$
P_{cavg} = 0
$$
- As the charge oscillates, energy flows into and then out of a capacitor. 
- Ideal capacitors and inductors don't dissipate any energy. 

### [[Inductors]]
$$
p_{L}(t) = \frac{V_{L}^{2}}{X_{L}} = \sin(\omega t)\cos(\omega t)
$$
$$
P_{Lavg}=0
$$
- As [[current]] oscillates, energy flows into and out of an inductor.


## Complex Exponential analysis
### Resistor
$$
v_{in}(t) = V_{0}\cos(\omega t) = \mathcal{R}e(V_{0}e^{j\omega t})
$$
Where $\mathcal{Re}$ is the real part. 
The relation between the voltage across a resistor and the current across is given by [[Ohm's Law]]. 

$$
v_{R}(t) - i(t)R
$$
$$
	i(t) - \frac{v_{0}(t)}{R}=\frac{V_{0}e^{j\omega t}}{R} = I_{0}e^{j\omega t}
$$
$$
Z_{R} = \frac{v_{r}}{i_{r}} = R
$$
[[Impedance]] across a resistor is given by the resistance
	(what is impedance)
In general, the impedance is given by $Z=R+jX$
The resistance is in phase and the reactance is out of phase part of current/voltage
$$
v(t) = Zj(t)
$$
	$R \to$ "in phase" part of $\frac{v}{i}$
	$X\to$ "out of phase" part of $\frac{v}{i}$

### Capacitors
$$
v_{in} (t) = v_{0} \cos(\omega t) = V_{0}e^{j\omega t}
$$
$$
v_{c}(t)=\frac{q_{c}(t)}{C}
$$
$$
\implies q_{c}(t)= Q_{0}e^{j\omega t}
$$
$$
i(t) - \frac{dq}{dt} = j\omega V_{0}Ce^{j\omega t}
$$
$$
Z_{c} = \frac{v(t)}{i(t)} = \frac{V_{0}e^{j\omega t}}{j\omega V_{0}Ce^{j\omega t}} = \frac{1}{j\omega c}
$$
$$
X_{c} = \frac{1}{\omega C}
$$
Phase change is given by $\frac{1}{j\omega c}$

### Inductors
$$
	v_{in} (t)= V_{0}\cos(\omega t) = V_{0} e^{j\omega t}
$$
$$
v_{in} + v_{2} = 0 \impliedby v_{in} = -v_{2} = L \frac{di}{dt}
$$
$$
	i(t) = \frac{1}{L}\int V_L(t)dt = \frac{V_{0}}{L} \int e^{j\omega t} \, dt = \frac{V_{0}}{j\omega L} e^{j\omega t}
$$
$$
Z_{L} = \frac{v}{i} = \frac{V_{0}e^{j\omega t}}{\frac{V_{0}}{j\omega L}e^{j\omega t}} = j\omega L
$$
Reactance across an inductor is given by $X_{L}=\omega L$ 
Multiply by $j$ = advancing the phase. 
Multiplying by $-j=\frac{1}{j}$ - delays the phase by $\frac{\pi}{2}$. 

## RC Circuit
![[/Attachments/Pasted image 20231102110216.png]]
$$
v_{in} = V_{0} e^{j\omega t}
$$
Loop rule: 
$$
v_{in}-v_{R}-v_{c} = v_{in}-iZ_{R}-iZ_{C} = 0
$$
$$
v_{in} = i\left( \frac{1}{j\omega c} + R \right)
$$The [[Impedance]] in the circuit is given by the content in the parentheses above

$$
i(t) = \frac{v_{in}}{R_{t} + \frac{1}{j\omega t}}
$$
Taking this equation and multiplying the top and bottom by the complex conjugate yields: 
$$
\frac{v_{in}\left( R-\frac{1}{j\omega c} \right)}{R^{2}+\left( \frac{1}{\omega} \right)^{2}} \implies v_{in} \frac{R+\frac{j}{\omega c}}{R^{2} + \left( \frac{1}{\omega c} \right)^2}
$$
and for current: 
$$
I = (i \cdot i^*)^{1/2} = v_{in} \frac{1}{\left[ R^{2} + \frac{1}{\omega c} ^{2}\right]^{1/2}}
$$
$$
V_{c} gain = g = | \frac{V_{c}}{V_{in}}| = | \frac{IX_{c}}{V_{in}}|
$$
## RL Circuit
![[Pasted image 20231102110156.png]]


$$
V_{in} = V_{0}e^{j\omega t} 
$$
Loop Rule: 
$$
v_{in}=[R+j\omega L]
$$
$$
i(t) = \frac{v_{in}}{R+j\omega L} = \frac{v_{in}}{R} \frac{1}{1 + j \frac{\omega L}{R}}
$$

fill this in later...

## RLC Circuit

![[Pasted image 20231102110638.png]]

$$
v_{in} = V_{0}e^{j\omega t}
$$
$$
v_{in} = i[Z_{i} + Z_{L} + R] = i\left( \frac{1}{j\omega c} +j\omega L + R \right)
$$
$$
i(t) = \frac{v_{in}}{R+j\left( \omega L-\frac{1}{\omega c} \right)}
$$
$$
v_{out} = Ri = v_{in} \frac{R}{R+j\left( \omega L - \frac{1}{\omega c} \right)}
$$
$$
g_{R} = | \frac{V_{out}}{V_{in}}| = | \frac{1-j\left( \omega  \frac{L}{R} - \frac{1}{\omega RC} \right)}{}
$$
finish above later
