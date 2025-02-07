- Multi-pole expansion is useful for molecular physics, where the size of the charge distribution is much smaller then where we are measuring the potential.
$$
V(r) = \frac{1}{4\pi\epsilon_{0}} \int \frac{\rho(\vec{r}')}{|\vec{r}-\vec{r}'|} \, dV' = V_{0} + V_{1}+V_{2}+V_{3} \dots
$$
$$
\frac{1}{|\vec{r}-\vec{r}'} = \sum^{\infty}_{n=0} 
$$
Consider: 
$$
|\vec{r}-\vec{r}|^{2} = r^{2}+{r}'^{2}-2r r' \cos\alpha
$$
$$
=r^{2}\left( 1+\frac{r'}{r}\left( \frac{r'}{r}-2\cos\alpha \right) \right)
$$
LHS Terms are small because $\frac{r'}{r}$ is small

Expand: 
$$
\frac{1}{|\vec{r}-\vec{r}'|} = \frac{1}{r} (1+\epsilon)^{-1/2}
$$
Result: 
$$
\frac{1}{|\vec{r}-\vec{r}'|} = \frac{1}{r} \sum^{\infty}_{n=0} \left( \frac{r'}{r} \right)p_{n}\cos\alpha = V_{1}+V_{2}+V_{3}+\dots
$$
### The first three terms of the multipole expansion
Electric Monopole:
$$
V_{0} =  \frac{1}{4\pi\epsilon_{0}} \frac{1}{r} \int _{V'}\rho(\vec{r}') \, dV'
$$
Electric Dipole: 
$$
V_{1} = \frac{1}{4\pi\epsilon_{0}} \frac{1}{r^{2}} \int _{V'} r'\cos\alpha \rho(\vec{r}') \, dV' 
$$
Electric Quadrapole:
$$
	V_{2} = \frac{1}{4\pi\epsilon_{0}} \frac{1}{r^{3}} \int _{V'} r'^{2}\left( \frac{3}{2}\cos ^{2}\alpha -\frac{1}{2}\right)\rho(\vec{r}') \, dV'
$$

	>insert diagram of mono, di, quadru and octo pole configurations





