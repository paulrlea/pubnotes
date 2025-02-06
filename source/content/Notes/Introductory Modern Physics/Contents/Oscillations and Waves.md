# What is an Wave?
- A wave refers to a "_propagating dynamic disturbance (change from equilibrium) of one or more quantities_." In laymen speak, this means any form of periodic motion that propagates through a medium. 
- To further explore this, we must first look at the concept of periodic motion. Periodic motion, as the name may imply, is motion that occurs cyclically, or periodically. The reader may scoff at this, thinking that this is a very simple concept. However, this simple concept is arguably one of the most central topics in every branch of physics and related subjects. 
- Periodic motions and waves govern the motion of everything from the atomic particles in [[Quantum Harmonic Oscillators]] to [[Gravitational Waves]] emitted by collapsing stars.

## Times and Positions

![[Pasted image 20250206191657.png]]

> Figure 1: A pendulum's motion plotted

As you can see above, this is an example of periodic motion. A pendulum swings in an ideal environment, yielding periodic motion and its **Amplitude** is represented by the displacement of the highest point in the swing. The **Equilibrium position** represents the vertical hanging position, where the pendulum would lie if stopped. We call the time period **between two consecutive peaks** the Period of the oscillation. 

The **Frequency** of the oscillation is the inverse of the time, measured in a unit called **Hertz**. The definition of 1 hertz, is $\frac{1}{s}$, or one inverse second. This might sound kind of counter-intuitive, but you can think of it as meaning that *something* happens once a second. So if a pendulum is oscillating at one hertz, that means its oscillating at a rate of 1 time per second. Therefore, we can convert period to frequency and vice versa by taking the inverse. 

$$
f = \frac{1}{T}
$$

In **Periodic motion**, the wave has consistent amplitude through time, and a consistent period. 

## Now for some maths

Unfortunately for us physicists, math is often used in physics. The following is one example of the infiltration of physics by the unknowable symbols of mathematics. 

$$
y(t) = A \sin (\omega t + \phi)
$$

Do not panic. There may be symbols here that would scare most people away, but I will shed light on them. 

The expression on the left, $y(t)$, represents the **current displacement** of the oscillator. In the case of the pendulum, this is how far it is currently away from the equilibrium position. 

The expression on the right has several quantities that we can define. $A$ represents the amplitude of the oscillator, or how far from equilibrium it will travel at its peak. $\omega$ is the Greek letter lowercase omega, and here it represents the [[angular frequency]] of the oscillator, defined by $\omega = \frac{2\pi}{T}$, where T is the period and $\pi$ is $\pi$. t represents the time since the system was started, and is the independent variable in this equation if you will. Lastly, $\phi$ represents the initial phase of the system, so at what initial state the system started at.

Now that we have gone through this, we can continue our mathematical conquest. 

## Oscillations in space

If we decide to leave our trusty pendulum analogy behind, we can explore the world of oscillations in space. Like a plucked string, or a light wave frozen in space. 

![[Pasted image 20250206194012.png]]

> Fig 2: Spatial Oscillations

Being savvy and good at pattern recognition, we can see that this graph is quite similar to the one above, if we just substitute $t$ for $d$. Therefore, we can reuse the equation from before as follows:

$$
y(x) = A \sin \left( \frac{2\pi}{\lambda} x + \phi \right)
$$
But wait! We have new and scary letters! The attentive reader may see that $\lambda$, or lambda, also appears in figure 2 labeled as wavelength. This is the analog of the period for waves in space, and likewise, frequency is the inverse. But wait, says the attentive reader, we said earlier that these waves are frozen in time. How can an oscillation happen at a frequency, when frequency is defined as inverse time? Good attention. I lied to you. For a wave trapped in time, frequency doesn't mean much. Luckily, in reality all waves are moving in time, and some in space. This means that the math gets a little more interesting and we can really begin to see how the [[Traveling Waves]] are formed.

See also: 
https://www.sciencelearn.org.nz/resources/119-fundamentals-of-waves#:~:text=As%20well%20as%20a%20defined,hertz%20(waves%20per%20second).

