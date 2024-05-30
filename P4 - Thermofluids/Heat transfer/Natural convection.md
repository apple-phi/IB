Although this is often negligible compared to forced convection, many environmental flows are driven by natural convection.

## Characteristics
tbc
## How big are the $\delta p$s?
tbc
## How big are the velocities that these $\delta p$$s$ drive?
tbc
## Scaling analysis
Take the Boussinesq Equation,
$$
\rho V\frac{\partial V}{\partial x} =\bar{\rho}\beta(T-T_{\infty})g+\mu \frac{ \partial^{2} V }{ \partial y^{2} } 
$$
To examine the size of the maximum boundary layer velocity, assume that the $\rho V\frac{ \partial v }{ \partial x }$ term is negligible. Then the rough scaling is
$$
\frac{\mu V}{\delta^{2}}\sim \rho\beta(T-T_{\infty})g
$$
So $V$ scales as 
$$
V_\text{scale}=\frac{\bar{\rho}\beta g\Delta T\delta^{2}}{\mu}
$$
where $\delta$ is the boundary layer thickness.

### Boundary conditions
At $y=0,$
- $V=0$
- $T=T_{y}$

At $y=\delta,$
- $V=\mu \frac{ \mathrm{d}V }{ \mathrm{d}y }=0$
- $T=T\infty \frac{ \mathrm{d}T }{ \mathrm{d}y }=0$

The simplest polynomial which fits these conditions is
$$
\begin{bmatrix}
V \\
T-T_{\infty}
\end{bmatrix}=\begin{bmatrix}
\frac{y}{\delta}V_\text{scale} \\
T-T_{\infty}
\end{bmatrix}\left( 1-\frac{y}{\delta} \right)^{2} 
$$
with $V_\text{scale}$ as before.

By a control volume analysis (and not the already-linearised Boussinesq equation), you can show that
$$
\begin{align}
\delta \propto \sqrt[4]{ x } \\
V_\text{scale}\propto \sqrt{ x }
 \end{align}
$$
For general problems we can consider an analog to $V_\text{scale}$ with $\delta$ replaced with any characteristic length scale $d.$
$$
V_\text{scale}=\frac{\bar{\rho}\beta g\Delta TD^{2}}{\mu}
$$
Similarly, we can define an analogous parameter to the Reynolds number called the *Grashof Number* $\mathrm{Gr}.$
$$
\mathrm{Gr}=\frac{\bar{\rho}V_\text{scale}D}{\mu}=
$$
tbc 

where $v=\frac{\mu}{\rho}$

## Typical free convection boundary layer type flows
tbc

## Dimensional analysis in general
A naive approach to dimensional analysis would lead to the naive expression
$$
\dot{Q}=\operatorname{f}(D,\rho,\mu,\lambda,c_{p},\beta,\Delta T, g)
$$
But we have extra information about the flow, so we can simplify this.

>$\beta\Delta Tg$ must appear together—they represent a single dimensional degree of freedom.

As in forced convection, use a heat transfer coefficient
$$
\frac{\dot{Q}}{A\Delta T}=h_\text{overall}=
$$
tbc
So the Nusselt number is
$$
\mathrm{Nu}_\text{overall}=\frac{h_\text{overall}D}{\lambda}=\operatorname{f}\left( \frac{\mathrm{Gr},\mu c_{p}}{\lambda} \right)
$$
where the Grashoff number is defined as 
$$
\mathrm{Gr}=\frac{\bar{\rho}^{2}\beta g\Delta TD^{3}}{\mu^{2}}
$$
## Key points
tbc


