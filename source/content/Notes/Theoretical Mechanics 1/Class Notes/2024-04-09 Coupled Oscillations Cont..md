---
dg-publish: true
---
# Summary from [[2024-04-05 General Coupled Oscillations]]

- Normal frequencies given by $\omega_{r}$ (eigenfrequencies)
- Eigenvectors  $\vec{a}_{r}$ with $a_{gr}$ composition
$$
\sum_{j} (A_{jk}q_{j}j+m_{jk} \ddot{q}_{j})=0
$$
Guessing
$$
q_{j}(t) = a_{j}e^{i(\omega t-\delta)}
$$
Given this
$$
\sum_{j}(A_{jk} - \omega^{2}m_{jk})a_{j}=0
$$
$$
\det |A_{jk} - \omega^{2}m_{jk}| =0
$$
to find $\omega_{r}$
## Revisiting first example of coupled oscillations with new notation 

> figure 1 

$$
T=\frac{1}{2}m\dot{x}^{2}_{1} + \frac{1}{2}m\dot{x}_{2}^{2}
$$
$$
u= \frac{1}{2}\kappa x_{1}^{2}+\frac{1}{2}\kappa x_{2}^{2}+\frac{1}{2}\kappa_{12} (x_{1}-x_{2})^{2}
$$
$$
u = \frac{1}{2} ( \kappa+\kappa_{12})x_{1}^{2} + \frac{1}{2}(\kappa+\kappa_{12})x_{2}^{2} -\kappa_{12}x_{1}x_{2}
$$
$$
\begin{matrix}
q_{1}=x_{1} & \dot{q}_{1} = \dot{x}_{1} \\
q_{2}=x_{2} & \dot{q}_{2} = \dot{x}_{2}
\end{matrix}
$$
$$
T=\frac{1}{2} m(\dot{x}_{1}^{2}+\dot{x}_{2}^{2})
$$
$$
=\frac{1}{2}m(\dot{q}_{1}^{2}+\dot{q}^{2}_{2})
$$
$$
T=\frac{1}{2}\sum_{jk} m_{jk} \dot{q}_{j}\dot{q}_{k}
$$
$$
\frac{1}{2} m_{11} \dot{q}_{1}\dot{q}_{1} \leftrightarrow  \frac{1}{2 }m\dot{q}_{1}^{2}
$$
$$
m_{11}=m=m_{22}
$$
$$
m_{12}=m_{21}=0
$$

Revisit this 
$$
u = \frac{1}{2} ( \kappa+\kappa_{12})x_{1}^{2} + \frac{1}{2}(\kappa+\kappa_{12})x_{2}^{2} -\kappa_{12}x_{1}x_{2}
$$
$$
A_{jk} = \frac{ \partial^{2} u }{ \partial q_{j} \partial q_{k} } 
$$
$$
A_{11}=\kappa+\kappa_{12}
$$
$$
A_{22} = \kappa+\kappa_{12}
$$
$$
A_{12}=A_{21} = -\kappa_{12}
$$
$$
\det|A_{jk} -\omega^{2} m_{jk}|=0
$$
$$
\det \begin{pmatrix}
(\kappa+\kappa_{12})-\omega^{2}m & \kappa_{12} \\
-\kappa_{12} & (\kappa+\kappa_{12})-\omega^{2}m
\end{pmatrix}=0
$$
$$
\omega = \sqrt{ \frac{\kappa+\kappa_{12} \pm\kappa_{12}}{2} }
$$
$$
\omega_{1} = \sqrt{\frac{\kappa+2\kappa_{12}}{m}}
$$
and 
$$
\omega_{2}=\sqrt{ \frac{\kappa}{m} }
$$
The eigenvectors $\vec{a}_{r}$ will form an orthogonal set. This set can be normalized to create an orthonormal set. This is shown mathematically in section 12. 5 (pg. 481) of the textbook. 
In this process to create an orthonormal set of eigenvectors, the ambiguity of $q_{j}$ is removed by the normalization of $a_{jr}$, so we must introduce a scale factor, $\alpha_{r}$which is dependent on the initial conditions. 

so
$$
q_{j}(t)  \sum_{r} a_{jr}\cos(\omega_{r}t-\delta_{r})
$$
or- 

