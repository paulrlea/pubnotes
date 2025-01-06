---
dg-publish: true
---

... missed first 30 min 


Longiudinal vs Transverse vibration of a linear molecule:

> diagrams here 

These are independent and can be solved separately

- 3 variables but only 2 longitudinal modes 

> figure here 


We can eliminate translation by requiring the center-of-mass to be stationary during vibration

$$
mx_{1}+Mx_{2} +mx_{3} = 0
$$
$$
x_{2} = -\frac{m}{M} (x_{1}+x_{3})
$$
$$
T = \frac{1}{2} m\dot{x}_{1}^{2} + \frac{1}{2} M \dot{x}_{2}^{2} +\frac{1}{2} m\dot{x}_{3}^{2}
$$
$$
\dots = \frac{1}{2}m(\dot{x}_{1}^{2}+\dot{x}^{2}_{3}) + \frac{1}{2} \frac{m^{2}}{M} (\dot{x}^{2}_{1}+\dot{x}^{2}_{3}+2\dot{x}_{1}\dot{x}_{3})
$$
We can decouple the system by switching coordinates. We must eliminate the $\dot{x}_{1}\dot{x}_{3}$ term. 

Generalized coordinates: 
$$
q_{1} = x_{1} + x_{3}
$$
$$
q_{2} = x_{3}-x_{1}
$$
$$
x_{3} = \frac{1}{2}(q_{1}+q_{2}), \ \ x_{1} = \frac{1}{2}(q_{1}-q_{2}), \ \ x_{2} = -\frac{m}{M}q_{1}
$$
Find the kinetic energy of this system 

$$
T= \frac{1}{2} m\dot{x}_{1}^{2} + \frac{1}{2}M\dot{x}_{2}^{2} + \frac{1}{2}m\dot{x}_{3}^{2}
$$
$$
=\frac{1}{2}m \frac{1}{4} (\dot{q}_{1} - \dot{q} _{ 2} )^{2}+\frac{1}{2}M \frac{m^{2}}{M^{2}} \dot{q}^{2}_{1} + \frac{1}{2} m \frac{1}{4}  (\dot{q}_{1}+\dot{q}_{2})^{2}
$$
$$
= \frac{1}{2}m \frac{1}{4} (\dot{q}_{1}^{2}+\dot{q}_{2}^{2}-\cancel{ 2\dot{q}_{1}\dot{q}_{2} })+\frac{1}{2} \frac{m^{2}}{M} \dot{q}_{1}^{2} + \frac{1}{2}m \frac{1}{4} ( \dot{q}_{1}^{2} ++ \dot{q}_{2}^{2} + \cancel{ 2\dot{q}_{1}\dot{q}_{2} })
$$
Our coupling term cancels out. Kinetic energy finally given by 

$$
T = \frac{1}{4} m \dot{q}_{2}^{2} + \frac{mM+2m^{2}}{4M} \dot{q}_{1}^{2}
$$
Finding potential: 
$$
u = \frac{1}{2} \kappa_{1} ( x_{2}-x_{1})^{2} + \frac{1}{2}\kappa_{1}(x_{3}-x_{2})^{2}
$$
$$
=\frac{1}{2}\kappa_{1}(x_{2}^{2}+x_{1}^{2}-2x_{1}x_{2})+ \frac{1}{2}\kappa_{1}(x_{3}^{2}+ x_{2}^{2}-2x_{2}x_{3})
$$
$$
= \frac{1}{2}\kappa_{1} \left( \frac{m^{2}}{M^{2}}q^{2}_{1}+\frac{1}{4}(q^{2}_{1}+q_{2}^{2}-q_{1}q_{2}) + 2 \left(  \frac{1}{2} \right)(q_{1}-q_{2}) \frac{m}{M}q_{1} \right) \dots
$$
$$
+\frac{1}{2} \kappa_{1}\left( \frac{1}{4} (q_{1}^{2}+q_{2}^{2}+2q_{1}q_{2}) + \frac{m^{2}}{M^{2}}q_{1}^{2} 2 \frac{1}{2} (q_{1}+q_{2}) \frac{m}{M}q_{1} \right)
$$
$$
=\kappa_{1} \frac{m^{2}}{M^{2}} q_{1}^{2} +\frac{1}{4} \kappa_{1} (q_{1}^{2}+q_{2}^{2}) + \kappa_{1}q_{1}^{2} \frac{m}{M}
$$
$$
\frac{1}{4} \kappa_{1} q_{2}^{2} + \kappa_{1}q_{1}^{2} \left[ \frac{4m^{2}}{4m^{2}}+\frac{m^{2}}{4m^{2}}+\frac{4mM}{4m^{2}} \right]
$$
$$
=\frac{1}{4} \kappa_{1} q_{2}^{2}+ \kappa_{1}q_{1}^{2} \left[  \frac{4m^{2} + 4mM + M^{2}}{4m^{2}} \right]
$$
$$
u= \left( \frac{2m+M}{2M} \right)^{2}\kappa_{1}q_{1}^{2} + \frac{1}{4} \kappa_{1} q_{2}^{2}
$$
$$
\sum_{k} (A_{jk} -\omega^{2}m_{jk}) q_{k} = 0
$$
$$
A_{jk} = \frac{ \partial^{2} u }{ \partial q_{j} \partial q_{k} } 
$$
$$
q_{k} (t) = q_{k} e^{i(\omega t-\delta)}
$$
$$
A_{11} = \frac{ \partial^{2} u }{ \partial q_{1}^{2} } = 2\left( \frac{2m+M}{2m} \right)\kappa_{1}
$$
$$
A_{22} = \frac{ \partial^{2} u }{ \partial q_{2}^{2} } = \frac{1}{2}\kappa_{1}
$$
$$
A_{12} = A_{21} = 0
$$
$$
T = \frac{1}{2}\sum_{jk} m_{jk} \dot{q}_{j}\dot{q}_{k}
$$
$$
\frac{1}{2} m_{11} \dot{q}_{1}^{2} = \frac{mM+2m^{2}}{4m} \dot{q}_{1}^{2} 
$$
$$
m_{11} = \frac{mM+2m^{2}}{2m}
$$
$$
\frac{1}{2} m_{22} \dot{q}_{2}^{2} = \frac{1}{4 } m \dot{q}_{2}^{2}
$$
$$
m_{22} = \frac{m}{2}
$$
$$
m_{12} = m_{21} = 0
$$
$$
A_{jk} = \begin{bmatrix}
2\left( \frac{2m+M}{2m} \right)^{2}\kappa_{1} & 0 \\
0 & \frac{1}{2}\kappa_{1}
\end{bmatrix}
$$
$$
m_{jk} = \begin{bmatrix}
\frac{mM+2m^{2}}{2m} & 0 \\
0 & \frac{m}{2}
\end{bmatrix}
$$
We have $A_{jk}$ and $m_{jk}$ matrices. 

