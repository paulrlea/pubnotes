# Reading Quick  Notes
- Rotations are basis of continuous group theory
- Example: 2d plane being rotated
- Rotation matrices acting on vectors 
- Invariance under linear transforms:
	- Using linear transformations, we get 2 orthogonal matrices, generating the group $O(2)$.
	- With Multiplication law $R(\theta_{1})R(\theta_{2}) = R(\theta_{1}+\theta_{2})$

## Reflections vs Rotations: 
- Reflection matrices have a determinant of -1, while rotations have a determinant of +1. (remember that matrices with det=1 are called special)

## Lie math
- Lie algebra has to do with infinitesimal rotations
- An infinitesimal rotation can be written as the sum of I and A, where A denotes an infinitesimal rotation of angle $\theta$
$$
R(\theta) \sim I + A
$$
- Applying the $R^{T}R=I$
$$
R^{T}R \approx (I+A)^{T}(I+A) = (I+A^{T}+A)=I
$$
- Therefore, A has to be anti-symmetric. $A^{T} = -A$, of the form 
$$
A=\mathscr{J} \theta
$$
where 
$$
\mathscr{J} = \begin{pmatrix}
0 & 1 \\
-1 & 0 
\end{pmatrix}
$$
This asymmetric matrix $\mathscr{J}$ is the "generator" of the rotation group in 2d
Given: 
$$
e^{x} = \lim_{ N \to \infty } \left( 1+\frac{x}{N} \right)^{N}
$$
Then for a finite angle: 
$$
R(\theta) = \lim_{ N \to \infty } \left( R\left( \frac{\theta}{N} \right) \right)^{N}
$$
Which is also equal to: 
$$
\lim_{ N \to \infty } \left( 1+\frac{\theta \mathscr{J}}{N} \right)^{N} = e^{\theta \mathscr{J}}
$$
$$
R(\theta) = e^{\theta \mathscr{J}}
$$

### Generalizing this to higher dimensions:
- Euler angles and other traditional ways to rotate things in 3d suck. Lie algebra is easier. 
- The rotation group in an N dimensional space is denoted by 
$$
SO(N)
$$
- Where "N" is the dimensionality of the space. 
- The rotation group for any space requires that $A$ is anti-symmetric. 

	There are 3 "generators" for 3 dimensional space. These $\neq$ the rotation matrices. 

Any rotation matrix in 3d space can be written as 
$$
A = \theta_{x} \mathscr{J}_{x} +\theta_{y}\mathscr{J}_{y} + \theta_{z}\mathscr{J}_{z}
$$
And then therefore any rotation can be written as:
$$
R(\theta) = e^{A}
$$

	N Dimensional space rotations? How many antisymmetric matrices?

- Spherical symmetry is heavily based in $SO(3)$

## Lie Algebra 
- The commutator represents the how much two rotations commute or don't commute
	- Generators for $SO(3)$ can be denoted by $j_{i}s$
	- Does not equal lie groups.
	- Lie Algebra is closed under commutation, while lie groups follow the composition rules of group theory. 

## Higher Dimensional Rotations
- the number of asymmetric rotations is given by 
$$
\frac{1}{2} N (N-1)
$$
 for an nth dimensional rotation

