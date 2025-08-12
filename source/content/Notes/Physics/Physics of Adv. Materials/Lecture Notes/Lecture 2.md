## OLED Distinctions
### OLED's vs PLED

- Both organi
- OLED made with smaller molecules, PLED made with polymers
- OLED created with vaccum evaporation
- PLED still in research
	- Has potential for very large cheap flexible displays

### AMOLED vs PMOLED
- PMOLED's consume more energy
	- Best for small screens
	- Easy to make
- AMOLED
	- Additional layer of transistors
	- Fsater refresh rates
	- Consumes less power 
	- Harder to make

### Bottom Emission vs Top Emission Vs Transparent
- Bottom Emission: Cathode is opaque, Anode/substrate transparent
- Top Emission: Anode is opaque, cathode transparent 
- Transparent: Both transparent 

### 3 Generations of OLED
1'st Generation: Fluorescent OLED:
- only utilizes singlet pairs
- 25% efficient
2nd Generation: Phosphorescent OLED:
- Utilizes triplet pairs as well

## Physics of OLED's
Traditional LED Operation:
![[Pasted image 20250122042353.png]]
In traditional LED, inject charges, fill holes, emit light


Most simple OLED has 3 layers: Annode, cathode, and active layer. This is circa 1965
In OLED: Injection of charges, charge transport, exciton formation, radiative recombination


Charges have to be fast enough to form exciton 
If exciton is slow/weak, then charges move and don't recombine radiatively

We want charges to move as fast as possible until the exciton phase

Structure helps with this. See diagram ![[Pasted image 20250122042928.png]]

EBL is electron blocking layer


Learn this diagram
![[Pasted image 20250122043144.png]]

Strong forward bias: When light is emittted
Reverse Bias: Hooked up OLED backwards
Equilibrium: Not hooked up to power


## Qualities of OLED's

### Luminous Efficiency 

$$
\eta_{lum} = \frac{\Phi_{L}}{V \cdot I} \left[ \frac{lumen}{W} \right] \propto \frac{i}{V \cdot I} \left[ \frac{cd}{VA} \right]
$$
V: Driving voltage
I: Current
$\Phi_{L}$: Luminous Flux

Lumens/Watts

proportional to Incandecence (Candellas)/ W

### Electroluminescence Quanum Efficiency:
Internal efficiency, disregarding losses in photon transport
Assumes Phosphoresence does not exist

$$
\eta_{EL} = \eta_{PL} \cdot r_{st} \cdot \gamma_{cap}
$$
$\eta_{PL}$ - Photo-luminescence efficiency. 
	Can be improved by supressing nonradiative channels
$r_{st}$ - Ratio of singlets to total excitons
	Maxes at 25%
	Increase radiative excitons
$\gamma_{cap}$ - Excition formation factor
	 Need more minority carrier to balance charge injection and transport


# Optimizing OLED's
## Increasing $\eta_{PL}$: Suppress non-radiative decay channels
1.  Prevent aggregation Quenching 
	2. Optimize optical design, ensure injected charges don't recombine too soon 
	3. Reduce contamination
Preventing Aggregation Quenching:
- Prevent close-packing of **chromospeheres**
- Dilute with matrix substance
- Or design chemicals to not stack 

A chemical that does this are polythiophenes
Lower Crystalinity leads to higher efficiency

Oligothiophenes also do this:
![[Pasted image 20250122050937.png]]

FET materials desire the opposite properties of this, as seen last lecture

#### Optical device design 
- Many engineering considerations
- Prevent waveguiding 
- Prevent reabsorbtion
- Prevent refraction
## Increase $R_{st}$: Boost # of radiative excitons
1. Maxes out at 25%

Methods:
#### Triplet-Triplet Annihilation: (TTA)
- Take two triplets, put it into a singlet
- Seen in Anthracene
- Total possible efficiency of 25% + 37.5% = 62.5% 
- In practice, triplets provide only about 15%, raising total efficiency to 40%

#### Thermaly activated Delayed Fluorescence: (TADF)
- Reverse Intersystem crossing: turning triplet to singlet
- Requires heavy molecules, complex
- Potential 100% efficency

#### Hybrid Local Charge Transfer: (HLCT)
- Theoretical 100% efficiency as well
- Uses donor-acceptor molecule with triplet and singlet energies that are siminlar

#### Harvesting Phosphorescence:
- Theoretical 100% PLQY

Three methods:
- Foerster Transfer
- Dexter Transfer
- E-H Direct capture

Issues
- Hard to find materials that don't have high TTA levels
- Difficult to find blue emitters
- Efficiency drop at large currents 
- Dexter transfer is slow because of range

## Increase $\gamma_{cap}$: Improve e-h balance
### Balancing Charge Injection:
 Cathode:
 - reduce work function by adding alkaline materials
 - very useful for blue materials
Anode:
- Reduce work function of ITO by:
	- Self-assembled monolayers
	- Spin Coated layers
	- Layer-by-Layer deposition of progressively dedoped layers
	- Oxygen plasma treatment
		- Standard now


### Balancing Charge Transport:
Make sure that charges move quickly
- Reduce excess majority carriers
- Introduce separate electrion and hole transporting layers
- Formation of hetrojunctions
# Organic Photovoltaics
- Goal is to turn light into electrons.
- Opposite of OLED's


