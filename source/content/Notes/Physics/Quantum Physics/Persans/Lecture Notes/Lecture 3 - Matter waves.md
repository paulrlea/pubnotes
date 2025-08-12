
$$
\lambda = \frac{h}{p}
$$
> "Probably your question is not that relevant"
> - Dr Persans
> "You should prove that"
> -Dr Persans 
> "Formal."
> -Dr Persans


$$
\hat{A}\Psi =a\Psi
$$
Set of all solutions are orthonormal
$$
\delta_{nm} = \int \Psi_{n}\Psi_{m} \, dx 
$$


Sin and cosine functions follow this property too

$$
f(x) = \frac{1}{\pi}\left[ \int ^{\infty}_{0}A(k)\cos k x \, dk + \int ^{\infty}_{0}B(k)\sin k x \, dk \right]
$$
Where
$$
	A(k) =\int ^{\infty}_{-\infty}f(x) \cos k \ x \, dx 
$$
$$
	A(k) =\int ^{\infty}_{-\infty}f(x) \sin k \ x \, dx 
$$
This is the [[Fourier transform]]

> "my question is..."
> -Persans

We can use Euler's equation to rewrite the Fourier transform

> "It might be"
> -Persans


## Gaussian pulse example 
We can think of a Gaussian pulse as a localized pulse, whose position we know to a certain accuracy $\Delta x = 2\sigma_{x}$

Normalizing this function such that integrating over all x is 1 we get 
$$
f(x) = \frac{1}{\sigma_{x} \sqrt{ 2\pi }} e^{-x^{2}/2\sigma_{x}^{2}}
$$
> "We're not mathematicians, we're physicists, so we're going to be somewhat practical about this"
> -Persans

$$
f(x) = \int_{0}^{\infty} A(k)\cos kx \, dx +\int_{0}^{\infty} B(k)\sin kx \, dx +
$$
$$
=\int^{\infty}_{0} A(k)e^{ikx} \, dx +  \int^{\infty}_{0} B(k)e^{-ikx} \, dx
$$
### Finding the transform
I will drop overall multiplicative constants because I am interested in the shape of $A(k)$

$$
	A(k)\propto \int^{\infty}_{-\infty}e^{x^{2}/2\sigma^{2}_{x}}e^{-ikx} \, dx = \int^{\infty}_{-\infty} e^{-ax^{2}-ikx} \, dx  
$$
$$
a=\frac{1}{2} \sigma^{2}_{x}
$$
$$
=\int ^{\infty}_{-\infty} e^{-(x\sqrt{ a }-(ik)/2\sqrt{ a })^{2}-k^{2}/4a} \, dx 
$$
letting $\beta=x\sqrt{ a}-\frac{ik}{2\sqrt{ a }}$
$$
A(k) \propto \frac{1}{\sqrt{ a }} e^{-k^{2}/4a} \int ^{\infty}_{-\infty} e^{-\beta^{2}}\, d\beta = \sqrt{ \frac{\pi}{a} }e^{-k^{2}/4a} = \sqrt{ \frac{\pi}{a} } e^{-k^{2}\sigma_{x}^{2}/2} 
$$

## Heisenberg Uncertainty Principle

The standard deviation of k 

$$
\sigma_{k}^{2} =\frac{1}{\sigma_{x}^{2}}
$$
	The result is that $\sigma_{x}\sigma_{k}=1$ for a Gaussian pulse
$k$ is the wave-number, defined as $k=\frac{2\pi}{\lambda}$. Also can be a vector to determine wave direction. The product of the wave-number width and spatial width is always equal to or greater then 1.
The deBroglie hypothesis relates wavelength to momentum, 
	deBroglie hypothesis
$$
p=\frac{h}{\lambda}=\hbar k
$$
Applying the deBroglie hypothesis to the above principle we get the following:
$$
\sigma_{x}\sigma_{p} =\frac{h}{2\pi}
$$

Which is the [[Heisenberg Uncertainty Principle ]]! It is frequently thought of as a measurement "problem" where you cannot know the position and momentum of a particle to an arbitrary accuracy simultaneously. 

### Conjugate variables
- Position and momentum are called conjugate variables and specify the trajectory of a classical particle
- If one wants to specify the position of a Gaussian wave packet, then:
$$
\Delta x\Delta p = \frac{\hbar}{2}
$$
- The Heisenberg uncertainty principle itself is uncertain. 


### Single Photon Experiments
- When single particles are sent through a system, there is interference even though there is no way for interference to occur with single particles. 
- The wave function takes all possible paths at once, which is cool and weird. The wave function interferes with itself, which allows an interference pattern to form. 
- If a measurement of which path the particle takes is done, the interference pattern is destroyed. 
- Leads to many-worlds hypothesis. Quack science but interesting to look into. See the book timeline
### Normalized Probability
$$
P_{density} dx = \Psi^{*}\Psi dx
$$
- Given the probabilities for a set of outcomes, we can find useful quantities, like the average* (or expectation value) of a result q
- Variance = Dispersion
average=mean=expectation value

### Continuous Distributions
Finding expectation value
	 Normalize first!!!
$$
\langle x \rangle = \int ^{\infty}_{0} xP(x)dx 
$$
$$
\langle q(x) \rangle = \int ^{\infty}_{-\infty} q(x)P(x) \, dx 
$$

## Superposition 
If you have two functions $\psi_{1}$ and $\psi_{2}$, two physically realizable states of a system, then the linear combination $\psi = c_{1}\psi_{1}+c_{2}\psi_{2}$ is also a possible state. 
## Normalization
Sometimes you have to normalize functions yourself that lead to an integrated probability that is not already 1. 
MAKE SURE YOUR FUNCTIONS ARE NORMALIZED

## [[Notes/Physics/Quantum Physics/Concepts/Schrodinger equation]]
There are relativistic forms of this equation. See [[Dirac Equation]]. Exists in 1d, 3d, time dependent, and time independent flavors. Time independent also known as energy eigenvalue equation. 
## Physical Constraints on wave functions
- has to be normalizable (gotta exist somewhere)
- has to be single-valued (cant have two probabilities at same point )
- has to be continuous (or you'll have infinite energy)
	- no kinks!
#### Examples of Wave functions 
![[Pasted image 20240116114625.png]]

## Expectation values
- Operators, quantum mechanics, etc etc etc 




