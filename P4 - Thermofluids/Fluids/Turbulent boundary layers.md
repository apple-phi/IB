So far we’ve only looked at laminar boundary layers, which behave like a stack of thin parallel fluid layers. Now lets face the horror of turbulent boundary layers.
## Reynolds numbers in a boundary layer
Instead of measuring $\mathrm{Re}$ relative to the wall distance $\delta$, it is often more convenient to take it relative to $x$,
$$
\mathrm{Re}_{x}=\frac{\rho Vx}{\mu}
$$
where the relationship between $\delta$ and $x$ has previously been established:
$$
\begin{align}
\delta & \sim \sqrt{ \frac{\mu x}{\rho V} } \\\\
\Rightarrow\quad \delta  & \sim \frac{x}{\sqrt{ \mathrm{Re}_{x} }}
\end{align}
$$

## Momentum loss
As the boundary layer grows, the flow loses momentum by fricative shear from the wall.
![[turb-mom-loss-layers.png]]
Relating the momentum loss to the wall shear stress:
$$
-\int_{0}^{x} \tau_{w} \, \mathrm{d}x =\int _{0}^{\delta}\rho vv \, \mathrm{d}y - \rho VVh
$$
The height $h$ is unknown, but by continuity, we have
$$
V_{x}\int _{0}^{\delta}\rho v \, \mathrm{d}y=V_{x}\cdot\rho Vh 
$$
So, eliminating $h$
$$
\int _{0}^{x}\tau_{w} \, \mathrm{d}x=V\int _{0}^{\delta} \rho v\, \mathrm{d}y-\int _{0}^{\delta}\rho v^{2} \, \mathrm{d}y   
$$
Using the previous approximate relationship for the boundary layer growth:
$$
v(y)=V\left[ \frac{3y}{2\delta}-\frac{1}{2}\left( \frac{y}{\delta} \right)^{3} \right]
$$
The wall shear stress is
$$
\tau_{w}=\mu \left.\frac{ \mathrm{d}v }{ \mathrm{d}y }  \right|_{y=0}= \frac{3\mu V}{2\delta}
$$
The momentum flux on entry is
$$
V\int _{0}^{\delta}\rho v \, \mathrm{d}y=\frac{5}{8}\rho v^{2}\delta 
$$
The momentum on leaving the CV is
$$
\int _{0}^{\delta}\rho v^{2} \, \mathrm{d}y=\frac{17}{35}\rho v^{2}\delta 
$$
Combining all that with the previous relationship between wall shear and net momentum loss eventually gives
$$
\int _{0}^{x}  \frac{\mathrm{d}x}{\delta} = \frac{13\rho V\delta}{140\mu}
$$
So differentiating with respect to $x$ gives
$$
\begin{align}
\delta^{2} & = \frac{280}{13} \frac{\mu x}{\rho V} \\
 \\
\Rightarrow\quad \delta & =4.64 \frac{x}{\sqrt{ \mathrm{Re}_{x} }}
\end{align}
$$
By combining the equation for momentum loss in a boundary layer with the velocity profile $v(y)$, we were able to calculate the boundary layer growth $\delta(x)$. However, this derivation is very sensitive to the velocity gradient at the wall.
## Transition to turbulence
The Reynolds number compares the strength of advective and viscous terms. In a boundary layer it increases as the flow moves downstream.

At high $\mathrm{Re}$, the viscosity is not able to support the flow shear and the flow breaks down into smaller, disorganised eddies, until the size scale is small enough for the viscosity to act. I.e., at some point down the boundary layer, it transitions to turbulence.
![[re-bound-layer-1.png]]
In controlled, ideal environments, this transition is very sudden, but in reality the transition is usually less organised, although it still occurs over a short distance scale.
## The effect of turbulence
Turbulence increases the rate of momentum transfer between the surface and the free stream. This has three main results:
- Faster boundary layer growth
- Fuller velocity profile
- Higher skin friction
![[turb-bound-layer.png]]
As we have seen previously, the trade-off between momentum transfer and the adverse pressure gradient, and this trade-off determines the possibility of flow reversal. Turbulence increases momentum transfer, and hence reduces the possibility of flow reversal.
![[turb-flow-rev.png]]

Therefore, turbulent flows are more resistant to flow separation due to the adverse pressure gradient.
![[turb-flow-sep.png]]

## Effect of separation on pressure
The separation gives rise to a low pressure zone on the back face of the obstacle, because the flow is, on a time average, approximately stationary. The pressure is approximately the same as at the separation point. This causes a suction force known as *pressure drag* or *form drag*.
![[form-drag.png|600]]

Since turbulence can delay boundary layer separation and hence produce a smaller separation region, turbulence also mitigates this form drag by reducing the size and magnitude of the low pressure region.
![[golf-ball-turb.png]]
>Golf balls are dimpled to trigger turbulence for exactly this reason!
## Transition vs. separation
Although boundary layer separation and turbulence transition are entirely different phenomena, the transition to turbulence often occurs in just-separated boundary layers.
![[transition-vs-separation.png]]
This is because just-separated laminar boundary layers have an inflection point in their velocity profile,
$$
\exists\quad\frac{ \mathrm{d}^{2}v_{x} }{ \mathrm{d}y^{2} } =0
$$
These adverse pressure gradients are inherently unstable and cause the flow to be more likely to become turbulent.
![[inflection-point.png]]
Most flows transition almost immediately to turbulence upon flow separation. However, very viscous separated flows have a high enough viscosity to damp any perturbations, and hence stay laminar. But without an adverse pressure gradient, these flows’ boundary layers will become turbulent *without* undergoing separation!
## Boundary layer reattachment

The fuller velocity profile of turbulent boundary layers may have a sufficiently enhanced momentum transfer to overcome the adverse pressure gradient that initially produced the separation, and will reattach!
![[separation-bubble.png|600]]

Aerofoils are often designed to minimise the size of the separation bubble. If it were too big, the form drag would reduce the lift.