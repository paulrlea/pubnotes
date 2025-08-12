## 16. Assume that $\psi(x)$ is an arbitrary normalized real function. 
A. Calculate $\left< P_{x} \right>$ for $e^{i(kx-\omega t)}\psi(x)$.
$$
\int\limits_{-\infty}^{\infty} e^{-i(kx-\omega t)}\psi^{*}(x) \frac{\hbar}{i} \frac{ \partial  }{ \partial x } (e^{i(kx-\omega t)}\psi(x)) \, dx 
$$
$$
\frac{\hbar}{i}\int\limits_{-\infty}^{\infty} \cancel{ e^{i(kx-\omega t)} }\psi^{*}(x) ik\cancel{ e^{i(kx-\omega t)} }\psi(x)  \, dx 
$$
$$
\frac{\hbar}{i}ki \int\limits_{-\infty}^{\infty} \psi^{*}\psi \, dx 
$$
$$
\left< p_{x} \right> = \hbar k
$$ 
B. Calculate $\left< P_{x} \right>$ for $e^{-i\omega t}\psi(x)$ 
$$
\int\limits_{-\infty}^{\infty} e^{i\omega t}\psi^{*}(x) \frac{\hbar}{i}\frac{ \partial  }{ \partial x } (e^{-i\omega t}\psi(x)) \, dx 
$$
$$
\int\limits_{-\infty}^{\infty} \cancel{ e^{i\omega t} }e\cancel{ ^{-i\omega t} } \frac{\hbar}{i} \psi^{*}(x)\psi(x) \, dx 
$$
$$
\frac{\hbar}{i}\int\limits_{-\infty}^{\infty} \psi^{*}\psi\, dx 
$$
$$
\left< p_{x} \right> = \frac{\hbar}{i}
$$
### 17. Show that there is no solution to the [[Notes/Physics/Quantum Physics/Concepts/Time independent Schrodinger equation]] for a particle in the infinite square well for E=0
$$
-\frac{\hbar^{2}}{2m} \frac{d^{2}\psi}{dx^{2}} = 0
$$
What is the most general solution to this second order differential equation 

$$
-\frac{\hbar^{2}}{2m}\iint \frac{d^{2}\psi}{dx^{2}} dx=0
$$
$$
\psi = c_{2}x+c_{1}
$$
$$
0 = c_{2}(0) + c_{1}
$$
$$
\therefore c_{1}=0
$$
$$
0= c_{2}L + c_{1}
$$
$$
\therefore c_{2} = 0
$$
$$
\therefore \psi = 0x + 0
$$
### 18. The wave function for a particle in a box is given where N is a constant.
$$
\psi(x)=\begin{cases}
N & 0<x<L \\
0 & \text{elsewhere}
\end{cases}
$$
a. Determine a value for N such that the wave function is appropriately normalized

$$
1=\int\limits_{0}^{L} \psi^*\psi \, dx 
$$
Assuming N is a real valued constant
$$
1=\int\limits_{0}^{L} N^{2} \, dx 
$$
$$
1= [N^{2}x] |^{L}_{0} \to 1 =N^{2}L-\cancel{ N^{2}0 }
$$
$$
1=N^{2}L \to N=\sqrt{ \frac{1}{L} }
$$
$$
N = \sqrt{ \frac{1}{L} }
$$
b. Calculate the uncertainty in the particles position
$$
\Delta x = \sqrt{ \left< x^{2} \right> -\left< x \right> ^{2} }
$$
$$
\left< x \right> = \int\limits_{0}^{L} \psi^{*}x\psi \, dx 
$$
$$
\left< x \right> = \int\limits_{0}^{L} \frac{1}{L}x \, dx \to \frac{1}{L}\int\limits_{0}^{L} x  \, dx \to \frac{1}{L}\left[ \frac{x^{2}}{2} \right]^{L}_{0}\to \frac{1}{L} \left( \frac{L^{2}}{2} \cancel{ - \frac{0^{2}}{2}  }\right)
$$
$$
\left< x \right> = \frac{L}{2}
$$
$$
\left< x^{2} \right> = \int\limits_{0}^{L} \psi^{*}x^{2}\psi \, dx 
$$
$$
\left< x^{2} \right> = \int\limits_{0}^{L} \frac{1}{L}x^{2} \, dx \to \frac{1}{L}\int\limits_{0}^{L} x^{2}  \, dx \to \frac{1}{L}\left[ \frac{x^{3}}{3} \right]^{L}_{0}\to \frac{1}{L} \left( \frac{L^{3}}{3} \cancel{ - \frac{0^{2}}{2}  }\right)
$$
$$
\left< x^{2} \right>  = \frac{L^{2}}{3}
$$
$$
\Delta x = \sqrt{ \left( \frac{L^{2}}{3}\right)-\left( \frac{L}{2} \right)^{2} } \to \sqrt{ \frac{L^{2}}{3}-\frac{L^{2}}{4} } \to \sqrt{ \frac{4L^{2}}{12}-\frac{3L^{2}}{12} } \to \sqrt{ \frac{L^{2}}{12} }
$$
$$
\Delta x = \frac{L\sqrt{ 12 }}{12}
$$

