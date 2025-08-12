---
dg-publish: true
---

## Scattering Cross Sections 
![[Attachments/Pasted image 20240318194056 1.png]]
In the above diagram, we have 2 particles, m1 and m2 with a repulsive force acting between them. 
- The **impact parameter**, $b$ represents the distance between m1 and m2 if there were no force. The impact parameter is related to the angular momentum, mass and potential energy in the following equation 
$$
l_{m_{1}} = m_{1} u_{1} b
$$
This can be rewritten into the following with the equation for initial kinetic energy: $T_{0} = \frac{1}{2}m_{1}u_{1}^{2}$
$$
l = b \sqrt{ 2m_{1}T_{0} }
$$
- In some cases, we cannot take a measurement of $b$. This is often the case in nuclear or atomic physics. 
- In these cases, we introduce the concept of a differential scattering cross section, denoted by $\sigma(\theta)$
-  This is the measure of the number of interactions on the impacted particle that lead to scattering into the solid angle $d\Omega'$ at the angle $\theta$, over the number of particles incident per unit area.
For example, if you have $dN$ particles scattered into $d\Omega'$ per unit time, then the probability is given by 
$$
\sigma(\theta)d\Omega' = \frac{dN}{I}
$$
Where I is the intensity of incoming particles

The relation between the impact parameter and scattering angle ($\Theta$) is given by the following equation 
$$
\Delta\Theta = \int\limits_{r_\text{min}}^{r_\text{max}} \frac{l/r^{2}}{\sqrt{ 2\mu\left[ E-U-\left( \frac{l^{2}}{2\mu r^{2}} \right) \right] }} \, dr
$$


### Central Force Problems 
![[Attachments/Pasted image 20240318203833 1.png]]
For rotational symmetry about the direction of motion of the incoming beam of particles we can define a ring around the approaching beam of thickness $db$ like in the above figure. We can also set the angles $\alpha$ and $\beta$ in the diagram below equal to each other, and $\Theta$, the scattering angle. 
![[Attachments/Pasted image 20240318204040 1.png]]

