---
dg-publish: true
---


[[Diamagnetism]]
[[Paramagnetism]]
[[ferromagnetism]]

The magnetic vector potential $\vec{A}$ of a magnetized object is given by
$$
\vec{A}(\vec{r}) = \frac{\mu_{0}}{4\pi} \int _{V} \frac{\vec{j}_{b}(\vec{r}')}{|\vec{r}-\vec{r}'} \, dV' + \frac{\mu_{0}}{4\pi}\oint \frac{k_{b}(\vec{r}')}{|\vec{r}- \vec{r}'|} da'
$$
![[Pasted image 20240229145625.png]]

$$
\mathbf{B} = \nabla \times \mathbf{A}
$$
$$
\nabla \times \mathbf{B} = \mu_{0}\mathbf{J}
$$
$$
\nabla \times  \mathbf{A} = \left[ \frac{1}{s}\frac{ \partial A_{z} }{ \partial \phi }- \frac{ \partial A_{\phi} }{ \partial z }  \right]\hat{s} + \left[ \frac{ \partial A_{s} }{ \partial z } - \frac{ \partial A_{z} }{ \partial s }  \right]\hat{\phi} + \frac{1}{s}\left[ \frac{ \partial  }{ \partial s } (sA_{\phi}) - \frac{ \partial A_{s} }{ \partial \phi }  \right] \hat{z}
$$
$$
k=A_{\phi}
$$
$$
\nabla \times \mathbf{A } = \left[ \frac{1}{s}(0)-0 \right]\hat{s}+0+\frac{1}{s}\left[ \frac{ \partial  }{ \partial s } (sk)-0 \right]\hat{z} = \frac{k}{s}\hat{z}
$$
$$
\mathbf{B}=\frac{k}{s}\hat{z} = \mathbf{B}_{z}
$$
$$
\nabla \times \mathbf{B} = \mu_{0}\mathbf{J}
$$
$$
\nabla \times \mathbf{B} = \dots + \left[ \frac{ \partial \mathbf{B_{s}} }{ \partial z }-\frac{ \partial \mathbf{B_{z}} }{ \partial s }   \right]\hat{\phi} + \dots = \left[ 0+\frac{k}{s^{2}} \right]\hat{\phi}  = \frac{k}{s^{2}} \hat{\phi}=\mathbf{J} \mu_{0}
$$
$$
\mathbf{J} = \frac{k}{s^{2}\mu_{0}} \hat{\phi}
$$
![[Pasted image 20240229153917.png]]





