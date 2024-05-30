## Darcy–Weisbach equation
The rate of pressure drop along a length of cylindrical pipe due to wall friction is
$$
\frac{\mathrm{d} P}{\mathrm{d}x}=\frac{f}{d}\cdot \frac{1}{2}\rho V^{2} 
$$
where $f$ is the friction factor and $d$ is a characteristic length, typically the pipe diameter.

This is a special case solvable analytically. Across a generic component, questions sometimes give a generic *pressure loss coefficient*, $K$ s.t.
$$
\Delta p=K\cdot \frac{1}{2}\rho V^{2}
$$
>The $\frac{1}{2}\rho V^{2}$ term is the dynamic pressure term from Bernoulli’s equation.

## Biot number condition
When the Biot number is sufficiently small, then the internal conduction within a body is so fast (compared to external convection) that the body can be assumed to be at a homogenous temperature.
$$
\mathrm{Bi}<0.1
$$
This is the *lumped heat capacity* assumption.
## Radiative surface resistance of non-black bodies
The surface resistance for heat transfer $\dot{Q}$ (current) driven by the potential difference between radiant exitance $E_{b}^{\circ}$ (energy flux) and radiosity $J$ (emitted radiant flux)

$$
R_{s} = \frac{E_{b}^{\circ}-J}{\dot{Q}}= \frac{1-\varepsilon}{\varepsilon A}
$$
See also: [[Heat transfer by radiation#Radiation to and from a non-black body]]

When calculating radiative heat transfer:
- Insulated surfaces are open-circuits, so they don’t consume “current” $\dot{Q}$
- Black bodies are short-circuits, so they also don’t consume current.

>Remember to split up the bodies into their ideal black body part and emissive resistance $\frac{1-\varepsilon}{\varepsilon A},$ then discard that term for insulators and black bodies.

## Shape factor algebra
Reciprocity
$$
A_{1}f_{12}=A_{2}f_{21}
$$
Unity
$$
\sum_{j}f_{ij}=1
$$
Convexity
$$
f_{ii}=0
$$

See also [[Heat transfer by radiation#Shape factor algebra]]

## Humidity
The relative humidity is the ratio of partial pressures of the water vapour to the theoretical saturation pressure at that temperature.
$$
\phi=\frac{p[\ce{H_{2}O} ]}{p_{\mathrm{sat}}}
$$
The specific humidity is the ratio of masses of the water vapour to the *dry* air.
$$
\omega= \frac{m_{v}}{m_{\mathrm{dry\ air}}} = \frac{\phi p_{\mathrm{sat}}}{p-\phi p_{\mathrm{sat}}} \cdot\frac{M_{\ce{H_{2}O} }}{M_{\mathrm{air}}}
$$
>Recall that the molar masses of water and air are $\pu{18g/mol}$ and $\pu{29g/mol}$ respectively.

See also: [[Dryness#Humidity]]

## Isolines
![[pv-ts-isolines.png|500]]

## Heat exchanger effectiveness 
For *any* configuration of heat exchanger (parallel flow, counter-flow etc.) the effectiveness is the fraction of heat exchanged compared to the theoretical maximum of any configuration.
$$
\varepsilon= \frac{q}{q_{\max}}=\frac{q}{c_{\min}\Delta T}
$$
where $c_{\min}$ is the lowest specific heat capacity of the two flows and $\Delta T$ is the temperature difference between the two inlets.

>The maximum effectiveness is usually given by the counter-flow configuration.

## Boundary layer assumptions
- No perpendicular pressure gradient since $\partial_{y}p\ll\partial_{x}p$ so
$$
\partial_{y}p\approx0
$$
- No friction effects outside the boundary layer
- Parallel flow within the boundary layer

