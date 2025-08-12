# Diffraction 
- Diffraction pattern is derived from the interference of all wavelets using the amplitude and phase difference of each. 
- Interference is superposition of a "few" waves, diffraction is used when there are many waves.
- Diffraction problems have two cases:
	- Fraunhofer (Far-Field)
	- Fresnel (Near-Field)
- Relative length scale set by $\lambda$ , size of aperture, and distance to observer. 
- For a circular aperture phase difference from center to edge is given by 
$$
\Delta \phi = \frac{2\pi}{\lambda}\left[ \sqrt{ d^{2}+\frac{a^{2}}{4} }-d \right] = \frac{2\pi}{\lambda}d\left[ \sqrt{ 1-\frac{a^{2}}{4dsr} }-1 \right] \approx \frac{2\pi}{\lambda}\left( \frac{a^{2}}{8d} \right)
$$
- If $d \gg \frac{a^{2}}{\lambda}$ then it is reasonable to treat rays as parallel and $\Delta \phi$ to be small. 
- If $d< \frac{a^{2}}{\lambda}$ then the phase differences become large and rays are not parallel. 

## Diffraction as N-source Interference
Assuming:
- No initial phase differences
- Sources are small compared to wavelength 
- Observation point P is far away
The amplitudes of waves arriving at P are equal 
$$
E_{0}(r_{1}) = E_{0}(r_{n})
$$
The phase difference between adjacent sources is given by:
$$
\frac{2\pi}{\lambda}d\sin \theta
$$
And maxima occurs when: 
$$
d\sin \theta_{m} = m\lambda
$$
Diffraction gratings are modeled by this: 
$$
m\Delta\lambda = d\cos \theta \Delta\theta \implies \Delta\theta = \frac{m\Delta\lambda}{d\cos \theta}
$$
Two different wavelengths show principle maxima @ different values of $\theta_{m}$. Thus, diffraction gratings are used to separate wavelengths. 

The width of a "strong peak" is approx $\delta\theta = \frac{\lambda}{Nd\cos \theta}$ where N = number of slits. 
![[/Attachments/Pasted image 20231130112319.png]]

# Single Slit Diffraction

We can model a single slit diffraction as $n$ wavelets emitting $n$ parallel rays at an angle $\theta$. Dividing the sources into two zones of width $\frac{a}{2}$, then the angle of the first intensity minimum occurs when destructive interference between all of zone 1 and 2.
First Destructive interference of a slit with width $a$ occurs when 
$$
\frac{a}{2}\sin \theta_{1} = \frac{\lambda}{2}
$$
This can be generalized to the $m$'th slit by dividing the slit width with larger numbers. Rearranging this idea, we get the formula below: 
$$
a\sin \theta _{m} = m'\lambda 
$$
where 
$$
m' = \pm 1, \pm 2, \pm 3\dots
$$
## Intensity of single slit diffraction 
Intensity is obtained by summing all the wavelets from the $n$ rays to get the amplitude. This can be modeled with phasors. 
![[/Attachments/Pasted image 20231204112428.png]]
![[/Attachments/Pasted image 20231204112437.png]]

