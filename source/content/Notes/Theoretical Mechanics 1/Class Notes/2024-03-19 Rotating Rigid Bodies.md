---
dg-publish: true
---
See video: Ellipsoids and the Bizarre Nature of Rotating Bodies
Very good resource on the weirdness of rotating bodies

## Continued Rigid Body and Inertia Tensors
Uniform Solid Cube Example:
Given length $a$, mass $M$, and the corner of the cube at the origin of the system

>> figure 1 here 

[[@Spring2024/Physics/Math Background/Kronecker delta]] review
$$
	I_{ij} = \int _{v} p(\vec{r}) \left( \delta_{ij}\sum_{k} x_{ k}^{2}-x_{ i} x_{ j} \right) \, dV
$$
Finding $I_{11}$ 
$$
I_{11} = \int _{V} \rho(\vec{r}) (y^{2}+z^{2}) \, dV
$$
We can pull out $\rho$ because the square is uniform
$$
I_{11} = \rho\iiint\limits_{0}^{a} (y^{2}+z^{2})  \, dxdydz
$$
Performing the integration: 
$$
=\rho \left[ \int\limits_{0}^{a}  \, dx \int\limits_{0}^{a} y^{2} \, dy \int\limits_{0}^{a}  \, dz + \int\limits_{0}^{a}  \, dx \int\limits_{0}^{a}  \, dy \int\limits_{0}^{a} z^{2} \, dz       \right]
$$
$$
\rho\left[ a\left( \frac{1}{3}y^{3}  |^{a}_{0}\right) +a\left( \frac{1}{3}z^{3}|^{a}_{0} \right)\right]
$$
$$
\rho a\left[  \frac{1}{3}a^{3}a + \frac{1}{3} a^{3}a \right] = \frac{2}{3}\rho a^{5}
$$
Because $M = \rho a^{3}$

$$
I_{11} = \frac{2}{3} Ma^{2} 
$$

Now finding the $I_{22}$ component 

$$
I_{22 } = \int\limits_{V}^{ }  \rho(x^{2}+z^{2}) \, dV 
$$
$$
I_{22} = I_{33} = \frac{2}{3}Ma^{2}
$$
This can be proven with symmetry or math

$$
I_{13} = \iiint\limits_{0}^{a} \rho xz  \, dxdydz
$$
$$
 - \rho \int\limits_{0}^{a} x \, dx \int\limits_{0}^{a}  \, dy \int\limits_{0}^{a} z \, dz  = \rho\left( \frac{1}{2}x^{2} |^{a}_{0} \right)a\left( \frac{1}{2}z^{2} |^{a}_{0} \right)
$$
$$
= -\rho   \frac{1}{2}a^{2} \cdot a \cdot \frac{1}{2} a^{2} = -\frac{1}{4}\rho a^{5}
$$
$$
I_{31} = -\frac{1}{4}Ma^{2}
$$
$$
I_{31} = I_{13}=I_{23} = I_{32})
$$
$$
\{\mathbf{I}\} =  \begin{bmatrix}
\frac{2}{3} Ma^{2}  &  -\frac{1}{4}Ma^{2} &  -\frac{1}{4}Ma^{2} \\
-\frac{1}{4}Ma^{2} & \frac{2}{3}Ma^{2} & -\frac{1}{4}Ma^{2} \\
-\frac{1}{4}Ma^{2} & -\frac{1}{4}Ma^{2} & \frac{2}{3}Ma^{2}
\end{bmatrix}
$$
Or simplified:
$$
\{\mathbf{I}\} = \frac{1}{12} Ma^{2} \begin{bmatrix}
8 & -3 & -3 \\
-3 & 8 & -3 \\
-3 & -3 & 8
\end{bmatrix}
$$
# Angular Momentum 
Previously in physics 1, angular momentum 
$$
\vec{L}=I\vec{\omega}
$$
and Angular kinetic energy 
$$
T = \frac{1}{2} I \omega^{2}
$$
In the past, we have treated the moment of inertia as a scalar, but that is only true in a special case where $\vec{L} \parallel \vec{\omega}$ 

In general: 
$$
\vec{L} = \{\mathbf{I}\} \vec{\omega}
$$
or 
$$
L_{i} = \sum_{j} I_{ij} \omega_{j}
$$
$$
\begin{pmatrix}
L_{1} \\
L_{2} \\
L_{3} 
\end{pmatrix} = \begin{pmatrix}
I_{11} & I_{12} & I_{13}  \\
I_{21} & I_{22} & I_{23}  \\ 
I_{31} & I_{32} & I_{33}  \\
\end{pmatrix} \begin{pmatrix}
\omega_{1} \\
\omega_{2} \\
\omega_{3}
\end{pmatrix}
$$
$$
\begin{matrix}
L_{1} = I_{11} \omega_{1} +I_{12} \omega_{2} & + I_{13} \omega_{3} \\
L_{2} = I_{21} \omega_{1} +I_{22} \omega_{2} & + I_{23} \omega_{3} \\
L_{1} = I_{31} \omega_{1} +I_{32} \omega_{2} & + I_{33} \omega_{3}
\end{matrix}
$$
Angular momentum of a rigid body with respect to the origin of rotating coordinate system. 
$$
\vec{L} = \sum_{\alpha} \vec{r}_{\alpha} \times \vec{P}_{\alpha}
$$

