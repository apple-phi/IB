#materials

Spontaneous reactions are entropically driven to minimise free energy. 
## Summary
- A reaction is feasible if $\mathrm d G\leq0$
- Miscibility depends on the trade-off between increasing internal energy and entropy
- Phase diagrams can be interpreted qualitatively in terms of how the free energy of phases evolves with temperature
## Gibbs free energy
It is useful in thermodynamics to define the extensive state function$$G\overset{\Delta}{=}\overbrace{H}^{U+pV}-TS$$For the isobaric and isothermal conditions where $\mathrm{d}p=\mathrm{d}T=0$,$$\mathrm{d}G=\mathrm{d}U+p\mathrm{d}V-T\mathrm{d}S$$From the [[Laws of Thermodynamics|First and Second Laws]],$$T\mathrm{d}S\geq\mathrm{d}Q=\mathrm{d}U+\overbrace{\delta W}^{\mathrm{p\mathrm{d}V+\delta W'}}$$where $\delta W'$ is non-pressure work in/out of the system. Then,$$\mathrm{d}G\leq-\delta W'=0$$Hence, during system evolution, $\mathrm{d}G\lt0$ and at equilibrium, $\mathrm{d}G=0$. Because the system evolves to minimise $G$, the Gibbs free energy is known as a *thermodynamic potential*.
## Free energy of states of matter
We expect the entropies and internal energies to order themselves according to kinetic energy, and for gases to occupy the greatest volume:$$\begin{align*}
U_s&<U_l<U_g\\
V_{s}&\approx V_l<V_g\\
S_s&<S_l<S_g
\end{align*}$$![[free-energy-states-of-matter.png]]
## Free energy of mixing
Consider a system of two isolated components $a$ and $b$ in the fractions $p$ and $q$ respectively. Since free energy is extensive,$$G_{\text{unmixed}}=pG_{a}+qG_{b}$$Upon mixing, there is a change in the free energy,$$G_{\text{mixed}}=G_{\text{unmixed}}+\underbrace{\Delta G}_{\Delta U +p \Delta V-T \Delta S}$$
- $\Delta U$ originates from the new electrostatic interactions between the components
- $\Delta V$ is usually negligible, but originates from any density changes upon mixing
- $\Delta S$ often dominates, and is the [[Entropy and materials#Entropy of mixing|entropy of mixing]].
### Miscible materials
To demonstrate the effect of $\Delta  G$ for miscible materials, assume $$\begin{align*}
\Delta G&\approx -T \Delta S\\
&= nk_BT\left(p\ln p + q\ln q\right)
\end{align*}$$Comparing the free energies of the mixed and unmixed states as the component proportion varies:![[free-energy-miscible.png]]
### Immiscible materials
In many cases, $\Delta U>T\mathrm{d}S\Rightarrow\Delta G>0$. This leads to a non-convex free energy curve:![[free-energy-immiscible.png]]
In this case, between the two local minima, the system will stabilise on the dotted line between them as a mixture of the states at each minimum. The fraction of each state goes according to the [[Lever rule]].
### On a phase diagram
This is particularly applicable to two-phase regions on [[Phase diagrams|phase diagrams]].![[free-energy-phase-diag.png]]
