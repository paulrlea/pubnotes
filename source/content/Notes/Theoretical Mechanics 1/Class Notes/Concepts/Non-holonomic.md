---
dg-publish: true
---
Non-Holonomic constraints can be functions of position, velocity, and time. Namely, 
$$
F = F(x_{i},\dot{x}_{i},t)=0
$$
Constraints must equal 0, and be of the general form for velocity
$$
\sum_{i} A_{i}\dot{x}_{i} + B=0 
$$
- These are generally not integrable, unlike [[Holonomic]] constraints  unless: 
$$
A_{i} = \frac{ \partial f }{ \partial x_{i} } , \ \ B =\frac{ \partial f }{ \partial t } 
$$
$$
f = f(x_{i},t)
$$
$$
\sum \frac{ \partial f }{ \partial x_{i} }  + \frac{ \partial f }{ \partial t  } = 0 \implies \frac{ \partial F(x,t) }{ \partial t } 
$$
For non-integrable constraints, we use the method of Lagrange multipliers

[[Lagrange Multipliers]]


