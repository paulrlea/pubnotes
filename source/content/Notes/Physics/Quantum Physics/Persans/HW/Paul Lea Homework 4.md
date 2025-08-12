22. Townsend problem 3.5 
![[Pasted image 20240208171232.png]]
The probability a measurement of $E$ yields $E_{1}$ is given by the following
$$
|c_{n}|^{2} =P_{n}  \implies \text{Prob. of } E_{1} = | \frac{i}{2}|^{2} \to \frac{1}{4}
$$
The probability of yielding $E_{1}$ is $\frac{1}{4}$
We can use the similar method to find the probability of yielding $E_{2}$.
$$
\text{Prob. of } E_{2} = \left( \frac{\sqrt{ 3 }}{2} \right)^{2} = \frac{3}{4}
$$
We can double check that this accurate because the following condition has to hold true: 
$$
\sum^{\infty}_{n=1} |c_{n}|^{2} = 1
$$
and the sum of $\frac{1}{4}$ and $\frac{3}{4}$ does equal 1. 

Finding the expectation value is relatively simple, by taking the weighted average of $E_{n}$ with the respective coefficients as follows: 
$$
\left< E \right>  = \sum^{\infty}_{n=1} P_{n}E_{n} = \frac{1}{4}E_{1}  +\frac{3}{4} E_{2}
$$
To find the uncertainty, we can first follow a similar procedure to find $\left< E^{2} \right>$
$$
\left< E^{2} \right>  = \sum^{\infty}_{n=1} P_{n}E_{n}^{2} = \frac{1}{4}E_{1}^{2}  +\frac{3}{4} E_{2}^{2}
$$
Putting these into the uncertainty equation: 
$$
\Delta E = (\left< E^{2} \right> -\left< E \right> ^{2})^{1/2}
$$
$$
=\left[ \frac{1}{4}(E^{2}_{1}+3E^{2}_{2})- \frac{1}{16}(E_{1}+E_{2})^{2}\right] \to \left[ \frac{1}{4}(E_{1}^{2}+3E_{2}^{2})-\frac{1}{16}(E_{1}^{2}+E_{2}^{2}+2E_{1}E_{2}) \right]
$$
$$
\left[ \frac{1}{4}E_{1}^{2}+\frac{3}{4}E_{2}^{2} -\left( \frac{1}{16}E_{1}^{2} + \frac{9}{16}E_{2}^{2} + \frac{3}{8 }E_{1}E_{2} \right) \right]
$$
Simplifies down to: 
$$
\frac{3}{16}(E_{1}-E_{2})^{2}
$$
Which is a logical answer, because the uncertainty when $E_{1}=E_{2}$
23. Townsend problem 3.8
![[Pasted image 20240208171237.png]]
We can exploit the orthogonality of eigenfunctions to solve this: 
$$
c_{n} = \int \Psi(x)\psi_{n}(x) \, dx 
$$
We are given the normalized wavefunction above, so we just need the generalized eigenfunction. This is for the bound state of the infinite square well, so we can use the following: 
$$
\psi_{n}=\sqrt{ \frac{2}{L} } \sin \frac{n\pi x}{L}
$$
Now we get to put it all together and solve: 
$$
c_{n} = \int\limits ^{L}_{0} \sqrt{ \frac{30}{L^{5}} }x(L-x) \sqrt{ \frac{2}{L} }\sin \frac{n\pi x}{L} \, dx 
$$
Start by pulling the constants out of the integration
$$
= \sqrt{ \frac{2}{L} } \int\limits_{0}^{L}\sin\left( \frac{n\pi x}{L} \right) \sqrt{ \frac{30}{L^{5}} } x(L-x)  \, dx 
$$
$$
\frac{2\sqrt{ 15 }}{L^{3}}\left[ L\int\limits_{0}^{L} L\sin\left( \frac{n\pi}{L}x \right) \, dx -\int\limits_{0}^{L} x^{2}\sin\left( \frac{n\pi}{L}x \right) \, dx  \right]
$$
$$
\frac{2\sqrt{ 15 }}{L^{3}} \left[ L\left[ \left( \frac{L}{n\pi}^{2} \right)\sin\left( \frac{n\pi}{L}x \right)- \frac{Lx}{n\pi}\cos(\frac{n\pi}{L}x) \right]^{L}_{0} \right]
$$
$$
-\left[ 2\left( \frac{L}{n\pi} \right)^{2}x\sin\left( \frac{n\pi}{L}x \right)-\frac{\left( \frac{n\pi x}{L} \right)^{2} -2}{\left( \frac{n\pi}{L} \right)^{3}}\cos \left( \frac{n\pi}{L}x \right)\right]^{L}_{0}
$$
$$
\frac{2\sqrt{ 15 }}{L^{3}}\left[ -\frac{L^{3}}{n\pi} \cos(n\pi) + L^{3} \frac{(n\pi)^{2}-2}{(n\pi^{3})}\cos(n\pi) + \frac{L^{3}}{(n\pi)^{3}}\cos(0)\right]
$$
$$
c_{n} = \frac{4\sqrt{ 15 }}{(n\pi)^{3}}[\cos(0)-\cos(n\pi)]
$$
$$
 c_{n} = \frac{4\sqrt{15 }}{(n\pi)^{3}} [1-(-1)^{n}]
