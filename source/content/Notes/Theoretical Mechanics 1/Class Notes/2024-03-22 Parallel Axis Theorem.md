---
dg-publish: true
---
## Steiner's Parallel Axis Theorem
It states 
$$
I_{ij} = J_{ij} - M(a^{2} \delta_{ij} - a_{i}a_{j})
$$
Where $I_{ij}$ is the center-of-mass inertia tensor and $J_{ij}$ is the inertia tensor a distance $a$ away from  $I_{ij}$ . This does require that the axes of the two coordinate systems are parallel.

#### Example: Homogeneous Cube with origin at the corner of the cube. 

$$
\{\mathbf{I}\} = Mb^{2} \begin{pmatrix}
\frac{2}{3} & -\frac{1}{4} & -\frac{1}{4}   \\
-\frac{1}{4} & \frac{2}{3} & -\frac{1}{4}   \\
-\frac{1}{4} & -\frac{1}{4} & \frac{2}{3} \\
\end{pmatrix} = J_{ij}
$$

![[Pasted image 20240322101500.png]]
Want origin at cube center 
$I_{ij}=?$

$$
\vec{a} = \left( \frac{b}{2}, \frac{b}{2}, \frac{b}{2} \right)
$$
$$
a=\sqrt{ \left( \frac{b}{2} \right)^{2}+ \left( \frac{b}{2} \right)^{2}+ \left( \frac{b}{2} \right)^{2}} = \sqrt{ \frac{3b^{2}}{4} }
$$
$$
I^{cc}_{ij}= J_{ij} - M(a^{2} \delta_{ij} - a_{i}a_{j})
$$
$$
I_{11}^{cc} =J_{11} - M(a^{2}-a_{1}a_{1})
$$
$$
= \frac{2}{3} Mb^{2} - M\left( \frac{3b^{2}}{4} - \frac{b^{2}}{4}  \right) = \frac{1}{6} Mb^{2}
$$
$$
I_{12}^{cc} = J_{22} - M(0-a_{1}a_{2})
$$
$$
=\frac{1}{4}Mb^{2} - M\left( -\frac{b^{2}}{4} \right)=0
$$
Continue to find the rest
$$
\{\mathbf{I}\} = \frac{1}{6}Mb^{2} \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix}
$$

## Euler Angles

Transformation from one coordinate system to another through rotation 

Represented as $\vec{x}=\lambda \vec{x}'$
Where $\lambda$ is the rotation matrix comprised of 3 independent angles 

Many choices but we use Euler's angle $\phi,\theta,\psi$
Start in x' system and convert to x system in the following way

> Remember the paul/emily/nate spinny coordinate thing

![[Pasted image 20240322101535.png]]

$$
\lambda_{\phi}= \begin{pmatrix}
\cos \phi & \sin \phi & 0 \\
-\sin \phi & \cos \phi & 0 \\
0 & 0 & 1
\end{pmatrix}
$$
$$
\vec{x}'' = \lambda_{\phi} \vec{x}'
$$
So we have rotation in the $x_{1}'-x_{2}'$ plane

Spun $\phi$ around $x_{3}'$ axis 
counterclockwise rotation 

Next rotation counterclockwise around $x_{1}''$ axis through angle $\theta$ 

![[Pasted image 20240322101559.png]]

![[Pasted image 20240322101624.png]]

$$
\lambda_{\theta} = \begin{pmatrix}
 1 & 0 & 0 \\
0 & \cos\theta & \sin \theta  \\
0  & -\sin\theta & \cos\theta
\end{pmatrix}
$$
$$
\vec{x} ''' = \lambda_{\theta} \vec{x}''
$$
Finally rotate $\psi$ around $x_{3}'''$
> fig 5 


Combine to get
$$
\vec{x} = \lambda_{\psi} \vec{x}''' = \lambda_{\psi}\lambda_{\theta}\vec{x}'' = \lambda_{\psi} \lambda_{\theta}\lambda_{\phi}\vec{x}'
$$
$$
\lambda = \lambda_{\psi}\lambda_{\theta}\lambda_{\phi}
$$
Rotation matrix is the following: 
$$
\begin{matrix}
\lambda_{11} = \cos \psi \cos \phi - \cos \theta \sin \phi \sin \psi \\
\lambda_{21} = -\sin \psi \cos \phi-\cos\theta \sin \phi \cos \psi \\
\lambda_{31} = \sin\theta \sin \phi \\
\lambda_{12} = \cos \psi \sin \phi  + \cos \theta \cos \phi \sin \psi \\
\lambda_{22} = - \sin \psi \sin \phi + \cos\theta \cos \phi \cos \psi \\
\lambda_{23} = -\sin\theta \cos \phi \\
\lambda_{13} = \sin \psi \sin \theta  \\
\lambda_{23} = \cos \psi \sin\theta \\
\lambda_{33} = \cos\theta
\end{matrix}
$$
At this point we could get into a discussion of rigid body Lagrangian problems using Euler rotation and Euler equations. We however will not do such things. 
 