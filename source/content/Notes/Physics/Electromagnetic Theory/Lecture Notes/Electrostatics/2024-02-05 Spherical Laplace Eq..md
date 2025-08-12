---
dg-publish: true
---
[[Laplace's equation]]
$$
\vec{\nabla}^{2} = 0
$$
Laplace equation in [[Spherical Coordinates]]
$$
\vec{\nabla}^{2}V ( r,\theta,\phi) = \frac{1}{r^{2}} \frac{ \partial  }{ \partial r } \left( r^{2}\frac{ \partial V }{ \partial r }  \right) + \frac{1}{r^{2}\sin\theta}\frac{ \partial  }{ \partial \theta }\left( \sin\theta \frac{ \partial V }{ \partial \theta }  \right) + \frac{1}{r^{2}\sin ^{2}\theta}\frac{ \partial^{2} V }{ \partial \phi^{2} } =0
$$
We will only deal with cases that involve azimuthal symmetry
$$
\frac{ \partial V }{ \partial \phi } =0
$$
Use separation of variables 
$$
V(r,\theta)= R(r)\Theta(\theta)
$$
$$
\frac{d}{dr} \left( r^{2} \frac{ \partial R }{ \partial r }  \right)-n(n+1)R = 0
$$
$$
\frac{ \partial  }{ \partial \theta } \left( \sin \frac{ \partial \Theta }{ \partial \theta } + n(n+1) \sin\theta \right) = 0
$$
Solution to these: [[Legendre Polynomials]]


Examples: 
Suppose the potential is a constant V0 over the surface of the sphere. Use the results of Ex. 3.6 and Ex. 3.7 to find the potential inside and outside the sphere. (Of course, you know the answers in advance—this is just a consistency check on the method.

$$
\vec{\nabla}^{2}V ( r,\theta,\phi) = \frac{1}{r^{2}} \frac{ \partial  }{ \partial r } \left( r^{2}\frac{ \partial V }{ \partial r }  \right) + \frac{1}{r^{2}\sin\theta}\frac{ \partial  }{ \partial \theta }\left( \sin\theta \frac{ \partial V }{ \partial \theta }  \right) + \frac{1}{r^{2}\sin ^{2}\theta}\frac{ \partial^{2} V }{ \partial \phi^{2} } =0
$$
$$
\frac{ \partial V }{ \partial \theta } = 0;  \ \ \frac{ \partial V }{ \partial \phi }  =0
$$
$$
\vec{\nabla}^{2}V ( r,\theta,\phi) = \frac{1}{r^{2}} \frac{ \partial  }{ \partial r } \left( r^{2}\frac{ \partial V }{ \partial r }  \right) 
$$
$$
\frac{1}{R} \frac{d}{dr}\left( r^{2} \frac{dR}{dr} \right)=0
$$
$$
V(r) = \sum^{\infty}_{l=0} A_{l}r ^{l}P_{l} = V_{0}
$$
$$
V_{0}= V_{0}P_{0} = B_{0}V_{0} + B_{1}V_{1} + B_{2}V_{2}\dots
$$
$$
\therefore B_{0} = V_{0}
$$