### 19. The two state functions
$$
\Psi_{1}(x,t) = A_{1}\cos\left( \frac{\pi x}{L} \right)e^{-i\omega_{1}t}
$$
$$
\Psi_{2}(x,t) = A_{2}\sin\left( \frac{2\pi x}{L} \right)e^{-i\omega_{2}t}
$$
Where the function is 0 for $x< -\frac{L}{2}$ and $x>\frac{L}{2}$
a. Find the A values that normalize the function
$$
1 =\int\limits_{-L/2}^{L/2} A_{1}\cos\left( \frac{\pi x}{L} \right)e^{+i\omega_{1}t} A_{1}\cos\left( \frac{\pi x}{L} \right)e^{-i\omega_{1}t}  \, dx 
$$
$$
1=A_{1}^{2}\int\limits_{-L/2}^{L/2}\cos ^{2}\left( \frac{\pi x}{L} \right)\cancel{ e^{i\omega_{1}t} }\cancel{ e^{-i\omega_{1}t} }  \, dx 
$$
$$
1 = A_{1}^{2}\int\limits_{-L/2}^{L/2} \cos ^{2}\left( \frac{\pi x}{L} \right)  \, dx 
$$
Computed integral 
$$
1= A^{2}_{1} \frac{L}{2}
$$
$$
\frac{1}{A_{1}^{2}} = \frac{L}{2} - > A_{1}^{2} = \frac{2}{L}
$$
$$
A_{1} = \sqrt{ \frac{2}{L} }
$$
For other function 
$$
1 =\int\limits_{-L/2}^{L/2} A_{2}\sin\left( \frac{2\pi x}{L} \right)e^{+i\omega_{2}t} A_{2}\sin\left( \frac{2\pi x}{L} \right)e^{-i\omega_{2}t}  \, dx 
$$
$$
1=A_{2}^{2}\int\limits_{-L/2}^{L/2}\sin ^{2}\left( \frac{2\pi x}{L} \right)\cancel{ e^{i\omega_{2}t} }\cancel{ e^{-i\omega_{2}t} }  \, dx 
$$
$$
1 = A_{2}^{2}\int\limits_{-L/2}^{L/2} \sin ^{2}\left( \frac{2\pi x}{L} \right)  \, dx 
$$
Computed Integral is also $\frac{L}{2}$, therefore 
$$
A_{2} =\sqrt{ \frac{2}{L} }
$$
B. Find the expectation value for x for each function. (Write down any integrals one would need to calculate. You may not need to do any integrals if you make a good logical argument. Hint: Making a variable substitution can help you to visualize whether functions are even or odd about the center of the region.)
$$
\left< x \right>_{1} = \int\limits_{-L/2}^{L/2} \sqrt{ \frac{2}{L} }\cos\left( \frac{\pi x}{L} \right)e^{+i\omega_{1}t} x\sqrt{ \frac{2}{L} }\cos\left( \frac{\pi x}{L} \right)e^{-i\omega_{1}t}   \, dx 
$$
$$
\left< x \right>_{1} = \frac{2}{L}\int\limits_{-L/2}^{L/2} \cos\left( \frac{\pi x}{L} \right)\cancel{ e^{+i\omega_{1}t} } x\cos\left( \frac{\pi x}{L} \right)\cancel{ e^{-i\omega_{1}t}  }  \, dx 
$$
$$
\left< x \right>_{1} = \frac{2}{L}\int\limits_{-L/2}^{L/2} \cos ^{2}\left( \frac{\pi x}{L} \right)x \, dx 
$$
Cosine is an even function. The product of an even function and an odd function is an odd function. The integral of an odd function over its domain is 0. Therefore, $\left< x \right>_{1}$ is 0. 
```mathpad
%$1:=[cos^2*x^2]
%$2:=0
plot (cos(x))^2*x==?
```
As seen in the graph above, the graph is mirrored over the x axis, meaning any integral over a symmetric domain would be 0


