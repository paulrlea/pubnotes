## Section 3.1
This section measured the response characteristics of the band-pass filter, calibrating it such that the gain integral would be usable in the upcoming Johnson Noise measurements. 
### Procedure
- We began by selecting several frequencies to test, in the range from 1-100 kHz.
- For each one of these frequency values, we measured the input and output voltage using the oscilloscope.
- After obtaining these voltage measurements, we were able to calculate the system gain and therefore obtained the correct calibration metrics for the Johnson noise 

### Data: 

> data

### Analysis: 
### Theoretical Gain Calculations: 
#### High Pass Filter: 
A high pass filter is designed to let higher frequencies pass through without being attenuated, while attenuating lower frequencies. The formula for the cutoff frequency on  a high pass filter is as follows: 
$$
f_{c} = \frac{1}{2\pi \tau} = \frac{1}{2\pi rc}
$$
We wanted a high-pass cutoff of around 5 kHz, so setting $f_{c}$ to 5  kHz we can solve for required values of $r$ while using a $0.1\mu F$ capacitor
$$
5000 (2\pi) (0.1 \times 10^{-6}) = \frac{1}{R}
$$
$$
R_\text{theoretical} = 318.31 \  \Omega
$$
#### Low  Pass Filter 
A low pass filter is the opposite of a high pass filter, where it allows the lower frequencies to pass through while attenuating higher frequencies out. The cutoff frequency is given by the same equation:
$$
f_{c} = \frac{1}{2\pi \tau} = \frac{1}{2\pi rc}
$$
We wanted a low-pass cutoff of around 20 kHz, and we used the same $0.1\mu F$ capacitor. Solving for required resistance: 
$$
20000(2\pi)(0.1\times  10^{-6}) = \frac{1}{R} 
$$
$$
R_\text{theoretical} = 79.5 \ \Omega
$$

Actual Resistances and capacitance's

| Actual Values    | R                      | C                       |
| ---------------- | ---------------------- | ----------------------- |
| Low Pass Filter  | $50.9 \pm 0.5 \Omega$  | $0.099 \pm 0.002 \mu F$ |
| High Pass Filter | $327.1 \pm 30.0\Omega$ | $0.103 \pm 0.002 \mu F$ |

Theoretical Cutoff Values using measured components: 
Low pass: 
$$
f_c = 31584.0017248904\begin{aligned} \Delta f_c &= \sqrt{\left( \frac{\partial f_c}{\partial R} \Delta R \right)^2 + \left( \frac{\partial f_c}{\partial C} \Delta C \right)^2} \\ &= \sqrt{\left( \left( -(C * 2 / (2 * pi * R * C) ^ 2 * pi) \right) \cdot \Delta R \right)^2 + \left( \left( -(pi * 2 / (2 * pi * R * C) ^ 2 * R) \right) \cdot \Delta C \right)^2} \\ &= 709.4926405004 \\ &= 7.094926405 \times 10^{2} \\ &= 7 \times 10^{2} \end{aligned}
$$
$$
f_c = \left( 3.16 \pm 0.07 \right) \times 10^{4}
$$
High pass: 
$$
f_c = 4723.9181358955\begin{aligned} \Delta f_c &= \sqrt{\left( \frac{\partial f_c}{\partial R} \Delta R \right)^2 + \left( \frac{\partial f_c}{\partial C} \Delta C \right)^2} \\ &= \sqrt{\left( \left( -(C * 2 / (2 * pi * R * C) ^ 2 * pi) \right) \cdot \Delta R \right)^2 + \left( \left( -(pi * 2 / (2 * pi * R * C) ^ 2 * R) \right) \cdot \Delta C \right)^2} \\ &= 442.8580100016 \\ &= 4.4285801 \times 10^{2} \\ &= 4 \times 10^{2} \end{aligned}
$$
$$
f_c = \left( 4.7 \pm 0.4 \right) \times 10^{3}
$$
Theoretical Gain Curve:

$$
g \equiv \frac{V_{out}}{V_{in}} = \frac{1}{\sqrt{ 1 + (\omega R_{1}C)^{2} }} \frac{\omega R_{2}C}{\sqrt{ 1+(\omega R_{2}C)^{2} }} 
$$









Experimental Data: 

| Pk-Pk Voltage      | 1kHz    | 3kHz    | 5kHz    | 25kHz    | 50kHz   | 100kHz  |
| ------------------ | ------- | ------- | ------- | -------- | ------- | ------- |
| Channel 1 (output) | $460mV$ | $940mV$ | $1.12V$ | $512 mV$ | $144mV$ | $44mV$  |
| Channel 2 (inpiut) | $10.0V$ | $10.2V$ | $10.2V$ | $10.0V$  | $10.0V$ | $10.0V$ |

