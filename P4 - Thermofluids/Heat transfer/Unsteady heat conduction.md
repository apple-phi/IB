Consider the case with internally generated heat $G$ per unit volume,
$$
\begin{align*}
\iiint_{V} \rho c\frac{\partial T}{\partial t}\mathrm{d}^{3}\mathbf{r}&= -\iint_{S}\mathbf{q}\cdot \mathrm{d}\mathbf{S} + \iiint_{V}G  \,\mathrm{d}^{3}\mathbf{r} \\
&= \iiint_{V}(G-\nabla \cdot\mathbf{q})\,\mathrm{d}^{3}\mathbf{r}
\end{align*}
$$
For this to hold for every possible volume $V$
$$
\begin{align}
\rho c\frac{\partial T}{\partial t}  & = -\nabla \cdot \mathbf{q}+G \\
 \\
\Rightarrow\quad \frac{\partial T}{\partial t} &=\alpha \nabla^{2}T+\frac{G}{\rho c}
 \end{align}
$$
by applying Fourier’s law where $\alpha=\frac{\lambda}{\rho c}$

## Conduction in a semi-infinite slab
![[heat-cond-semi-inf-slab.png|600]]
$$
\theta= \frac{T-T_{0}}{T_{s}-T_{0}}=1-\operatorname{erf}\left( \frac{x}{2\sqrt{ \alpha t }} \right)
$$
Generally, the characteristic time for heat to penetrate a distance $x$ is 
$$
t= \frac{s^{2}}{\alpha}
$$
where $s$ is a characteristic length dimension of the body.

Another useful non-dimensional group is the Fourier number.
$$
\begin{align} 
\mathrm{Fo}&= \frac{\mathrm{time,}\,\tau}{\text{characteristic time for heat diffusion}} \\
&= \frac{\alpha \tau}{s^{2}}
 \end{align}
$$
>A body can be considered to have heated up when $\mathrm{Fo}>1$

## Lumped heat capacity
Consider a lump of material assumed to have no internal temperature gradient.
$$
V\rho c\frac{\mathrm{d} T}{\mathrm{d}t} =hA(T_{\infty}-T)
$$
With initial condition $T(t=0)=T_{0}$ the solution is
$$
\frac{T-T_{\infty}}{T_{0}-T_{\infty}}=\exp\left( -\frac{t}{\tau_{c}} \right)
$$
where $\tau_{c}=\frac{V\rho c}{hA}$

This assumption of negligible internal temperature gradient is valid when
$$
\begin{align}
\mathrm{Bi}=\frac{\text{internal thermal resistance}}{\text{surface thermal resistance}} & =\frac{\frac{s}{\lambda A}}{\frac{1}{hA}} \\
&= \frac{hs}{\lambda}\ll 1
 \end{align}
$$
where $\mathrm{Bi}=\frac{hs}{\lambda}$ is the Biot number. The condition $\mathrm{Bi}<0.1$ is often used as an acceptable condition for a lumped heat capacity analysis.
