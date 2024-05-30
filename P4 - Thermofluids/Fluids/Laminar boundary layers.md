Inviscid flows are governed by the Euler equations,
$$
\rho \frac{ \partial \mathrm{v} }{ \partial t } +\rho(\mathrm{v}\cdot \nabla \mathrm{v})=-\nabla p
$$
The more general Navier-Stokes equation is
$$
\rho \frac{ \partial \mathrm{v} }{ \partial t } +\rho(\mathrm{v}\cdot \nabla \mathrm{v})=-\nabla p+\mu \nabla^{2}\mathrm{v}
$$
Now when $$\mathrm{Re}=\frac{\rho v^{2}/D}{\mu v/D^{2}}=\frac{\rho vD}{\mu} \gg1$$
then the viscous term $\mu \nabla^{2}\mathrm{v}$ becomes negligible and we return to the Euler equations.
![[increasing-re.png]]

However, the no-slip condition will *still* be satisfied at high $\mathrm{Re}$, leaving a boundary layer at the wall. If the layer is a thickness $\delta$,
$$
\mathrm{Re}_{\delta}= \frac{\rho v\delta}{\mu}
$$
## Boundary layer growth
The boundary layer grows over time due to the cumulative effects of the no-slip condition. At the wall, the fluid layer near the plate has the same velocity as the plate, which then exchanges momentum with layer above via shear to accelerate it towards same wall velocity. This can be thought of as a diffusion of momentum.

Considering this from both Eulerian and Lagrangian reference frames:
![[boundary-layer-growth.png|600]]

Let’s get a prediction of the order of magnitude of the boundary layer size as we travel downstream.
Continuity:
$$
\nabla \cdot \mathrm{v}=0\Rightarrow v_{y}\sim \frac{\delta v_{x}}{x}
$$
$x$-momentum:
$$
\begin{align}
\cancel{\rho \frac{ \partial \mathrm{v} }{ \partial t }}+\rho(\mathrm{v}\cdot \nabla \mathrm{v}) & =-\cancel{\nabla p}+\mu \nabla^{2}\mathrm{v} \\
\rho\left( v_{x}\cdot \frac{v_{x}}{x} + v_{y}\cdot \frac{v_{x}}{\delta}\right) & = \mu\left( \frac{v_{x}}{x^{2}}+\frac{v_{x}}{\delta^{2}} \right)
\end{align}
$$
with $x\gg\delta$ the $\frac{1}{x^{2}}$ term is negligible, so
$$
\delta^{2}\sim \frac{\mu x}{\rho v_{x}}
$$
$y$-momentum:
$$
\begin{align}
\cancel{\rho \frac{ \partial \mathrm{v} }{ \partial t }}+\rho(\mathrm{v}\cdot \nabla \mathrm{v}) & =-{\nabla p}+\mu \nabla^{2}\mathrm{v} \\
\rho\left( v_{x}\cdot \frac{v_{y}}{x} + v_{y}\cdot \frac{v_{y}}{\delta}\right) & = -\frac{y\Delta p}{\delta} +\mu\left( \frac{v_{y}}{x^{2}}+\frac{v_{y}}{\delta^{2}} \right)
\end{align}
$$
These terms are all much smaller than the $x$-momentum terms, so the wall-normal velocity is much smaller than the downstream velocity. In summary,
$$
\begin{align}
\delta & \sim \sqrt{ \frac{\mu x}{\rho v_{x}} } \\
v_{y}&\sim \frac{\delta}{x}v_{x}\ll v_{x} \\
\frac{ \partial p }{ \partial y } &\approx 0
\end{align}
$$
![[boundary-layer-growth-downstream.png]]

## Bernoulli and boundary layers
Bernoulli’s equation as we know it does not hold within the boundary layer due to the viscous effects. However, for flows with a low viscosity, we can solve the motion as if it were totally inviscid and then use that solution as the limiting boundary condition.

![[bernoulli-outside-layer.png]]
## Boundary layers in flows with a pressure gradient
- For a *favourable* pressure gradient, the flow accelerates towards the lower pressure region and the velocity gradient at the boundary layer increases so the friction increases.
![[fav-bound-layer.png]]

- Conversely, for an adverse pressure gradient, the flow decelerates and the boundary layer is depleted with a lowed velocity gradient at the wall. The flow can even reverse!
![[adverse-pressure-grad.png|600]]
## Boundary layer separation
Around an ellipse, the velocity and pressure distribution is
![[bound-layer-sep.png|500]]
All real fluids are viscous and obey no-slip, so a thin boundary layer forms around the surface, growing downstream.
![[bound-layer-growth.png|500]]
At the front there is a favourable pressure gradient due to streamline curvature, but at the back the pressure gradient is adverse and eventually causes *flow reversal*!

The reversing fluid has to go somewhere, but it cannot reverse back to the front because there is a favourable pressure gradient there and the fluid is moving forwards. Instead it separates at a mini-stagnation point—the point of separation.
![[bound-layer-stagnation-point.png]]
This was first realised by Ludwig Prandtl:
>*”A fluid layer which is set into rotation by friction at the wall pushes itself out into the free fluid where it causes a complete transformation of the motion.”*

![[bound-layer-sep-examples.png]]

## Delaying boundary layer separation
Flow reversal depends on the trade-off between the adverse pressure gradient against the momentum diffusion. Hence more viscous flows delay their boundary layer separation by transferring momentum more effectively.

In aerodynamics, separation is bad because it increases drag, but increasing viscosity
- increases wall shear stress
- is totally impossible to engineer reasonably
So it is common to *inject* momentum near the separation point to increase momentum diffusion! This is one of (although not the main) purpose of leading-edge wing slats.

![[boundary-layer-momentum-injection.png]]

Another technique is to suck out the low momentum part of the boundary layer into the wing. This is possible but needs high power.
