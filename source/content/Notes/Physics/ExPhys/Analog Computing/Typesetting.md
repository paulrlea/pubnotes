# Analog Computing Lab Report
## Objective:
Solve Differential Equations with analog circuits using Op-Amp based integrators, differentiators, adders and inverters. 

## Equipment 
- Breadboard
- Oscilloscope
- Jumper Cables
- Resistor Assortments
- Capacitor Assortments
- Op-Amps (TLE2071CP)
- Digital Multi-meter
- 9v Battery and Harness
- USB Flash Drive
- 2 Function Generators

## Section 1
### Objective
- Familiarize ourselves with components of the analog computer, including inverters, integrators, differentiators and adders. 
### Equipment: 
- Same as above 

### Section 1.1: Inverting Amplifier
#### Objective: 
The objective of this portion of the lab is to use an Operational amplifier, or Op-Amp integrated circuit to create an inverting amplifier and test if the theoretically calculated amplification values are in line with the experimentally measured and verified values. 

#### Equipment: 
- 4x Resistors
- 1x Op-Amp
- Breadboard
- 9v battery and power harness 
- Oscilliscope
- Digital Multimeter
- Jumpers


#### Procedure:
Begin by selecting 4 appropriate resistors. To experience the effects of the op-amp without overloading the power supply we will need to use a voltage divider that has approximately the inverse of the gain of the inverting Op-Amp. The calculated resistor values will be below in the data subsection, as well as the experimentally measured values. After acquiring these resistors, firstly construct a voltage divider, as shown in figure 1 below. 
![[Pasted image 20240613190017.png]]
>Figure 1

After constructing the voltage divider, we can construct the inverting op-amp as per figure 2 below, and connect the $V_{out}$ from the voltage divider to the $V_{in}$ point on the inverting Op-Amp. 

![[Pasted image 20240613185548.png]]
> Figure 2 

After building the circuit testing the circuit can be done with both a static DC voltage applied through the voltage divider as well as a waveform applied with a function generator. Ideally, 4 tests would be performed with different resistor values, but in our case we were unable to perform these many tests. After these two tests are run and voltage measurements before and after both the voltage divider and op-amp circuit are gathered, we now are able to determine the experimental gain and compare to the theoretical gain. 
#### Data
Resistance values for Voltage divider

|            | Resistance (kilo-ohms) |
| ---------- | ---------------------- |
| $R_1$      | 10 $\pm 0.9 \%$        |
| $R_2$      | 1.196 $\pm 0.9 \%$     |
| $R_2$ Real | 0.6012 $\pm 0.9 \%$    |
Resistance Values for Inverting op-amp

|          | Resistance (kilo-ohms) |
|----------|------------------------|
| $R_{in}$ | 1.209 $\pm 0.9 \%$     |
| $R_{f}$  | 4.72 $\pm 0.9 \%$      |
Potential in volts for input and output from circuit

|       | Potential (Volts)   |
| ----- | ------------------- |
| V_in  | 9.45 $\pm 0.5 \%$   |
| V_out | -2.094 $\pm 0.5 \%$ |
#### Analysis 
Voltage Divider Calculations: 
$$
V_{out} = \frac{R_{2}}{R_{1}+R_{2}} 
$$
We have a virtual ground point on the op-amp, so we need to consider $R_{2}$ to be in parallel with $R_{in}$ on the op-amp circuit when calculating the voltage divider drop. 

