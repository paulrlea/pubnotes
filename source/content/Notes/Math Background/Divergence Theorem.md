---
dg-publish: true
---
- Also known as Gauss's Theorem and the Gauss-Ostrogradsky Theorem
- Relates surface integrals to triple (volume) integrals. 
- For a simple solid region denoted by $E$ 
$$
\oint \vec{F} \cdot \hat{n} \ d\vec{\Sigma} = \iiint_{E} \nabla \cdot \vec{F} \ dV
$$
- The LHS term is equivalent to the flux of the vector field through the surface enclosing the region E. It is the integral over the surface, finding the net flux through the surface. 
	- The $\hat{n}$ term represents a function that gives a vector normal to every infinitesimal point on the surface. 
	- The $d\vec{\Sigma}$ term is the area of one of those infinitesimal areas.
	- Putting it together, the $\vec{F} \cdot \hat{n}$ term represents how much fluid enters and leaves in an area given by $d\vec{\Sigma}$. The vectors are **outwards facing**, so flow out of the surface is positive, and flow into the surface is considered negative. 
- The RHS term measures the outward fluid flow from each individual point in the volume, which is equivalent to the total flux. 
	- Divergence, $\nabla \cdot \vec{\mathbf{F}}(x_{0},y_{0},z_{0})$ , is equivalent to the outward flow from a point in space. If you take an infinitesimal volume around the point, $V_{tiny}$, the flow out of the volume is approximately given by 
	$$
	\nabla \cdot \vec{\mathbf{F}}(x_{0},y_{0},z_{0}) \ \  |V_{tiny}|
	$$
	- To equate this to the LHS, the flux term, we have to add up the outward flow from each infinitesimal volume inside the larger volume by multiplying the divergence of each little point by the volume of the infinitesimal volume and then add it all together. 


NB: The divergence theorem only applies to closed surfaces. 

## Divergence Theorem in Electrostatics

- Calculating the divergence of $\mathbf{E}$ from $\mathbf{E(r)} = \frac{1}{4\pi\epsilon_{0}} \int\frac{\rho(\mathbf{r^{\prime}})}{r^{2}}\hat{r} \, d\tau^{\prime}$ gives us the following
$$
\mathbf{\nabla \cdot E} = \frac{1}{4\pi\epsilon_{0}} \int \nabla \cdot \left( \frac{\hat{r}}{r^{2}} \right) \rho(r ^{\prime}) d\tau^{\prime} 
$$
- The generic solution of a vector field is given by
$$
\nabla \cdot\left( \frac{\hat{r}}{r^{2}} \right) = 4\pi\delta^{3}(r)
$$
- Where $\delta$ is the delta function which is 0 everywhere except for 0, where its $\infty$
- This can derive the differential form of Gauss's law
$$
\nabla \cdot \mathbf{E} = \frac{1}{\epsilon_{0}}\rho(r)
$$
- To convert from the differential form to the integral form we can use the following
$$
	\int _{v}\nabla \cdot \mathbf{E} d\tau = \oint_{\mathcal{S}} \mathbf{E} \cdot d\mathbf{a} = \frac{1}{\epsilon_{0}} \int_{\mathcal{S}} \rho d\tau = \frac{1}{\epsilon_{0}}Q_{enc}
$$
