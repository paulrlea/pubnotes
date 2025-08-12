The spatial wavefunction for two identical particles where one is in the ground state and the other is in the first excited state of a particle in a one dimensional box of length L can be expressed as either a combination that is symmetric under exchange or antisymmetric. Calculate the probability that the position of the two particles finds them both in the left hand side of the box, that is 0<𝑥1<𝐿/2 and 0<𝑥2<𝐿/2, for each of these symmetry combinations. Carry out this calculation symbolically showing steps and then evaluate the probability.


This is the solution for a particle in a box
$$
\varphi(x) = \sqrt{ \frac{2}{L} } \sin\left( \frac{n\pi x}{L} \right)
$$
Where n is the energy level (starting with 1)

For 2 separate particles, we have 2 locations to assign variables to. We represent these with $x$ and $y$. 
We can set up the symmetric and asymmetric combinations for the case of the particles being on one side as follows: 

## Symmetric: 
$$
\int\limits_{0}^{L/2}\int\limits_{0}^{L/2} \frac{1}{2}\left( \frac{2}{L}\sin \frac{\pi x}{L}\sin \frac{2\pi y}{L} + \frac{2}{L}\sin \frac{\pi y}{L}\sin \frac{2\pi x}{L} \right)^{2} \, dx   \, dy
$$
We can simplify these integrals : 
$$
\int\limits_{0}^{L/2} \int\limits_{0}^{L/2} \frac{1}{2} \left( \frac{2}{L} \right)^{2} \left[ \sin\left( \frac{\pi x}{L} \right)\sin\left( \frac{2\pi y}{L} \right) \right]^{2} + \left[ 2 \sin \left( \frac{\pi x}{L} \right)\sin\left( \frac{2\pi x}{L} \right)\sin\left( \frac{\pi y}{L} \right)\sin\left( \frac{2\pi y}{L} \right) \right]\dots
$$
$$
+ \left[ \sin\left( \frac{\pi y}{L} \right)\sin\left( \frac{2\pi x}{L} \right) \right]^{2}  \, dx  \, dy
$$
This breaks down the integral into 3 separate integrals
$$
\frac{2}{L^{2}}\int\limits_{0}^{L/2} \int\limits_{0}^{L/2} \sin ^{2}\left( \frac{\pi x}{L} \right)\sin ^{2}\left( \frac{2\pi y}{L} \right) \, dx  \, dy \dots
$$
$$
+\frac{2}{L^{2}}\int\limits_{0}^{L/2} \int\limits_{0}^{L/2} \sin ^{2}\left( \frac{\pi y}{L} \right)\sin ^{2}\left( \frac{2\pi x}{L} \right) \, dx  \, dy\dots
$$
$$
+\frac{2}{L^{2}} \int\limits_{0}^{L/2} \int\limits_{0}^{L/2} \left[ 2 \sin \left( \frac{\pi x}{L} \right)\sin\left( \frac{2\pi x}{L} \right)\sin\left( \frac{\pi y}{L} \right)\sin\left( \frac{2\pi y}{L} \right) \right] \, dx  \, dy 
$$
We can evaluate these 3 integrals separately:
$$
\frac{2}{L^{2}}\int\limits_{0}^{L/2} \int\limits_{0}^{L/2} \sin ^{2}\left( \frac{\pi x}{L} \right)\sin ^{2}\left( \frac{2\pi y}{L} \right) \, dx  \, dy =\frac{1}{8}
$$
$$
\frac{2}{L^{2}}\int\limits_{0}^{L/2} \int\limits_{0}^{L/2} \sin ^{2}\left( \frac{\pi y}{L} \right)\sin ^{2}\left( \frac{2\pi x}{L} \right) \, dx  \, dy = \frac{1}{8}
$$
$$
\frac{2}{L^{2}} \int\limits_{0}^{L/2} \int\limits_{0}^{L/2} \left[ 2 \sin \left( \frac{\pi x}{L} \right)\sin\left( \frac{2\pi x}{L} \right)\sin\left( \frac{\pi y}{L} \right)\sin\left( \frac{2\pi y}{L} \right) \right] \, dx  \, dy = \frac{2}{a^{2}}\frac{8a^{2}}{9\pi^{2}} = \frac{16}{9\pi^{2}}
$$
Reassembling this integral, we get the following 
$$
\frac{1}{8} + \frac{1}{8} + \frac{16}{9\pi^{2}}
$$
$$
\frac{1}{4} + \frac{16}{9\pi^{2}}
$$
This gives us the probability to find the particles in the left hand side of the box in the symmetric case: 
$$
\approx0.43012654869
$$
## Asymmetric:
$$
\int\limits_{0}^{L/2}\int\limits_{0}^{L/2} \frac{1}{2}\left( \frac{2}{L}\sin \frac{\pi x}{L}\sin \frac{2\pi y}{L} - \frac{2}{L}\sin \frac{\pi y}{L}\sin \frac{2\pi x}{L} \right)^{2} \, dx   \, dy
$$
$$
\int\limits_{0}^{L/2} \int\limits_{0}^{L/2} \frac{1}{2} \left( \frac{2}{L} \right)^{2} \left[ \sin\left( \frac{\pi x}{L} \right)\sin\left( \frac{2\pi y}{L} \right) \right]^{2} - \left[ 2 \sin \left( \frac{\pi x}{L} \right)\sin\left( \frac{2\pi x}{L} \right)\sin\left( \frac{\pi y}{L} \right)\sin\left( \frac{2\pi y}{L} \right) \right]\dots
$$
$$
+ \left[ \sin\left( \frac{\pi y}{L} \right)\sin\left( \frac{2\pi x}{L} \right) \right]^{2}  \, dx  \, dy
$$
This breaks down the integral into 3 separate integrals 

