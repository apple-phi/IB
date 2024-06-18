## Assumptions

The eye needs to maintain its shape. Assume it is a shell that is
- thin-walled
- spherical
- pressurised
- no bending stresses (only biaxial stress)

The wall properties are given by the sclera and cornea, neglecting more detailed features like the optic nerve.

$$
\sigma= \frac{pr}{2t}
$$
where $p$ is the intraocular pressure (IOP).

## Ocular rigidity
Using a linear relationship between biaxial wall stress $\sigma$ and strain $\varepsilon,$
$$
E= \frac{\sigma}{\varepsilon}(1-\nu)
$$
The 1-form of the spherical volume is
$$
\begin{align}
\mathrm{d}V&=\mathrm{d}\left\{ \frac{4}{3}\pi r^{3} \right\}  \\
&=4\pi r^{2}\,\mathrm{d}r \\
\Rightarrow\quad  \frac{\mathrm{d}V}{V}&=\frac{3}{R}\mathrm{d}R \\
&=3\,\mathrm{d}\varepsilon
 \end{align}
$$
## Tonometry

Changes in $\mathrm{IOP}$ are implicated in diseases like glaucoma. We can indirectly measure $\mathrm{IOP}$ by measuring deformation of the cornea.

Goldmann tonometry:
- Anaesthetize cornea
- Place tonometer on cornea with force W

tbc


## Blood flow

- No vasculature in the lens and cornea—nourishment from the aqueous humour instead
- Model blood flow as a fricative pipe
	- This is the Starling resistor model

![[blood-pipe.png]]

## Fluid flow in tissues

We can apply a linear poro-elastic model:
- Solid phase is isotropic, linear elastic
- Time dependence due to fluid flow

![[fluid-tissues.png]]

## Darcy’s Law for convection flow

The volumetric fluid flow rate $Q$ along a medium with length $L$ due to pressure difference $p$ through an area A with hydraulic permeability $\kappa$ is
$$
Q= \frac{\kappa pA}{L}
$$
The time constant of the fluid flow is given by
$$
\tau=\frac{L^{2}}{E\kappa}
$$
The intrinsic permeability for a fluid with fluid viscosity is $k=\eta \kappa.$

### Example

Bruch’s membrane is a five-layer barrier limiting transport between the choroid and the outer retina, where water moves under the action of hydrostatic and osmotic pressure gradients.

As you age, lipid accumulation increases the hydraulic resistivity.

![[hydraulic-resistance.png|400]]

### Example

Scleral drug delivery is a promising alternative to corneal drug delivery. To find out the direction of fluid transport, consider the trade-off between convection flow and diffusion.

The result is that $\kappa p\gg D,$ confirming that the drug delivery pathway has a sufficient transport rate.

## Aqueous humour flow regulation

The aqueous humour has several key functions:
- Pressurises eye (source of IOP)
- Nourishes cornea and lens (which have no vasculature)
- Clears debris from eye

Production of the aqueous humour peaks in the morning, and is minimised at night. It is drained principally at trabecular meshwork (the conjunction of the iris, cornea and sclera) as well as via Schlemm’s canal.

It has a fluid resistance of $3\!-\!\pu{4mmHg/(\mu L/min)},$ due to
- Proteoglycan-rich gels in the trabecular meshwork
- Endothelial lining of Schlemm’s canal

## Drainage control of IOP

### Resistance of the trabecular meshwork 

The amount of fluid-resistive gels is produced to set the IOP.

![[trabecular-control-of-iop.png|500]]

### Resistance of Schlemm’s canal (mechanotransduction)

The arteries adjust their diameter in response to the wall shear stress to set the rate of fluid flow. This mechanism is supported by the preferential alignment of endothelial cells in the canal.

> Assume laminar Poiseuille flow governed by viscous forces (low Reynolds number since the vessels are small).

## Glaucoma
tbc

