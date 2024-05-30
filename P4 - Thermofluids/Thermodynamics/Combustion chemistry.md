Combustion often does not occur at the exact stoichiometric ratio, so an analysis of this is useful.

Assume that air is 21% oxygen and 79% nitrogen. Then, under stoichiometric conditions, for methane combustion in air we have,
$$
\mathrm{CH_{4} + 2\left( O_{2} + \frac{79}{21}N_{2} \right) \longrightarrow CO_{2}+2\,H_{2}O + \frac{158}{79}N_{2}}
$$
## Air-Fuel Ratio (AFR)
The AFR is defined as the ratio of *mass flows* in the combustion,
$$
\mathrm{AFR}= \frac{\dot{m}_{a}}{\dot{m}_{f}}
$$
## Air-Fuel equivalence ratio ($\lambda$)
This provides a relative measure of closeness of the AFR to the AFR at stoichiometry,
$$
\lambda= \frac{\mathrm{AFR}}{\mathrm{AFR}_{\mathrm{stoichiometry}}}
$$
### Excess air ($\lambda>1$)
For $\lambda\geq1$ in methane combustion, 
$$
\begin{align}
\mathrm{CH_{4} + 2\lambda\left( O_{2} + \frac{79}{21}N_{2} \right)} \longrightarrow\; &\mathrm{CO_{2}+2\,H_{2}O + \frac{158}{79}N_{2} + \overbrace{ 2(\lambda-1)\left( O_{2} + \frac{79}{21}N_{2} \right) }^{ \text{excess due to }\lambda\geq1 }} \\
 \\
\equiv\  &\mathrm{CO_{2}+2\,H_{2}O + \underbrace{ \lambda \cdot\frac{158}{79}N_{2} + 2(\lambda-1)\,O_{2} }_{\text{unreacted reactants}} }
\end{align}
$$
### Excess fuel ($\lambda<1$)
For $\lambda\leq1$ in methane combustion, 
$$
\mathrm{CH_{4} + 2\lambda\left( O_{2} + \frac{79}{21}N_{2} \right) \longrightarrow (4\lambda-3)\,CO_{2} + (4\lambda-4)\,CO+2\,H_{2}O +\lambda \cdot\frac{158}{79}N_{2}} 
$$
## Fuel-Air equivalence ratio ($\phi$)
Sometimes the inverse ratio is used,
$$
\phi=\frac{1}{\lambda}
$$