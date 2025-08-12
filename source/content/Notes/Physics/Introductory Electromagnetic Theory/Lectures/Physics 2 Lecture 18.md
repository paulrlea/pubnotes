# AC Circuits
#phys #lecture 
# Harmonic Signals
- Harmonic [[EMF]] occurs when a coil is spun in a magnetic field. 
- Sinusoidal voltages can be transformed with [[inductor]]s
- Any periodic signal can be represented with a Fourier Series as a series of sines and cosines
- Any pulse can be represented as the integral of sine and cosine signals [[Fourier transform]]
# [[Phasor]] Representation of Harmonic quantities.
Given Harmonic quantity:
$$
v=V_{0} \cos(\omega t+\phi)
$$
it can be represented as a rotating vector known as a [[Phasor]]. Phasors follow the following rules: 
1. They rotate in the CCW direction with a given angular speed $\omega$. 
2. The length of each phasor is proportional to the AC amperage. 
3. The projection of the phasor on the x-axis yields an instantaneous value for the phasor.
![[Attachments/Pasted image 20231030152406.png]]
When we want to add instantaneous voltages around a loop, we need to know the phase. 
$$
v_{1}(t) = V_{1}\cos(\omega t)
$$
$$
v_{2}(t)=V_{2}\cos(\omega t+\phi)
$$
Phasors can be added just like vectors, adding two AC voltages that are 90 degrees yields the following: 
$$
v_{1}(t)=V_{1}\cos(\omega t)
$$
$$
v_{2}(t)=V_{2}\cos\left( \omega t+\frac{\pi}{2} \right)
$$
$$
v_{1}(t) + v_{2}(t) = V_{T}\cos(\omega t + \varphi)
$$
Where $\varphi$ represents the phase angle

$$
V_{T}=\sqrt{ V_{1}^{2} +V_{1}^{2}}
$$
and
$$
\varphi=\tan ^{-1}\left( \frac{V_{1}}{V_{2}} \right)
$$
# Resistor in an AC circuit
![[Attachments/Pasted image 20231030155502.png]]
- Resistance in an AC circuit does not depend on the frequency of the AC source.
- Voltage and [[current]] are related by [[Ohm's Law]]$$
V_{r}=I_{0}R
$$
- The [[Phasor]]s for current and voltage are in phase with one another. 
- Functionally very similar to a DC circuit.

# Capacitors in an AC circuit
![[Attachments/Pasted image 20231030162019.png]]
$$
v_{c}(t) = V_{c}\sin(\omega t)
$$
$$
\implies q_{c} = Cv_{c}= CV_{c}\sin(\omega t)
$$
$$
i_{c} = \frac{dq_{c}}{dt} = cv_{c}\cos(\omega t) =\frac{V_{c}}{I/C\omega }\cos (\omega t)
$$
$$
\implies i_{c}= I_{c}\sin(\omega t+\phi)
$$
Capacitor Connected to an AC sources voltage current amplitudes related by
$$
V_{c} = I_{c}X_{c}
$$

$$
X_{c}=\frac{1}{\omega c}
$$
Where $X_{c}$ is known as the *reactance*
- The voltage curve "lags" behind the current curve by a quarter cycle, so $\phi=-\frac{\pi}{2}$. 
# Inductors in AC circuit
![[Attachments/Pasted image 20231030162411.png]]
$$
v_{L}(t)= V_{c}\sin(\omega t) = +L \frac{di}{dt}
$$
$$
\implies i(t) = -\frac{V_{L}}{\omega L} \cos(\omega t)
$$
Voltage in inductors is 90 degrees ahead of current. 
![[Attachments/Pasted image 20231030162520.png]]
When an inductor is connected to an AC source, the voltage and current are related by: 
$$
V=IX_{L}
$$
$$
X_{L} \equiv \omega L
$$
**eLi** the **iCe** man

Where in an inductor (L), voltage leads current and vice versa for capacitors. 
# [[Complex number]] Review

Complex numbers are important because they can represent [[Phasor]]s, which have both a real and imaginary component. 

The complex number $j = \sqrt{ -1 }$. [[Complex number]]s have a real and imaginary part, and can be represented graphically. 
$$
\tilde{z} = x + jy
$$
alternate form of: 
$$
\tilde{z} = \mathrm{re}^{i\theta}
$$
$$
r=\sqrt{ \vec{r} \cdot \vec{r} } = \sqrt{ x^{2}+y^{2} }
$$
$$
\theta = \tan ^{-1}\left( \frac{y}{x} \right)
$$
Another alternate form using [[Euler's Formula]]
$$
\tilde{z}=r(\cos \theta_+j\sin \theta)
$$
Multiplying a harmonic function by $j$ increases the phase by $\frac{\pi}{2}$.
Increasing the phasor by 90* ccw.

$$
\tilde{A}(t) = jae^{j\omega t} =  ae^{j(\omega t + \pi/2)}
$$
$$
\sin(\omega t) = \cos\left( \omega t - \frac{\pi}{2} \right)
$$
$$
\tilde{z}_{i}  + \tilde{z}_{l} = e^{j_{4}}[(A_{1}+A_{2}e^{j\
})]
$$
## Basic complex arithmetic
If $\tilde{z}_{1} =A_{1}e^{j}$ and $\tilde{z}_{2}=A_{2}e^{j(\varphi+\delta)}$ then
$$
\tilde{z}_{1} + \tilde{z}_{2} = e^{j\varphi} (A_{1}+A_{2}e^{j\delta})
$$
$$
\dots
$$
$$
=e^{j\varphi}Me^{j\beta} = Me^{j(\beta+\varphi)}
$$
where
$$
M = \sqrt{ (A_{1}+A_{2}\cos \delta)^{2} + (A_{2}\sin\delta)^{2} }
$$
If $\tilde{z}_{2} = r_{1}e^{j\theta_{1}}$ and $\tilde{z}_{2} = r_{2}e^{j\theta_{2}}$
then
$$
\tilde{z}_{1}\tilde{z}_{2} =  r_{1}e^{j\theta_{1}}r_{2}e^{j\theta_{2}} = r_{1}r_{2}e^{j(\theta_{2}+\theta_{1})}
$$
and
$$
\frac{\tilde{z}_{1}}{\tilde{z}_{2}} = r_{1}e^{j(\theta_{1}-\theta_{2})}
$$
Complex Conjugate: invert complex components (put negative sign in front of j)
Complex ratios: $$\frac{a+jb}{c+jd} = \frac{(a+jb)(c-jd)}{(c+jd)(c-jd)}$$
$$
=\left( \frac{ac+bd}{c^{2}+d^{2}} \right) + j\left( \frac{-ad+bc}{c^{2}+d^{2}} \right)
$$


