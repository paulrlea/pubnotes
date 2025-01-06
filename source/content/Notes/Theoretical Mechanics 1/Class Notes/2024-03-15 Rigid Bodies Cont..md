---
dg-publish: true
---
## Rotational Kinetic Energy 
$$
T_\text{rot} = \frac{1}{2} \sum_{\alpha} m_{\alpha} ( \vec{\omega} \times \vec{r}_{\alpha})^{2} \tag{1}
$$
Where 
$$
\begin{matrix}
\vec{r}_{\alpha} = (x_{\alpha 1}, x_{\alpha 2}, x_{\alpha 3}\dots) \\
\vec{\omega} = (\omega_{1}, \omega_{2}, \omega_{3}) \\
\end{matrix}
$$
and 
$$
(\vec{A} \times \vec{B} ) ^{2} = A^{2}B^{2} - (\vec{A} \cdot \vec{B})^{2}
$$
	Using these two relations we can rewrite (1) as the following

$$
=\frac{1}{2} \sum_{\alpha} m_{\alpha} [\omega^{2}r_{\alpha }^{2} - (\vec{\omega} \cdot \vec{r}_{\alpha}^{2})]
$$
Expanding this
$$
T_\text{rot}=\frac{1}{2} \sum_{\alpha} m_{\alpha} \left[ \left( \sum_{i} \omega_{i} ^{2} \right)\left( \sum_{k} x_{a,k}^{2} \right) - \left( \sum_{i} \omega_{i}x_{\alpha,i}  \right)\left( \sum_{j}\omega_{j}x_{\alpha,j} \right) \right]
$$
Using [[@Spring2024/Physics/Math Background/Kronecker delta]] to simplify this:

$$
\frac{1}{2} \sum_{\alpha} \sum_{i,j} m_{\alpha} \left[ \omega_{i}\omega_{j}\delta_{ij}\left( \sum_{k}x_{\alpha k}^{2} \right) - \omega_{i}\omega_{j} x_{\alpha,i}x_{\alpha,j} \right]
$$
$$
=\frac{1}{2} \sum_{ij} \omega_{i}\omega_{j} \sum_{\alpha} m_{\alpha} \left[ \delta_{ij}\sum_{k} x_{\alpha,k}^{2} - x_{\alpha,i} x _{\alpha,j} \right]
$$
Content after second summation is called the [[Inertia tensor]]

For a discrete distribution of particles, the inertia tensor looks like the following: 
$$
I_{ij} = \sum_{\alpha} m_{\alpha} \left( \delta_{ij} \sum_{k} x_{\alpha,k}^{2} - x_{\alpha,i} x_{\alpha,j} \right)
$$
Continuous Distribution
$$
	I_{ij} = \int _{v} p(\vec{r}) \left( \delta_{ij}\sum_{k} x_{\alpha k}^{2}-x_{\alpha i} x_{\alpha j} \right) \, dV
$$
Example: 
Consider 3 masses (all with mass m) $\alpha$ will sum from 1->3 3D problem. They have the following positions: 
$$
\begin{matrix}
\vec{x}_{1} = a,0,0 \\
\vec{x}_{2} = 0,a,2a \\
\vec{x}_{3} = 0,2a,a
\end{matrix}
$$
![[Pasted image 20240315085645 1 1 1.png]]

$$
I_{11} = \sum_{\alpha}^{3}m_{\alpha}(x_{\alpha_{2}}^{2}+x_{\alpha_{3}}^{2})
$$
$$
=m[(x_{1,2}^{2}+x_{1,3}^{2})+ (x_{2,2}^{2}+x_{2,3}^{2})+(x_{3,2}^{2}+x_{3,3}^{2})]
$$
$$
=m[(0^{2}+0^{2}) + (a^{2}+2a^{2}) + ((2a)^{2} + a^{2})]
$$
$$
=m[a^{2}+4a^{2}+4a^{2}+a^{2} ] = 10ma^{2}
$$
Finding $I_{22}$

$$
 \sum_{\alpha} m_{\alpha}(x_{\alpha,1}^{2}+x_{\alpha,3}^{2})
$$
$$
m[(x_{1,1}^{2}+x_{1,3}^{2})+(x^{2}_{2,1}+x_{2,3}^{2})+(x^{2}_{3,1} + x^{2}_{3,3})]
$$
$$
m[a^{2}+0^{2}+0^{2}+4a^{2}+0^{2}+a^{2}] 
$$
$$
I_{22}=6ma^{2}
$$
$$
I_{33} = m[a^{2}+a^{2}+4a^{2}] = 6ma^{2}
$$
$$
I_{12}=-m[(a \times 0) + (0 \times a)+ (0 \times 2a)] = 0 = I_{21}
$$
$$
I_{13} = -m[(a \times 0 ) + ( 0 \times 2a ) + (0 \times a ) ] = I_{3,1}
$$
$$
I_{23} = -m[(0 \times 0 ) + (a \times 2a) + ( 2a \times a)] = -4ma^{2}=I_{32}
$$
$$
\{I\}=\begin{pmatrix}
10ma^{2} & 0 & 0 \\
0 & 6ma^{2} & -4ma^{2} \\
0 & -4ma^{2} & 6ma^{2}
\end{pmatrix}
$$

