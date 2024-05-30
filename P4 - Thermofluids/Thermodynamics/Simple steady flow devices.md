## Reversible heat extractor
tbc

## Isentropic turbine
Consider perfect gas flow through a reversible turbine with temperature variation $\Delta T$. A First Law analysis gives the Steady Flow Energy Equation (SFEE). Considering a control volume around the turbine system:
$$\begin{align}
\cancel{\dot{Q}_{\mathrm{in}}}-\dot{W}_{\mathrm{out}} & =\dot{m}\Delta h \\
 \\
\Rightarrow\quad {w}_{\mathrm{out}} & = \frac{\dot{W}_{\mathrm{out}}}{\dot{m}} =-c_{p}\Delta T
\end{align}$$
So when there is a temperature drop ($\Delta T<0$), the work done by the system on each unit mass of gas is $w_{\mathrm{out}}>0$

Now, under [[Perfect gas relationships#Isentropic changes|isentropic expansion]],
$$
\frac{T_{2}}{T_{1}}=\left( \frac{p_{2}}{p_{1}} \right)^{\frac{\gamma-1}{\gamma} }
$$
So the pressure ratio used to generate the temperature difference can be easily found.
![[isentropic-turbine.png|400]]
## Throttle

Consider the adiabatic throttling of a perfect gas flow, increasing entropy. 
![[throttle-diagram.png|300]]
The First Law dictates that
$$
\dot{m}\Delta h=\cancel{\dot{Q}}_{\mathrm{in}}- \cancel{\dot{W}}_{\mathrm{out}}=0
$$
while the Second Law implies that
$$
\begin{align}
\dot{m}\Delta s & =\int \frac{\cancel{\mathrm{d}\dot{Q}}}{T}+\dot{m}{\Delta s}_{\mathrm{irreversible}}  \\
 \\
\Rightarrow\quad \Delta s & ={\Delta s}_{\mathrm{irreversible}}
\end{align}
$$
For a [[Perfect gas relationships#Change in specific enthalpy|perfect gas]]:
$$
\Delta s=c_{p}\ln r_{T}-R\ln r_{p}
$$
So the generation of irreversible entropy per unit mass is
$$
\begin{align}
{\Delta s}_{\mathrm{irreversible}} & =c_{p}\cancel{\ln r_{T}}-R\ln r_{p} \\
 & =-R\ln\left( \frac{p_{2}}{p_{1}} \right)
\end{align}
$$
![[isothermal-Ts.png|400]]