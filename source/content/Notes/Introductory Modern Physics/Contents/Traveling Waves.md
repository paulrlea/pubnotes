# Waves, but moving
Now that we have mastered the domain of waves that do not move, lets look at the ones that do. This will consist of the real stuff, like light waves, gravitational waves, and ocean waves. (We'll put that quantum harmonic oscillator in the back of our minds until we learn about [[standing waves]]) 

Armed with the knowledge from stationary waves, we can write a multi-varied function for traveling waves as follows: 
$$
y(x,t) =  y_{m} \sin\left( \frac{2\pi}{\lambda} x-\frac{2\pi}{T}t +\phi \right) = y_{m}\sin \left[ \frac{2\pi}{\lambda}\left( x-\frac{\lambda}{T}t \right)+\phi \right]
$$
This is a long equation, but pretty simple at heart. The displacement of the wave at a time $t$ and a place $x$ is given by the right-hand side. The amplitude here is $y_{m}$.

## Wave Speed and Wave Number

From the equation above, we can identify key parameters of a traveling wave. Most of these should be familiar from the section on [[Oscillations and Waves]]:

- **Wavelength ($\lambda$)**: The spatial period of the wave, or the distance over which it repeats.
    
- **Period ($T$)**: The time it takes for one full oscillation at a fixed point.
    
- **Wave Number ($k$)**: Defined as $k = \frac{2\pi}{\lambda}$, representing the spatial frequency of the wave.
    
- **Angular Frequency ($\omega$)**: Defined as $\omega = \frac{2\pi}{T}$, representing the temporal frequency of the wave.
    
- **Wave Speed ($v$)**: The speed at which the wave propagates, given by: $v =\frac{\lambda}{T} = \frac{\omega}{k}$
    

This tells us that the wave travels with a velocity $v$, moving in the **positive** $x$-direction if the phase term is $x - vt$ and in the **negative** $x$-direction if it is $x + vt$.

## The General Solution

More generally, we can express any traveling wave as:
$$
y(x,t) = A\sin (kx-\omega t+\phi)
$$
or equivalently in cosine form:
$$
y(x,t) = A\cos (kx-\omega t+\phi)
$$
where the choice of sine or cosine depends on the **initial phase** conditions of the wave.
## Applications of Traveling Waves

### Sound Waves

Sound waves are longitudinal waves where pressure variations travel through a medium. The equation for a sound wave is similar but describes compressions and rarefactions rather than transverse displacements from an equilibrium. However, this can still be modeled as the graph we are familiar with. 

### Electromagnetic Waves

Maxwell's equations describe traveling electromagnetic waves, where electric and magnetic fields oscillate perpendicular to each other and to the direction of propagation. The wave equation applies to both electric and magnetic field components. You'll learn more about this in Intro Electromagnetic Theory. 

### Water Waves

Ocean waves are complex since they exhibit both transverse and longitudinal motion. Their behavior depends on water depth, with deep-water and shallow-water waves following different dispersion relations. 



