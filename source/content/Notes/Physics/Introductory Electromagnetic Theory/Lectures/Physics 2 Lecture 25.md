# Wave superposition
- The resultant superposition of any two waves in space is given by the sum of the two constituent waves. 
- This can leave to various interesting effects
## - Example: Harmonic Traveling Waves
$$
y(t) = y_{m}\sin(kx-\omega t) = y_{m}  \sin(k[x-vt])
$$
- This represents a wave of amplitude $y_{m}$ traveling in the x direction at wave speed $v_{phase} = \frac{\lambda}{t}= \lambda f$. 
- The **[[phase]]** of the wave is given by the argument of the sin function. For the example above: 
$$
\varphi (t) = kx-\omega t +\phi
$$
- Where $\phi$ is the initial phase of the wave. A point with a specific phase moves to the right w/ velocity $v$. 
## Phase difference
- Phase difference, $\Delta \varphi$, refers to how the argument of the sin function differs at different times or places in the wave. 
- 2 times at the same point: 
$$
\Delta \varphi = \left[ \frac{2\pi}{\lambda}v\Delta t \right]=\omega \Delta t
$$
- 2 points at the same time
$$
\Delta \varphi = \left[ \frac{2\pi}{\lambda}\Delta x \right]=k\Delta x
$$
## Separating time and space
- Consider a plane wave: 
$$
E(x, t) = E_{0}\sin[\omega t-(kx+\phi)]
$$
- To separate the time and space elements, let $a(x, \phi) = -kx-\phi$
- In the case of two waves coexisting in space, we get: 
$$
E_{1} = E_{01} \sin (\omega t + \alpha_{1}) = E_{01}[\sin(\omega t)\cos \alpha_{1} + \cos(\omega t)\sin \alpha_{1}]
$$
and 
$$
E_{2} = E_{02} \sin (\omega t + \alpha_{2}) = E_{02}[\sin(\omega t)\cos \alpha_{2} + \cos(\omega t)\sin \alpha_{2}]
$$
And the traveling wave is given by 
$$
E_{T} = E_{1} + E_{2} = [E_{01} \cos\alpha_{1} + E_{02}\cos\alpha_{2}]\sin(\omega t) + [E_{01}\sin\alpha_{1} + E_{02}\sin\alpha_{2}]\cos(\omega t)
$$
Adding and squaring the two terms gives: 
$$
E_{0}^{2} = E_{01}^{2} + E_{02}^{2} +2E_{01}E_{02}\cos(\alpha_{2}-\alpha_{1})
$$
Where the $2E_{01}E_{02}\cos(\alpha_{2}-\alpha_{1})$ term is known as the interference term. Once we have the field, we can find the intensity: 
$$
I=\frac{E^{2}}{2\mu_{0}c} \implies I=I_{1} + I_{2} +2\sqrt{ I_{1}I_{2} }\cos \delta
$$
where $\delta=\alpha_{2}-\alpha_{1}$

- The intensity of resulting wave is not just sum, but there is also interference term.
- There is constructive and destructive interference
![[Attachments/Pasted image 20231127104627.png]]

- Special case $I_{1}=I_{2}$: 
$$
I=4I_{1}\cos ^{2}\left( \frac{\delta}{2} \right)
$$
## Complex Expression of waves: 

$$
E_{n}=E_{0n}e^{j(\omega t+\alpha_{1})} 
$$
Then 
$$
E_{T}=e^{j\omega t}[E_{01}e^{j\alpha_{1}} + E_{02} e^{j\alpha_{2}}] = E_{0}e^{jx}e^{j\omega t}
$$
and intensity is given by: 
$$
I = (E_{0}e^{j\alpha})(E_{0}e^{j\alpha})^{*}
$$
Where 
$$
\tan\alpha=\frac{E_{01}\sin\alpha_{1}+E_{02}\sin\alpha_{2}}{E_{01}\cos\alpha_{1}+E_{02}\cos\alpha_{2}}
$$
Cool thing about complex exponentials is that they can be graphically represented with [[Phasor]]s. We can represent the superposition of many waves graphically as an addition of vectors in the complex plane. 
	![[/Attachments/Pasted image 20231127105205.png]]For cosine waves, $E_{0}$ will be the projection onto the horizontal axis and sine waves will be onto the vertical axis. 

Since $a=-kx-\epsilon$ where $k=\frac{2\pi}{\lambda}$ we can write $\delta=\alpha_{2}-\alpha_{1}=(k_{1}x_{1}+\epsilon_{1})-(k_{2}x_{2}+\epsilon_{2})$
$$
=\left[ \frac{2\pi}{\lambda_{1}}x_{1} - \frac{2\pi}{\lambda_{2}}x_{2} \right] + (\epsilon_{1}-\epsilon_{2})
$$

## What causes Phase Differences? 
- Difference in wave generation
- Path length differences 
- Reflections

To find total phase shift: 
$$
\delta = \delta_{i n i t a l \ ph a s e} + \delta_{p a t h \ l e n g t h} + \delta _{ r e f lectio n}
$$
$$
=\epsilon+\delta_{opl} + \delta_{R}
$$
Supposing the two waves are initially in phase $(\epsilon_{1} = \epsilon_{2})$ we have: 
$$
\delta = \frac{2\pi}{\lambda_{1}}k_{1} - \frac{2\pi}{\lambda_{2}}k_{2}=\frac{2\pi}{\Lambda_{0}}n_{1}L_{1} - \frac{2\pi}{\lambda_{0}}n_{2}L_{2}
$$
$$
\delta = \frac{2\pi}{\lambda_{0}}[n_{1}L_{1}-n_{2}L_{2}]
$$
Where the $[n_{1}L_{1}-n_{2}L_{2}]$ term is the optical path differences

## Young's Double Slit Experiment
![[/Attachments/Pasted image 20231127110322.png]]
Above is a diagram of [[Young's Double Slit Experiment]]. R is distance from slit to screen, d is distance between slits. R >> d. 
Path length difference is given by $\Delta L=d\sin\theta$
- Constructive interference occurs when 
	$\Delta L=d\sin\theta=m\lambda$
- Destructive Interference occurs when
	$\Delta L = d\sin\theta=\left( m+\frac{1}{2} \right)\lambda$
Where $m \in$ integers. It is known as the order of the maxima/minima. 
We can also use the small angle approximation for this: 
$$
\sin \theta \approx \tan \theta + \frac{y}{s}
$$
in this limit, the position of the m'th bright fringe is 
$$
y_{m} = m\lambda    \frac{D}{d} 
$$
or
$$
\theta_{m} = \frac{m\lambda}{d}
$$
Then the distance between adjacent maxima is given by 
$$
\Delta y = y_{m+1} -y_{m} = \frac{(m+1)\lambda D}{d} - \frac{m\lambda D}{d}
$$
$$
\implies \Delta y=\frac{\lambda D}{d}
$$
The intensity for the two slit interference is given by
$$
I=4I_{0}\cos ^{2}\left( \frac{\pi d}{\lambda D}y \right)

$$
