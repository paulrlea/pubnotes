# Thermodynamics Review 
## Temperature: 
The temperature of two objects "a" and "b" in thermal contact will reach thermal equilibrium eventually. This is the "0th" law of thermodynamics. 

$$
T_{a} = T_{b} 
$$
## Equation of state: T,P,V,N
> what is N? Avogadro number?
> 	- N ![{\displaystyle N}](https://wikimedia.org/api/rest_v1/media/math/render/svg/f5e3890c981ae85503089652feb48b191b57aae3) is the number of particles (usually atoms or molecules) of the gas.
$$
P=P(T,P)
$$

$$
P = \frac{N}{V}
$$

Ideal Gas: 
$$
PV=NkT, \ \ \ P=kTP
$$
Van Der Wahls Gas:
$$
\left( P+a\left( \frac{N}{V} \right)^{2} \right) (V-bN)=NKT
$$
## Work
$W$ is the work done on a system 
$$
=\int F_\text{ext} dx 
$$
> is this below equation equiv to the above?
$$
\int(-p\cdot a) dx = -\int PdV
$$

![[Pasted image 20240906083143.png]]

Where $\Delta x$ is an infinitesimal change in distance, and thus $\Delta V = A\Delta x$ where A is the area of the cylinder above. 

$$
\delta W = -p dV
$$
infinitesimal work can be given as a derivative of volume. 

We can use the equation of state: 

> Quasi-static Process: $P = P(T,V)$. I think

$$
W = -\int P(T,V) dV
$$
For an Ideal gas compressed at constant temperature: 

$$
P=\frac{NkT}{V}
$$
If we go from some volume $V_{1}$ to some volume $V_{2}$
$$
W = -NkT \int_{V_{1}}^{V_{2}}  \, dV = -NkT \ln \frac{V_{2}}{V_{1}}
$$
If $\oint\delta W \neq_{0}$, then it is **not** a state function

![[Pasted image 20240906083905.png]]

> Is this the total work done? I believe so. 
$$
\oint \delta W = P_{2}(V_{2}-V_{1}) - P_{1}(V_{1}-V_{2}) = -(P_{2}-P_{1})(V_{2}-V_{1})
$$
## The first law of thermodynamics

Given a thermally isolated system: ([[adiabatic process]])
$$
dE = \delta W
$$
E (energy) is a state function, uniquely determined by T,P,N...

In the case of thermal contact, where $\delta Q$ is not 0, this is heating/cooling.


> Q is temprature? or heat? so $\delta Q$ is heating/cooling?

$$
dE = \delta Q = \delta W
$$
$$
\delta E = \delta Q - pdV
$$

$$
\oint dQ \neq 0
$$
(not a state function)

### Equation of state for the energy
If N is constant (not adding or removing mass from the system )
$$
E(T,V) 
$$
Ideal Gas: (mono-atomic gas)
$$
E=\frac{3}{2} NkT
$$
Van Der Whals gas:
$$
E = \frac{3}{2} NkT - N\left( \frac{N}{V} \right)a
$$
Notice how energy does not depend on volume in the ideal gas case. 

Using statistical mechanics to derive this from "microcopies"

> what is a microcopy

Isothermal Process for ideal gas, where T is constant 

> isothermal means constant temperature? 

$$
dE = \delta Q +\delta W = 0
$$
$$
\delta Q = -\delta W
$$
$$
Q_{1\to 2} = -W_{1\to 2} = NkT \ln\left( \frac{V_{2}}{V_{1}} \right)
$$
This is the work done from a change in volume, i.e compression or expansion. 

## Heat Capacity and Enthalpy


Heat capacity (aka specific heat) is the amount of heating needed to change the temperature by a unit amount. 

$$
c = \lim_{ \delta T \to 0 } \frac{\delta Q}{\delta T}
$$
For a constant volume: 
$$
\delta Q = dE + \cancel{ pdV }
$$
and 
$$
c_{v} = \frac{\delta Q}{\delta T}|_{V}=\left(  \frac{ \partial E }{ \partial T }  \right)_{V}
$$
As an example: The monoatomic ideal gas: 
$$
c_{v} = \frac{3}{2} Nk
$$
### Enthalpy 
Enthalpy is thermodynamic potential?
Denoted by H, where H is
$$
H=E+pV
$$
and 
$$
dH = dE + pdV + Vdp = \delta Q + VdP
$$

You can use enthalpy to find heat capacity?
For constant pressure: 
$$
\left( \frac{ \partial H }{ \partial T }  \right)_{P} = \frac{\delta Q}{\delta T} _{P} = c_{P}
$$
## General Relationship between Constant pressure and volume
This is constant pressure and temperature enthalpy. 

$$
H=E+pV
$$
$$
E(T,V)
$$
$$
C_{v} = \left( \frac{ \partial E }{ \partial T }  \right)_{V}
$$
$$
C_{p} = \left( \frac{ \partial H }{ \partial T }  \right)_{p}
$$
$$
C_{p} = \left( \frac{ \partial H }{ \partial T }  \right)_{P} = \left( \frac{ \partial E }{ \partial T }  \right)_{p} + p \left( \frac{ \partial V }{ \partial T }  \right)_{p}
$$
$$
dE = \left( \frac{ \partial E }{ \partial T }  \right)_{V}dT + \left( \frac{ \partial E }{ \partial V }  \right)_{T} dV
$$
$$
C_{p} = C_{v} + \left( \frac{ \partial V }{ \partial T }  \right)_{p} \left[ \left( \frac{ \partial E }{ \partial V }  \right)_{T} +p \right]
$$
## Adiabatic Processes
An adiabatic process is a process that excludes heat transfer or exchange. Perfectly insulated. 

$$
dE = \delta W + \delta Q
$$
The definition of an adiabatic process: 
$$
\delta Q =0
$$
There is no energy exchange due to temperature difference.
$$
\delta W = -PdV
$$
This is a "quasistatic" process. Quasistatic adiabatic process. 

$$
dE =dW = -pdV
$$

![[Pasted image 20240910085054.png]]
## The second Law of thermodynamics

