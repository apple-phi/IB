#materials
## Summary
- The elasticity of flexible polymer chains is due to entropy
- The larger the end-to-end distance of a chain, the higher number of possible microstates there are
- A flexible chain with $n$ monomers of size $a$ has:
	- a radius of gyration (mean end-to-end distance) $r_{g}=\sqrt{n}a$
	- an entropic spring constant of $\frac{k_{B}T}{r_{g}^{2}}=\frac{k_{B}T}{na^{2}}$
## The origins of compliance
### Polymers
- Below the glass transition temperature $T_g$, there is insufficient thermal energy for the chains to easily slide past each other, so stiffness is dominated by the covalent bonding in the chains themselves
- Above $T_g$, they display viscoelasticity
### Elastomers
- These are cross-linked polymer networks, e.g. rubber, which has sulphur cross-links due to *vulcanisation*
- They behave like polymers below $T_g$, but have a higher stiffness than polymers above $T_g$

The following diagram shows the effect of these cross-links:

![[polymer-elastomer stiffness.png]]

## Polymer thermodynamics
Consider a single polymer chain with length $L$ and end-to-end distance $r$. The [[Laws of Thermodynamics#The First Law of Thermodynamics|First Law of Thermodynamics]] tells us that$$\mathrm{d}U=\overbrace{\delta Q}^{\text{in}}-\underbrace{\delta W}_{\text{out}}$$If this chain reversibly deforms by a distance $\delta r$ due to an external force $f$, then the work done into the system is $-\delta W=+f \delta r$ so $$T\mathrm{d}S=\mathrm{d}U-f \delta r$$Assuming a fully flexible chain with $r\ll L$, the contribution of bond stretching to $\mathrm d U$ is negligible so $U=U(T)$ only, i.e. $\frac{\partial U}{\partial r}=0$ thus$$T\frac{\partial S}{\partial r}=-f$$To solve this we need an expression for $\frac{\partial S}{\partial r}$.
### Random walk
The radius of gyration is the RMS end-to-end displacement,$$r_{g}=\sqrt{{\left|\mathbf{r}\right|}^2}=\sigma$$and is mathematically equivalent to the standard deviation in the node distribution. Consider a single node covalently linked to the origin node with an average radius of gyration $a$ which can be described by the continuous random variable$$X'\sim\mathrm N(0, a^{2})$$Let $X=\sum\limits {X'}$, the sum of multiple observations of $X'$. Then,$$\begin{align*}
X(r)&\sim\mathrm N\left(0,\sigma^{2}=na^{2}\right)\\
&\propto \frac{1}{\sigma}\exp(-\frac{r^{2}}{2\sigma^{2}})
\end{align*}$$$X(r)$ is the probability density function of the end-to-end radius [[Entropy and materials#Microstates|microstates]]. A key result here is that $r_{g}=\sigma=\sqrt{n}a$.

Assuming all microstates are equally probable,$$\begin{align*}
\Omega(r)&\propto X(r)\\
\\
\Rightarrow \quad S&=k_{B}\ln \Omega\\
&= \frac{-k_{B}r^{2}}{2\sigma^{2}} + C
\end{align*}$$Now, using $f=-T\frac{\partial S}{\partial r}$ from before:$$\begin{align*}
f&=\frac{k_{B}T}{\sigma^{2}}r\\
&= \frac{k_{B}T}{na^{2}}r
\end{align*}$$So $\frac{k_{B}T}{na^{2}}$ is the entropic spring constant of the polymer chain. This result holds in 3D, but is non-trivial to prove.
### Polymer fluctuation energy
tbc
## Elastomer thermodynamics
Now we can investigate the effect of crosslinks. Consider an elastomer with a bulk average crosslink distance $r_{c}$. We can approximate a region without crosslinks as a cube of side $r_c$ with the property$${r_{c}}^{2}=n_{c}a^{2}$$as before, where $n_{c}$ is the average number of monomers along a length of chain between crosslinks and $a$ is the average monomer length.

As before, the effective spring constant of a polymer in this region is $$k_e=\frac{k_{B}T}{{r_{c}}^{2}}$$We also need the number of chains in this region. Given that the average volume occupied by a monomer is $v_{m}$, the number of monomers in the cube is $\frac{{r_{c}}^{3}}{v_{m}}$. The number of monomers per chain is $n_c$ so the number of chains per cube is,$$N_c=\frac{{r_{c}}^{3}}{v_{m}}\div n_{c}= \frac{r_{c}a^{2}}{v_{m}}$$Now consider an external force applied to one side of the cube region:$$\begin{align*}
F&=N_{c}k_{e}\delta x\\
&= \frac{r_{c}a^{2}}{v_{m}}\frac{k_{B}T}{{r_{c}}^{2}}\delta x\\
&= \frac{r_{c}k_{B}T}{n_{c}v_{m}}\delta x\\
\\
\Rightarrow\quad E&=\frac{F L}{\delta xA}\\
&= \frac{\frac{r_{c}k_{B}T}{n_{c}v_{m}}\delta x\cdot r_{c}}{\delta x\cdot {r_{c}}^{2}}\\
&= \boxed{\frac{k_{B}T}{n_{c}v_{m}}}
\end{align*}$$Hence elasticity is dependent on the trade-off between temperature and crosslink density. For pure polymers, $n_{c}\rightarrow\infty$ so $E$ is very small after $T_g$. For highly crosslinked materials, $E$ increases at high temperatures (somewhat counterintuitively).

In some cases this increase in elasticity with temperature can be obscured by the behaviour around the glass transition temperature.