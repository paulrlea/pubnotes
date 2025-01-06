---
dg-publish: true
---
The Inertia Tensor can be described as a general description of how the mass of a rigid body is distributed relative to all of the axes of distribution. 
- Inertia tensor takes the form of a 3x3 matrix. 
- It will change based on how you describe your coordinates. 
- Can be also thought of how "hard" it is to spin an object from a **specific axes**. Think of spinning a meter-stick at the end or the middle.

$$
\{I\} = \begin{pmatrix}
I_{11} & I_{12} & I_{13} \\
I_{21} & I_{22} & I_{23} \\
I_{31} & I_{32} & I_{33} \\
\end{pmatrix}
$$
Where 
$$
I_{11} = \sum_{\alpha} m_{\alpha} \left( \sum_{k} x_{\alpha,k}^{2}-x_{\alpha ,1}x_{\alpha,1} \right)
$$
$$
=\sum_{\alpha} m_{\alpha} (\vec{r}_{\alpha}^{2} - x_{\alpha,1}^{2}) = \sum_{\alpha} m_{\alpha} (x_{\alpha,2}^{2}+x^{2}_{\alpha,3})
$$
$$
\{I\} = \begin{pmatrix}
\sum_{\alpha} m_{\alpha}(x_{\alpha,2}^{2}+x_{\alpha,3}^{2}), & -\sum_{\alpha} m_{\alpha}(x_{\alpha,1}x_{\alpha,2}),  & -\sum_{\alpha} m_{\alpha}x_{\alpha,1}x_{\alpha,3} \\
-\sum_{\alpha} m_{\alpha}x_{\alpha,2}x_{\alpha,1}, & \sum_{\alpha} m_{\alpha}(x_{\alpha,1}^{2}+x_{\alpha,3}^{2}),  & -\sum_{\alpha} m_{\alpha}x_{\alpha,2}x_{\alpha,3} \\
-\sum_{\alpha} m_{\alpha}x_{\alpha,3}x_{\alpha,1}, & -\sum_{\alpha} m_{\alpha}x_{\alpha,3}x_{\alpha,2},  & \sum_{\alpha} m_{\alpha}(x_{\alpha,1}^{2}+x_{\alpha,2}^{2})
\end{pmatrix}
$$
This is the general inertia tensor for particles

