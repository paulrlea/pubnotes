# Linear Algebra
### Coupled Linear Equations
- Think Chicken and Rabbit problem
- Can be modeled with matrices and solved with matrix operations
### Indices
- Basically a way to "choose" an element of a matrix.
- Determines rank of tensor later on. Rank three tensor has 3 indices, etc. 
### [[@Spring2024/Physics/Math Background/Kronecker delta|Kronecker delta]]

$$
\delta_{ij} \begin{cases}
0 \text{ if } i\neq j \\
1 \text{ if } i = j 
\end{cases}
$$
### Repeated index summation
- If indices on one side are repeated, it is understood to be a sum over that index.

### Transpose 
$$
M_{ij} \to M_{ji}
$$
### Trace
- Sum of diagonal Elements 
- Later, comes from collapsing two indices

$$
\mathrm{Tr}M = M_{ii}
$$
### Inverse
- Defined as what the matrix has to be multiplied as to be the identity
$$
m^{-1} = \frac{1}{m}
$$
or 
$$
m^{-1}m = I
$$
### Inverting a matrix
- sucks ass
$$
M^{-1} = \frac{1}{D} \begin{pmatrix}
d & -b \\
-c & a
\end{pmatrix}
$$
### Determinant and Laplace Expansion 
- Determinant is given by many ways. these ways are called Laplace expansion
$$
\det M = \det M^{T}
$$
### Hermitian Conjugation
- dagger
- defined by the following
$$
(M^{*}) ^{T} = (M^{T})^{*} = M^{\dagger}
$$

A matrix/tensor where 
$$
M^{T} = M 
$$
is called **Symmetric**. A matrix whose transpose is equal to its negative is called asymmetrical
$$
M^{T} = -M
$$

A matrix where
$$
M^{\dagger} = M 
$$
is called hermitian
Very important for later...

### Invertible Matrices 

- If the determinant is 0, the matrix is not invertible

### Eigenvectors and Eigenvalues 

- Eigenvectors = eigenstates = eigenfunctions

- Each eigenvector/state/function has a corrosponding eigenvalue

This is given by
$$
M \vec{\psi} = \lambda \vec{\psi}
$$

### Hermitian and Real symmetric matrices


- All eigenvalues of a hermitian matrix are real
- Different eigenvectors are complex orthogonal

### Scalar Products in a complex vector space 
- Scalar product of two complex vectors is defined as 

$$
\phi ^{\dagger} \psi = \sum ^{n}_{i=1} \phi^{*}_{i} \psi_{i}
$$
- The length squared of a complex vector is real and positive. 

### Upper/Lower notation 
- Lower and upper indices sum together
-  Only matters for vectors? tensors? idfk

### Diagonalization of Matrices
- Put the eigenvalues along the diagonal
- Or do the whole thing: 
$$
S^{-1}MS = \Lambda
$$

### Simultaneously Diagonalizable
- When matrices A and B are diagonalizable using the same S matrices.


### Direct Product of matrices
Direct product of two matrices given by: 
$$
M = C \otimes \Gamma
$$
$$
M_{\alpha\alpha, \alpha\beta} = C_{ab} \Gamma_{\alpha\beta}
$$
### Dirac Bra-Ket notation
- $\ket{\alpha}$ Represents an eigenstate $\psi_{\alpha}$
- The corresponding $\bra{\alpha}$ represents the complex conjugate of that eigenstate
- Orthonormality is represented by $\left< b|a \right> = \delta_{ba}$  
- Useful because it does not depend on base and is cleaner 


# Groups
- Groups! A group is a set of entities that can be composed together and remain within the set. The set of all relations between group elements is called the multiplication of the group.
- Axioms of a group 
	1. Associativity. Composition is associative 
	2. Existence of an identity, where the identity element multiplied by any element is that element 
	3. Existence of the inverse, where any group element G has to have a corresponding $G^{-1}$ that satisfies the relationship $GG^{-1} =I$/

- Commutation is not required, if it occurs, then the group is known as abelian
- Existence of the inverse implies that all transformations can be undone

Group examples:
- Rotations in 3d space. Denoted by rotation matrices that swap two basis vectors. Don't commute in 3d.
	- They commute in 2d!
- Permutation group $S_{n}$, which rearranges an ordered set of $N$ objects, which we can name arbitrarily. For example, $S_{4}$ element could be written as 1->3, 2->4, 3->2 and 4->1, and the group $S_{4}$ has 4! elements, so 24
- Even permutations form groups known as $A_{n}$. Even permutations are half of the associated odd permutations, so $A_{4}$ would have 12 elements.
- Group $Z_{n}$ is the n number of roots of 1

There are many more examples of groups. These are page 42 of the text. 


### Subgroups:
- This is pretty easy. A group, contained within another group, that satisfies all the requirements of a group.
- Example:
$$
A_{n} \subset S_{n}
$$
### Cyclic subgroups
- For any finite group, if you take an element and multiply it by itself over and over, you'll eventually end up at the identity. This is a cyclic subgroup denoted by $Z_{k}$ for k elements

### Lagrange's Theorem
- Groups with $n$ elements must have a subgroup with m elements that satisfies the relation $\frac{n}{m}$ is an integer number

### [[Direct product]] of groups
- Denoted as 
$$
H \equiv F \otimes  G
$$
- Consists of the elements $(f,g)$
Properties
$$
(f,g)(f',g') = (ff',gg')
$$
Identity given by 
$$
(II)
$$
inverse of $(f,g)$ is $(f^{-1}, g^{-1})$. $H$ has $mn$ elements if F has n elements and G has m elements. 
### Klien's Vierergruppe $V$
 - Sounds super cool
$$
Z_{2} \otimes  Z_{2}
$$
- Square of any element is identity

