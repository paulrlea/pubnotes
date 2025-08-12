# Problem 1: General Physics

a). There exists a variety of applications in which organic semiconductors offer significant overall advantage compared to traditional silicon semiconductors. One specific application of OLED displays, a subset of organic semiconductors, is in flexible display technology. This technology is commonly used in wearable technology. Its light weight, flexibility, and relative ease of manufacturing make it far more appealing then silicon based alternatives. 

b). Increasing the conjugation length will decrease the band gap. This occurs because the highest occupied molecular orbital, or HOMO, increases in energy and the LUMO, or Lowest unoccupied molecular orbital, decreases in energy. This therefore decreases the "distance" between states and reduces the materials band gap. 

c). The presence of polarons leads to the formation of new absorption bands, which can modify a materials optical properties in a region of the light spectrum. These effects can affect the optoelectronic performance of OSC materials, for example in solar panels. 

# Problem 2: OLEDs

a). Luminance is a primary measure of OLED performance and efficiency. Luminance refers to the amount of light produced per unit volume, typically measured in "nits", which is equivalent to candelas per square meter. The higher the Luminance, the more light the OLED surface is able to output. This is especially important in display technologies, where high dynamic range displays require high luminance to provide deep contrasts between colors.

b). The electroluminescence quantum efficiency is given by the following relationship:
$$
\eta_{EL} = \eta_{PL} \cdot r_{st} \cdot \gamma_{cap}
$$
If we assume that the ratio of singlet and triplet excitons is 1:1, the ratio of singlet excitons to total excitons is 0.5. Additionally assuming that the exciton formation factor is ideal at 100%, then we can write the ratio of ELQE to PLQE as follows:
$$
\frac{\eta_{EL}}{\eta_{PL}} = r_{st} \cdot \gamma_{cap} \implies 0.5 \cdot 1 = 0.5
$$
Therefore the ideal maximum ratio between ELQE and PLQE is 0.5, in the given situation. 

c). Aggregation quenching is the reduction in photoluminescence efficiency caused by the formation of stacked $\pi$ bonds between molecules, also known as dimers, in a material. It can also be caused by  This prevents radiative decay and reduces overall efficiency. 


d). In a head-tail structured organic semiconductor with minimized steric hindrance long alkyl chains reduce charge mobility, increase photo-luminescence and cause a blue shift in the emission spectrum due to decrease $\pi-\pi$ stacking and suppressed aggregation effects.

# Problem 3: OPV's 
a). The AM1.5 condition is a standardized testing condition for photovoltaic devices to be tested. It takes into consideration atmospheric absorption from specific elements, as well as atmospheric attenuation equivalent to 1.5x the thickness of the atmosphere normal to the earths surface. This is equivalent to a solar angle of 48 degrees.

b). The maximal efficiency of a single junction solar cell is 33.7% at an band gap of 1.34 eV. This limitation is caused by several factors, including spectral losses, non-radiative recombination, and black body radiation. Spectral loss refers to the phenomena in which photons less then band-gap energy are unable to create an exciton in the target material, and any photon with energy greater then the band-gap loses the excess energy. Non-radiative recombination occurs when charge carriers recombine and emit heat instead of contributing to power production. Black body radiation losses occur because working solar cells are hotter then the surroundings, and therefore emit heat, which is a loss of energy. 

c).  
Equation for External Quantum Efficiency: 
$$
EQE = \frac{I_{sc} (\lambda)hc}{P_{in}(\lambda )e\lambda}
$$
Given Values Converted to SI units:
$EQE: 60\%$
$E_\text{photon}: 2eV =3.20436 \times 10^{-19} J$
$P_{in} =100mW/cm^{2} =1000W/m^{2}$

We can use this to calculate the photon flux $\Phi _\text{photon}$:
$$
\frac{1000 J}{s\cdot m^{2}} \cdot \frac{1 \text{ photon}}{3.204 \times 10^{-19} J} = \frac{3.1207\times 10^{21}\text{ Photons}}{s \cdot m^{2}}
$$
Given an EQE of 60%, 60% of incident photons are converted into electron-hole pairs. We can then find the number of electron-hole pairs generated:
$$
\frac{3.1207\times 10^{21}\text{ Photons}}{s \cdot m^{2}} \cdot 0.60 = \frac{1.8724\times 10^{21} \text{ E-H pairs}}{s\cdot m^{2}}
$$
Therefore, $1.8724 \times 10^{21}$ electron-hole pairs are generated per $m^{2}$ per second. 

d). a). 
Given values: 
$I_\text{sc} = 3mA$
$FF = 0.5$
$V_{oc} = 1.2V$
$P_{in} = 30mW$

We can calculate $P_\text{m}$ through the following relation: 
$$
FF = \frac{P_\text{m}}{J_{sc}V_{oc}}
$$
$$
0.5 = \frac{P_\text{m}}{0.003A \cdot 1.2V}
$$
Maximum power is 
$$
P_\text{m} = 0.5 \cdot 0.003A \cdot 1.2V = 0.0018 \ W = 1.8\ mW 
$$
Taking this and using the PCE (Power Conversion Efficiency) Relation we can derive the efficiency of the cell. 
$$
PCE = \frac{P_{m}}{P_{in}} = \frac{1.8 \ mW}{30 \ mW} \approx 0.06
$$
This is a PCE of 6%

b). The state of the art solar cells have reached efficiencies of up to 18.2%, therefore an efficiency of 6% is very feasible. 

# Problem 4: OFET's

a) The given equation describes the energy transfer rate in a material as a function of the Förster radius, the donor-acceptor separation distance, and the donor's fluorescence lifetime. 

b)
The condition:
$$
k _{ET} = \frac{1}{2} k_{\exp}
$$
Plugging into original equation:
$$
\frac{1}{2} k_{\exp} = \tau_{0}^{-1} \times \left( \frac{R_{f}}{R} \right)^{6}
$$
Rearrange: 
$$
\left( \frac{R_{F}}{R} \right) ^{6} = \frac{1}{2 }\times k_{\exp} \tau_{0}
$$
Take sixth root:
$$
R = R_{F} \times \left( \frac{2}{k_{\exp}\tau_{0}} \right)^{1/6}
$$
This is the expression for donor-acceptor distance where the energy transfer rate is half the "experimental" radiative decay rate. 

c)
Using typical values for $k_{\exp}$ and $\tau_{0}$ of $10^{9} s ^{-1}$ and $10^{-9}s$ respectively. 
$$
R = 4.5 \left( \frac{2}{(10^{9} \times 10^{-9})} \right) ^{1/6}
$$
$$
R \approx 5.05 \ \text{nm}
$$

d)
This result makes sense, a slight increase in R would cause a halving of 50% in efficiency due to the strong $R^{-6}$ dependence. 