$$
\det \begin{bmatrix}
\frac{1}{2}\left( \frac{2m+M}{m} \right)\kappa_{1} - \omega^{2}\frac{ mM+2m^{2}}{2m} & 0 \\
0 & \frac{1}{2}\kappa_{1}-\frac{\omega^{2}m}{2}
\end{bmatrix}=0
$$
$$
\omega^{2}_{1} = \frac{1}{2} \left( \frac{2m+M}{m} \right)^{2} \kappa_{1} \frac{2M}{m(2m+M)}
$$
$$
\omega_{1}^{2} = \frac{2m+M}{mM} \kappa_{1}
$$
$$
\omega_{2}^{2} = \frac{\kappa_{1}}{m}
$$
Tensor is diagonalized which means that $q_{1}$ and $q_{2}$ are my normal coordinates. 

$$
q_{1} = a_{11}\eta_{1}+a_{1}\eta_{2}
$$
$$
q_{2} = a_{21}\eta_{1} + a_{22}\eta_{2}
$$
$$
\begin{bmatrix}
A_{11} - \omega^{2}_{1} m_{11}  &  0 \\
0 & A_{22}-\omega^{2}_{1}m_{22}
\end{bmatrix}
\begin{bmatrix}
a_{11} \\
a_{22}
\end{bmatrix} = \begin{bmatrix}
0 \\
0
\end{bmatrix}
$$
$$
0a_{11} + a_{21} = 0
$$
$$
0a_{11} + [ \ \ \ \ ] a_{21} = 0
$$
$$
a_{21} = 0
$$
$$
a_{11} = \text{free var.}
$$
$$
\begin{bmatrix}
1 \\
0 \\
\end{bmatrix}
$$
Transverse Vibrations: 
> figure here 


$$
m(y_{1}+y_{3}) + My_{2} = 0 
$$
$$
y_{2} = -\frac{m}{M} (y_{1}+y_{3})
$$
We will assume small oscillations, meaning that $\alpha$ is a small angle therefore 
$$
\alpha = \frac{\Delta y}{b} = \frac{(y_{1}-y_{2})+(y_{3}-y_{2})}{b}
$$
$$
y_{1}=y_{3}
$$
and substitute $y_{2}$

$$
 \alpha = \frac{2y_{1}}{bM}(2m+M)
$$
$$
T= \frac{1}{2}m(\dot{y}_{1}^{2}+\dot{y}_{3}^{2}) + \frac{1}{2}My^{2}_{2}
$$
$$
T=\frac{m}{M} (2m + M )\dot{y}_{1}^{2}
$$
$$
T = \frac{mMb^{2}}{4(2m+M)} \dot{\alpha}^{2}
$$
$$
u= \frac{1}{2}\kappa_{2} (b\alpha)^{2}
$$
$$
\omega_{3}^{2}=\frac{2(2m+M)}{mM}\kappa_{2}
$$
From the first and third normal modes EM radiation is detected because the electrical dipole moving. 
2nd no radiation b/c no dipole 

## The Loaded Spring (12.9)

- n masses separated by distance d in equilibrium 
- masses  m are connected by springs or elastic strings
- Total length of string $L=(n+1)d$ and fixed at both ends

> figure here 


Want to treat small transverse oscillations about equlibrium

consider particles: 
$$
\begin{matrix}
j-1, & j, & j+1
\end{matrix}
$$
displaced vertically

The force on the $j^{th}$ particle (considering only nearest neighbors)

>graph here
>