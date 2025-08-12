
First we need to find the amperage using
$$
V=IR \to \frac{V}{R} = I
$$
We are given the voltage $(12.7 \pm 0.2 V)$ and the resistance $(8.3 \pm 0.4 \Omega)$, and using this we can find the current, and uncertainty of current.
$$
I = \frac{12.7 \pm 0.2 V}{8.3 \pm 0.4 \Omega}
$$
$$
I = 1.53\begin{aligned} \Delta I &= \sqrt{\left( \frac{\partial I}{\partial V} \Delta V \right)^2 + \left( \frac{\partial I}{\partial R} \Delta R \right)^2} \\ &= \sqrt{\left( \left( 1 / R \right) \cdot \Delta V \right)^2 + \left( \left( -(V / R ^ 2) \right) \cdot \Delta R \right)^2} \\ &= 0.0775779185 \\ &= 7.75779185 \times 10^{-2} \\ &= 8 \times 10^{-2} \end{aligned}I = \left( 1.53 \pm 0.08 \right)
$$
$$
I = 1.53 \pm 8 \times 10^{-2}
$$
With the current, we can use the Biot-Savart law for coils to derive the magnetic field
$$
B = 0.0588831971\begin{aligned} \Delta B &= \sqrt{\left( \frac{\partial B}{\partial I} \Delta I \right)^2 + \left( \frac{\partial B}{\partial r} \Delta r \right)^2 + \left( \frac{\partial B}{\partial z} \Delta z \right)^2} \\ &= \sqrt{\left( \left( r ^ 2 * (2 r ^ 2 + z ^ 2) ^ (-3 / 2) \right) \cdot \Delta I \right)^2 + \left( \left( (2 * I * r * (2 r ^ 2 + z ^ 2) ^ (3 / 2) - 6 * (2 r ^ 2 + z ^ 2) ^ (1 / 2) * r ^ 3 * I) / (2 r ^ 2 + z ^ 2) ^ 3 \right) \cdot \Delta r \right)^2 + \left( \left( -(3 * (2 r ^ 2 + z ^ 2) ^ (-5 / 2) * I * r ^ 2 * z) \right) \cdot \Delta z \right)^2} \\ &= 0.011977196 \\ &= 1.1977196 \times 10^{-2} \\ &= 1 \times 10^{-2} \end{aligned}
$$
$$
B = \left( 6 \pm 1 \right) \times 10^{-2}
$$

Part B:

Using the angle version of the cross product:
$$
\vec{\tau} = \vec{\mu} \times \vec{B} \to |\vec{\mu}| |\vec{B}| \sin(\theta) \vec{n} = \vec{\tau}
$$
Where $\vec{n}$ is the unit vector orthogonal to $\vec{\mu}$ and $\vec{B}$. 
We don't care about direction, so we can rewrite this, with the values we derived above and values given, as the following
$$
0.051 \pm 0.20 \text{ Nm} = \sin(45 \pm 1) (6\pm 1)^{-2} |\mu|
$$
And solving for $\mu$, the magnetic moment, we can rearrange this: 
$$
\frac{0.051 \pm 0.20 \text{ Nm}}{\sin(45 \pm 1) (6\pm 1)^{-2}} = |\mu|
$$
Solving this with error propagation, we have the following:
$$
m = 1.0178844301\begin{aligned} \Delta m &= \sqrt{\left( \frac{\partial m}{\partial T} \Delta T \right)^2 + \left( \frac{\partial m}{\partial a} \Delta a \right)^2 + \left( \frac{\partial m}{\partial B} \Delta B \right)^2} \\ &= \sqrt{\left( \left( B * sin(a) / (sin(a) * B) ^ 2 \right) \cdot \Delta T \right)^2 + \left( \left( -(T / (sin(a) * B) ^ 2 * B * cos(a)) \right) \cdot \Delta a \right)^2 + \left( \left( -(T / (sin(a) * B) ^ 2 * sin(a)) \right) \cdot \Delta B \right)^2} \\ &= 0.7642771649 \\ &= 7.642771649 \times 10^{-1} \\ &= 8 \times 10^{-1} \end{aligned}\
$$
$$
m = \left( 1 \pm 0.8 \right)
$$

Part 3: 

## c) This experiment is a good example of a combination of statistical and systematic uncertainty. Repeated measurements of the torque will reduce the uncertainty on the torque, but not on the magnetic field or angle. Thus, the torque exhibits statistical uncertainty while the errors on the B field and angle are systematic. What will the uncertainty on the torque be by making 100 measurements? What about the uncertainty on the magnetic moment?

The uncertainty in the torque will be reduced with more measurements by a factor of $\frac{1}{\sqrt{ N }}$. With N=10, it measures to be  $\pm 0.02$ Nm, and if we compare the ratio of N=10 and N=100
$$
\frac{\frac{1}{\sqrt{ 100 }}}{\frac{1}{\sqrt{ 10 }}}  = \frac{\tau_{100}}{0.02}
$$
And therefore $\tau_{100} = 0.006324$

The uncertainty of the magnetic moment is systematic, and with more measurements it will remain the same. 
