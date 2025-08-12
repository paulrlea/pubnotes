---
dg-publish: true
---
Continued from [[2024-02-02 General Coordinates Continued]]

![[Pasted image 20240206085832.png]]

We went briefly over two methods to solve the ball rolling down a slope problem. Here is the first method, Substitution 

$$
L=\frac{1}{2}M\dot{x}^{2} + \frac{1}{2}I \frac{\dot{x}^{2}}{R^{2}}-Mg(l-x)\sin \phi
$$
$$
\frac{d}{dt} \frac{ \partial L }{ \partial \dot{x} } -\frac{ \partial L }{ \partial x } =0
$$
$$
\frac{ \partial L }{ \partial \dot{x} } = M\dot{x}+ \frac{I\dot{x}}{R^{2}}\tag{1}
$$
$$
\frac{d}{dt}  (\text{Equation 1}) = M\ddot{x}+\frac{I}{R^{2}}\ddot{x}
$$
$$
\frac{ \partial L }{ \partial x }  = Mg\sin \phi
$$
$$
\left( M+\frac{I}{R^{2}} \right)\ddot{x}-Mg\sin \phi = 0
$$
$$
\ddot{x} =\frac{ Mg\sin \phi}{M+\frac{I}{R^{2}}}
$$
Method 2, using [[Lagrange Multipliers]]
$$
\tilde{L}=L + \lambda f = \frac{1}{2}\dot{x}^{2}M + \frac{1}{2}I\dot{\theta}^{2} - Mg(l-x)\sin \phi+\lambda(x-R\theta)
$$
Resulting equations: 
For x
$$
\frac{d}{dt} \frac{ \partial \tilde{L} }{ \partial \dot{x} } -\frac{ \partial \tilde{L} }{ \partial x } =0
$$
$$
\frac{ \partial \tilde{L} }{ \partial \dot{x} } =M\dot{x}
$$
$$
\frac{d}{dt} \frac{ \partial \tilde{L} }{ \partial \dot{x} } = M\ddot{x} 
$$
$$
\frac{ \partial \tilde{L} }{ \partial x }  = Mg\sin \phi+\lambda
$$
$$
M\ddot{x}-Mg\sin \phi-\lambda=0 \tag{2}
$$
For $\theta$
$$
\frac{d}{dt} \frac{ \partial \tilde{L} }{ \partial \dot{\theta} }  - \frac{ \partial \tilde{L} }{ \partial \theta }  = 0
$$
$$
\frac{d}{dt}  \frac{ \partial \tilde{L} }{ \partial \dot{\theta} } =I \ddot{\theta }
$$
$$
\frac{ \partial \tilde{L} }{ \partial \theta } = -R\lambda
$$
$$
I \ddot{\theta}+ \lambda R=0
$$
Use Acceleration relationships
$$
\ddot{\theta} = \frac{\ddot{x}}{R}
$$
$$
I \frac{\ddot{x}}{R} + \lambda R = 0 \to \lambda = -\frac{I\ddot{x}}{R^{2}}
$$
Plug into equation 2
$$
M\ddot{x}-Mg\sin \phi + \frac{I\ddot{x}}{R^{2}}=0
$$
$$
\ddot{x}\left( M+\frac{I}{R^{2}} \right)=Mg\sin \phi
$$
$$
\ddot{x}= \frac{Mg\sin \phi}{Mr+\frac{I}{R^{2}}}
$$
This matches the last equation! they both give the right answer. Lets solve for $\lambda$ now
$$
\lambda = \frac{-Mg\sin \phi I}{\left( M+\frac{I}{R^{2}} \right)R^{2}} = \frac{-Mg\sin \phi I}{MR^{2}+I}
$$
What is $\lambda$?
After some dimensional analysis, we can determine that it is a force. In fact, you could call it the [[forces of constraint]] (singular). It turns out that in this equation, it is the force of friction on the ball.

For a disk $I = \frac{1}{2}MR^{2}$

$$
\ddot{x} = \frac{Mg\sin \phi}{M + \frac{1}{2}M}  = \frac{2g\sin \phi}{3}
$$
$$
\lambda = \frac{-Mg\sin \phi\left( \frac{1}{2}MR^{2} \right)}{MR^{2}+\frac{1}{2}MR^{2}}=-\frac{1}{3}Mg\sin \phi
$$

![[Pasted image 20240206085844.png]]

$$
\sum F = m\ddot{x}
$$
$$
mg\sin \phi -F = M\ddot{x}
$$
$$
mg\sin\theta-\frac{I\ddot{x}}{R^{2}}=m\ddot{x}
$$