Voltage divider attenuation calculations: 
$$
A = 0.056657117\begin{aligned} \Delta A &= \sqrt{\left( \frac{\partial A}{\partial R_1} \Delta R_1 \right)^2 + \left( \frac{\partial A}{\partial R_2} \Delta R_2 \right)^2} \\ &= \sqrt{\left( \left( -(R_2 / (R_1 + R_2) ^ 2) \right) \cdot \Delta R_1 \right)^2 + \left( \left( R_1 / (R_1 + R_2) ^ 2 \right) \cdot \Delta R_2 \right)^2} \\ &= 0.0006802704 \\ &= 6.802704 \times 10^{-4} \\ &= 7 \times 10^{-4} \end{aligned}
$$
$$
A = \left( 5.67 \pm 0.07 \right) \times 10^{-2}
$$
Where A is attenuation of the voltage divider. 
Op-Amp Gain Calculations: 
$$
\text{Op-Amp gain} = - \frac{R_{f}}{R_{in}} 
$$Op-Amp Resistor Values
Gain Calculation
$$
g = -3.9040529363\begin{aligned} \Delta g &= \sqrt{\left( \frac{\partial g}{\partial R_in} \Delta R_in \right)^2 + \left( \frac{\partial g}{\partial R_f} \Delta R_f \right)^2} \\ &= \sqrt{\left( \left( R_f / R_in ^ 2 \right) \cdot \Delta R_in \right)^2 + \left( \left( -(1 / R_in) \right) \cdot \Delta R_f \right)^2} \\ &= 0.0496904815 \\ &= 4.96904815 \times 10^{-2} \\ &= 5 \times 10^{-2} \end{aligned}
$$
$$
g = \left( -3.9 \pm 0.05 \right) \times 10^{0}
$$
Combining the attenuation and gain we should have a combined gain of: 
$$
t = -0.22113\begin{aligned} \Delta t &= \sqrt{\left( \frac{\partial t}{\partial g} \Delta g \right)^2 + \left( \frac{\partial t}{\partial a} \Delta a \right)^2} \\ &= \sqrt{\left( \left( a \right) \cdot \Delta g \right)^2 + \left( \left( g \right) \cdot \Delta a \right)^2} \\ &= 0.0039357496 \\ &= 3.9357496 \times 10^{-3} \\ &= 4 \times 10^{-3} \end{aligned}
$$
$$
t = \left( -2.21 \pm 0.04 \right) \times 10^{-1}
$$
Total gain is  $-0.221 \pm 0.004$
Experimentally measured gain:
$$
g_e = -0.2215873016 [\begin{aligned} \Delta g_e &= \sqrt{\left( \frac{\partial g_e}{\partial V_in} \Delta V_in \right)^2 + \left( \frac{\partial g_e}{\partial V_out} \Delta V_out \right)^2} \\ &= \sqrt{\left( \left( -(V_out / V_in ^ 2) \right) \cdot \Delta V_in \right)^2 + \left( \left( 1 / V_in \right) \cdot \Delta V_out \right)^2} \\ &= 0.0015668588 \\ &= 1.5668588 \times 10^{-3} \\ &= 2 \times 10^{-3} \end{aligned}
$$
$$
g_e = \left( -2.22 \pm 0.02 \right) \times 10^{-1}
$$
The experimentally measured total gain is $-0.222 \pm 0.002$

The experimentally measured gain and theoretically calculated gain are within 0.001, less then the uncertainty of our measuring equipment. This is evidence that confirms that our circuit performs as expected. 

### Section 1.2: Integrating Amplifier
#### Objective: 
The objective of this portion of the lab is to use an Operational amplifier, or Op-Amp integrated circuit to create an integrating amplifier and test if the theorized values and waveforms are in line with the experimentally measured and verified values and waveforms. 

#### Equipment: 
- 1x Resistor
- 1x Capacitor 
- 1x Op-Amp
- Breadboard
- 9v battery and power harness 
- Oscilloscope
- Digital Multimeter
- Jumpers
#### Procedure: 
As before, we first select appropriate values for the capacitor and multimeter. The lab reference material suggests nominal values of 10 $k\Omega$ for the resistor and 0.01 $\mu f$ for the capacitor, which is what we used. The actual values and error propagation calculations are below in the data section. 

After selecting appropriate components, it is now appropriate to construct the circuit on the breadboard according to figure 3 below. 
![[Pasted image 20240613191446.png]]

> Figure 3

After the circuit is constructed, we can use the function generator to test the integrating capacities using 2 different waveforms:
- Square wave $\pm$ 1V at 1kHz
- Triangular wave $\pm$ 1V at 1kHz
Record data on oscilloscope, using channel one to record raw input from the function generator, and channel 2 to record the waveforms after they've been integrated. Compare this to the theoretically derived values and explain any discrepancies in the results. 

To find the theoretically derived values for $V_{out}$ we can use the following formula: 

$$
V_{out} = V_{0}(0) - \frac{1}{RC} \int V_{in} dt
$$

Where $V_{0}(0)$ is an initial condition, which we can ignore because our circuit continuously integrates. 

#### Data:

![[Pasted image 20240617164246.png]]
Figure Showing the integration of a square wave.


#### Analysis 

The continuous integration of the waveforms is in line with the theoretical model of $V_{out} = V_{0}(0) - \frac{1}{RC} \int V_{in} dt$, with some slight variation at the extrema, likely due to the Op-Amp receiving interference or reaching its maximum output. 

### Section 1.3 Differentiating Op-Amp
#### Objective: 
The objective of this portion of the lab is to convert our integrating op-amp circuit into a differentiating op-amp circuit. 

#### Equipment: 
- 1x Resistor
- 1x Capacitor 
- 1x Op-Amp
- Breadboard
- 9v battery and power harness 
- Oscilloscope
- Digital Multimeter
- Jumpers
- differentiating circuit 
#### Procedure: 
We will continue to use the same resistors and capacitors from the integrating amplifier for ease of construction, to change the integrating circuit to a differentiating circuit it is a simple matter of swapping the location of the capacitor and resistor. The diagram for this can be seen below in figure 4
![[Pasted image 20240614191551.png]]
> Figure 4

After this circuit is complete, we will proceed to due the same tests performed upon the integrating amplifier to see if the differentiating amplifier circuit matches its theoretically derived values. 
To find the theoretically derived values for this portion of the lab we use the following equation: 
$$
V_{out}(t) = V_{0}(0) - RC \frac{dV_{in}}{dt} 
$$
Where, as before, $V_{0}(0)$ is the initial condition term that we can safely ignore for our continuously differentiating case. 
After computing the theoretical values, we can test the circuit for the three cases as in the integrator section, a square and triangle wave. 

#### Data: 
>data

#### Analysis: 

The differentiation of the waveforms follows the given theoretical model, $V_{out}(t) = V_{0}(0) - RC \frac{dV_{in}}{dt}$.  We can also logically think about the derivative of a function like a square wave, and what pattern it would follow, and the circuit produces an inverted derivative. While the derivative of a square wave at the leading and falling edges should be $\pm \infty$, that is obviously not physically possible, and this is represented by the op-amp maxing out its voltage supply at the leading and falling edges.

### Section 1.4 Summing Amplifier 
#### Objective: 
The objective of this portion of the lab is to convert our inverting op-amp circuit into a summing op-amp circuit. 

#### Equipment: 
- 1x Resistor
- 1x Capacitor 
- 1x Op-Amp
- Breadboard
- 9v battery and power harness 
- Oscilloscope
- Digital Multimeter
- Jumpers
- inverting circuit
#### Procedure: 
We can convert the inverting circuit into a summing circuit by adding a secondary resistor to the input leg of the op-amp. Choose appropriate resistors, between 1-5k$\Omega$, to find appropriate values of amplification. Keep in mind that any difference in resistors will result in a different weighting for each added component. Follow figure 5 below for more detailed instructions. 
![[Pasted image 20240614192506.png]]
> Figure 5

After constructing the adder, we need to test it. We can test this circuit using 2 waveforms, finally utilizing both function generators. The first function generator will be set to a square wave of about 500 Hz, and the second will be a higher frequency sine wave, at about 10 kHz. We can observe the qualitative effects of this on the oscilloscope to confirm our adder is working correctly. 

# Section 2: Solving the simple harmonic oscillator

## Objective: 
Use the components constructed in section 1 to solve the simple harmonic oscillator's differential equation continuously. 

## Equipment:
- Breadboard
- Oscilloscope
- Jumper Cables
- Resistor Assortments
- Capacitor Assortments
- Op-Amps (TLE2071CP)
- Digital Multi-meter
- 9v Battery and Harness
- USB Flash Drive
- Function Generator


## Procedure: 
The first step to building the analog computer and solving these differential equations is to design the aforementioned analog computer. This can be done by analytically thinking about the task at hand, and breaking it down into components that can be built. The task at hand can be accomplished with 2 integrating circuits and an adder. It can be helpful to think of individual signals between components as parts of the differential equation, $x$, $\dot{x}$ and $\ddot{x}$. The design that we settled on is pictured below (figure 6) as a block form, and in figure 7 as a circuit form. 

![[Pasted image 20240614193448.png]]
> Figure 6

![[Pasted image 20240614193502.png]]
> Figure 7

Before we construct this circuit we have to consider what values of resistance and capacitance we should use to ensure the broadest possible range of integration. The literature for this lab suggests values of 0.01 $\mu$f and 1 k$\Omega$, which is what we used. It is also worth noting that due to the inverting nature of the op-amps, we will get an inverted answer. This will be proven in the data and analysis section. 

After constructing this circuit, we have to provide a driving force. Connecting a function generator to the input leg of the analog adder will yield the required forcing and allow us to observe the harmonic oscillations. 

Finally it is time to gather data, beginning by providing a low-frequency square pulse, we can use the oscilloscope to view and capture the resulting oscillatory action. It is also suggested to change values of the resistance on the adder such that continual, non-dampened oscillations can be observed. We made sure to capture data on oscillation amplitude and frequency using the cursor function on the oscilloscope. 

## Data

|     | Components                   |
| --- | ---------------------------- |
| R_1 | 0.994 $k \Omega \pm 0.9 \%$  |
| R_2 | 0.995 $k \Omega \pm 0.9 \%$  |
| R_3 | 0.986 $k \Omega \pm 0.9  \%$ |
| R_4 | 0.987 $k \Omega \pm 0.9 \%$  |
| R_5 | 0.986 $k \Omega \pm 0.9 \%$  |


|     | Capacitors         |
| --- | ------------------ |
| C_1 | 10 nF $\pm 1.9 \%$ |
| C_2 | 11 nF $\pm 1.9 \%$ |

## Analysis


Following the method described in the appendix of the Analog Computer Theory, we have the following relations:

$$
V_{out} = -\frac{1}{RC} \int V_{in} dt
$$
and in the context of the analog computer 
$$
\dot{x} = \alpha \int \ddot{x} dt
$$
and
$$
x = \beta \int \dot{x} dt
$$
Therefore 
$$
x = \beta \int\alpha \int \ddot{x} dt \ dt
$$
We can factor out beta and alpha 
$$
x = \beta \alpha \iint \ddot{x}  \ dt
$$
And we know that $\beta\alpha$ is equal to the following: 
$$
-\frac{1}{R_{1}C_{1}} \left(- \frac{1}{R_{2}C_{2}} \right)
$$
Or using our experimentally measured values: 
$$
\alpha\beta = 9341427493.4278\begin{aligned} \Delta ab &= \sqrt{\left( \frac{\partial ab}{\partial R} \Delta R \right)^2 + \left( \frac{\partial ab}{\partial C} \Delta C \right)^2 + \left( \frac{\partial ab}{\partial R_1} \Delta R_1 \right)^2 + \left( \frac{\partial ab}{\partial C_1} \Delta C_1 \right)^2} \\ &= \sqrt{\left( \left( -(C_1 / (R * C * R_1 * C_1) ^ 2 * R_1 * C) \right) \cdot \Delta R \right)^2 + \left( \left( -(C_1 / (R * C * R_1 * C_1) ^ 2 * R_1 * R) \right) \cdot \Delta C \right)^2 + \left( \left( -(C_1 / (R * C * R_1 * C_1) ^ 2 * R * C) \right) \cdot \Delta R_1 \right)^2 + \left( \left( -(R / (R * C * R_1 * C_1) ^ 2 * C * R_1) \right) \cdot \Delta C_1 \right)^2} \\ &= 277740606.63077885 \\ &= 2.7774060663 \times 10^{8} \\ &= 3 \times 10^{8} \end{aligned}
$$
$$
ab = \left( 9.3 \pm 0.3 \right) \times 10^{9}
$$

To find the final proportionality constant, the gain of the summing circuit also has to be accounted for. We can use the following to find this gain: 
$$
-\frac{R_{f}}{R_{in}}
$$
And for our summing amplifier

$$
R = -4.5146520147\begin{aligned} \Delta R &= \sqrt{\left( \frac{\partial R}{\partial R_f} \Delta R_f \right)^2 + \left( \frac{\partial R}{\partial R_i} \Delta R_i \right)^2} \\ &= \sqrt{\left( \left( -(1 / R_i) \right) \cdot \Delta R_f \right)^2 + \left( \left( R_f / R_i ^ 2 \right) \cdot \Delta R_i \right)^2} \\ &= 0.057462139 \\ &= 5.7462139 \times 10^{-2} \\ &= 6 \times 10^{-2} \end{aligned}
$$
$$
R = \left( -4.51 \pm 0.06 \right)
$$
Finally, we get our total proportionality constant: 
$$
\alpha\beta \cdot R = 
$$
$$
p = -41943000000\begin{aligned} \Delta p &= \sqrt{\left( \frac{\partial p}{\partial R} \Delta R \right)^2 + \left( \frac{\partial p}{\partial ab} \Delta ab \right)^2} \\ &= \sqrt{\left( \left( ab \right) \cdot \Delta R \right)^2 + \left( \left( R \right) \cdot \Delta ab \right)^2} \\ &= 1463548085.9882944 \\ &= 1.463548086 \times 10^{9} \\ &= 1 \times 10^{9} \end{aligned}
$$
$$
p = \left( -4.2 \pm 0.1 \right) \times 10^{10}
$$

Applied to the harmonic oscillator differential equation
$$
\ddot{x} = -\frac{k}{m} x 
$$
$$
-\frac{k}{m} = \left( -4.2 \pm 0.1 \right) \times 10^{10}
$$
and therefore the frequency is related in the following manner:
$$
\omega = \sqrt{ \frac{k}{m} } = 204939.015319 \pm31622.7766017
$$
And with this, we can see the frequency obtained in the sinusoidal regression in the python script is within the propagated uncertainty values.




# Section 3: Damping the harmonic oscillator 

## Objective: 
Using the circuit from section 2 our goal is to introduce a damping term $\frac{\gamma}{m}$ using an inverting op-amp circuit tied into our existing circuit. 

## Equipment:

Everything from section 2, plus another op-amp chip, resistors and necessary jumper cables. 

## Procedure: 

Begin by designing the appropriate modifications to include the damping term by connecting in to the "$\dot{x}$" signal in the analog computer and adding it to the $\ddot{x}$ term using the existing  adder circuit. Using two more resistors, we can adjust the value of damping to something that will be easy to visualize on the oscilloscope. 

After making the appropriate modifications to the circuit, we can proceed to collect our data. It is important to first take a screenshot of the oscilloscope with the damper portion deactivated to account for any changes in the natural damping of the circuit. Compare this reading to the reading obtained after the damper is connected. Use the theoretical values of damping and compare to the experimental values. 

## Analysis

We want to find the theoretical damping coefficient $\gamma$. This is going to be equivalent to the coefficient of the inverting amplifier combined with the gain applied to it from the summing amplifier multiplied by alpha from the previous section. 
$$
\alpha = \frac{1}{R_{3}C_{1}} , \text{ Inverter gain =} -\frac{R_{8}}{R_{9}}, \text{ Summer gain } = -\frac{R_{5}}{R_{7}}
$$
$$
\frac{\gamma}{m} = -\frac{R_{8}R_{5}}{R_{3}C_{1}R_{7}R_{9}}
$$
$$
\gamma/2m = -28262.2831133571\begin{aligned} \Delta \gamma/2m &= \sqrt{\left( \frac{\partial \gamma/2m}{\partial R_9} \Delta R_9 \right)^2 + \left( \frac{\partial \gamma/2m}{\partial R_8} \Delta R_8 \right)^2 + \left( \frac{\partial \gamma/2m}{\partial R_7} \Delta R_7 \right)^2 + \left( \frac{\partial \gamma/2m}{\partial C_1} \Delta C_1 \right)^2 + \left( \frac{\partial \gamma/2m}{\partial R_5} \Delta R_5 \right)^2 + \left( \frac{\partial \gamma/2m}{\partial R_3} \Delta R_3 \right)^2} \\ &= \sqrt{\left( \left( R_8 / (R_3 * C_1 * R_7 * R_9) ^ 2 / 2 * R_5 * R_3 * C_1 * R_7 \right) \cdot \Delta R_9 \right)^2 + \left( \left( R_5 * -1 / 2 / (R_3 * C_1 * R_7 * R_9) ^ 2 * R_3 * C_1 * R_7 * R_9 \right) \cdot \Delta R_8 \right)^2 + \left( \left( R_8 / (R_3 * C_1 * R_7 * R_9) ^ 2 / 2 * R_5 * R_9 * R_3 * C_1 \right) \cdot \Delta R_7 \right)^2 + \left( \left( R_8 / (R_3 * C_1 * R_7 * R_9) ^ 2 / 2 * R_5 * R_9 * R_7 * R_3 \right) \cdot \Delta C_1 \right)^2 + \left( \left( R_8 * -1 / 2 / (R_3 * C_1 * R_7 * R_9) ^ 2 * R_3 * C_1 * R_7 * R_9 \right) \cdot \Delta R_5 \right)^2 + \left( \left( R_8 / (R_3 * C_1 * R_7 * R_9) ^ 2 / 2 * R_5 * R_9 * R_7 * C_1 \right) \cdot \Delta R_3 \right)^2} \\ &= 782.20687253 \\ &= 7.8220687253 \times 10^{2} \\ &= 8 \times 10^{2} \end{aligned}
$$
$$
\gamma/2m = \left( -2.83 \pm 0.08 \right) \times 10^{4}
$$
Divided by two to yield the $\frac{\gamma}{2m}$ term we need


This yields our theoretical damping constant introduced from the addition of the inverting amplifier. 

The general form for the oscillator with damping: 
$$
x(t) = A \cdot e ^{-\gamma t/2m} \cos(\omega t - \phi)
$$
Using exponentially decaying sinusoidal regression, we were able to find the parameters that matched the naturally damped case above. 

Fitted parameters: A=2.004, lambda=1090.942, omega=100664.100, phi=2.210

Plugging these in:
$$
x(t) = 2.004 \cdot e^{1090.942t} \cos(100664.1 t - 2.210)
$$
Now, with the damping circuit constant of $\left( -2.83 \pm 0.08 \right) \times 10^{4}$ we can compare and see if this yields the expected result. 

$$
x'(t) = 2.004 \cdot e^{1090.942 + \left( -2.83 \pm 0.08 \right) \times 10^{4}t} \cos(100664.1 t - 2.210)
$$





# Section 4: Nonhomogenous boundary beats

## Objective: 
Using two function generators we want to observe beating behavior occurring at the natural oscillation frequency of the analog computer. 

## Equipment:
Everything from section 2 plus a second function generator

## Procedure : 
Begin by adding a second input to the adder circuit with the same resistor value as the existing adder leg. Connect the second function generator to this new input and set it to a sine wave of approximately the natural harmonic frequency. Adjust the frequency until clear beating motion can be observed, and capture data. 

## Data:

> Data

## Analysis: 

The general solution to a beat problem is given by the following: 
$$
V_{o}(t) = \frac{A}{\omega_{0}^{2} -\omega^{2}} \cos\omega t + B\sin\omega t
$$
The beat frequency should be the difference between the natural frequency of the harmonic oscillator and the frequency of the second function generator. 

Calculating the theoretical beat frequency: 
Natural Harmonic Frequency $\approx$ 15.6 kHz as measured on oscilloscope
Function Generator is set to 17.83 kHz
$$
17.83-15.3 =2.53 \text{kHz}
$$
This isn't exactly the expected value, but given the uncertainty in measuring beat frequency due to the unclear edges in our oscilloscope reading, it is a reasonably close value. 