Calculated Gain: 

|                 | 1kHz  | 3kHz  | 5kHz  | 25kHz | 50kHz | 100kHz |
| --------------- | ----- | ----- | ----- | ----- | ----- | ------ |
| Calculated gain | 0.046 | 0.092 | 0.110 | 0.051 | 0.014 | 0.004  |

### Conclusion: 
In this section we successfully fit a pair of mathematical models to model the frequency response of our band-pass filter/amplifier circuit. These models qualitatively fit the data well, however, the chi squared parameter tells us that the data model is highly over-constrained. This logically makes sense, we have limited data points and several parameters to fit to. Despite this, we are able to use these models to evaluate the integral that we need for section 3.2.
## Section 3.2
After we calibrated the experimental setup's band pass filter and obtained the total op-amp gain, we were ready to take measurements of the generated Johnson noise using a variety of resistors. 
### Procedure
- We began this portion of the lab by removing the function generator and voltage divider circuit from the experimental setup. 
- After these components were removed, a selection of resistors from between 10 $\Omega$ and 10 $k\Omega$ were selected to serve as the generators of the Johnson noise. 
- At this point the room's air temperature was recorded for usage during the analysis. 
- Finally, we recorded the oscilloscope output of the Johnson noise for 6 different resistance values. 
### Data
Room temperature: 26 degrees Celsius
![[Pasted image 20240716095122.png]]

Resistance for each trial:

| Trial | R                      |
| ----- | ---------------------- |
| 1     | $326.1 \pm 3 \ \Omega$ |
| 2     | $50.8 \pm 0.5\ \Omega$ |
| 3     | $815 \pm 7\ \Omega$    |
| 4     | $1200 \pm  10\ \Omega$ |
| 5     | $3851 \pm 40 \ \Omega$ |
| 6     | $9950 \pm 90 \ \Omega$ |

### Analysis: 

We evaluate this integral to find the expectation value of $\left< V^{2} \right>$
$$
\left< V^{2} \right> = 4kTR \int_{0}^{\infty} g^{2}(v)  \, dx 
$$
For each value of R we will evaluate this. Then we will fit a curve fit to this function to solve for Boltzmann's constant. 

### Conclusion: 
This section yielded mixed results, our data acquisition had large discrepancies from the model. This is evidenced by the large chi-squared model in figure 6 of 255.9. This signals a very poor correlation to the model. This initial analysis additionally yielded a calculated Boltzmann constant that was incoherent with the literature values of the Boltzmann constant by a factor of approximately 10,000. Possible reasons for these large discrepancies may include temperature fluctuations or errant spikes in background radiation interfering with readings on the oscilloscope. The data's fit was improved by removing the 4th data point, which yielded a Chi-squared value of 16.8, an approximate tenfold decrease over the previous fit. This signaled a much better fit, and the value of the calculated Boltzmann constant was also correspondingly closer to the literature values, but still 3 orders of magnitude away from the correct value. This experiment could be improved by adding more robust temperature monitoring capabilities, as well as EM radiation shielding around the experimental setup in the form of a Faraday cage. 
## Section 3.3: Johnson Noise- Teachspin Approach

### Procedure
- The experiment was set up by following the parameters outlined in the "Teachspin Approach" document. The band pass filter components, gain, multiplier and output were all set to specific values. 
- After we had set up the experiment with the appropriate settings, we  collected data for different resistance values using a high-precision digital multimeter. 
- These data values along with the corresponding resistances were recorded into a table for further analysis. 
### Data
Pre-amp gain: 600x
Amp Gain: 400x

| Resistance | Voltage  |
|------------|----------|
| 1 Ohm      | 38.90mV  |
| 10 Ohms    | 39.03mV  |
| 100 Ohms   | 40.05mV  |
| 1k Ohms    | 49.94mV  |
| 10k Ohms   | 149.01mV |
| 100k Ohms  | 861.1 mV |
### Analysis

Measured Voltage follows this formula: 
$$
V_{out}(t) = G[V_{j}(t) +V_{N}(t)]
$$
Where $V_{j}$ is the Johnson noise and $V_{N}$ represents the intrinsic noise of the system. 

Taking the RMS of this system: 
$$
\left< V_{out}^{2}(t) \right> = G^{2} \{ \left< V_{j}^{2}(t) \right> + \left<  V_{N}^{2}(t)\right>  \}
$$



### Conclusions: 
This section yielded much better values then the previous section. The data fit the linear model much more accurately, leading to the literature-accurate value within the calculated error for the Boltzmann constant. The last data point at 100 $k\Omega$ had a large error due to the multimeter auto-ranging to the volt range as opposed to the milli-volt range before, but the model fits all of the other points very well, with a overall chi-squared value of 0.79, signifying a well-constrained, accurate fit. 
