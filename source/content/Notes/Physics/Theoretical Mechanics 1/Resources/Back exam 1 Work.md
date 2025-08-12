Problem 1:

Relevant Equations:
$$
F=ma = m \frac{dv}{dt}
$$
$$
F(v) = -F_{0}e^{v/B} =m \frac{dv}{dt}
$$
This is a velocity dependent force.

1a. 

Finding an expression for velocity using separation of variables
$$
-F_{0}e^{v/B}=m \frac{dv}{dt}
$$
$$
dt = \frac{m}{-F_{0}e^{v/B}} dv
$$
Integrate both sides
$$
t = \frac{m}{-F_{0}}\int \frac{1}{e^{v/B}} \, dv
$$
$$
t = \frac{m}{-F_{0}}\int {e^{-v/B}} \, dv
$$

$$
t=\frac{m}{-F_{0}} (-B)e^{-v/B} +c
$$
$$
t = \frac{m}{BF_{0}}e^{-v/B}+c
$$
Solve for V, removing constant and will add in $v_{0}$ at the end
$$
\frac{F_{0}t}{mB}-c= e^{-v/B} 
$$
Take Ln of both side
$$
\ln\left( \frac{F_{0}t}{mB} -c\right) = -\frac{v}{B}
$$
$$
v(t) = -B\ln\left( \frac{F_{0}t}{mB}-c\right) 
$$
Solving for c: 
$$
v(0) = -B\ln\left( 0-c \right)
$$
$$
e^{-v_{0}/B} = -c
$$
$$
c=-e^{-v_{0}/B}
$$
$$
v(t) = -B\ln\left( \frac{F_{0}t}{mB}+e^{-v_{0}/B} \right)
$$
1b. 
$$
0= -B \ln\left( \frac{F_{0}t}{mB}+e^{-v_{0}/B} \right)
$$
Because $B\neq 0$, we have to find the value of t that makes the argument of the $\ln$ function 1, because that will be equal to 0

$$
1 = \frac{F_{0}t}{mB}+e^{-v_{0}/B}
$$
$$
1-e^{-v_{0}/B} = \frac{F_{0}t}{mB}
$$
$$
t = \frac{mB}{F_{0}}(1-e^{-v_{0}/B})
$$
1c. Find the equation of motion
$$
\frac{dx}{dt} = -B\ln\left( \frac{F_{0}t}{mB}+e^{-v_{0}/B} \right)
$$
$$
dx = -B\ln\left( \frac{F_{0}t}{mB}+e^{-v_{0}/B} \right)dt
$$
$$
\int  \, dx =\int \ln\left( \frac{F_{0}t}{mB} +e^{v_{0}/B}\right) \, dt
$$
$$
x(t) = \frac{\frac{F_{0}t}{mB}+e^{v_{0}/B}}{\frac{F_{0}}{mB}}\ln\left( \frac{F_{0}t}{mB} + e^{-v_{0}/B} \right)-t
$$
Problem 2 (special relativity)

Robbers vehicle is traveling at 0.9c. Police vehicle is traveling at 0.75c. Dart traveling at 0.75c relative to police vehicle. 
$$
v' = \frac{v_{1}-v_{2}}{1- \frac{v_{1}v_{2}}{c^{2}}}
$$
$$
v' = \frac{v_{1}+v_{2}}{1+\frac{v_{1}v_{2}}{c^{2}}}
$$
$$
v' = \frac{3/4+3 / 4}{1+ 9/16}
$$
$$
v' = \frac{6/ 4}{25/16}
$$
$$
v' = \frac{6}{4} \cdot \frac{16}{25}
$$
$$
v'=\frac{96}{100}
$$
$$
v' = \frac{24}{25} > \frac{9}{10}
$$
Therefore the dart will catch up.

