# Why Group Theory 

- Symmetries are described by groups
- Group theory implicitly underlines all of physics

## Poincare Invariance of the Action 
Newtons laws are frame-invariant. The experiment will yield the same results regardless of inertial reference frames. [[2024-01-16  Reference Frames]] for more. 
- Translations work in 3 axes and time, so 4 total. Going from one **place** to another
- Rotations mix one coordinate and another. (z rotation: x <-> y)
- Momentum is conserved over space, while energy is conserved over time. 
- Boosts transform from one inertial reference frame to another. 

### Poincare Invariance
The Poincare group has 10 operations. The Lorentz group has 8 operations, including the boosts.

> All equations in physics **have** to be Poincare invariant. 

## Group theory and the standard model

Group theory implicitly underlies the interactions of the standard model. The following group governs the standard model: 
$$
Su(3) \otimes Su(2) \otimes Su(1)
$$
The first term represents the Strong force. The second represents the electroweak force. The third breaks the electroweak force into the electric and weak forces. By the end of the course, we will fully understand this group. 


# Linear Algebra
The linear algebra will be mostly regarding matrix operations.
## Matrix multiplication 
With a matrix $M$, we can transform a vector as follows

$$
M = \begin{pmatrix}
a & b  \\
c & d 
\end{pmatrix}
$$
$$
M \vec{x} = \vec{u} \equiv \begin{pmatrix}
a & b \\
c & d  \\
\end{pmatrix} \begin{pmatrix}
x \\
y
\end{pmatrix} = \begin{pmatrix}
ax + by \\
cs+dy
\end{pmatrix} \tag{1}
$$
We also take a matrix N where: 
$$
N\vec{u} = \vec{p}
$$
and 
$$
\vec{p} = N\vec{u}  = NM\vec{x} = P\vec{x} 
$$
with 
$$
P = NM
$$

## Series and Sums Convention
Elements of a matrix $M$ can be represented by the following: 
$$
M_{ij}
$$
where $i$ represents the column index, and $j$ represents the row index.

Using the above notation, we can rewrite the vector transformations as the following: 
$$
n_{i} = m_{ij} x_{j}
$$
This is using Einstein index summation notation, and is equivalent to writing:
$$
\sum_{j}^{n} m_{ij}x_{j}
$$
The sum of all products of elements of m and x over j

The indices on both sides have to "match". In the above example, There is only $i$ left on both sides after summing. Anything summed "goes away"

For 2 $n\times m$ matrices: 

$$
p_{ij} = n_{ik}m_{kj}
$$
Where k is known as the dummy index. 

## Other matrix operations
### Transpose: 
Transpose of a matrix is given by: 
$$
(M^{T})_{ij} = M_{ji}
$$
Properties of transpose: 
$$
(MN)^{T} = N^{T}M^{T}
$$
### Trace: 
The trace is the sum along the diagonal. 
$$
\text{tr}M = m_{ii} = \sum_{i} m_{ii}
$$
$$
\text{tr} \begin{pmatrix}
a & / & /  \\
/ & b & / \\
/ & / & c \\

\end{pmatrix}
= a+b+c
$$
All matrices we care about are square, so taking trace is pretty easy. 
Product of matrices is non-commutative. But the traces are the same: 
$$
\text{tr}(AB) = \text{tr}(BA)
$$
For 3 matrix multiplication, they have to be cyclic-ly commuting. 
$$
\text{tr}(ABC) = \text{tr}(BCA) =\text{tr}(CAB) \neq \text{tr}(ACB)
$$
### Inverse: 
$$
MM^{-1} = I = M^{-1}M
$$
And
$$
\vec{x} = I\vec{x} = MM^{-1} \vec{x} = M^{-1}\vec{u}
$$
See matrix operations for relation between u and x

### Determinant: 
$$
M^{-1} = \frac{1}{\mathscr{D}} \begin{pmatrix}
d & -b \\
-c & a
\end{pmatrix}
$$
With 
$$
\mathscr{D} = ad-bc
$$
Properties: 
1. Row scalar multiplication multiplies determinant by scalar 
2. Row scalar multiplication and subtract from another row doesn't change determinant
3. If any 2 rows are identical determinant is 0 
4. Interchange any 2 rows -> determinant changes sign
5. All also true for columns 
$$
\det M = \det M^{T}
$$
## Eigenvectors and Eigenvalues
$$
M\vec{\psi} = \lambda \vec{\psi}
$$
Where $\lambda$ is an [[Eigenvalue]] and $\vec{\psi}$ is an Eigenvector. 

Only non-trivial solutions are given by 
$$
\det| M - \lambda I| = 0
$$
## Hermitian Matrices

Complex conjugate: 
$$
(M^{*}) _{ij} = M_{ij} ^{*}
$$
Hermitian conjugate: 
$$
(M^{*})^{T} = (M^{T})^{*} = M^{^{\dagger}}
$$
If 
$$
M^{\dagger} = M
$$
Then M is hermitian. 

Eigenvalues of hermitian matrices are real, and eigenvectors are orthogonal

## Scalar Products 
For a complex vector space: 
$$
(\psi, \phi)\to \psi^{*} \phi
$$
$$
\phi ^{\dagger} \psi  = \phi^{*^{t}} \psi = \sum_{i} \phi_{i} ^{*} \psi
$$
Notation for complex vectors: 
Given a vector $\psi^{i}$ (complex), there is a vector $\psi^{i*}\equiv \psi_{i}$. Complex conjugate flips position of index.

Scalar products: 
$$
\phi^{*}\psi=\phi_{i}\psi^{i}
$$
Diagonalizing a matrix via a similarity transform: 
$$
S^{-1}MS = diag(\lambda_{1}, \lambda_{2}\dots \lambda_{k})
$$
See book for more. 

## Degrees of freedom
A $n\times n$ complex matrix has $2n^{2}$ degrees of freedom. Each element has 2 components, independent of each other. 

A hermitian matrix has $n^{2}$ degrees of freedom.

$$
2n^{2} - \left( n+2 \left( \frac{1}{2} \right)n(n-1) \right) = n^{2}
$$


