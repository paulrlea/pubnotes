# The fundamental thermodynamic relation

First Law
$$
dE = \delta Q +\delta W
$$
$$
\delta W = pdV
$$
$$
\delta Q = TdS \text{ ( Quasistatic Reversible Process)}
$$
$$
dE = TdS -pdV = \text{"heat" + "work"}
$$
If particle number is not held constant: 
$$
dE = TdS - pdV + \mu dN
$$
$$
dS = \frac{1}{T} dE + \frac{P}{T} dV - \frac{\mu}{T} dN \implies S(E,V,N)
$$
$$
\frac{1}{T} = (\partial S)
$$
$$
\frac{1}{T} = \left( \frac{ \partial { S } }{ \partial E }  \right)_\text{V,N} \ , \ \ \frac{P}{T} = \left( \frac{ \partial S }{ \partial R }  \right)_\text{E,N} \ , \ \ \frac{\mu}{T} = -\left( \frac{ \partial \sqrt{ y } }{ \partial N }  \right)_{E,V}
$$

> Example: Ideal gas (assuming fixed N)

$$
E = \frac{3}{2} NkT; \ \ \ PV = NkT
$$
$$
\frac{1}{T} = \frac{3}{2} \frac{Nk}{E} + Nk \frac{dV}{V}
$$
 > S is entropy? yes!
 
$$
dS = \frac{3Nk}{2} \frac{dE}{E} + Nk \frac{dV}{V}
$$
$$
dS = \frac{3Nk}{2} \frac{dE}{E} + Nk \frac{dV}{V}
$$

$$
S(E,V)  \frac{3}{2} Nk \ln \frac{E}{E_{0}} + Nk \ln \frac{V}{V_{0}}
$$
Where $E_{0} \ \& \ V_{0}$ are arbitrary

**Often Needed:**

$$
S(T,V) = \frac{3}{2} Nk \ln \frac{T}{T_{0}} + Nk\ln \frac{V}{V_{0}}
$$
and 
$$
\Delta S (1\to2) = \frac{3}{2}Nk \ln \left( \frac{T_{2}}{T_{1}} \right)+Nk\ln\left( \frac{V_{2}}{V_{1}} \right)
$$
This approximation works only at high temp and low density. Falls apart at low temps. 
## Gibbs - Duharm Relation 

$$
S = S(E,V,N)
$$
Maximum at fixed E,V,N

If you double the size of the system , you will ideally have double the entropy. 

$$
dS = \left( \frac{ \partial S }{ \partial E }  \right)_\text{V,N} dE + \left( \frac{ \partial S }{ \partial V } \right)_\text{E,N} dV + \left( \frac{ \partial S }{ \partial \mu }  \right) _\text{ E,V} dN
$$
Extensive State Function: (?)
$$
E = E(S,V,N) 
$$


> $\lambda$ is the size of the system?

> extensibility?  

$$
\frac{ \partial E }{ \partial (\lambda S)  } \frac{ \partial \lambda S }{ \partial \lambda }  + \frac{ \partial E }{ \partial (\lambda V) }  + \frac{ \partial E }{ \partial (\lambda V) } + \frac{ \partial E }{ \partial (\lambda N) }  \frac{ \partial(\lambda N) }{ \partial \lambda } = E(S,V,N)
$$
$$
\frac{ \partial E }{ \partial (\lambda S) } S + \frac{ \partial E }{ \partial (\lambda V) }V + \frac{ \partial E }{ \partial(\lambda N)N  }  = E(S,V,N)
$$
Then set $\lambda = 1$

$$
E(S,V,N) = TS - PV +\mu N
$$

$$
dE = TdS + SdT - pdV - Vdp + \mu dN + Nd\mu
$$
Compare with first law:
$$
SdT - Vdp + Nd\mu = 0 
$$
This is the Gibbs-Duham relation

## The third law of thermodynamics
$$
\lim_{ T \to 0 } S = 0
$$
(With exceptions)

Quasi-static case:
$$
\frac{\delta Q}{T} = dS
$$
@ constant volume
$$
\delta Q = C_{V}(T)dT
$$
The heat capacity isn't always a constant, it may depend on temperature. 
$$
\int_{T_{1}}^{T_{2}}  \, dS = \int_{T_{1}}^{T_{2}} \frac{\delta Q}{T} \, = \int_{T_{1}}^{T_{2}} \frac{C_{v} (T)}{T} \, dT
$$
$$
S(T_{2}, V) - S(T_{1},V) = \int_{T_{1}}^{T_{2}}  \frac{C_{V}(T)}{T} \, dT
$$
$$
S(T_{1},V) = \lim_{ T_{1} \to 0 } \int_{T_{1}}^{T_{2}} \frac{C_{V}(T)}{T} \, dT \implies \lim_{ T \to 0 } C_{V}(T)=0
$$
Similarly, you can repeat the same for constant pressure P 
$$
\lim_{ T \to 0 } C_{p} (T) = 0
$$
## Generalized Thermodynamic Potentials
Equilibrium with Gradients

System small compared to a large reservoir. 
![[Pasted image 20240906104231.png]]


### Subcase: Hemholtz Free energy
- Fixed volume



## Maxwell Relation and Applications

Why does this Maxwell dude do literally everything