Question 3. Relativistic Lagrangian 
$$
L(x,\dot{x}) = -mc^{2}\sqrt{ 1-\frac{\dot{x}^{2}}{c^{2}} }-\frac{1}{2}kx^{2}
$$
Equations of motion 
$$
\frac{d}{dt} \frac{ \partial L }{ \partial \dot{x} } -\frac{ \partial L }{ \partial {x} }  =0 
$$
$$
-mc^{2}\left( 1-\frac{\dot{x}^{2}}{c^{2}} \right)^{1/2}-\frac{1}{2}kx^{2}
$$
$$
\frac{ \partial L }{ \partial \dot{x} }  = \frac{2mc^{2}\dot{x}}{2c^{2}}\left( 1-\frac{\dot{x}^{2}}{c^{2}} \right)^{-1/2}
$$
$$
\frac{ \partial L }{ \partial \dot{x} }= \frac{m\dot{x}}{\sqrt{ 1-\frac{\dot{x}^{2}}{c^{2}} }}
$$
$$
\frac{ \partial L }{ \partial \dot{x} } = m\dot{x}\left( 1-\frac{\dot{x}^{2}}{c^{2}} \right)^{-1/2}
$$
$$
\frac{d}{dt} \frac{ \partial L }{ \partial \dot{x}} = m\ddot{x}\left( 1-\frac{\dot{x}^{2}}{c^{2}} \right)^{-1/2} - \frac{\ddot{x}^{2}}{2c^{2}}m\dot{x}\left( 1-\frac{\dot{x}^{2}}{c^{2}} \right)^{-3/2}
$$
$$
\frac{ \partial L }{ \partial x }  = -\frac{1}{2}2kx
$$
$$
\frac{ \partial L }{ \partial x }  =-kx
$$
Euler Lagrange Equation 
$$
m\ddot{x}\left( 1-\frac{\dot{x}^{2}}{c^{2}} \right)^{-1/2} - \frac{\ddot{x}^{2}}{2c^{2}}m\dot{x}\left( 1-\frac{\dot{x}^{2}}{c^{2}} \right)^{-3/2} + kx = 0
$$
At non-relativistic speeds
$$
m\ddot{x}\left( 1-\cancel{ \frac{\dot{x}^{2}}{c^{2}} } \right)^{-1/2} - \cancel{ \frac{\ddot{x}^{2}}{2c^{2}}m\dot{x}\left( 1-\frac{\dot{x}^{2}}{c^{2}} \right)^{-3/2} } + kx = 0
$$
$$
m\ddot{x} +kx = 0
$$

Question 4. Lagrangian Mechanics 

a. Find the Lagrangian of the system
+y is up, +x is to the right
$$
L=T-U
$$
$$
T = \frac{1}{2}mv^{2}, U=mgh
$$
$$
x=L\cos\theta ; \ \ \dot{x} = \dot{L}\cos\theta - L\dot{\theta}\sin\theta
$$
$$
y =L\sin\theta; \ \dot{y} = \dot{L}\sin\theta +L\dot{\theta}\cos\theta
$$
$$
T = \frac{1}{2}m(\sqrt{(\dot{L}\cos\theta-L\dot{\theta}\sin\theta)^{2}+(\dot{L}\sin\theta +L\dot{\theta}\cos\theta)^{2} }^{2}
$$
$$
T = \frac{1}{2}m((\dot{L}\cos\theta-L\dot{\theta}\sin\theta)^{2}+(\dot{L}\sin\theta +L\dot{\theta}\cos\theta)^{2})
$$
$$
T=\frac{1}{2}m((\dot{L}^{2}\cos ^{2}\theta+L^{2}\dot{\theta}^{2}\sin ^{2}\theta-2\dot{L}L\dot{\theta}\cos\theta \sin\theta)\dots
$$
$$
+(\dot{L}^{2}\sin ^{2}\theta + L^{2}\dot{\theta}^{2}\cos^{2}\theta+2\dot{L}L\dot{\theta}\sin\theta \cos\theta))
$$
$$
T = \frac{1}{2}m((\dot{L}^{2}\cos ^{2}\theta+L^{2}\dot{\theta}^{2}\sin ^{2}\theta)+(\dot{L}^{2}\sin ^{2}\theta+L^{2}\dot{\theta}^{2}\cos ^{2}\theta)
$$
$$
T=\frac{1}{2}m(\dot{L}^{2}(\cos ^{2}\theta + \sin ^{2}\theta) + L\dot{\theta}^{2}(\cos ^{2}\theta + \sin ^{2}\theta))
$$ $$
T = \frac{1}{2}m(\dot{L}^{2}+L\dot{\theta}^{2})
$$
$$
U = mg(L\cos\theta)
$$
$$
L = \frac{1}{2}m(\dot{L}^{2}+L\dot{\theta}^{2}) +mg(L\cos\theta)
$$
Sub in $\alpha$ and apply small angle approx.
$$
L = \frac{1}{2}m(\alpha^{2}+L\dot{\theta}^{2}) + mgL
$$

Solve the [[Euler-Lagrange Equation]]
$$
L = \frac{1}{2}m\alpha^{2}+\frac{1}{2}mL\dot{\theta}^{2}+mgL\cos\theta
$$
$$
\frac{ \partial L }{ \partial \dot{\theta} } = mL\dot{\theta}
$$
$$
\frac{d}{dt} \frac{ \partial L }{ \partial \dot{\theta} } =m\dot{L}\dot{\theta} + mL \ddot{\theta}
$$
$$
\frac{ \partial L }{ \partial \theta } = mg\dot{L}\cos\theta - mgL\sin\theta 
$$

















