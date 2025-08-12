
Error Analysis and propagation for each theoretical period:

$$

T_{1}= 0.0311697124[\begin{aligned} \Delta T &= \sqrt{\left( \frac{\partial T}{\partial R} \Delta R \right)^2 + \left( \frac{\partial T}{\partial r} \Delta r \right)^2 + \left( \frac{\partial T}{\partial c} \Delta c \right)^2} \\ &= \sqrt{\left( \left( c * 693 / 1000 \right) \cdot \Delta R \right)^2 + \left( \left( c * 693 / 500 \right) \cdot \Delta r \right)^2 + \left( \left( (2 * r + R) * 693 / 1000 \right) \cdot \Delta c \right)^2} \\ &= 0.0005927819 \\ &= 5.927819 \times 10^{-4} \\ &= 6 \times 10^{-4} \end{aligned}

$$

$$
T_{1} = \left( 3.12 \pm 0.06 \right) \times 10^{-2}
$$

$$
T_{2} = 0.0249433708\begin{aligned} \Delta T &= \sqrt{\left( \frac{\partial T}{\partial R} \Delta R \right)^2 + \left( \frac{\partial T}{\partial r} \Delta r \right)^2 + \left( \frac{\partial T}{\partial c} \Delta c \right)^2} \\ &= \sqrt{\left( \left( c * 693 / 1000 \right) \cdot \Delta R \right)^2 + \left( \left( c * 693 / 500 \right) \cdot \Delta r \right)^2 + \left( \left( (2 * r + R) * 693 / 1000 \right) \cdot \Delta c \right)^2} \\ &= 0.0004742521 \\ &= 4.742521 \times 10^{-4} \\ &= 5 \times 10^{-4} \end{aligned}
$$
$$
T_{2} = \left( 2.49 \pm 0.05 \right) \times 10^{-2}
$$
$$
T_{3} = 0.399359961\begin{aligned} \Delta T &= \sqrt{\left( \frac{\partial T}{\partial R} \Delta R \right)^2 + \left( \frac{\partial T}{\partial r} \Delta r \right)^2 + \left( \frac{\partial T}{\partial c} \Delta c \right)^2} \\ &= \sqrt{\left( \left( c * 693 / 1000 \right) \cdot \Delta R \right)^2 + \left( \left( c * 693 / 500 \right) \cdot \Delta r \right)^2 + \left( \left( (2 * r + R) * 693 / 1000 \right) \cdot \Delta c \right)^2} \\ &= 0.0075955924 \\ &= 7.5955924 \times 10^{-3} \\ &= 8 \times 10^{-3} \end{aligned}
$$
$$
T_{3} = \left( 3.99 \pm 0.08 \right) \times 10^{-1}
$$
$$
T_{4} = 0.1812163122\begin{aligned} \Delta T &= \sqrt{\left( \frac{\partial T}{\partial R} \Delta R \right)^2 + \left( \frac{\partial T}{\partial r} \Delta r \right)^2 + \left( \frac{\partial T}{\partial c} \Delta c \right)^2} \\ &= \sqrt{\left( \left( c * 693 / 1000 \right) \cdot \Delta R \right)^2 + \left( \left( c * 693 / 500 \right) \cdot \Delta r \right)^2 + \left( \left( (2 * r + R) * 693 / 1000 \right) \cdot \Delta c \right)^2} \\ &= 0.0034472648 \\ &= 3.4472648 \times 10^{-3} \\ &= 3 \times 10^{-3} \end{aligned}
$$
$$
T_{4} = \left( 1.81 \pm 0.03 \right) \times 10^{-1}
$$



# Section 2: Voltage divider

### Objective: 
Create and use a voltage divider for use in section 3, the Op-Amp circuit. Utilize previous circuits knowledge and analyze voltage divider theoretically and experimentally.

### Equipment: 
Resistors, Multimeter, Osciliscope, Jumper Cables, 555 Timer circuit from section 1, 9v battery and harness.
### Procedure:
Perform calculations to determine theoretical voltage attenuation given certain resistors value. Target for voltage attenuation is 10x. Use breadboard, resistors, and jumpers to create circuit outlined in diagram below. Apply voltage and use multi-meter to verify the calculated voltage attenuation is accurate.

Beginning with the target attenuation (10x), we can calculate the ratio of resistance we need.

$$

V_(out) = \frac{R_2}{R_1+R_2} \cdot V_(in)

$$

Rearrange to solve for attenuation
$$
\frac{V_{out}}{V_{in}} = \frac{1}{10} = 0.1 = \frac{R_{2}}{R_{1}+R_{2}}
$$
Rearrange this to solve for the required resistance
$$
0.1R_{1} + 0.1R_{2} = R_{2}
$$
$$
R_{1}  = 9R_{2}
$$
This is the required ratio between our two resistors. 

Experimentally measured resistance of the resistors:

| | R1 | R2 |

|------------|------------|------------|

| Resistance | 19.89 +- 0.9% kohm | 2.189 +- 0.9% kohm |

  

Given these resistance values, we can calculate the theoretical voltage attenuation with the measured resistance.

$$

\frac{2.189\text{ k}\Omega}{2.189 \text{ k}\Omega+ 19.89 \text{ k}\Omega} = 0.991 \sim 0.1

$$

Performing Error Propagation on the results:
$$
a = 0.09914398\begin{aligned} \Delta a &= \sqrt{\left( \frac{\partial a}{\partial R} \Delta R \right)^2 + \left( \frac{\partial a}{\partial r} \Delta r \right)^2} \\ &= \sqrt{\left( \left( -(r / (R + r) ^ 2) \right) \cdot \Delta R \right)^2 + \left( \left( R / (R + r) ^ 2 \right) \cdot \Delta r \right)^2} \\ &= 0.0011367874 \\ &= 1.1367874 \times 10^{-3} \\ &= 1 \times 10^{-3} \end{aligned}
$$
$$
a = \left( 9.9 \pm 0.1 \right) \times 10^{-2}
$$
### Results
Above is the Oscilloscope reading for $V_{in}$ and $V_{out}$, with $V_{in}$ on channel 1 and $V_{out}$ on channel 2. You can clearly see the attenuation, however, the scaling on channel 2 was increased relative to channel 1 to retain clarity. Measurements of $V_{out}$ with a steady power supply yielded an experimental $V_{out}$ of 0.951 volts, with a $V_{in}$ of 9.60 volts. 

### Analysis

Looking at these results, we can easily calculate the experimentally measured attenuation. With a $V_{in}$ of 9.60 and a $V_{out}$ of 0.951, gain is calculated by: 
$$
\frac{V_{out}}{V_{in}} = \frac{0.951 \text{ volts}}{0.960 \text{ volts}} = 0.0991 \sim 0.1
$$
As seen here, the experimental value matched the theorized value for our measured resistances to the extent of the accuracy of our measuring equipment. 

### Conclusions:

This experiment verified that the experimentally measured attenuation matched the theoretically calculated attenuation to the highest accuracy we could measure with our lab equipment. We were not able to perfectly match our goal of 10x attenuation due to a lack of properly matched resistors. 

# Section 3
### Objective:
The objective of this portion of the lab is to use an Operational amplifier, or Op-Amp integrated circuit to create an inverting amplifier and  "reverse" the previous attenuation performed with the voltage divider and testing if the theoretically calculated amplification values are in line with the experimentally measured and verified values. 

### Equipment: 
T-I Op-amp chip, breadboard, circuits from Section 1 and 2, oscilloscope, multi-meter, pair of resistors to yield desired gain and 9v power supply. 

### Procedure:
First begin by calculating the appropriate gain while taking care to ensure that the amplifier is not being pushed beyond its limits. Since section 2 yielded an attenuation of $\sim$ 10x, the operational amplifier circuit has to have a less then 10x gain. To achieve this, a pair of resistors has to follow the following relation: 
$$
\frac{V_{out}}{V_{in}} = -\frac{R_{f}}{R_{in}}
$$
Where $R_{f}$ and $R_{in}$ are labeled in the diagram below
![[Pasted image 20240609115252.png]]

After computing the theoretical gain from the resistors, we can proceed to compute the experimental gain. Using the oscilloscope or DMM to measure the gain produced from the inverting Op-Amp circuit. 

### Data
Picture of the Op-Amp circuit (Top IC) and 555 Timer circuit (Bottom IC)

> !picture here!

Our measured resistor values: 

|            | $R_f$                    | $R_{in}$                  |
| ---------- | ------------------------ | ------------------------- |
| Resistance | 830 $\pm$ 0.9% $k\Omega$ | 98.7 $\pm$ 0.9% $k\Omega$ |

Using equation for inverting Op-Amp gain:
$$
\text{Gain } = -\frac{R_{f}}{R_{in}}
$$
We can plug in our measured values to calculate gain and uncertainty in gain

$$
g = 8.4093211753\begin{aligned} \Delta g &= \sqrt{\left( \frac{\partial g}{\partial r_f} \Delta r_f \right)^2 + \left( \frac{\partial g}{\partial r_i} \Delta r_i \right)^2} \\ &= \sqrt{\left( \left( 1 / r_i \right) \cdot \Delta r_f \right)^2 + \left( \left( -(r_f / r_i ^ 2) \right) \cdot \Delta r_i \right)^2} \\ &= 0.1070331845 \\ &= 1.070331845 \times 10^{-1} \\ &= 1 \times 10^{-1} \end{aligned}
$$
Computed Gain:
$$
g = 8.4 \pm 0.1 
$$

Results with constant 9v signal:
$$
\begin{aligned}
&V_{in}  = 9.98 \pm 0.5\% \text{ V} \\ 
&V_{out} \text{ from voltage divider } =0.927 \pm 0.5\% \text{ V} \\
&V_{out} \text{ from Op-Amp} = 7.79 \pm 0.5\% \text{ V} 
\end{aligned}
$$

Calculated gain and uncertainty from experimental voltage measurements

$$
g = 8.4034519957\begin{aligned} \Delta g &= \sqrt{\left( \frac{\partial g}{\partial v_o} \Delta v_o \right)^2 + \left( \frac{\partial g}{\partial v_i} \Delta v_i \right)^2} \\ &= \sqrt{\left( \left( 1 / v_i \right) \cdot \Delta v_o \right)^2 + \left( \left( -(v_o / v_i ^ 2) \right) \cdot \Delta v_i \right)^2} \\ &= 0.0594213789 \\ &= 5.94213789 \times 10^{-2} \\ &= 6 \times 10^{-2} \end{aligned}
$$
Experimental Gain
$$
g =  8.4 \pm 0.06 
$$
### Conclusion: 
The theoretical and experimental gain and uncertainty produced from the inverting Op-Amp correlated very closely, both within the uncertainties of each other. This evidence verifies the operation of the inverting Op-Amp circuit being regulated by the equations stated above. 


### Analytical Design Problem:

> ! Insert picture here

Given this non-inverting amplifier circuit, we need to find how to calculate the gain based on values of $R_{2}$ and $R_{F}$. We can accomplish this using the golden rules: 
1.  The voltage across $R_{2}$ and $R_{f}$ in series is equivalent to $V_{out}$.
2.  Using the voltage divider equation we can find $V_{1}$, the potential between $R_{f}$ and $R_{2}$. In the below equation, $V_{in}$ is $V_{out}$ from the op-amp and $V_{out}$ is $V_{1}$
$$

V_{out} = \frac{R_{2}}{R_f+R_{2}} \cdot V_{in}

$$
3. $V_{in}$ to the op-amp is always kept the same as $V_{1}$ due to golden rule #1. We can rewrite the above formula with these substitutions
$$
V_{in} = \frac{R_{2}}{R_f+R_{2}} \cdot V_{out}
$$
4. Rewrite to solve for $\frac{V_{out}}{V_{in}}$
$$
\frac{R_{f}+R_{2}}{R_{2}} = \frac{V_{out}}{V_{in}} = 1 + \frac{R_{f}}{R_{2}}
$$







# Section 4
### Objective: 
The objective of this section was to combine passive elements such as capacitors and inductors to create a low-pass frequency filter. This will build upon the previous sections, using the amplified signal from section 3 as an input. 
### Equipment:
Previously built circuits, capacitors, resistors, multi-meter, oscilloscope, jumper wires, 9v power supply. 

### Procedure: 

To create and test this low pass filter, we need to combine a resistor and a capacitor in the diagram shown below: 
![[Pasted image 20240610151757.png]]
The problem gives us values to use for the capacitor and resistor, 47 $nF$ and 4.7 $k\Omega$ respectively. We will first calculate the theoretical voltage attenuation at 100Hz and 10kHz. After performing these calculations, we next must experimentally verify them. However, we are not given a 47 $nF$ capacitor, but we have 95 $nF$ capacitors. We can combine 2 95 $nF$ capacitors in series to achieve our desired capacitance.  

Using these components and building the circuit, the next step is to connect the output of section 3 into the $V_{in}$ of the low pass filter. Next, we are to test the circuit with a 100Hz signal and a 10kHz signal. Finally, we will take measurements and compare this to our theoretical findings. 

### Data:

This above photo shows the rising and falling edges of the waveform. You can see how the square wave is separated and the lower frequency components are passed while the higher frequency components are attenuated out. 


The above photo shows both the rising and falling edges, with a few wave cycles. This photo shows, in less detail, the attenuation of the higher frequency components of the square wave. This correlates with the diagrams presented in the lab instructions as well.

### Conclusions:

The low pass filter functioned as expected, resulting in expected attenuation of higher frequency components of the square wave. 