For the other function, a similar argument can be made because it will turn out to be the product of 3 odd functions, sin(x), sin(x) and x. The product of 3 odd functions is still an odd function
```mathpad
%$1:=[cos^2*x^2]
%$2:=0
%$4:=[cos(x)^2*x]
%$5:=[sin(x)^2*x]
%$6:=plot
plot sin(x)^2*x==?
```
Graph of $\sin ^{2}(x)x$ proving this concept


C. Is the expectation value for each function equal to the most probable value for each function? If not, explain

It is not the most probable value, but the "average" of all possible values. The most probable values are the values where amplitude of the wavefunction is greatest, so in both of these cases it would be as far away from the origin, so either at $-\frac{L}{2}$ or $\frac{L}{2}$

D. Find the expectation value of $x^{2}$ for each function
$$
\left< x^{2} \right>_{1} = \int\limits_{-L/2}^{L/2} \sqrt{ \frac{2}{L} }\cos\left( \frac{\pi x}{L} \right)e^{+i\omega_{1}t} x^{2}\sqrt{ \frac{2}{L} }\cos\left( \frac{\pi x}{L} \right)e^{-i\omega_{1}t}   \, dx 
$$
$$
\left< x^{2} \right>_{1} = \frac{2}{L}\int\limits_{-L/2}^{L/2} \cos\left( \frac{\pi x}{L} \right)\cancel{ e^{+i\omega_{1}t} } x^{2}\cos\left( \frac{\pi x}{L} \right)\cancel{ e^{-i\omega_{1}t}  }  \, dx 
$$
$$
\left< x^{2} \right>_{1} = \frac{2}{L}\int\limits_{-L/2}^{L/2} \cos ^{2}\left( \frac{\pi x}{L} \right)x^{2} \, dx 
$$
$$
\left< x^{2} \right>_{1} = \frac{2}{L}\left[ \dfrac{\left(6{\pi}^2Lx^2-3L^3\right)\sin\left(\frac{2{\pi}x}{L}\right)+6{\pi}L^2x\cos\left(\frac{2{\pi}x}{L}\right)+4{\pi}^3x^3}{24{\pi}^3} \right]^{L/2}_{-L/2}
$$
$$
\left< x^{2} \right>_{1} = \frac{2}{L}[\dfrac{\left({\pi}^2-6\right)L^3}{24{\pi}^2}] = \frac{L^{2}(\pi^{2}-6)}{12\pi^{2}}
$$
Solving the other 
$$
\left< x^{2} \right>_{2} = \int\limits_{-L/2}^{L/2} \sqrt{ \frac{2}{L} }\sin\left( \frac{2\pi x}{L} \right)e^{+i\omega_{1}t} x^{2}\sqrt{ \frac{2}{L} }\sin\left( \frac{2\pi x}{L} \right)e^{-i\omega_{1}t}   \, dx 
$$
$$
\left< x^{2} \right>_{2} = \frac{2}{L}\int\limits_{-L/2}^{L/2} \sin\left( \frac{2\pi x}{L} \right)\cancel{ e^{+i\omega_{1}t} } x^{2}\sin\left( \frac{2\pi x}{L} \right)\cancel{ e^{-i\omega_{1}t}  }  \, dx 
$$
$$
\left< x^{2} \right>_{2} = \frac{2}{L}\int\limits_{-L/2}^{L/2} \sin ^{2}\left( \frac{2\pi x}{L} \right)x^{2} \, dx 
$$
$$
\left< x^{2} \right> _{2} = \frac{2}{L}\left[ -\dfrac{\left(24{\pi}^2Lx^2-3L^3\right)\sin\left(\frac{4{\pi}x}{L}\right)+12{\pi}L^2x\cos\left(\frac{4{\pi}x}{L}\right)-32{\pi}^3x^3}{192{\pi}^3} \right]^{2/L}_{-2/L}
$$