Example:
Rectangular plate of uniform density $\rho$ with total mass M, length a, width b and height c
- Put the origin at the center of the plate 

![[Pasted image 20240315092019 1 1 1.png]]
$$
\begin{matrix}
-\frac{a}{2} \leq x_{1} \leq \frac{a}{2} \\
-\frac{b}{2} \leq x_{2} \leq \frac{b}{2} \\
-\frac{c}{2} \leq x_{3} \leq \frac{c}{2}
\end{matrix}
$$
$$
\rho= \frac{M}{abc}
$$
$$
I_{ij} = \int _{v} \rho(r) \left( \delta_{ij} \sum_{k} x_{\alpha k}^{2} - x_{\alpha i}x_{\alpha j} \right) \, dV 
$$
$$
I_{ii}=\rho \int _{V}(x^{2}_{2} + x_{3}^{2}) \, dV = \rho\left[ \int _{V} x_{2}^{2} \, dV +\int _{V} x_{3}^{2} \, dV  \right] 
$$
$$
\rho\left[ \int\limits_{-\frac{a}{2}}^{a/2} \int\limits_{-\frac{b}{2}}^{b/2}\int\limits_{-\frac{c}{2}}^{c/2}  x_{2}^{2}\, dx_{1}   \, dx_{2}  \, dx_{3} + \int\limits_{-\frac{a}{2}}^{a/2} \int\limits_{-\frac{b}{2}}^{b/2}\int\limits_{-\frac{c}{2}}^{c/2}  x_{3}^{2}\, dx_{1}   \, dx_{2}  \, dx_{3} \right]
$$
$$
=\rho \left[ ac \frac{1}{3}x_{2}^{3}|^{b/2}_{-b/2} + ab \frac{1}{3} x_{3}^{3} |^{c/2}_{-c/2} \right]
$$
$$
=\rho\left[ ac \frac{1}{3} \frac{b^{3}}{8} + ac \frac{b^{3}}{8} \frac{1}{3} + ab \frac{c^{3}}{8} \frac{1}{3} + ab \frac{c^{3}}{8} \frac{1}{3} \right]
$$
$$
\rho\left[ \frac{ab^{3}c}{12}+\frac{abc^{3}}{12} \right]=\frac{1}{12} \frac{M}{abc} [ab^{3}c+abc^{3}]=\frac{1}{12}M[b^{2}+c^{2}]
$$
$$
I_{22} = \frac{1}{12}M [a^{2}+c^{2}] 
$$
$$
I_{33} = \frac{1}{12} M(a^{2}+b^{2})
$$
$$
I_{12} = \int _{V}\rho(-x_{\alpha_{1}}x_{\alpha_{2}}) \, dV - \int \rho x_{1}x_{2} \, dV 
$$
$$
=-\rho \left[  \int\limits_{-c/2}^{c/2}  \, dx_{3} \int\limits_{-b/2}^{b/2} x_{2}  \, dx_{2} \int\limits_{-a/2}^{a/2} x_{1}  \, dx_{1}    \right]
$$
$$
=\rho c\left( \frac{1}{2}x_{2}^{2} |^{b/2}_{-b/2} \right) \left( \frac{1}{2} x_{1}^{2} |^{a/2}_{-a/2} \right)
$$
$$
=-\rho c \left[ \cancelto{ 0 }{ \frac{1}{2 } \frac{b^{2}}{4} - \frac{1}{2} \frac{b^{2}}{4} } \right] = \left[ \cancelto{0}{ \frac{1}{2} \frac{a^{2}}{4} -\frac{1}{2} \frac{a^{2}}{4}  }\right] = 0= I_{21}
$$
Similarly
$$
I_{13} = I_{31} = 0
$$
$$
I_{23} = I_{32} = 0 
$$
$$
\{I\} = \frac{1}{12}M 
\begin{pmatrix} 
b^{2}+c^{2} & 0 & 0 \\
0 & a^{2}+c^{2} & 0 \\
0 & 0 & a^{2}+b^{2}
\end{pmatrix}
$$
$$
T_{rot} = \frac{1}{2} \sum_{ij} 2\omega_{i}\omega_{j}
$$
Particular case where $\vec{\omega} = (0,0,\omega_{3})$
$$
=\frac{1}{2} \sum_{i=1}^{3} \sum_{j=1}^{3} \omega_{i}\omega_{j} I_{ij}
$$
$$
= \frac{1}{2}\sum^{3}_{i=1} \omega_{i} [ \cancelto{ 0 }{ \omega_{1}I_{i1} } + \cancelto{ 0 }{ \omega_{2}I_{i 2} } + \omega_{3}I_{i 3}]
$$
$$
=\frac{1}{2} I_{33} \omega_{3}^{2}
$$

The dzhanibhanibekov effect or tennis racket theorem arises from this ! very cool videos. 

