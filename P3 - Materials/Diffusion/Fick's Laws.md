#materials

Diffusion is the thermally-assisted stochastic migration of particles.
## Summary
- The stochastic nature of microscopic movements leads to diffusive transport at large length-scales.
- Fick’s Laws:$$\begin{cases}
\mathbf{J}&=-D\nabla C \\
\frac{\partial C}{\partial t}&=D\nabla ^2C
\end{cases}$$
- Particles spread distances on the order of $\sqrt{ Dt }$, which can be related to the microscopic particle dynamics.
## Microscopic scale
Consider a particle that travels a length scale $\lambda$ in a time $\tau$. From the analysis on [[Elasticity of compliant materials#Random walk|random walks]], we know that the expected distance the particle will move in a time $t$ is:$$r=\sqrt{ n }\lambda=\sqrt{ \frac{t}{\tau} }\lambda$$And this is one standard deviation $\sigma$ of the normal distribution of possible 1D end locations. In more than one dimension the expected distance will still be on this order.
## Macroscopic scale
### Fick’s First Law
Consider the relationship between diffusive flux $\mathrm{[atoms/s/m^2]}$ and concentration gradient. Fick modelled this as directly proportional:$$\mathbf{J}=-D\nabla C$$for constant $D$.
### Fick’s Second Law
This relates how the diffusive flux affects the concentration distribution over time and relates it back to the concentration gradient.$$\frac{\partial C}{\partial t}=D\nabla ^2C$$
>*Proof*. Conserving mass:$$
\begin{align*}
\iiint_{V} \frac{\partial C}{\partial t}\mathrm{d}^{3}\mathbf{r}&= -\iint_{S}\mathbf{J}\cdot \mathrm{d}\mathbf{S}\\
&= -\iiint_{V}\nabla \cdot\mathbf{J}\,\mathrm{d}^{3}\mathbf{r}
\end{align*}$$For this equation to hold for _every_ possible volume V, it is necessary (and sufficient) for the integrands to be equal everywhere.$$\begin{align}
\frac{\partial C}{\partial t} & =-\nabla \cdot \mathbf{J} \\
 & =D\nabla ^{2}C
\end{align}$$
### Combining the micro- and macro-
If we take a 1D delta function $C(x, t=0)=\delta(x)$ as an example, the evolution is$$C(x, t)\sim N(0,\sigma^{2}= 2Dt)$$So the expected distance from the origin of a particle in this example is$$\begin{align}
\sigma & =\sqrt{ 2Dt }=\sqrt{ \frac{t}{\tau} }\lambda \\
 \\
\Rightarrow\quad D & = \frac{\lambda^2}{2\tau}
\end{align}$$In the case of a fixed external concentration of diffusive flux, the solution for $C(x,t)$ will have a linear coefficient of $\mathrm{erf}\left( \frac{x}{2\sqrt{ Dt }} \right)$ due to the integral of the above solution for a delta function source.