## Square Well Worksheet
A general space solution for a particle in a region where V(x)=0 is 𝜓(𝑥) = 𝐴 sin 𝑘𝑥 + 𝐵 cos 𝑘𝑥.


1) We will deduce the form of the solutions for a potential that is symmetric about x=0, that is, the potential is zero for -L/2<x<L/2 and infinite for |x|>L/2

a) What are the boundary conditions at $x=\pm \frac{L}{2}$ on $\psi(x)$ for a particle in the box?
$$
\psi(x) = 0 \ @  \ x\pm \frac{L}{2}
$$
b) Rewrite the general solution above for each of the boundary conditions. (You will have two equations.)
$$
\psi(x) = A\sin(kx) + B\cos(kx) 
$$
where $x=\pm \frac{L}{2}$ = 0
$$
\psi\left( \frac{L}{2} \right) = A\sin\left( k\left( \frac{L}{2} \right) \right) + B\cos\left( k\left( \frac{L}{2} \right) \right) = 0  \tag{1}
$$
$$
	\psi\left( -\frac{L}{2} \right) = A\sin\left( k\left( -\frac{L}{2} \right) \right) + B\cos\left( k\left( -\frac{L}{2} \right) \right) = 0
$$
You can rewrite $\sin(-x)$ as $-\sin(x)$ and $\cos(-x)$ as $\cos (x)$
$$
-A\sin\left( k\left( \frac{L}{2} \right) \right) + B\left( \cos\left( k\left( \frac{L}{2} \right) \right) \right) = 0 \tag{2}
$$
Adding and taking the difference of these two above functions 1 & 2
$$
1) + 2) = B\cos\left( k\left( \frac{L}{2} \right) \right) = 0
$$
$$
1) - 2) = 0 = 2A\sin\left( k\left( \frac{L}{2} \right) \right)
$$

c) What can you conclude about the allowed values of k for sin(kx) solutions and cos(kx) solutions?
For $\sin(kx)$
$$
k = \frac{n\pi}{L} \text{ where }n \text{ is an even integer}
$$
For $\cos(kx)$
$$
k= \frac{n\pi}{L} \text{ where } n \text{ is an odd integer} 
$$

d) What is the functional form of the ground state (longest wavelength) wavefunction for this well?
For ground state $n=1$
$$
k = \frac{\pi}{L}
$$
$$
\psi_{1} = B\cos\left( \frac{\pi x}{L} \right)
$$
![[Pasted image 20240130112855.png]]

> ignore scale on above graph i couldnt figure out how to be rid of them


e) What is the wavefunction for the first excited state wavefunction for this well?
$$
k=\frac{2\pi}{L}
$$
$$
\psi_{2} = A\sin\left( \frac{2\pi x}{L} \right)
$$
![[Pasted image 20240130112904.png]]
>ignore scale on above graph i couldnt figure out how to be rid of them