### Multiplication tables
- Discussed above. Multiply every element by every element. 
- Once and only once should a group element show up in any row. 

### [[Homomorphisims]] and [[Isomorphisms]]
#### Homomorphisims:
- Keep multiplication structure
$$
f(g_{1}) f(g_{2}) = f(g_{1}g_{2})
$$
#### Isomorphisms: 
- Both keeps multiplicative structure and also is 1-1? Means that they are the same group. Still fuzzy on the difference. 

## [[Finite Groups ]]
### Permutation Groups and Cayley's Theorem
- Permutation group denoted as $S_{n}$, with even group denoted as $A_{n}$
- All finite groups are isomorphic to a subgroup of $S_{n}$
### Cycles and Transpositions
- You can denote a permutation using the following notation: 
$$
g = \begin{pmatrix}
1 & 2 & 3 & 4 & 5  \\
4 & 1 & 5 & 2 & 3
\end{pmatrix}
$$
- This represents a group element that maps 1->4, 2-> 1 etc etc.
- Also can be written as (142)(35). This is a more compact way to write this element, denoting a mapping of 1->4, 4->2, 2->1 and etc. for the second cycle. 
- A cycle is a circular permutation of elements $a_{1}$ to $a_{k}$ in a cycle of k length. 
- All permutations can be written as cycles
- 1 cycles are trivial

### Multiplying Permutations
- All permutations can be written as a product of 2-cycles, because you can make any per-mutative 'map' by exchanging two objects at a time 
- Permutations are odd or even depending if they decompose into even or odd numbers of 2-cycles/exchanges/transpositions respectively.
### Identity sqrt
- Any even permutation has to have at least one element that squares to the identity
### [[Equivalence Classes]]
- We have elements that can be considered essentially the same. An example is a 17 degree rotation around the x vs z axis. We can just call the x axis the z axis. 
- Example: (132) and (123) are in the same equivalence class, because we could rename 3 -> 2 and 2-> 3. We can represent this with the following: 
$$
(23)^{-1}(123)(23) = (32)(12)(23)(32) = (32)(21) =(321) = (132)
$$
Where we use the rules we just learned to multiply them 
Class properties: 
- Abelian Groups have every element in their own class
- The identity is always in its own class

## [[Lie Algebra]]
- Based on the concept of infinitesimal rotation. You can rotate something by rotating it a little bit at a time 
$$
R(\theta) \approx I + A
$$
Where $\theta$ is an infinitesimal angle. A must be anti symmetric, and there is only one such matrix that is 2x2. 

$$
J = \begin{pmatrix}
0 & 1  \\
-1 & 0
\end{pmatrix}
$$
This is called a generator, the generator of the rotation group. 
- A vector transforms like a vector under rotations
### Higher dimensional Spaces
- 3d trig sucks. Lie's approach sucks less. Rotations are defined as the linear transformations that leave $ds^{2}$ unchanged. $ds^{2}$ is the "distance" between the 'origin' and the point being rotated. Given by the generalization of Pythagorean theorem 
$$
ds^{2} = \sum ^{N} _{i=1} (dx^{i})^{2} = (dx^{1})^{2} + (dx^{2}) ^{2} + \dots + (dx^{N})^{2}
$$
- The matrices, R, that satisfy this condition, as well as having a determinant of 1 (rotation not reflection), are called SO(N) where N is the dimensionality of the matrices
- These form a group. The product of two rotations is another rotation. 
- The generators for a N dimensional rotation group are the collection of all NxN antisymmetric matrices. 

As an example, any three dimensional rotation can be written as 
$$
R(\theta) = e^{\theta_{x}j_{x} + \theta_{y}j_{y}+ \theta_{z}j_{z}} = e^{\sum_{i}\theta_{i} j_{i}}
$$
For physics reasons, we multiply the generators by some multiple of the imaginary unit $i$ because that makes it hermitian, and we need hermitian matrices/operators to represent observable quantities. 

The [[Notes/Physics/Quantum Physics/Concepts/Commutation Relations|Commutation Relations]] between any two generator can be written as a linear combination of the generators. 

Lie groups are created from a group that is labeled by a set of continuous parameters. 

There are 
$$
\frac{1}{2}N (N-1)
$$
real, antisymmetric matrices in an N dimensional space.

# Representing Group Elements with Matrices


- Representation of a group element is denoted by the following:
$$
D(g_{1})D(g_{2}) = D(g_{1}g_{2})
$$
- The matrices represent the group elements. Representation Theory. Represent. tada
- The set of matrices $D(g)$ reflects/mirrors the multiplicative table of the group. 
![[Pasted image 20240626181728.png]]

- See page 90 in the textbook for some easy examples with elements from $S_{4}$
- Instead of 4 balls, we have 4 vectors now. 
- There always exists a trivial representation, $D(g) = 1$
- All groups we deal with can be represented by matrices
- Faithful vs Unfaithful representations 
	- Faithful representations are isomorphic and represents a 1-1 structure of the group

### Character is a function of class
- $D^{(r)}(g)$ is the representation $r$ of a group element $g$ 
- The character, $\chi^{r}$ of a representation is given by 
$$
\chi^{r}(g) \equiv \mathrm{Tr} D^{(r)}(g)
$$
- The trace of the group element representation matrix is equivalent to the character of the group element
- All elements of an equivalence class have the same character. 
- Character is a function of (equivalence) class 
- If $\chi'(c)=\chi(c)$ for all c, then the representations are the same
### Reducible and irreducible representations
- You can make an irreducible representation of any size by stacking representations along a diagonal of an "n" dimensional matrix. 
- The resulting matrix is known as being "block diagonal"
- We don't really care about reducible representations.
- We want to find out how many irreducible representations a given group has. That is the goal of representation theory.

