---
dg-publish: true
---
System described by 
$$
k=1,2,3,\dots s
$$
With [[generalized coordinates]] described by $q_{k}(t)$

Finding the [[Lagrangian]] 
$$
L=T-u
$$
and 
$$
\frac{d}{dt} \frac{ \partial L }{ \partial \dot{q}_{k} } -\frac{ \partial L }{ \partial q_{k} } =0
$$
Where we get $s$# of equations

For a system where a stable equilibrium exist: 
$$
q_{k}=q_{k_{0}}, \ \ \dot{q}_{k}=0, \ \ \ddot{q}_{k}=0
$$
Find $u(q_{1},q_{2},q_{3}\dots q_{s})$ for coupled oscillations by expansion of the appropriate Taylor series about the equilibrium 

## Taylor Series, Potential and Equilibrium

$$
u(q_{1},q_{2},\dots q_{s})=u_{0} + \sum^{s}_{k} \frac{ \partial u }{ \partial q_{k} } |_{q_{k}}+\frac{1}{2}\sum^{s}_{j,k} \frac{ \partial^{2} u }{ \partial q_{j} \partial q_{k} } |_{0} q_{j}q_{k} 
$$
This is cumbersome. Defining the following makes it less so 
$$
\frac{ \partial^{2} u }{ \partial q_{j} \partial q_{k} } |_{0} = A_{jk} 
$$
$$
u=\frac{1}{2} \sum^{s}_{jk} A_{jk} q_{j}q_{K}
$$

## Kinetic Energy 

$$
T= \frac{1}{2} \sum^{s}_{j,k} m_{jk} \dot{q}_{j}\dot{q}_{k}
$$
$m_{jk}$ will depend on actual mass of the system and a coordinate transformation. 

Quadratic function of generalized velocity. 

Coordinate transform into Cartesian coordinates:
$$
T=\frac{1}{2 } \sum^{n}_{\alpha} \sum^{3}_{i=1}m_{\alpha}\dot{x}^{2}_{\alpha i}
$$
$$
x_{\alpha i} = \sum^{s}_{k=1} \frac{ \partial x_{\alpha i} }{ \partial q_{k} } \dot{q}_{k}
$$
$$
T = \frac{1}{2} \sum_{\alpha}\sum^{s}_{i,j,k} m_{\alpha} \frac{ \partial x_{\alpha i} }{ \partial q_{j} } \frac{ \partial x_{\alpha i} }{ \partial q_{k}  } \dot{q}_{j} \dot{q}_{k}
$$
$$
m_{jk} = \sum_{\alpha} \sum_{i} m_{\alpha} \frac{ \partial x_{\alpha i} }{ \partial q_{j} }  \frac{ \partial x_{\alpha i} }{ \partial q_{k} } 
$$
Expanding $m_{jk}$ about the equilibrium 
$$
m_{jk} = m_{jk} (q_{l0}) + \sum_{l} \frac{ \partial m_{jk} }{ \partial q_{i} } |_{0} q_{l}
$$
We can ignore the last term because its cubic $\therefore$ small

$$
T=\frac{1}{2} \sum^{s}_{j,k} m_{jk} \dot{q}_{j} \dot{q}_{k}
$$
$$
L = T-U
$$
$$
=\frac{1}{2} \sum^{s}_{jk} m_{jk} \dot{q}_{j} \dot{q}_{k} - \frac{1}{2}\sum^{s}_{j,k} A_{jk} q_{j}q_{k}
$$
$$ 
=\frac{1}{2} \sum^{s}_{j,k} (m_{j,k} \dot{q}_{j}\dot{q}_{k} - A_{jk} q_{j}q_{k})
$$
$$
-\frac{ \partial L }{ \partial q_{k} }  + \frac{d}{dt}  \frac{ \partial L }{ \partial \dot{q}_{j} } =0
$$
Remove $\frac{1}{2}$ 
$$
\frac{ \partial L }{ \partial q_{k} }  = -\sum_{j} A_{jk} q_{j}
$$
$$
\frac{ \partial L }{ \partial \dot{q}_{k} }  = \sum_{j} m_{jk} \dot{q}_{j}
$$
$$
\frac{d}{dt} \frac{ \partial L }{ \partial \dot{q}_{k} }=\sum_{j}m_{jk} \ddot{q}_{j}
$$
Equation of motion:
$$
\sum_{j} (A_{jk}q_{j} + m_{jk}\ddot{q}_{j})=0
$$
Solutions of the form
$$
q_{j}(t) = q_{j} e^{i(\omega t-\delta)}
$$
Plug in and get 
$$
\sum^{s}_{J} (A_{jk} -\omega^{2} m{_{jk}})a_{j} = 0
$$