$$
\left< x^{2} \right> _{2} = \frac{2}{L}(\dfrac{\left(2{\pi}^2-3\right)L^3}{48{\pi}^2})
$$
$$
\left< x^{2} \right> _{2} = \frac{(2\pi^{2}-3)L^{2}}{24\pi^{2}}
$$
e) Find the uncertainty in position $\Delta x \equiv \sqrt{ \left< x^{2} \right> - \left< x \right>^{2} }$ for each function.
For $\Psi_{1}$:
$$
\Delta x_{1} = \sqrt{\frac{L^{2}(\pi^{2}-6)}{12\pi^{2}} - 0^{2}}
$$
$$
\Delta x_{1} = \sqrt{ \frac{L^{2}(\pi^{2}-6)}{12\pi^{2}} }
$$
$$
\Delta x_{1} = \frac{L\sqrt{(\pi^{2}-6) }}{\pi\sqrt{ 12 }}
$$
$$
\Delta x_{1} = \frac{L\sqrt{ 12(\pi^{2}-6) }}{12\pi}
$$
For $\Psi_{2}$:
$$
\Delta x_{2} = \sqrt{ \frac{(2\pi^{2}-3)L^{2}}{24\pi^{2}} - 0^{2} }
$$
$$
\Delta x_{2} = \sqrt{ \frac{(2\pi^{2}-3)L^{2}}{24\pi^{2}}}
$$
$$
\Delta x_{2} = \frac{L\sqrt{ (2\pi^{2}-3) }}{\pi\sqrt{ 24 }}
$$
$$
\Delta x_{2} = \frac{L\sqrt{ 24(2\pi^{2}-3) }}{24\pi}
$$
20.
a) Find the state function in the wave-vector representation, $A(k)$, for the wavefunction $\Psi_{1}(x,t) =A_{1}\cos\left( \frac{\pi x}{L} \right)e^{-i\omega_{1}t}$ where the wave function is zero for $x < -\frac{L}{2}$ and $x> \frac{L}{2}$ (outside the box).
Normalized
$$
1 = \int\limits_{-L/2}^{L/2} A_{1}^{2}\cos ^{2}\left( \frac{\pi x}{L}\right)   \, dx 
$$
$$
1 = A^{2}_{1}  \int\limits_{-L/2}^{L/2} \cos ^{2}\left( \frac{\pi x}{L} \right) \, dx 
$$
$$
\frac{1}{A_{1}^{2}} = \int\limits_{-L/2}^{L/2} \cos ^{2}\left( \frac{\pi x}{L} \right) \, dx 
$$
$$
\frac{1}{A_{1}^{2}} =  \frac{L}{2}
$$
$$
A_{1}^{2}= \frac{1}{L} \to A = \sqrt{ \frac{2}{L} }
$$
$$
A_{1} = \sqrt{ \frac{2}{L} }
$$
$$
\Psi_{1}(x,t) = \sqrt{ \frac{2}{L} } \cos\left( \frac{\pi x}{L} \right){ e^{-i\omega_{1}t} }
$$
$$
A(k) = \frac{1}{\sqrt{ 2\pi } } \int\limits_{-\infty}^{\infty} \psi(x,0)e^{-ikx} \, dx 
$$
$$
A(k) = \sqrt{ \frac{2}{L} }\frac{1}{\sqrt{ 2\pi }} \int\limits_{-L/2}^{L/2}\cos\left( \frac{x\pi}{L} \right)e^{-ikx}  \, dx 
$$

