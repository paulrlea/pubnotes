## Ensemble Theory:
- Given N particles, we want to find the probability of the system being in a certain state.
- "For the most part, the two methods give rise to the same averages"

> what are the two methods

Ensemble Ave 
$$
\bar{f} = \int f(p, q) P(p,q) d\Gamma
$$
Time Ave
$$
\bar{f} = \lim_{ T \to \infty } \frac{1}{T} \int_{0}^{T} f(t) \, dt
$$

However, hard to use time approach. Takes too long. 



...


The mean scales with the number of subsystems you divide a system into. 

A probability distribution for macroscopic quantities is very narrow, almost a [[@Spring2024/Physics/Math Background/Kronecker delta|Kronecker delta]]function. The average is going to be approximately the most probable value of a system, the details can be ignored. 

>"Effective Delta Function"

For independent statistical subsystems:
$$
\frac{\sqrt{( \Delta f)^{2} }}{\bar{f}} \approx \frac{1}{\sqrt{ n }}
$$
where f is a "sharp function"



## Liouville's Theorem

Describes to the evolution of ensembles in phase space. Is a fundamental conservation law, all realizations must stay in phase space regardless of evolution.

No sources, no sinks, just evolution of ensembles. 

>" Stuff cannot get lost"

This is similar to the continuity equation. 

Similar to fluid flow, but generalized to phase space which means it can be any variable (energy, momentum, etc etc)

$$
p(t,p,q) , \ \  \bar{v}(\dot{p},\dot{q})
$$
[[Liouville's Theorem]]
$$
\frac{ \partial p }{ \partial t }  + \text{div}(p\bar{v} )= 0 
$$

This is related to [[Theoretical Mechanics]], especially the [[Hamiltonian]] and [[Lagrangian]]

Recall Hamilton's equations.

> what is a Poisson bracket

## Microcanonical Ensemble

- An ensemble that is applicable to a real system
- Almost fixed energy 
- 