![[Pasted image 20240206085856.png]]
$$
T = I\vec{\alpha} = \vec{r} \times \vec{F} \implies I\alpha = Rf
$$
$$
\frac{I\ddot{x}}{R} = Rf
$$
$$
f = \frac{I\ddot{x}}{R^{2}}
$$

>NB: there will be problems on the exam that require classical Newtonian mechanics


## Conservation laws in Lagrangian Motion
### Conservation of energy 
If the following is true, energy is conserved
1:
$$
\frac{ \partial L }{ \partial t }  = 0
$$
Time is homogeneous, L is invariant under translation in time.
- No explicit time-dependent forces of constraint
2: Kinetic energy is only a function of generalized velocity
$$
T(\dot{q}_{j})\propto \dot{q}_{j}\dot{q}_{k}
$$
3: Velocity and time are independent
$$
u = u (q_{j})
$$
Generalized Lagrangian is
$$
L = L (q_{j},\dot{q}_{j}) = T(\dot{q}_{j})-u(q_{j})
$$


$$
\frac{dL}{dt} (q_{j},\dot{q}_{j},t) = \sum_{j}\left[ \frac{ \partial L }{ \partial {q}_{j} } \dot{q}_{j} + \frac{ \partial L }{ \partial \dot{q} _{j}} \ddot{q}_{j} \right] + \cancel{ \frac{ \partial L }{ \partial t }  } = 0
$$
Remember: 
$$
\frac{d}{dt}  \frac{ \partial L }{ \partial \dot{q} } -\frac{ \partial L }{ \partial q }  = 0 \to \frac{ \partial L }{ \partial q  } = \frac{d}{dt} \frac{ \partial L }{ \partial \dot{q} } 
$$
$$
\frac{dL}{dt} = \sum_{j}\left[ \frac{d}{dt}  \frac{ \partial L }{ \partial \dot{q}_{j} } \dot{q}_{j} + \frac{ \partial L }{ \partial \dot{q}_{j} } \ddot{q}_{j} \right]
$$
$$
\frac{dl}{dt} = \sum_{j} \dots =0
$$
so the sum has to be a constant 
$$
\frac{d}{dt}  \left[  L -\sum_{j} \dot{q}_{j} \frac{dL}{d\dot{q}_{j}} \right] = 0
$$
we can call this constant $-H$
$$
-H = L - \sum_{j}\dot{q}_{j} \frac{ \partial L }{ \partial \dot{q}_{j} } 
$$
for H is constant if $\frac{ \partial L }{ \partial t } =0$
$$
H = \sum_{j} \dot{q}_{j} \frac{ \partial L }{ \partial \dot{q}_{j} - L  } =E
$$
Show H = E
Remember $T(\dot{q}_{j})\propto \dot{q}_{j}\dot{q}_{k}$
$$
\frac{ \partial L }{ \partial \dot{q}_{j} } = \frac{ \partial   }{ \partial \dot{q}_{j} } (T-u) = \frac{ \partial T }{ \partial \dot{q}_{j} } 
$$
if $u=u(q_{j})$
$$
H = \sum \dot{q}_{j} \frac{ \partial T }{ \partial  \dot{q}_{j} }  - L = \sum_{j} \dot{q}_{j} \frac{ \partial T }{ \partial \dot{q}_{j} }  - (T-u)
$$
$$
T = \sum_{j_{1}k} a_{j,k} \dot{q}_{j}\dot{q}_{k}
$$
$$
\frac{ \partial T }{ \partial \dot{q}_{l} } = \sum_{k} q_{l,k} \dot{q}_{k} + \sum_{j}a_{jl}\dot{q}_{j}
$$
$$
\sum_{l} \dot{q}_{l}\frac{ \partial L }{ \partial \dot{q}_{l} }  = \sum_{l,k}a_{l,k}\dot{q}_{l}\dot{q}_{k}+\sum_{l,j}a_{j,l}\dot{q}_{j}\dot{q}_{l} = 2T
$$
So
$$
H = \sum_{j}\dot{q}_{j}\frac{ \partial L }{ \partial \dot{q}_{j} }  - L = 2T - (T-u)
$$
$$
=2T - T+ u= T+ u = E_\text{total}
$$
This is the [[Hamiltonian]], the same one from [[Quantum Physics]]

