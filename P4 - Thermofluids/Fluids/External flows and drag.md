## Lift and drag
Expressing the coefficients of lift and drag as dimensionless,
$$
\begin{align}
C_{\ell} & = \frac{\mathrm{lift}}{1 /2\rho V^{2}A} \\
C_{d} & = \frac{\mathrm{drag}}{1 /2\rho V^{2}A}
\end{align}
$$
If the flow is incompressible (at low Mach number) these coefficients are functions of
- geometry
- surface roughness
- angle of attack
- Reynolds number

Real fluids with non-zero viscosity produce boundary layers near solid surfaces which generate a frictional shear stress—skin friction drag.

When the flow separates, a low pressure region forms behind the separation point—form drag.

These two phenomena trade-off against each other.

Bluff bodies:
- lower skin friction
- higher form drag

Streamlined bodies:
- higher skin friction
- lower form drag

Consider the $C_{d}$ for a sphere:
![[sphere-cd 1.png]]

>Note that spheres *don’t* produce lift due to their geometric symmetry.

## Flows at low Reynolds numbers
Here the viscous forces dominate and the flow is perfectly attached and unseparated. Hence there is no form drag. 

![[low-re-flow 1.png|600]]
The whole flow resembles a very thick boundary layer.

>The viscosity is so high that our intuition breaks down somewhat.

Applying Navier-Stokes,
$$
\rho \frac{\partial \mathbf{v}}{\partial t}+\rho \mathbf{v}\cdot \nabla \mathbf{v}=-\nabla p+\mu \nabla^{2}\mathbf{v}
$$
The inertial (advective) terms are negligible relative to the viscous terms hence
$$
\nabla p = \mu \nabla^{2}\mathbf{v}
$$
This is known as Stokes creeping flow. For the flow around a sphere there is an analytical solution.

![[stokes-flow-sphere 1.png|500]]

![[sphere-stokes-flow-geometry 1.png|500]]
The total drag is $6\pi \mu RV$ so the drag coefficient is
$$
\begin{align}
C_{d} & = \frac{6\pi \mu RV}{\frac{1}{2}\rho V^{2}\pi R^{2}} \\
 & =\frac{24\mu}{\rho Vd} \\
 & =\frac{24}{\mathrm{Re}}
\end{align}
$$
Stokes' flows have a similar streamline profile to inviscid flow but they differ in that they
- only exist at very small length scales
- satisfy the no-slip boundary condition

## Flows at moderately low Reynolds number (10-100)
Behind a sphere, the low pressure zone forms a toroidal region due to circulation.
![[sphere-toroidal-flow 1.png]]
The low pressure in the toroidal region is approximately the same as at the separation point—this is the origin of form drag.

Hence, form drag begins to dominate $C_{d}$.

![[form-drag-sphere 1.png]]
The separation point is determined by the trade-off between the free stream momentum diffusion and the adverse low pressure gradient.

As the Reynolds number increases, the effects of viscous forces decreases so the significance of the momentum diffusion decreases and the low pressure region grows.

## Flows at moderately high Reynolds number

The form drag dominates more and more and skin friction becomes negligible. The separation point remains very near the shoulder and the drag coefficient remains approximately at
$$
C_{d}=0.4
$$

## Flows are very high Reynolds number

At extremely high Reynolds numbers (>200000), the boundary layer becomes turbulent before it reaches the shoulder. This turbulence increases the momentum diffusion into the free stream, and the flow is more able to resist separation. 

The separation drops back and there is a sudden drop in form drag.

## Use and limitations of inviscid flow models

Inviscid flow models imply perfect slip and no boundary layers. Hence there is no boundary layer separation, even at very high adverse pressure gradients.

>Although it is tempting to assume, inviscid flow is *not* the solution as Reynolds number tends to infinity.

Assuming inviscid flow is only reasonable is boundary layers are tin and closely attached. This requires favourable pressure gradients.

However, solving the inviscid flow model is much simpler than the full Navier-Stokes solution. The resulting pressure gradients can be used to estimate the separation point, and in turn include these separated regions to obtain the new inviscid solution in the modified domain.

## Drag reduction—streamlining

$$
\begin{align}
\text{skin friction drag} & \sim \text{surf. area }\times \frac{\mu V}{\delta} \\
\text{form drag} & \sim \text{wake area }\times \frac{1}{2}{\rho V^{2}}
\end{align}
$$Many important applications (cars, planes, ships) are at high Reynolds number so form drag dominates skin friction. Hence the priority is to reduce the form drag by delaying boundary layer separation through altering the geometry.

![[drag-reduction.png|700]]

Streamlining has the side-effect of increasing skin friction, but this is still negligible unless at low Reynolds number.

## Drag reduction—other methods
We previously mentioned two ways to delay boundary layer separation:

![[flow-injection-and-suction.png]]
An easier method is to reduce form drag by triggering turbulence earlier by roughening the surface. Once again, this also increases skin friction, but the benefits outweigh this cost.

![[bluff-body-drag-reduction.png]]

## Resonance due to the laminar-turbulent transition

The sudden drag reduction at the laminar-turbulent transition and the corresponding separation delay can lead to resonance.
![[drag-resonance.png|600]]
Consider a lamppost free to move. The incoming wind changes the lamp velocity, and if the Reynolds number is just right, this change in lamppost velocity trips a sudden change in drag in phase with the lamppost oscillations.

## Flow instability and vortex shedding
Separated boundary layers create a shear layer that is inherently unstable due to inflection points in their velocity profiles. They develop waves that rolls up into Kelvin-Helmholtz vortices.
![[kelvin-helmholtz.png]]

Returning to the bluff cylinder example, there are two approximately-parallel layers behind the sphere. They feed back on each other and resonate, and the resting flow is even more unstable than a single shear layer.

![[bluff-cylinder-vortices.png]]

The shear layers snake up and down together and roll up into vortices that are shed alternately from each side of the cylinder, known as vortex shedding.

The vortex shedding frequency is a function of the flow velocity and the distance between the shear layer. This has importance consequences for slender structures which risk resonance.