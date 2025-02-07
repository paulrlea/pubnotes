#phys #lecture
## Review
- [[Notes/Introductory Electromagnetic Theory/Concepts/Faraday's law|Faraday's law]] from last class:
$$
\oint \vec{E}\cdot d\vec{s} =  -\frac{\partial\Phi_{B}}{\partial t}
$$
- Relates change in magnetic flux to induced EMF
- [[Inductance]] is the influence or effect of changing current on a device
- An [[inductor]] is a device whose function is to mitigate rapid changes in current through stored [[Magnetic Field]] energy
Magnetic Flux from a current will have form
$$
\Phi_{b} = Gi
$$
Where G is a factor of geometry and i is current. This is sometimes refereed to as "flux linkage" 
[[Inductance]] as a quantity can be define as either self inductance (L) of a device
$$
\Phi_{B} = Li
$$
or mutual inductance
$$
\Phi_{1} = Mi_{2}
$$

## Example 1: Self inductance of a solenoid
![[Attachments/Pasted image 20231025070016.png]]
Calculate the self-inductance of a [[solenoid]]:
$$
L_{oneturn} = |\frac{\Phi_{B,oneturn}}{i} | = \frac{\Phi_{B,turn}}{i}= \frac{BA_{turn}}{i}
$$
The magnetic field induced due to [[current]] through a coil is given by 
$$
 B=\mu_{0} \frac{N}{l}I
$$
Where N is number of turns, l is length, and I is current.
The flux through **one** loop is given by 
$$
\Phi_{B} = BA 
$$
$$
A = \pi r^{2}
$$
The flux linkage is therefore given by 
$$
\Phi_{BLink} = NBA = N\mu_{0} \frac{N}{l} I\pi r_{s}^2 = LI
$$
Where L is self inductance, rearranging above we get 
$$
L = \mu_{0} \frac{N^{2}}{l}\pi r_{s}^{2} = \mu_{0}n^{2}\pi r^{2}_{s}l
$$
## Persan's story

Henry Rowland did a bunch of experiments here where he saw how signals were sent from one wire to another. There is a walking tour of Albany where they show you Henry's poles where he was studying inductance. Now we know the unit of inductance to be known as a "Henry"

Persan's story over :(

An average inductance value for a [[solenoid]] is usually measured in millihenry. 
The inductor we used in the laboratory is 9.9E-3 Henry.

- For activity 
	- You can ignore b inside wire 
	- Ignore inside outer conductor
	- The current goes into paper

### Self Inductance of a coaxial cable: Activity 1

## [[Faraday's law]], [[Inductance]] and [[EMF]]
If you combine the concept of inductance with Faraday's law, you get a phenomenon in which the inductors within a system attempts to maintain the current within the system. This is why you see a little spark when a power supply is unplugged. Because they oppose sudden changes in current, they are often used for protection devices such as surge protectors.
Inductors allow us to do ""calculus"" with current. Capacitors also ""integrate"". 
*first lab in exphys is this 

Differentiating the inductance-current relationship yields: 
$$
\frac{d\Phi_{B}}{dt} = \frac{d}{dt}(Li) = L \frac{di}{dt}
$$
And using [[Notes/Introductory Electromagnetic Theory/Concepts/Faraday's law|Faraday's law]] we get 
$$
\mathcal{E}_{L} =  -L \frac{di}{dt}
$$
### In class example: 

An ideal solenoid has length 𝑙 = 1.5 cm, cross-sectional area $𝐴_{𝑙𝑜𝑜𝑝}$ = 0.78 cm^2, and number of turns 𝑁 = 2500. At time 𝑡 = 0.0 s a steady current 𝑖0 = 2.0 A flows through the solenoid. Suppose the current were to be cutoff as shown in the graph at right. (This is consistent with pulling a power supply plug from the wall.) The magnitude of the emf induced in the inductor is close to 1.6E4 V.

$$
L = \pi \mu_{0}n^{2}r_{s}^{2}l = 0.041H
$$
$$
\mathcal{E}=|-L \frac{\partial i}{\partial t} = 0.041 \cdot \frac{2.0}{5\cdot10^{-6}}
$$

Due to Lenz's law, [[inductor]]s can be used as surge protectors. 
## Change in potential across a conductor 
- Fields can be non-conservative, opposing jerkoffs junction law. 
$$
 \oint\vec{E}_{nc} \cdot d\vec{l} = -\frac{d\Phi_{B}}{dt}
$$
- Because the change in magnetic flux is confined inside the inductor, $\vec{E_{nc}}$ is also confined between the terminals of the inductor. 
- $$\int _{b}^a \,\vec{E}_{nc} \cdot d \vec{l} = -\frac{d\Phi_{B}}{dt} = - L \frac{di}{dt}$$
- Because the non conservative electric field is not 0 between a and b only, integrating [[@SchoolFall 2023/School/Physics/Physics 1250/Concepts/Faraday's law]] clockwise gives the above equation when you use the inductance-flux relation from earlier.( $\frac{d\Phi_{B}}{dt} = \frac{d}{dt}(Li) = L \frac{di}{dt}$ )
- An ideal inductor has 0 resistance. To have a finite current density, the total electric field acting on charges inside the conductor has to be close to 0. 
$$
\vec{E}_{tot} = \vec{E}_{c}+\vec{E}_{nc} = 0 \implies \vec{E}_{c} = -\vec{E}_{nc}
$$

TLDR: 
Potential Generated across an inductor is generated to maintain potential? across a circuit. If current increases in a circuit, an inductor will cause a current in the opposite direction. 
## Inductors in circuits
- They behave like ""batteries"" in circuits, supplying a "restoring" current
- Magnetic energy can be stored in inductors, given by 
	$$
 P_{L} - iV_{ab} = iL \frac{di}{dt}
$$
- This can be found by integrating supplied power over time. The energy is stored in the field. 
$$
 enter eq here
$$
- Energy density of the magnetic field is given by *insert here*
- [[Mutual Inductance]] occurs between two different devices. This is how transformers work. This is when the field generated by one coil passes through a different coil, which allows for power transfer and transformers. 
- Easier to calculate large-->small vs small-->large coil. 
- 
 