$$
$$
c_{n}^{2} = \frac{240}{n^{6}\pi^{6}}[1-(-1)^{n}]^{2}
$$
24. Townsend problem 3.12
![[Pasted image 20240208171252.png]]
a. Probability of finding the ground state in the new well is given by $c_{1}^{2}$ if $c_{1}$ is real
$$
	c_{1} = \int\limits_{-\infty}^{\infty} \psi_{1}(x)\Psi(x) \, dx 
$$
$$
	c_{1} = \int\limits_{0}^{L} \sqrt{ \frac{2}{2L} }\sin \left( \frac{\pi x}{2L} \right)\sqrt{ \frac{2}{L} } \sin\left( \frac{\pi x}{L} \right) \, dx 
$$
$$
c_{1}=\frac{\sqrt{ 2 }}{L} \int\limits_{0}^{L} \sin\left( \frac{\pi x}{2L} \right)\sin\left( \frac{\pi x}{L} \right) \, dx 
$$
$$
c_{1} = \frac{4\sqrt{ 2 }}{3\pi}
$$
$$
c_{1}^{2}= \frac{32}{3\pi}
$$
This is the probability of finding the system in the ground state. The probability of finding the system in the first excited state, $c_{2}$ can be found with a similar process.
$$
	c_{2} = \int\limits_{0}^{L} \sqrt{ \frac{2}{2L} }\sin \left( \frac{2\pi x}{2L} \right)\sqrt{ \frac{2}{L} } \sin\left( \frac{\pi x}{L} \right) \, dx 
$$
$$
	c_{2} =\frac{\sqrt{ 2 }}{L} \int\limits_{0}^{L} \sin \left( \frac{\pi x}{L} \right)\sin\left( \frac{\pi x}{L} \right) \, dx 
$$
$$
c_{2}=\frac{\sqrt{ 2 }}{L} \frac{L}{2}
$$
$$
c_{2}^{2}  = \frac{1}{2}
$$
b. The time development of the system, we will use the following procedure:

$$
\psi_{n}(t) = \sqrt{ \frac{1}{L} } \sin\left( \frac{n\pi x}{2L} \right)e^{iE'_{n}t/\hbar}
$$
The system is in a stationary state. 
25 Townsend 4.04
![[Pasted image 20240208171109.png]]
Correct:
1. The figure shows the eigenfunction decaying to 0 at both ends, which makes sense because the potential is greater then the energy level. 
2. The figure shows the frequency of oscillation increasing when the potential decreases, corresponding to higher energy levels and lower wavelength in that region.  
3. The figure shows the correct overall waveform for the 5th energy level. 

Incorrect:
1. Wave-function should have higher amplitude on the left side of the sloped potential. 




 