## Superposition and Wave Interference

One of the most fundamental principles of wave motion is **superposition**. If two or more waves travel through the same medium, their displacements add algebraically. This gives rise to **constructive** and **destructive** interference:

- **Constructive interference**: When two waves are in phase, their amplitudes add, leading to a larger resultant wave.
- **Destructive interference**: When two waves are out of phase by $\pi$ radians (or $180^\circ$), they cancel out.
### What do we observe?

- Optical and sound power
- Quantum probability

### Adding Waves

- **Linear superposition**
- **Interference**
- **Intensity and Probability**

## Where are we going with this?

- Understanding waves helps transition into quantum mechanics.
- Quantum physics of photons passing through two paths.
- Single photon experiments as tests of quantum mechanics.
- Interference of two waves at the same point.

## Intensity, Probability, and Amplitude

- Energy of sinusoidal waves $\propto A^2$
- Examples:
    - **String waves**: $P_{\text{avg}} \propto A^2$
    - **Sound waves**: $I \propto A^2$
    - **Electromagnetic waves**: $I \propto E_{\max}^2$

## Quantum Waves

- Probability of finding a particle: $|\Psi|^2 dV$
- Probability current density: $J = \frac{\hbar k}{m} A^2$

## Key Takeaways

- To determine probability or rate, square the amplitude of the wave.
- Though discussed using sound waves, concepts apply broadly.

## Power and Wavefunctions

- **Sound wave displacement**:  
  $$y(x,t) = A \sin k(x - vt)$$
- **Instantaneous power per unit area**:  
  $$\frac{P}{\text{area}} = \rho B \omega^2 y^2(x,t) = \rho B \omega^2 A^2 \sin^2(kx - vt)$$
- **Time-averaged intensity**:  
  $$\left\langle \frac{P}{\text{area}} \right\rangle = \frac{1}{2} \rho B \omega^2 A^2$$

---

## Time Averages of Waves

- **Mathematical definition**:  
  $$\langle y(t) \rangle = \frac{1}{T} \int_0^T y(t) dt$$
- **Sine and cosine functions**:
    - Averages over a full cycle are zero.
    - Average of $\sin^2(\omega t)$ and $\cos^2(\omega t)$ is $1/2$.

## Addition of Waves

- **Linear Superposition**:  
  $$y(x,t) = y_{1}(x,t) + y_{2}(x,t)$$
- **Interference**:
    - Waves overlap in space.
    - Coherent waves (constant phase difference) show strong interference effects.
    - Resultant amplitude = sum of individual field amplitudes.

## Adding Two Waves

- **Equal amplitudes**:  
  $$\sin a + \sin b = 2 \sin \left(\frac{a+b}{2}\right) \cos \left(\frac{a-b}{2}\right)$$
- **Unequal frequencies**:  
  $$\sin(\omega_1 t) + \sin(\omega_2 t) = 2 \sin \left(\frac{\omega_1 + \omega_2}{2} t \right) \cos \left(\frac{\omega_1 - \omega_2}{2} t \right)$$
- **Beats**:
    - Rapid oscillation at average frequency $\frac{\omega_1 + \omega_2}{2}$.
    - Slow modulation at beat frequency $\frac{\omega_1 - \omega_2}{2}$.

## Interference of Waves

- Two waves with equal amplitudes and frequencies but different phase:  
  $$y_{\text{tot}} = y_1 + y_2 = 2 y_0 \cos \left( \frac{\Delta \phi}{2} \right) \sin\left(\omega t + \frac{\phi_1 + \phi_2}{2}\right)$$
- **Interference Intensity**:  
  $$I_R = 4I_0 \cos^2 \left( \frac{\Delta \phi}{2} \right)$$

## Controlling Phase Difference

- Methods:
    - Splitting a wave with a partially reflecting mirror.
    - Sending waves through different paths.
See [[Mach-Zehnder Interferometer]]
