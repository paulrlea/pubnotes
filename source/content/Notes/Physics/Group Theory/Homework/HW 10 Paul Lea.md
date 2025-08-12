Problem 1 N9.3
The contribution to the anomaly by a given irreducible representation is determined by the trace of the product of a generator and the anti-commutator of two generators, namely, $\mathrm{Tr} T^{A}\{T^{B}T^{C}\}$ Here T A denotes a generator of the gauge group G. Show that for G = SU (5), the anomaly cancels between the $5^{*}$ and the 10. Note that for SU (N), we can, with no loss of generality, take A, B, and C to be the same, so that the anomaly is determined by the trace of a generator cubed (namely, $\mathrm{Tr} T^{3}$ ). It is rare that we get something cubed in physics, and so any cancellation between irreducible representations can hardly be accidental.

Easiest to use diagonal generator. 
$$
T = \text{diag} \left( \frac{1}{3}, \frac{1}{3}, \frac{1}{3},-\frac{1}{2},-\frac{1}{2} \right)
$$
Taking this diagonal generator, we evaluate the trace of the generator cubed in the 5* dimensional representation. 

All entries are real: (multiply by 6)
$$
T^{*} =\text{diag} \left(2,2,2,-3,-3 \right)
$$
Cubing this matrix:
$$
T^{*3} = \text{diag} \left( 8,8,8,-27,-27\right)
$$
Taking the trace: 
$$
\mathrm{Tr}(T^{*3}) = -30
$$
Now for the 10-dimensional representation: 
Basis for 10-d representation: 
$$
(1,2),(1,3),(1,4),(1,5),(2,3),(2,4),(2,5),(3,4),(3,5),(4,5)
$$
Converting the 5-d diagonal matrix to a 10-d representation
$$
T_\text{10 d} = \text{diag}(d_{1}+d_{2},d_{1}+d_{3},d_{1}+d_{4},d_{1}+d_{5},d_{2}+d_{3},d_{2}+d_{4},d_{2}+d_{5},d_{3}+d_{4},d_{3}+d_{5},d_{4}+d_{5})
$$
$$
T_\text{10 d} = \text{diag}(4,4,-1,-1,4,-1,-1,-1,-1,-6)
$$
Cubing this diagonal matrix:
$$
T_\text{10 d}^{3} = \text{diag}(64,64,-1,-1,64,-1,-1,-1,-1,-216)
$$
Taking the trace:
$$
\mathrm{Tr} T^{3}_\text{10 d} = 3(64) - 222 = 192-222 = -30
$$

$$
30-(-30) = 0
$$

Problem 3 N9.3
Work out how the 3-indexed antisymmetric 10 dimensional tensor in SO(10) decomposes on restriction to $SO(4)\otimes SO(6)$. 

- 3 indexed antisymmetric 10-d tensor has 120 elements. 

- Symmetric tensor rep of SO(6) has 20 elements $\frac{1}{2} (6)(7)-1$ 
- Adjoint rep of SO(6) has 15 elements $\frac{1}{2}(6)(5)$
- The vector representation of SO(6) has 6 (obviously)
- Trivial representation has 1

- The vector representation of SO(4) has 4 elements
- The trivial representation has 1 element 
- Tensor product representations (3,1) and (1,3)



Decomposing
Using the following equation (credit Nate Laposky and Hannah Turner)
$$
\Lambda^3(V \oplus W) = \Lambda^3(V) \oplus \left(\Lambda^2(V) \otimes W\right) \oplus \left(V \otimes \Lambda^2(W)\right) \oplus \Lambda^3(W)

$$

We can plug in our representations: 
$$
\Lambda^3(10) = \Lambda^3(4,1) \oplus \left(\Lambda^2(4,1) \otimes (1,6)\right) \oplus \left((4,1) \otimes \Lambda^2(1,6)\right) \oplus \Lambda^3(1,6)
$$

And from this we can start pulling out our representations:
We have a (4,1) representation from $\Lambda^3(4,1)$
$$

$$
From $\left(\Lambda^2(4,1) \otimes (1,6)\right)$ we get 
$$
(6,6)
$$

From $\left((4,1) \otimes \Lambda^2(1,6)\right)$ we get 

$$
Λ^{2}(6)≅15 \to (4,15)
$$
From $\Lambda^3(1,6)$ we get the 20 dimensional representation of $SO(6)$
$$
(1,20)
$$


Decomposing
Using the following equation (credit Nate Laposky and Hannah Turner)
$$
\Lambda^3(V \oplus W) = \Lambda^3(V) \oplus \left(\Lambda^2(V) \otimes W\right) \oplus \left(V \otimes \Lambda^2(W)\right) \oplus \Lambda^3(W)

$$

We can plug in our representations: 
$$
\Lambda^3(10) = \Lambda^3(4,1) \oplus \left(\Lambda^2(4,1) \otimes (1,6)\right) \oplus \left((4,1) \otimes \Lambda^2(1,6)\right) \oplus \Lambda^3(1,6)
$$

And from this we can start pulling out our representations:
We have a (4,1) representation from $\Lambda^3(4,1)$
$$

$$
From $\left(\Lambda^2(4,1) \otimes (1,6)\right)$ we get 
$$
(6,6)
$$
From $\left((4,1) \otimes \Lambda^2(1,6)\right)$ we get 
$$
Λ^{2}(6)≅15 \to (4,15)
$$
From $\Lambda^3(1,6)$ we get the 20 dimensional representation of $SO(6)$
$$
(1,20)
$$

Taking this collection of representations, we can 
$$
120 \to (20,1) \oplus (15,4) \oplus (6,6) \oplus (1,4)
$$
$$
 \to (20,1) \oplus (15,4) \oplus (6,3) \oplus (6,3) \oplus (1,4)
$$
