$$
\vec{L} = \sum_{\alpha} m_{\alpha} ( \vec{r}_{\alpha} \times (\vec{\omega} \times \vec{r}_{\alpha}))
$$
$$
=\sum_{\alpha} m_{\alpha} [r^{2}_{\alpha} \vec{\omega}- \vec{r}_{\alpha}(\vec{r}_{\alpha}\cdot\vec{\omega})]
$$
Where 
$$
\vec{P}_{\alpha} = m_{\alpha} \vec{v}_{\alpha} = m_{\alpha} \vec{\omega} \times \vec{r}_{\alpha}
$$
and 
$$
\vec{r}_{\alpha} = \sum_{K} x_{\alpha k} ^{2}
$$
$$
\omega_{i} = \sum_{j} \omega_{j} \delta_{ij}
$$
the $i^{th}$ component only remains due to the [[@Spring2024/Physics/Math Background/Kronecker delta]]

$$
L_{i} = \sum_{\alpha} m_{\alpha} \left[ \omega_{i} \sum_{k} x^{2}_{\alpha k}- x_{\alpha i} \sum_{j} x_{\alpha j} \omega_{j} \right]
$$
$$
= \sum_{\alpha} m_{\alpha} \sum_{j}\left( \omega_{j}\delta_{ij}\sum_{k}x_{\alpha k}^{2} - \omega_{j}x_{\alpha i} x_{\alpha j} \right)
$$
$$
=\sum_{j} I_{ij} \omega_{j}
$$
$$
L_{i} = \sum_{j} I_{ij }\omega j
$$
Multiply by 1... ($\frac{1}{2}\omega_{i}$ on both sides)
$$
\frac{1}{2}L_{i}\omega_{i} = \frac{1}{2} \sum_{ij} I_{ij} \omega_{j}\omega_{i} = T_\text{rot}
$$
$$
T_\text{rot} = \frac{1}{2}\vec{\omega} \{\mathbf{I}\} \vec{\omega}
$$

# Principle Axis of Inertia 
For the case when none of the components of $\{\mathbf{I}\}$ are 0 then the calculation of energy and angular momentum can be annoying/complicated. (annoying if simple, etc)

Instead, if we assume our inertia tensor only has non-zero diagonal elements such that 
$$
\{I\} = \begin{pmatrix}
I_{11} & 0 & 0 \\
0 & I_{22} & 0 \\
0 & 0 & I_{33}   \\
\end{pmatrix}
$$
$$
I_{ij} = I _{ij} \delta_{ij}
$$
Much easier. Would be nice if this is the case. Examples of how nice everything is:
$$
L_{i} = \sum_{j} I_{ij}\omega_{j} \to \sum_{j} I_{ij} \delta_{ij} \omega_{j} = I_{ii} \omega_{i}
$$
$$
\begin{pmatrix}
L_{1} \\
L_{2} \\
L_{3}  \\
\end{pmatrix} = \begin{pmatrix}
I_{11}  &  0  & 0 \\
0 & I_{22} & 0  \\
0 & 0 & I_{33} \\
\end{pmatrix} \begin{pmatrix}
\omega_{1} \\
\omega_{2} \\
\omega_{3}
\end{pmatrix} =\begin{pmatrix}
I_{11} \omega_{1} \\
I_{22} \omega_{2} \\
I_{33} \omega_{3} \\
\end{pmatrix}
$$
$$
T_\text{rot} = \frac{1}{2} \sum_{ij} I_{ij} \omega_{i}\omega_{j} \to \frac{1}{2} \sum_{ij} \delta_{ij} \omega_{i} \omega_{j} = \frac{1}{2} \sum_{i} I_{ii} \omega_{i}^{2}
$$

How do we get here?

The diagonal elements are the principal moments of inertia and the principle axes of inertia are the coordinates (axes) used such that $\{\mathbf{I}\}$ is diagonal. 

Since we can pick the coordinate system and axes, we can make selections such that we diagonalize $\{\mathbf{I}\}$ 

There are a few ways to go about this: 

Method 1:
Simply choose the right axes such that there is symmetry about the axes. Just literally pick better axes. 

Method 2:
If no obvious symmetries exist, pick arbitrary coordinate system, then diagonalize $\{\mathbf{I}\}$

The eigenvalues of $\{\mathbf{I}\}$ in the arbitrary coordinate system are the principal moments of inertia and the corresponding eigenvectors are the principal axes. The inertia tensor should always have real eigenvalues

For a matrix $A$: 
$$
A\vec{v} = \lambda \vec{v}
$$
Where $\lambda$ are the eigenvalues and $\vec{v}$ are eigenvectors

for an $n\times n$ matrix, has n eigenvalues $(\lambda_{n})$ and eigenvectors $\vec{v}_{n}$ 

1) So $(A-\lambda  \mathbf{I})\vec{v} = 0$
So for a non-trivial this is true when $\det(A-\lambda \mathbf{I})=0$
Use this to solve for $\lambda_{n}$
$$
(A-\lambda_{n} \mathbf{I}) \vec{v}_{n} =0
$$
In which $\mathbf{I}$ is the [[identity matrix]]
2) Use this to construct the matrix $P$ from the eigenvectors 
$$
P = \begin{pmatrix}
v_{1x} & v_{2x}  &  v_{3x} \\
v_{1y} & v_{2y}  &  v_{3y} \\
v_{1z} & v_{2z}  &  v_{3z}
\end{pmatrix}
$$
3) Find $P^{-1} : PP^{-1} = \mathbf{I}$
4) Diagonalize A: $B = P^{-1}AP$

