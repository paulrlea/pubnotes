---
dg-publish: true
---
# Non-Inertial reference frames 

Recall: an inertial reference frame is at rest or moves with a constant velocity & newtons laws are valid 

- Non-inertial reference frame:
	- Rotating Reference frame
		- WWII Artillerymen had to account for the spin of the earth to accurately hit their targets

Rotating coordinate systems: 
Example: Rotating reference frame on earth compared to stationary reference frame 

From last time: 
$$
\vec{v}_{fixed} = \vec{V} + \vec{v}_{r}+ \vec{\omega}\times \vec{r}
$$
Where 
$$
\begin{matrix}
\vec{v}_{fixed} = \text{velocity relative to fixed frame} \\
\vec{V} = \text{Linear velocity relative to origin of moving frame} \\
\vec{v}_{r} = \text{ velocity relative to rotating frame} \\
\vec{\omega} \times \vec{r} = \text{angular velocity}
\end{matrix}
$$
Using Newtons Second Law: 
$$
\vec{F}=m\vec{a} = m \frac{d\vec{v}}{dt} |_{\text{fixed}}
$$
$$
\frac{d\vec{v}_{fixed}}{dt}|_{fixed} = \frac{d\vec{V}}{dt}|_{fixed} + \frac{d\vec{v}_{r}}{dt}|_{fixed} + \vec{\omega}\times \vec{r} + \vec{\omega}\times \frac{d\vec{r}}{dt}|_{fixed}
$$
In which the first term on the RHS is $\ddot{\vec{R}}_{f}$ , the acceleration relative to the origin. The second term becomes 
$$
\frac{d\vec{v}}{dt}|_{rot} + \vec{\omega}\times \vec{r}
$$
The third term remains the same, angular velocity is the same, and the forth term becomes 
$$
\vec{\omega} \times \frac{d\vec{r}}{dt}|_{rot} + [\vec{\omega} \times \vec{r}]
$$
Putting this all together we get 
$$
=\vec{\omega}\times \frac{d\vec{r}}{dt}|_{rot} + \vec{\omega} \times (\vec{\omega} \times \vec{r})
$$
$$
=\vec{\omega}\times \vec{v}_{r} + \vec{\omega} \times (\vec{\omega}\times \vec{r})
$$

Using this we can find force measured in the fixed frame 
$$
\vec{F} = m\vec{a}_{f} =m\ddot{\vec{R}}_{f} + m\vec{a}_{r} +m \dot{\vec{\omega}} \times \vec{r}+m\vec{\omega}\times(\vec{\omega} \times \vec{r}) + 2m\vec{\omega} \times \vec{v}_{r}
$$
Finding the force measured in the rotating frame
$$
\vec{F}_{eff} = m\vec{a}_{r} = \vec{F} - m\ddot{\vec{R}}_{f}- m\vec{\dot{\omega}} \times \vec{r} - m\vec{\omega} \times (\vec{\omega} \times \vec{r})-2m\vec{\omega} \times \vec{v}_{r}
$$
What each term represents in physical quantities
- $m \ddot{\vec{R}}_{f}$ is the **translation** of the rotating frame relative to the fixed frame
- $m\dot{\vec{\omega}}\times \vec{r}$ is the angular acceleration of the coordinate system
- $m\vec{\omega} \times (\vec{\omega}\times \vec{r})$ is the centrifugal "force" 
- $-2m\vec{\omega} \times \vec{v}_{r}$ is the Coriolis force

$$
\vec{F} = m\vec{a}_{f}
$$
$$
\vec{F}_{eff} = m\vec{a}_{r} = m\vec{a}_{f} + \text{ non inertial terms}
$$

![[Pasted image 20240327164344.png]]


Forces in the fixed frame
$$
\vec{F}_{f} = m\vec{a}_{r} =\vec{S} + m\vec{g}_{0}
$$
where
$$
\vec{g}_{0} = -\frac{Gm_{\otimes }}{\vec{R}}\vec{\rho}_{r}
$$
See HW 8

> Gravity is different across the world based on lattitudes


![[Pasted image 20240327164524.png]]


$$
\vec{F}_{eff} = \vec{S} +m\vec{g}_{0} - m\ddot{\vec{R}}_{f} -m\vec{R}_{f} -m\vec{\omega} \times (\vec{\omega}\times \vec{r}) -2m\vec{\omega} \times \vec{v}_{r}
$$
For the earth, $\vec{\omega}=\omega \vec{\rho}_{z}$
and $\vec{\dot{\omega}} \approx_{0}$
![[Pasted image 20240327165219.png]]
![[Pasted image 20240327165306.png]]
![[Pasted image 20240327165141.png]]