$$
q_{j}(t)=\sum_{r}a_{jr} e^{i(\kappa rt-\delta r)}
$$
Normalized: 
$$
q_{j}(t) = \sum_{r}\alpha_{r} a_{jr} e^{i(\omega _{r}t-\delta_{r})}
$$
$$
=\sum_{r} \beta_{r} a_{jr} e^{i\omega_{r}t}
$$
Where $\beta_{r}$ is a new scale factor (complex) which incorporates phase $\delta_{r}$
- Defining a quantity $\eta_{r}(t)=\beta_{r}\epsilon^{i\omega_{r}t}$ such that 
$$
q_{j}(t)= \sum_{r} a_{jr}\eta_{r}(t)
$$
- This recovers our normal coordinates (only oscillates at one frequency)
- $\eta_{r}(t)$ is normal coordinate

From our example
$$
\det\begin{bmatrix}
\kappa+\kappa_{12} -m\omega^{2} & -\kappa_{12} \\
-\kappa_{12} & \kappa+\kappa_{12} -m\omega^{2}
\end{bmatrix}=0
$$
Found $\omega_{1}$ and $\omega_{2}$

To find $a_{jr}$ components we only need 1 equation (for this 2 mass case) since we are only after a ratio of components $\frac{a_{1r}}{a_{2r}}$

$$
r=1
$$
$$
\omega^{2}_{1}= \left( \sqrt{ \frac{\kappa+2\kappa_{12}}m } \right)^{2}= \frac{\kappa+2\kappa_{12}}{m}
$$
Eigenvector $\vec{a}_{1}$ with components $a_{11}$ and $a_{21}$
Choose first equation: 
$$
(A_{11}-m_{11}\omega_{1}^{2}) a_{11}+ (A_{12}-m_{12}\omega_{1}^{2})a_{12}=0
$$
$$
[\kappa+\kappa_{12}-m(\kappa+2\kappa_{12})]a_{11}- \kappa_{12} a_{21}=0
$$
$$
-\kappa_{12} a_{11} - \kappa_{12}a_{21} = 0
$$
$$
-a_{11} = a_{21}
$$
The general equation of motion: 
$$
q_{j}(t) = \sum_{r} a_{jr} \eta_{r}(t)
$$
$$
q_{1}(t) = a_{11} \eta_{1} + a_{12}\eta_{2}
$$
$$
q_{2}(t) = a_{21} \eta_{1} + a_{22}\eta_{2}
$$
Use the fact that $-a_{11} = a_{21}$

Rewrite: 
$$
q_{1}(t) = a_{11} \eta{1} + a_{22}\eta_{2}
$$
$$
q_{2}(t) = -a_{11} \eta_{1} + a_{22}\eta_{2}
$$
So now we can find normal coordinates; 
$$
q_{1}+q_{2} = 2a_{22} \eta_{2}
$$
$$
q_{1}-q_{2} = 2a_{11} \eta{1}
$$
$$
\eta_{2} = \frac{1}{2a_{22}} (q_{1}+q_{2})
$$
$$
\eta_{1} = \frac{1}{2a_{11}} (q_{1}-q_{2})
$$

Can use these relationships to ask what conditions are needed for only 1 coordinate to oscillate. 
$\eta_{1}=0$  if $q_{1}=q_{2}$, therefore $q_{1}=q_{2}$ makes only $\eta_{2}$ oscillate with frequency $\omega_{2} = \sqrt{ \frac{\kappa}{m} }$, which is "in-phase" oscillation. 
$\eta_{2}=0$ if $q_{1}=-q_{2}$ therefore, opposite to the above, $q_{1}=-q_{2}$ makes only $\eta_{1}$ oscillate with frequency $\omega_{1} = \sqrt{ \frac{\kappa+\kappa_{12}}{m} }$, an "out-of-phase" oscillation.

## Molecular Vibrations (12.7)
Good application of small oscillations
In 3 dimensions a molecule with n atoms will have 3n degrees of freedom. 

3 degrees of freedom for translation, 3 degrees of freedom for rotation 

3n-6 degrees of vibrational freedom

If the molecule is colinear then there is 3n-5 degrees of vibration freedom. 

