## Question 1: 
The figure below shows, several [[conductors]] that carry currents through the plane of the figure. $I_1 = 3.8A ,  I_2 = 5.6A, I_3 = 2.2A$ 
$$
\oint \vec{B} \cdot dl = \mu _{0} I_{enc}
$$
[[Ampere's Law]]
Find the line integral for path A: 
$A=0$ because $I_{enc}= 0$

Find the [[path integral]] for path b:
$$
\oint \vec{B}\cdot dl = \mu_{0}I_{1}=(1.25663706E-6)(3.8)=0.00000477522082770519
$$
NB: It was negative b/c [[right hand rule]], current is coming out of paper.

Find the path integral for path c: 

$$
\oint \vec{B}\cdot dl = \mu_{0}(I_{2}-I_{1})=(1.25663706E-6)(5.6-3.8)=0.00000226194670786035
$$
Find the path integral for path d: 
$$
\oint \vec{B}\cdot dl = \mu_{0}(I_{3}+I_{2}-I_{1})=(1.25663706E-6)
(2.2+5.6-3.8)=0.00000502654823968968
$$


## Question 2:
Toroidal [[solenoid]]s
This demonstrates amperes law quite well. For a solenoid of $N$ Turns and $r$ radius, the strength of a toroidal solenoid is given by $B=\frac{\mu NI}{2\pi r}$ .  This is true because the current enclosed by the amperian surface surrounding the toroid is given by multiplying number of loops N by [[current]] I within each loop. 

$$
r=\frac{r_{1} + r_{2} }{2}
$$
$$
B_{16.1}  = \frac{\mu NI}{2\pi r} = \frac{190*8.4\mu}{2\pi * 0.161}
$$

NB: I was a fucking nonce and didn't realize that the phrase "from the center of the solenoid" meant from the center of the solenoid RADIALLY, not perpendicular to the solenoid. 

Part A is zero because enclosed current is 0

Part C is also zero because the amperian surface encloses 0 net charge

## Question 3:
[[solenoid]]

The [[Magnetic Field]] within a long solenoid is given below:

$$
B = \frac{\mu NI}{L}
$$
For our problem $N = 600, L=0.15, I=8$
Therefore, 
$$
B=\frac{\mu*600*8}{0.15} = 0.04021238591751741933
$$
## Question 4:
Hint 1: Find the current enclosed in an amperian loop
	Current enclosed is given by $IN$ because for N wires enclosed with I current in each. 
Hint 2:
	Use right hand rule to find that the direction of the magnetic field above the infinite sheet is in the $-\hat{i}$ direction 
Hint 3: 
	Evaluate $\oint\vec{B}(\vec{r})\cdot \vec{d}l$ around the amperean loop
	$=2Ba$

Final Answer: 
$$
2Ba = I_{enc} \mu_{0} 
$$
$$
-B = \frac{I_{enc}\mu_{0}}{2a} = \frac{NI\mu_{0}}{2a}\hat{i}
$$