$$
\frac{2}{L^{2}}\int\limits_{0}^{L/2} \int\limits_{0}^{L/2} \sin ^{2}\left( \frac{\pi x}{L} \right)\sin ^{2}\left( \frac{2\pi y}{L} \right) \, dx  \, dy \dots
$$
$$
+\frac{2}{L^{2}}\int\limits_{0}^{L/2} \int\limits_{0}^{L/2} \sin ^{2}\left( \frac{\pi y}{L} \right)\sin ^{2}\left( \frac{2\pi x}{L} \right) \, dx  \, dy\dots
$$
$$
-\frac{2}{L^{2}} \int\limits_{0}^{L/2} \int\limits_{0}^{L/2} \left[ 2 \sin \left( \frac{\pi x}{L} \right)\sin\left( \frac{2\pi x}{L} \right)\sin\left( \frac{\pi y}{L} \right)\sin\left( \frac{2\pi y}{L} \right) \right] \, dx  \, dy 
$$
We can evaluate these 3 integrals separately:
$$
\frac{2}{L^{2}}\int\limits_{0}^{L/2} \int\limits_{0}^{L/2} \sin ^{2}\left( \frac{\pi x}{L} \right)\sin ^{2}\left( \frac{2\pi y}{L} \right) \, dx  \, dy =\frac{1}{8}
$$
$$
\frac{2}{L^{2}}\int\limits_{0}^{L/2} \int\limits_{0}^{L/2} \sin ^{2}\left( \frac{\pi y}{L} \right)\sin ^{2}\left( \frac{2\pi x}{L} \right) \, dx  \, dy = \frac{1}{8}
$$
$$
-\frac{2}{L^{2}} \int\limits_{0}^{L/2} \int\limits_{0}^{L/2} \left[ 2 \sin \left( \frac{\pi x}{L} \right)\sin\left( \frac{2\pi x}{L} \right)\sin\left( \frac{\pi y}{L} \right)\sin\left( \frac{2\pi y}{L} \right) \right] \, dx  \, dy = \frac{2}{a^{2}}\frac{8a^{2}}{9\pi^{2}} = \frac{16}{9\pi^{2}}
$$
Reassembling this integral, we get the following 
$$
\frac{1}{8} + \frac{1}{8} - \frac{16}{9\pi^{2}}
$$
$$
\frac{1}{4} - \frac{16}{9\pi^{2}}
$$
This gives us the probability to find the particles in the left hand side of the box in the asymmetric case:
$$
\approx0.06987345131
$$