![[Pasted image 20240217194445.png]]
$$
L = T - u = \frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2}) -mgy
$$
$$
x = l\sin\theta \implies \dot{x} = l\dot{\theta}\cos\theta
$$
$$
y = -l\cos\theta \implies \dot{y} = l\dot{\theta}\sin\theta
$$
$$
H = \sum_{j} \dot{q}_{j} \frac{ \partial L }{ \partial \dot{q}_{j} } \implies H = \dot{\theta} \frac{ \partial L }{ \partial \dot{\theta} } -L
$$
However, lets look at an accelerated [[pendulum]]- 

![[Pasted image 20240217194422.png]]

$$
L = T-u = \frac{1}{2} m(\dot{x}^{2}+ \dot{y}^{2}) -mgy
$$
$$
x = l\sin\theta+\frac{1}{2}at^{2}
$$
$$
\dot{x} = at + l\dot{\theta}\cos\theta
$$
$$
y = -l\cos\theta
$$
$$
\dot{y}=l\dot{\theta}\sin\theta
$$
$$
x^{2} = a^{2}t^{2} + l^{2}\dot{\theta}^{2} \cos ^{2}(\theta) + 2atl\dot{\theta}\cos\theta
$$
where $\frac{ \partial L }{ \partial t } \neq 0$
$$
L = \frac{1}{2}m[a^{2}t^{2}+l^{2}\dot{\theta}^{2}+2atl\dot{\theta}^{2}\cos\theta] + mgl\cos\theta
$$
its not conserved. Makes sense because the system is accelerating

### Conservation of momentum
1: Space is homogeneous, the [[Lagrangian]] is invariant under space translation in the direction of $q_{j}$
$$
\frac{ \partial L }{ \partial q_{j} } = 0 \tag{3}
$$
$$
P_{j} = \frac{ \partial L }{ \partial \dot{q}_{j} } 
$$
> This is our generalized momentum, conserved if (3) is true

In Cartesian coordinates: 
$$
\frac{ \partial L }{ \partial x }  = 0 ,  \ \ P_{i}=\frac{ \partial L }{ \partial \dot{x}_{i} }  \text{ is conserved}
$$
Consider [[Euler-Lagrange Equation]] again
$$
\frac{d}{dt} \frac{ \partial L }{ \partial \dot{q}_{j} } -\frac{ \partial L }{ \partial q_{j} } =0
$$
$$
\frac{d}{dt} \frac{ \partial L }{ \partial \dot{q}_{j} } = \frac{ \partial L }{ \partial q_{j} } = 0?
$$
$$
\frac{ \partial L }{ \partial q_{j} }=\dot{P}_{j} 
$$
Force is the negative [[gradient]] of potential

If we look at the LHS of the above equation, 

$$
\frac{d}{dt} \frac{ \partial L }{ \partial \dot{q}_{j} }  = 0
$$
means that 
$$
\frac{ \partial L }{ \partial \dot{q}_{j}  } = P_{j} = \text{constant }
$$
Newton
$$
\frac{d\vec{P}}{dt} = \vec{F} 
$$
Example: 3d projectile
$$
\vec{F} = \begin{pmatrix}
0 \\
0 \\
-mg
\end{pmatrix}
$$
$$
L = \frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2}+\dot{z}^{2})-mgz
$$
$$
\frac{ \partial L }{ \partial x } = 0 \to \frac{d}{dt} \frac{ \partial L }{ \partial \dot{x} } =0 
$$
$$
\frac{ \partial L }{ \partial \dot{x} }  = P_{x} = \text{constant}
$$
$$
\frac{ \partial L }{ \partial y } = 0 \implies \frac{d}{dt}  \frac{ \partial L }{ \partial \dot{y} } =0
$$
$$
\frac{ \partial L }{ \partial  \dot{y} }  = P_{y} = \text{constant}
$$
$$
\frac{ \partial L }{ \partial z } = - mg
$$
$$
P_{z} \neq \text{constant}
$$
$$
\frac{ \partial L }{ \partial \dot{x} }  = m\dot{x}
$$
$$
\frac{ \partial L }{ \partial \dot{y} }  = m\dot{y}
$$
Another example: [[pendulum]]
Skipping setup, go straight to [[Lagrangian]]
$$
L = \frac{1}{2}ml^{2} \dot{\theta}^{2} + mgl\cos\theta
$$
$$
\frac{ \partial L }{ \partial \theta } = -mgl\sin\theta \neq 0
$$
$$
P_{\theta} \neq \text{constant}
$$
$$
P_{0} = \frac{ \partial L }{ \partial \dot{\theta} } = ml^{2}\dot{\theta} 
$$
[[Angular Momentum]]










