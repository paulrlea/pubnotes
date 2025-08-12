# Problem 1: 
 2D perovskite is formed with alternating layers of inorganic lead iodide octahedra and organic spacer cations. The thickness of each inorganic layer is 0.6 nm, and the thickness of each organic layer is 1.2 nm
 
a). Calculate the effective band gap of the 2-D perovskite, assuming that the band gap of the bulk lead iodide perovskite is 1.5 eV and that quantum confinement effects lead to a band gap increase inversely proportional to the square of the inorganic layer thickness. 

We can use the following relation to calculate the band gap shift: 
$$
\Delta E = \frac{\hbar^{2}\pi^{2}}{d^{2}} \left(  \frac{1}{m^{\star}_{e}}+ \frac{1}{m^{\star}_{h}} \right)
$$
Using a typical effective electron and hole mass of 0.298 and 0.275 [https://www.osti.gov/servlets/purl/1492304]  free electron masses respectively, we can calculate the shift in band gap energy. 

$$
\Delta E = \frac{1}{(0.6\times 10^{-9})^{2}} \cdot 2.682\times 10^{-37} = 7.449\times 10^{-19} J
$$
Converting back to eV: 4.649 eV

This is the band gap shift. Adding original band-gap gives a total effective band-gap of

6.149 eV

b) Discuss the advantages and disadvantages of using 2D perovskites in solar cells compared to 3D perovskites. 

2D perovskites are more stable and resistant against moisture, oxygen, and heat compared to 3D perovskites. This makes them more durable for long-term use. However, their lower charge carrier mobility and wider band gap limit their efficiency in solar cells. While 3D perovskites achieve higher power conversion efficiencies due to better charge transport and optimal band gaps, they suffer from rapid degradation if exposed to sub-optimal conditions. 

# Problem 2
a)  Explain what is ion intermixing, giving advantages of this method over the conventional perovskite structure. 

Ion intermixing in perovskites requires the diffusion and exchange of ions, enhancing material properties compared to conventional perovskites. In practice, this means Depending on which component of the perovskite is mixed, this can yield different effects:

- Anion Substitution: Allows for tunable band-gaps, increased carrier lifetimes, and improved chemical and structural stability.
- B-Site Cation Substitutions: Also allows for tunable band-gaps, improves low temperature stability, and increases luminescence
- A-Site Cation Substitutions: Helps improve stability of the perovskite and increases defect tolerance

b) 
>Analyse the composition of the perovskite given by the formula:

$$
(FA_\text{0.83} MA_\text{9.17})_\text{0.95} Cs_\text{0.05}Pb(I_\text{0.83}Br_\text{0.17}) _\text{3}
$$
This is a mixed-cation, mixed-halide type perovskite. The A site large cation is a mixture of formamidinium, cesium, and methylammonium, the B site small cation is lead, and the x site anion is a mixture of Iodide and Bromide. 

> For each component, give a rationale for using it in the material.

The intermixed methylammonium, formamidinium and cesium A site allows for improved thermal stability and defect tolerance, while slightly adjusting the bandgap as well.

FA reduces degradation under heat, while also slightly narrowing the band-gap. 
MA improves crystalinity and improves charge transport properties. 
Cs improves resistance to environmental factors

The B site cation is lead. Lead is a good option because of its excellent charge transport properties and high absorption coefficient, making it suitable for solar cell applications. Unfortunately it is very toxic. 

The x-site anion is a hybrid mixture of iodide-bromide. This does the bulk of the band-gap adjustment, allowing for a specific regime of light to be captured. 

Pure iodide based perovskites ($FAPbI_{3}$) have a bandgap of 1.48eV

Pure bromide based perovskites ($FAPbBr_{3}$) have a bandgap of 2.25eV

The mixture of these two materials allows for a specific bandgap between the two to be selected. 

> Estimate qualitatively the difference between the original material and:

$$
(FA_\text{0.83}MA_\text{0.17})_\text{0.95} Cs_\text{0.05} PbI_{3}
$$
This material will likely have a lower bandgap then the original material. Additionally, it may display slightly worse moisture resistance. 

$$
MA_\text{0.95}Cs_\text{0.05}Pb(I_\text{0.83}Br_\text{0.17})_\text{3}
$$
This material will have a slightly wider bandgap, but may display reduced resistance to thermal degradation.

$$
(FA_\text{0.83} MA_\text{9.17})_\text{0.95} Pb(I_\text{0.83}Br_\text{0.17}) _\text{3}
$$
This material will have the same or very similar bandgap, but will be less resistant to environmental factors such as moisture, light and heat. 

