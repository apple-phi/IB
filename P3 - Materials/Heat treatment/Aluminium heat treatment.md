#materials 
## Slow-cooling
Consider the Al-Cu [[Phase diagrams|phase diagram]] and the transition across the *solvus* from a single-phase solid solution to a two-phase region via [[Hardening methods#Precipitation hardening|precipitation]]: ![[al-cu-phase-diag.png]] As the two-phase state becomes the equilibrium by minimising [[Spontaneous reactions#Gibbs free energy|free energy]], the precipitating Cu primarily [[Nucleation#Heterogeneous nucleation|nucleates heterogeneously]] at the phase boundaries to form $\mathrm{CuAl_{2}}$.
![[cual2-precipitates.png|200]]
The Gibb’s free energy drives precipitate coarsening to minimise the surface area-to-volume ratio due to the surface energy penalty—slow cooling gives sufficient time for this.

Therefore, slow cooling provides ineffective precipitation hardening.

## Quenching (rapid-cooling)
The [[Transformation diagrams#CCT (Continuous Cooling Transformation)|CCT]] diagram displays a critical cooling rate after which a super-saturated solid solution results instead. The super-saturated solid solution has effective [[Hardening methods#Solid solution hardening|solid solution hardening]] with higher yield strength than the slow-cooled Al.

![[Al-supersaturated.png]]
However, this is still not the microstructure that optimises strength.

## Ageing
The optimum microstructure would have many small precipitates in close proximity. To achieve this, the following approach is taken for aluminium:
1. Dissolve alloying elements at high temperatures to achieve a stable single-phase solid solution
2. Quench to form a metastable super-saturated solid solution 
3. Age either
	- naturally—at room temperature, for a few days
	- artificially—at warm temperatures (~200°C), for a few hours

This additional ageing step allow the fine-grained (haha) control of precipitate size and spacing by adjusting the ageing time and temperature and limiting the process before too much coarsening occurs.
![[ageing.png|500]]

Natural ageing often leaves the result *underaged* at an intermediate metastable microstructure which forms before $\mathrm{CuAl_{2}}$—however this result is still strong while being cheap. This process is shown on this [[Transformation diagrams#CCT (Continuous Cooling Transformation)|TTT diagram]]:
![[ageing-TTT.png|500]]

The metastable precipitates form in a sequence ending with $\mathrm{CuAl_{2}}$ and initially have a structure coherent with the $\mathrm{Al}$ lattice. Therefore, the slip planes are continuous across the interface and dislocation planes allow easy shear.
![[coherent-lattice.png|200]]![[incoherent-lattice.png|200]]

As the coarsening proceeds driven by free energy minimisation, the precipitate lattice grows and the difference in cell size compared with the $\mathrm{Al}$ strains the coherent interface. At the peak yield strength, the majority of the precipitates will be fine and metastable—large $\mathrm{CuAl_{2}}$ precipitates would be present in the over-aged material.

Not all alloys form these metastable precipitates and remain as a solid solution that relies on solid solution hardening and work hardening to resist shear.
![[unageable-alloys.png|500]]
An example of this is many $\mathrm{Al-Mg}$ systems.