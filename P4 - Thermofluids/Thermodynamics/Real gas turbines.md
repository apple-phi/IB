The ideal reversible cycle modelling a simple gas turbine is the air-standard Joule cycle, known in the USA as the Brayton cycle. In a simple gas turbine the inlet and outlet are in the atmosphere.

Unlike the air-standard Joule cycle, a real gas turbine:
- There is a 2-4% pressure drop across the combustor
- Combustion changes the gas composition so the properties of the working fluid in the turbine are different from the compressor
- In the compressor and turbines there is viscous dissipation in the boundary layer and mixing of discrete flows. These generate entropy and lower the available power.

> We will focus on the latter, which is the dominant effect, however the other inefficiencies are trivial to model.
![[real-joule-cycle-Ts.png|400]]
In the compressor (1→2) and turbine (3→4) stages, they are ideally isentropic so any entropy is irreversible, $\Delta S={\Delta S}_{\mathrm{irrev}}$
## First Law analysis
Consider a Joule cycle where we are given $T_{1}$, $T_{3}$, $r_{p}=\frac{p_{2}}{p_{1}}=\frac{p_{3}}{p_{4}}$ and the thermal efficiencies of the compressor and turbine stages.
### Compressor (1→2)
Applying the isentropic relationship of a [[Perfect gas relationships|perfect gas]],
$$
\frac{T_{\mathrm{2 s}}}{T_{1}}={r_{p}}^{\frac{\gamma-1}{\gamma}}
$$
Applying the SFEE to a given compressor efficiency $\eta_{c}$
$$
\begin{aligned}
\eta_{c} =\frac{\dot{W}_{\mathrm{real}}}{\dot{W}_{\mathrm{rev}}} = \frac{-\dot{m}{\Delta h}_{\mathrm{real}}}{-\dot{m}{\Delta h}_{\mathrm{rev}}} & = \frac{{\Delta T}_{\mathrm{2s}/1}}{{\Delta T}_{2/1}} \\
 \\
\Rightarrow\quad \Delta T_{\mathrm{2 /1}}  & = \frac{T_{\mathrm{2s}}-T_{1}}{\eta_{c}} \\
& = \frac{T_{1}}{\eta_{c}}\left({{r_{p}}^{\frac{\gamma-1}{\gamma}}-1}\right)  \\
 \\
\Rightarrow\quad \dot{W}_{c,\mathrm{in}} & =\dot{m}c_{p}\Delta T_{\mathrm{2 /1}}
\end{aligned}
$$
### Combustor (2→3)
Applying the SFEE,
$$
\dot{Q}_{2\to 3}= \dot{m}\Delta h=\dot{m}c_{p}{\Delta T}_{3 /2} 
$$
### Turbine (3→4)
Applying the isentropic relationship of a [[Perfect gas relationships|perfect gas]],
$$
\frac{T_{3}}{T_{\mathrm{4s}}}={r_{p}}^{\frac{\gamma-1}{\gamma}}
$$
Applying the SFEE to a given compressor efficiency $\eta_{c}$,
$$
\begin{align}
\eta_{c} =\frac{\dot{W}_{\mathrm{real}}}{\dot{W}_{\mathrm{rev}}} = \frac{-\dot{m}{\Delta h}_{\mathrm{real}}}{-\dot{m}{\Delta h}_{\mathrm{rev}}} & = \frac{{\Delta T}_{4 /3}}{{\Delta T}_{\mathrm{4s}/3}} \\
 \\
\Rightarrow\quad \Delta T_{4 /3} & =\eta_{t}(T_{\mathrm{4s}}-T_{3}) \\
 & =\eta_{t}T_{3}\left( {r_{p}}^{\frac{1-\gamma}{\gamma}} -1 \right)  \\
 \\
\Rightarrow\quad \dot{W}_{t,\mathrm{out}} & =-\dot{m}c_{p}\Delta T_{4 /3}
\end{align}
$$
### Cycle efficiency 
Consider the relationship between work output and energy input,
$$
\begin{align}
\eta=\frac{\dot{W}_{\mathrm{out}}}{\dot{Q}_{\mathrm{in}}} & =\frac{\dot{W}_{t, \mathrm{out}}-\dot{W}_{c, \mathrm{in}}}{\dot{Q}_{2\to 3}} \\
 & = \frac{-\cancel{ \dot{m}c_{p} }\Delta T_{4 /3}-\cancel{ \dot{m}c_{p} }\Delta T_{\mathrm{2 /1}}}{\cancel{ \dot{m}c_{p} }{\Delta T}_{3 /2} } \\
 & =  \frac{\eta_{t}T_{3}\left( {r_{p}}^{\frac{1-\gamma}{\gamma}} -1 \right)+\frac{T_{1}}{\eta_{c}}\left({{r_{p}}^{\frac{\gamma-1}{\gamma}}-1}\right)}{T_{1} +\frac{T_{1}}{\eta_{c}}\left({{r_{p}}^{\frac{\gamma-1}{\gamma}}-1}\right) - T_{3}}
\end{align}
$$

## Second Law analysis
Consider the [[Availability balance|availability balance]] of the working fluid as it passes through the gas turbine. Of the total available $\int \eta_{\mathrm{carnot}} \ dS$ power from the inlet flow, some will be lost as inefficiencies in the turbine and compressor and some will leave in the output flow as remaining availability—only some of it is extracted as shaft work.
### Transfer of available power into the combustor
The working fluid gains availability from the fuel combustion. Applying assumptions about [[Perfect gas relationships#Change in specific entropy|perfect gases]],
$$
\begin{align}
{\Delta b}_{3 /2} & =\Delta h-T_{\mathrm{env}}\Delta s \\
 & =c_{p}{\Delta T}_{3/2}-T_{\mathrm{env}}\left( c_{p}\ln \frac{T_{3}}{T_{2}} -R\cancel{ \ln \frac{p_{3}}{p_{2}} }  \right)  \\
 & =c_{p}\left({\Delta T}_{3/2}-T_{\mathrm{env}} \ln \frac{T_{3}}{T_{2}}\right)
\end{align}
$$

### Net availability change
A similar analysis can be applied to the flow between the inlet and outlet since we assume no net pressure change.
$$
\begin{align}
{\Delta b}_{4 /1} & =\Delta h-T_{\mathrm{env}}\Delta s \\
 & =c_{p}{\Delta T}_{4/1}-T_{\mathrm{env}}\left( c_{p}\ln \frac{T_{4}}{T_{1}} -R\cancel{ \ln \frac{p_{4}}{p_{1}} }  \right)  \\
 & =c_{p}\left({\Delta T}_{4/1}-T_{\mathrm{env}} \ln \frac{T_{4}}{T_{1}}\right)
\end{align}
$$

### Availability loss due to irreversibility
Although the working fluid gains availability by fuel combustion, some of this is lost irreversibly in the compressor and turbine. These are given by $T_{\mathrm{env}}{\Delta S}_{\mathrm{component}}$, as shown in the [[Availability balance|availability balance]].