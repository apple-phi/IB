Work availability sets the [[Maximum steady flow power|maximum steady flow power]] that can be drawn from a working fluid. This system parameter can vary over time by work and heat input/output. By definition,
$$
\begin{align}
\dot{m}\Delta b & =\dot{m}(\Delta h-T_{\mathrm{env}}\Delta s) \\
 & = (\dot{Q}_{\mathrm{in}}-\dot{W}_{\mathrm{out}}) -T_{\mathrm{env}}\left( \int \frac{\mathrm{d}\dot{Q}_{\mathrm{in}}}{T}+\Delta \dot{S}_{\mathrm{env}}\right) \\
 & = -\dot{W}_{\mathrm{out}}+\int \left( 1-\frac{T_{\mathrm{env}}}{T} \right) \, \mathrm{d}\dot{Q}_{\mathrm{in}}  - (T\Delta \dot{S})_{\mathrm{env}} \\
& = -\dot{W}_{\mathrm{out}}+\int \eta_{\mathrm{carnot}} \, \mathrm{d}\dot{Q}_{\mathrm{in}}  - (T\Delta \dot{S})_{\mathrm{env}}
\end{align}
$$
This fits our intuition of how thermal and shaft power transfer should affect the working fluid work availability:
- Shaft power generation decreases availability 
- Thermal power input under reversible conditions is limited in its contribution to work availability by the [[Carnot efficiency]]
- Entropy generation decreases availability

