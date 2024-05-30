The HRSG (Heat-Recovery Steam Generator) is a *counter-flow* heat exchanger used in a [[Power plant cycles#Combination cycles|combined gas-steam cycle]].
![[HRSG-placement.png|400]]
>Because irreversible entropy generation over a finite temperature difference is the main source of inefficiency, heat exchangers are generally designed to minimise the temperature difference at every point.

## Analysis
Consider the temperature profile of the gas flow 8→9 counter to the water/steam flow 2→3.
![[pinch-point.png|400]]
Conversing energy flow across the boundary using the SFEE,
$$
\begin{align}
\dot{Q}_{\mathrm{gas}} & =\dot{Q}_{\mathrm{steam}} \\
(\dot{m}{\Delta h})_{\mathrm{gas}} & =(\dot{m}{\Delta h})_{\mathrm{steam}} \\
 \\
 & \Rightarrow\quad \boxed{\frac{\dot{m}_{\mathrm{gas}}}{\dot{m}_{\mathrm{steam}}}  = \frac{{\Delta h}_{3 /2}}{-c_{p}{\Delta T}_{9 /8}}}
\end{align}
$$
The net irreversible entropy generation is the sum of net entropy generations in each flow,
$$
{\Delta S}_{\mathrm{irrev}}=\overbrace{ \dot{m}_{\mathrm{gas}}{\Delta s}_{9/8} }^{ \mathrm{negative} }+\underbrace{ \dot{m}_{\mathrm{steam}}{\Delta s}_{3 /2} }_{ \mathrm{positive} }\geq0
$$
where the gas entropy change can be given by the [[Perfect gas relationships|perfect gas relationships]] and the steam entropy changes established experimentally.