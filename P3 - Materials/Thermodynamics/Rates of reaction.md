#materials 
## Summary
- Reaction rate can be modelled by the Arrhenius law
- There is a trade-off between thermodynamics and kinetics that sets the optimum reaction rate
## Temperature-dependence
The probability $p$ of an atom having enough kinetic energy to overcome a reaction activation energy barrier $q_{a}$ follows a Boltzmann distribution:$$p\propto \exp\left(- \frac{q_{a}}{k_{B}T}\right)=\exp\left(- \frac{Q_{a}}{RT}\right)$$This probability is proportional to the net reaction rate in simple cases.

The [[Fick's Laws#Macroscopic scale|diffusion coefficient]] also follows this Arrhenius law, with$$D\propto p\propto\exp\left(- \frac{Q_{a}}{RT}\right)$$
## Rates of phase transformations
Consider again the case of [[Nucleation#Homogenous nucleation|homogenous nucleation]]. There is a reversible reaction with some activation energy $Q_{a}$ and a change in free energy $\Delta G$ between the solid and liquid phases,$$L\rightleftharpoons S$$The probability of an atom moving in the forwards direction, $p_{L\to S}$ is given by$$p_{L\to S}\propto \exp \left(-\frac{Q_{a}}{k_{B}T}\right)$$while the probability of an atom moving in the reverse direction $p_{S\to L}$ is$$p_{S\to L}\propto \exp\left (-\frac{Q_{a}+|\Delta G|}{k_{B}T}\right)$$So the net nucleation rate is proportional to$$\begin{align}
\mathrm{rate}&\propto p_{L\to S}-p_{S\to L} \\
 & \approx\exp \left(-\frac{Q_{a}}{k_{B}T}\right)-\exp\left (-\frac{Q_{a}+|\Delta G|}{k_{B}T}\right) \\
 & =\left[1-\exp \left(-\frac{|\Delta G|}{k_{B}T}\right)\right]\exp \left(-\frac{Q_{a}}{k_{B}T}\right) \\
 & \approx\frac{|\Delta G|}{k_{B}T}\exp \left(-\frac{Q_{a}}{k_{B}T}\right)
\end{align}$$Now, returning to the discussion about [[Nucleation#Undercooling for nucleation|undercooling]], we recall that$$\Delta G= \Delta H\left(1-\frac{T}{T_{f}}\right)$$for $T<T_{f}$. Note that $\Delta H<0$ because freezing is exothermic.

Therefore,$$\mathrm{rate} \propto \left( \frac{1}{T}-\frac{1}{T_{f}} \right)\exp \left(-\frac{Q_{a}}{k_{B}T}\right)$$Hence, there is a trade-off between free energy release at high undercooling and the activation energy (which is more easily overcome at high temperatures).

![[activation-energy-undercooling.png]]