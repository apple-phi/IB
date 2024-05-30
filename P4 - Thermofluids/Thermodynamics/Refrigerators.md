## The reversed Carnot cycle
Consider a reverse [[Carnot efficiency|Carnot cycle]].
![[carnot-fridge.png|250]]
The change in global entropy is
$$
\begin{align}
\dot{m}\Delta S & = \frac{\dot{Q}_{\mathrm{hot}}}{T_{\mathrm{hot}}}-\frac{\dot{Q}_{\mathrm{cold}}}{T_{\mathrm{cold}}} \\
 & =\frac{\dot{Q}_{\mathrm{cold}}+\dot{W}_{x}}{T_{\mathrm{hot}}}-\frac{\dot{Q}_{\mathrm{cold}}}{T_{\mathrm{cold}}}
\end{align}
$$
Note that for $\Delta S\geq0$ to satisfy the [[Laws of Thermodynamics#The Second Law of Thermodynamics|Second Law of Thermodynamics]], the Coefficient of Performance for the refrigerator is
$$
\mathrm{COP}_{\mathrm{R}}\leq \frac{\dot{Q}_{\mathrm{cold}}}{\dot{W}_{x}}= \frac{T_{\mathrm{cold}}}{T_{\mathrm{hot}}-T_{\mathrm{cold}}}
$$
Also note that the equivalent heat pump has
$$
\begin{align}
\mathrm{COP_{HP}}  \leq \frac{\dot{Q}_{\mathrm{hot}}}{\dot{W}_{x}} & = \frac{T_{\mathrm{hot}}}{T_{\mathrm{hot}}-T_{\mathrm{cold}}} \\
 & =\mathrm{COP_{R}}+1
\end{align}
$$
![[reversed-carnot-cycle.png]]

## Real refrigeration cycles
Several practical improvements can be made to the reversed Carnot cycle:
- Compression not in two-phase region by superheating
- Turbine replaced with throttle which handles the two-phase region better

![[real-refridgeration-cycles.png|600]]
![[ts-ph-real-fridge.png|600]]

## Choice of refrigerant
- Cheap, inert, non-toxic
- Pressure range in operating temperature range must be small to minimise work for compression
- Vapour pressure low (cost) but high enough to stop air leaking in
- Latent heat of evaporation high so mass flow rate across heat exchangers can be low