$$
A(k) =\frac{1}{2} \sqrt{ \frac{1}{\pi L} } \int\limits_{-L/2}^{L/2} (e^{ixk_{0}}+e^{-ixk_{0}})e^{-ikx} \, dx 
$$
$$
A(k) =\frac{1}{2} \sqrt{ \frac{1}{\pi L} } \int\limits_{-L/2}^{L/2} e^{ixk_{0}}e^{-ikx} \ dx + \int\limits_{-L/2}^{L/2}e^{-ik_{0}x}e^{-ikx}  \, dx 
$$
$$
A(k)=\frac{1}{2}\sqrt{ \frac{1}{\pi L} }\left( -\dfrac{2L\cos\left(\frac{Lk}{2}\right)}{Lk-{\pi}} + \dfrac{2L\cos\left(\frac{Lk}{2}\right)}{Lk+{\pi}} \right)
$$
$$
A(k) = \sqrt{ \frac{1}{\pi L} }\frac{2 \pi L \cos\left(\frac{kL}{2}\right)}{\pi^2 - k^2 L^2}
$$

This is the wave-vector representation
b) Find the uncertainty in 𝑘 by completing appropriate integrals.
$$
\left< p \right> = \int\limits_{-L/2}^{L/2}  A_{1}\cos\left( \frac{\pi x}{L} \right)e^{i\omega_{1}t} \frac{\hbar}{i} \frac{d}{dx}( A_{1}\cos\left( \frac{\pi x}{L} \right)e^{-\omega_{1}t} ) \, dx
$$
$$
A_{1}^{2} \int\limits_{-L/2}^{L/2} \cos\left( \frac{\pi x}{L} \right) \frac{\pi}{L}\sin\left( \frac{\pi x}{L} \right)\, dx 
$$
$$
A_{1}^{2} \frac{\hbar}{i}\frac{\pi}{L} \int\limits_{-L/2}^{L/2} \cos\left( \frac{\pi x}{L} \right)\sin\left( \frac{\pi x}{L} \right)\, dx 
$$
Odd function goes to 0
 $$
\left< p \right> =0
$$
$$

\left< p ^{2}\right> = \int\limits_{-L/2}^{L/2}  A_{1}\cos\left( \frac{\pi x}{L} \right)e^{i\omega_{1}t} \frac{\hbar^{2}}{i^{2}} \frac{d^{2}}{dx^{2}}( A_{1}\cos\left( \frac{\pi x}{L} \right)e^{-i\omega_{1}t} ) \, dx
$$
$$
\left< p ^{2}\right> = \int\limits_{-L/2}^{L/2}  A_{1}^{2}\cos\left( \frac{\pi x}{L} \right)\cancel{ e^{i\omega_{1}t} } \frac{\hbar^{2}}{\cancel{ i^{2} }}\left(\cancel{  - }\dfrac{{\pi}^2\cos\left(\frac{{\pi}x}{L}\right)}{L^2} \cancel{ e^{-\omega_{1}t} }\right)dx
$$
$$
\left< p ^{2}\right> =A_{1}^{2}e^{-2\omega_{1}t} \frac{\pi^{2}}{L^{2}} {\hbar^{2}} \int\limits_{-L/2}^{L/2} \cos\left( \frac{\pi x}{L} \right)\left( {\cos\left(\frac{{\pi}x}{L}\right)}{} \right)dx
$$
$$
\left< p ^{2}\right> =A_{1}^{2} \frac{\pi^{2}}{L^{2}} \frac{\hbar^{2}}{1} \frac{L}{2}
$$
$$
\left< p^{2} \right> = \left( \sqrt{ \frac{2}{L} } \right)^{2}  \frac{\pi^{2}\hbar^{2}}{2L} \to \frac{2}{L} \frac{\pi^{2}\hbar^{2}}{2L}
$$
$$
\left< p^{2} \right> = \frac{\pi^{2}\hbar^{2}}{L^{2}}
$$
$$
\Delta k=\frac{\Delta {p}}{\hbar} = \frac{\sqrt{ \left< p^{2} \right> -\left< p \right> ^{2} }}{\hbar} = \frac{\sqrt{   \frac{\pi^{2}\hbar^{2}}{L^{2}} }}{\hbar}
$$
$$
\Delta k=\frac{\pi}{ L}
$$
c) Make an argument for why your calculated uncertainty in k is reasonable

It seems like all the appropriate terms canceled out to yield a mathematically possible answer. There is no dependency on time, and the uncertainty is a function of the size of the infinite square well, which also makes logical senseP

