> Calculate the correct values of x, y and z in the perovskite formulae below

$$
La(Al_\text{x}Mg_\text{0.5}Ta_\text{0.25})O_\text{3}
$$
We know that the proportions of Al, Mg, Ta have to add up to one. Therefore, we can deduce that $x=0.25$, defining a proportion of 0.25 parts aluminum to 0.5 parts Magnesium and 0.25 parts tantalum. 

$$
(La_\text{x}Sr_\text{0.2})_\text{y} (Mn_\text{0.2}Fe_\text{z}Co_\text{0.4}Al_\text{0.2})O_{3}
$$
Similarly to the last material, we can solve for x by knowing that the proportions of Lanthanum and Strontium have to add up to one, therefore $x=0.8$. There exists no other A site cation, so y has to be 1. The proportions in the B site cation also have to add up to one, from this we can deduce that $z =0.2$

# Problem 3
Compare and contrast charge carrier properties of hybrid perovskites and organic semi- conductors. In particular, outline the difference in:
> a) nature of charge carriers and their main properties

Perovskites exhibit inorganic-like transport with free electrons and holes, low effective mass, and high mobility (10–100 cm²/Vs), enabling efficient charge transport over long distances. A low exciton binding energy (~10–50 meV) allows for easy charge separation, making them suitable for photovoltaic devices. Organic semiconductors rely on "hopping" transport, where charge carriers exist as polarons with low mobility (<1 cm²/Vs) and high exciton binding energy (0.1–1 eV), requiring additional mechanisms for charge separation. These differences make perovskites more suitable for high-performance solar cells and optoelectronics, while organic semiconductors are better in flexible electronics and OLEDs.

> b) importance of polarons for optoelectronic applications in both materials 

In organic semiconductors, polarons are the primary charge transport mechanism. Charge carriers move via hopping transport, where strong polaronic effects stabilize carriers but also limit mobility (~0.01–10 cm²/Vs). 

In perovskites, polarons also form, but instead of inhibiting charge transport, large polaron formation screens carrier scattering, reducing recombination and enhancing mobility (10–100 cm²/Vs). This effect benefits perovskite-based photovoltaic devices and optoelectronics. 



# Problem 4
a) Briefly explain the importance of surface plasmon polaritons in nanomaterials applicati- ons:

Surface plasmon polaritons (SPPs) are electromagnetic waves coupled to collective oscillations of free electrons at the interface between a metal and a dielectric. They allow for strong light confinement at subwavelength scales, making them crucial for various nanomaterial applications such as optoelectronics and lasers.

b) A silver nanostructure embedded in air ($\epsilon_{air}$ = 1) is illuminated by a He-Ne laser ($\lambda_{0}$ = 632.8 nm). At this wavelength, silver has permittivity $\epsilon_{silver}$ = −15.88. Calculate the effective wavelength of surface plasmon polaritons in this nanostructure. 

This is given by: 
$$
\lambda_{eff} \approx\lambda_{0} \sqrt{ \frac{\epsilon_{d} + \epsilon_{m}}{\epsilon_{d}\epsilon_{m}} }
$$
We can plug in the respective values and solve for $\lambda_{eff}$
$$
\lambda _\text{eff} = 612.5516 \text{ nm}
$$

c) A nanometer-sized optical cavity is formed by creating a thin layer of SiO2 sandwiched between Au claddings. A red light (λ = 651 nm in vacuum) is confined in the cavity as a surface plasmon polariton with a wavelength of λef f = 51 nm.

> Calculate the effective refractive index of the cavity. 

$$
\lambda _\text{eff}  = \frac{\lambda _\text{0}}{n_\text{eff}} \implies n_{eff} = \frac{\lambda_{0}}{\lambda_{eff}}
$$
Solving this with $\lambda_{0} = 651\text{ nm}$ and $\lambda _\text{eff} = 51 \text{ nm}$ we get an effective refractive index of 12.76.

> Comment on viability of obtaining such refractive index in bulk materials. 

It is not possible with current materials. The highest known bulk refractive index is rhenium diselenide with a refractive index of ~5 (https://pubs.acs.org/doi/10.1021/acsphotonics.2c01898)

> Suggest two ways the cavity in the previous question could be applied outside of the lab. 

This technology can be used to make nano-scale, on-chip plasmonic laser sources, useful for nanooptoelectronics and sensing applications. Additionally, this can be used for enhanced photovoltaic sensors by enhancing light absorption in photocells. 