Therefore, $\theta = \pi-2\Theta$, and the scattering angle $\Theta$ is given by the following integral
$$
\int\limits_{r_\text{min}}^{\infty} \frac{\frac{b}{r^{2}}}{\sqrt{ 1-\left( \frac{b^{2}}{r^{2}} \right)-\left( \frac{U}{T_{0}'} \right) }} \, dr
$$ 
using the modified initial kinetic energy equation from above, $l=b\sqrt{ 2\mu T_{0}' }$



We can use this axial symmetry of the beam to 
Total potential energy

$$
u = \sum^{n}_{i=1}u_{i} + \sum_{i<j} u_{ij}
$$
The first term is the potential from external forces, the second term is known as [[interaction potential]]. 

## 2 particle collision 
Recall there is [[Elastic collisions]] and [[Inelastic collisions]]

Consider a collisions in the lab frame: 

$$
\frac{1}{2}m_{1} \vec{v}_{1}^{2}+ \frac{1}{2}m_{2} \vec{v}_{2}^{2} = \frac{1}{2}m_{1} \vec{v}_{1}'^{2} + \frac{1}{2} m_{2} \vec{v}_{2}'^{2}
$$
 Where $v_{i}'$ is post collision velocity

Similarly:

$$
m_{1}\vec{v}_{1} + m_{2}\vec{v}_{2} = m_{1} \vec{v}_{1}' + m_{2}\vec{v}_{2}' = m_\text{tot}\vec{V}_\text{tot}
$$
$$
\therefore  \sum \vec{p}_{i} = \vec{P}_\text{tot}
$$
Same collision viewed from thze center of mass frame
$$

$$
Since center of mass frame and center of mass at rest in the center of mass at rest in the center of mass frame are the same 

$$
\vec{v}_{2}^{*} = \frac{m_{1}}{m_{2}} \vec{v}_{1}^{*}, \ \ \vec{v}_{2}^{*} = -\frac{m_{1}}{m_{2}}\vec{v}_{1}'^{*}
$$
Vectors are anti-parallel, means the two particles approach head on in the center of mass frame. 

> figure 1 here


Scattering angle is the same, not generally true in the lab frame. 

Consider now kinetic energy in the center of mass frame: 
$$
\frac{1}{2}m_{1}\vec{v}_{1} ^{2} + \frac{1}{2} m_{2}\vec{v}_{2}^{*^{2}}= \frac{1}{2} m_{1} \vec{v}_{1}{^{*^{2}}} + \frac{1}{2} m_{2} \vec{v}_{2}'^{*^{2}}
$$
This can be rewritten as 
$$
\frac{1}{2} m_{1}\vec{v}^{*^{2}}_{1}+\frac{1}{2}m_{2} \frac{m_{1}^{2}}{m_{2}^{2}} \vec{v}_{1}^{*^{2}}=\frac{1}{2}m_{1}\vec{v}_{1}^{*^{2}} + \frac{1}{2} m_{2}\frac{m_{1}^{2}}{m_{2}^{2}} \vec{v}_{1}'^{*^{2}}
$$
or 
$$
\frac{1}{2}\left( m_{1}+\frac{m_{1}^{2}}{m_{2}} \right) \vec{v}_{1}^{*^{2}} = \frac{1}{2} \left( m_{1} + \frac{m_{1}^{2}}{m_{2}} \right)\vec{v}_{1}' ^{*^{2}}
$$
Since elastic 
$$
T^{*} = T'^{*}
$$
Meaning 
$$
|\vec{v}_{1}^{*}| = |\vec{v}_{1}'^{*}|
$$
and 
$$
|\vec{v}_{2}^{*}| = |\vec{v}_{2}'^{*}|
$$
Laboratory system: 

> insert figure 2 here 

m2 is at rest 
$$
\vec{R} = \frac{m_{1}\vec{r}_{1}+m_{2}\vec{r}_{2}}{m_{1}+m_{2}}
$$
$$
\dot{\vec{R}} = \frac{m_{1}}{m_{1}+m_{2}}\vec{v}_{1}
$$
Center of mass system: 

$$
\vec{r}_{1}^{*} = \vec{r}_{1}-\vec{R}
$$
$$
\vec{r}_{2}^{*}  = \vec{r}_{2}-\vec{R}
$$

> figure 3 here 


### Trajectories in lab frame 
$$
m_{1}\vec{v}_{1} + m_{2}\vec{v}_{2} = m_{1}\vec{v}_{1}' + m_{2}\vec{v}_{2}' = m \dot{\vec{R}}
$$
Seperating in 2d
X component
$$
m_{1}v_{1} = m_{1}v_{1}'\cos \psi + m_{2}v_{2}' +\cos \xi
$$
Y component
$$
0=m_{1}v_{1}' \sin \psi + m_{2}v_{2}' \sin \xi 
$$
- This is because the momentum upwards is the same as the momentum downwards

### Trajectories in COM frame

> figure 4

$$
\dot{\vec{R}}=0 \ \ \ \ \ \ m_{1}\vec{v}_{1}^{*} +m_{2}\vec{v}_{2}^{*} = m_{1}\vec{v}_{1}'^{*} + m_{2}\vec{v}_{2}'^{*}=0
$$
Relationship between $\psi, \xi$ in lab frame with angle $\theta$ in lab frame

$$
\vec{r}_{i} ^{*} = \vec{r}_{i} - \vec{R} \tag{1}
$$
$$
\vec{v}_{i}^{*} = \vec{v}_{i}- \dot{\vec{R}} \tag{2}
$$
$$
\vec{v}_{i}'^{*} = \vec{v}'_{i} - \dot{\vec{R}} \tag{3}
$$
$$
\vec{R} = \frac{m_{1}\vec{r}_{1}+ m_{2}\vec{r}_{2}}{m_{1}+m_{2}}
$$
$$
\dot{\vec{R}} = \frac{m_{1}}{m_{1}+m_{2}} \dot{\vec{v}_{1}}
$$
Break eq. 3 into components
x: 
$$
v_{1}'^{*} \cos\theta = v_{1}'\cos \psi  - \frac{m_{1}}{m_{1}+m_{2}}v_{1} \tag{1a}
$$
$$
v_{1}'^{*} \cos\theta +\frac{m_{1}}{m_{1}-m_{2}}v_{1} = v_{1}\cos \psi \tag{2a}
$$
y:
$$
v_{1}'^{*} \sin\theta = v_{1}'\sin \psi \tag{3a}-0
$$
$v_{1}$ is only in the x direction 
$$
v_{1}'^{*} \sin\theta = v_{1}' \sin \psi \tag{4a}
$$
$$
\frac{(4a)}{(2a)}= \frac{v_{1}'^{*}\sin\theta}{v_{1}'^{*}\cos\theta   \frac{m_{1}}{m_{1}+m_{2}}v_{1}} = \tan \psi
$$
$$
v_{1}'^{*} = v_{1}^{*}
$$
$$
v_{1}'^{*} = v_{1}-\dot{\vec{R}}
$$
$$
v_{1}^{*} = v_{1} - \frac{m_{1}}{m_{1}+m_{2}}v_{1} = v_{1}\left[ \frac{m_{1}+m_{2}}{m_{1}+m_{2}} - \frac{m_{1}}{m_{1}+m_{2}} \right]
$$
$$
v_{1}^{*}=\frac{m_{2}}{m_{1}+m_{2}} v_{1} = v_{1}^{*'}
$$
$$
\tan \psi = \frac{\sin\theta}{\cos\theta + \frac{m_{1}}{m_{1}+m_{2}}v_{1} \frac{1}{v_{1}'^{*}}}
$$
$$
\tan \psi = \frac{\sin\theta}{\cos\theta +\frac{m_{1}}{m_{2}}}
$$
Testing this for edge cases 
$$
m_{1} \ll m_{2} \to \tan \psi \approx \tan\theta \therefore \psi \approx\theta
$$
$$
m_{1}=m_{2} \tan \psi = \frac{\sin\theta}{\cos\theta+1} = \tan \frac{\theta}{2}
$$
Similar correct method for product 2
$$
\tan \xi = \tan\left( \frac{\pi}{2} - \frac{\theta}{2} \right)
$$
$$
m_{1}=m_{2} \xi + \psi =\frac{\pi}{2}
$$




