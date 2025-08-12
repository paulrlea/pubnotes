2/28/2025

  

After re-reading the assignment details, I realized that the three body motion was meant to be modeled after an orbital system with a star, planet and moon, not 3 similiarly massive objects. I adjusted the initial masses appropriately, and solved for orbital motion using the following relation due to the large difference in masses.

$$

v = \sqrt{ \frac{GM}{r} }

$$

Placing the star in a stationary position in the middle of the system, we can solve for the orbital speed of the planet and moon. The values in the briefing consist of the following:

$$

\begin{cases}

r_{12} & : 1 \\

r_{23} & : 0.0025 \\

m_{1} & : 1 \\

m_{2} & :3\times 10^{-6} \\

m_{3} & :3.6 \times 10^{-8} \\

  

\end{cases}

$$

The simplest method to calculate the velocities would consist of placing all three bodies in a vertical line, and calculating the relative velocities. This yields the following:

$$

v_{12} = \sqrt{\frac{ 1 \times 1 }{1}} = 1

$$

$$

v_{23} = \sqrt{\frac{ 1\times 3 \times 10^{-6}}{0.0025} } \approx 0.03464

$$

And adding them together we get the total orbital velocity of body 3 to be 1.03464. These values yielded a stable 3 body orbital motion.


$$
\mathbf{\vec{F}}_{12} = \frac{G m_1 m_2}{|\mathbf{r}_{12}|^3} \mathbf{r}_{12}
$$

$$
y_{n+1} = y_n + \Delta t  \frac{dy}{dt} f(t_n, y_n)

$$
$$
F = ma
$$
$$
a = \frac{dv}{dt} = \frac{dx^{2}}{d^{2}t} ;  \ \ \ v = \frac{dx}{dt}
$$
$$
x(t+\Delta t) = x(t) + \Delta t \cdot v(t) + \Delta t^{2} \frac{F(t)}{2m}
$$
$$
v(t + \Delta t) = v(t) + \Delta t \frac{F(t)+ F(t+\Delta t)}{2m}
$$

