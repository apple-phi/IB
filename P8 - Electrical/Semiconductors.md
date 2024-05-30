Depending on the affinity of the electrons to electrostatic bonds, there is an *energy gap* between the valence band and the conduction band orbitals. Electrons in the conduction band are delocalised.

![[energy-gap.png|500]]

## Charge carriers

Both electrons in the conduction band and holes in the valence band contribute to current flow.
![[valence-band-holes.png|300]]

The intrinsic carrier concentration (number density of free carriers at thermal equilibrium) $n_{i}$ is related to the temperature by
$$
n_{i}\propto \sqrt{ T }^{3}\exp \left\{- \frac{1}{2} \frac{E_{g}}{k_{b}T} \right\} 
$$
Or, equivalently,
$$
n_{i}^{2}\propto T^{3}\exp \left\{ -\frac{E_{g}}{k_{b}T} \right\} 
$$
[charge - Semiconductor intrinsic carrier concentration is given by ni=BT^(3/2)\*exp(-E/2kT), how is this derived? - Physics Stack Exchange](https://physics.stackexchange.com/a/164788)

>Thermal equilibrium requires that the material is kept in the dark with no electrical bias.

At thermal equilibrium, the number of electrons $n$ and the number of holes $p$ are both equal to the intrinsic carrier concentration $n_{i}.$

$$
n=p=n_{i}
$$
This can be extended to extrinsic (non-intrinsic) cases with the following equality:
$$
n^{2}_{i}=np
$$

## Doping

By adding impurities to the lattice, the electron and hole concentrations can be changed from the intrinsic.

### N-type
By adding atoms with 5 valence $\mathrm{e}^{-},$ into a silicon (diamond-like) lattice, there is one delocalised $\mathrm{e}^{-}$ unused in bonding which is donated to the lattice. Then the $\mathrm{e}^{-}$ number concentration is
$$
\begin{align}
n&=n_{i}+N_{d} \\
&\approx N_{d}
 \end{align}
$$
>Example: $\ce{P},$ phosphorus

### P-type

By adding atoms with 3 valence $\mathrm{e}^{-}$ into a silicon (diamond-like) lattice, there is one missing bond. This hole accepts an electron from the lattice, leaving behind a positively charged hole. The hole number concentration is then:

$$
\begin{align}
p&=n_{i}+N_{a} \\
&\approx N_{a}
\end{align}
$$

> Example: $\ce{B},$ boron

## Carrier velocity

Charge carriers move in a random walk by repeatedly accelerating and scattering upon collision. Under **small** electric fields, the drift velocity $v_{d}$ is
$$
v_{d}\approx \mu E
$$
where $\mu$ is the mobility constant.

The mobility can be intuitively described by the force balance
$$
\begin{align}
\dot{p}&=F \\
\frac{m^{*}v_{d}}{\tau}&=qE \\ \\
\Rightarrow\quad v_{d}&=\overbrace{ \frac{q\tau}{m^{*}}}^{\mu}E

 \end{align}
$$
where $m^{*}$ is the effective mass accounting for inertia due to lattice collisions.
$$
\begin{align}
m^{*}&=\frac{\hbar^{2}}{\partial_{k}^{2}E} \\
&=\frac{ \partial^{2} p }{ {2\,\partial E}^{2} } 
 \end{align}
$$
where $E$ is the charge carrier energy and $k$ is the wavenumber s.t. $p=\hbar k$

![[drift-velocity.png|300]]

>Non-examinable—the dip in $\ce{GaAs}$ is the Gunn effect caused by inter-valley transfer in the E-$k$ diagram

## E-$k$ diagram

![[effective-mass.png|600]]
The effective mass of an $\mathrm{e}^{-}$ with energy $E$ at wavenumber $k$ is given by the instantaneous curvature of the E-$k$ curve.

Direct gap semiconductors:
- e.g. GaAs
- the conduction band minimum and valence band maximum occur at the same k-value
- efficient energetic transitions

Indirect gap semiconductors:
- e.g. Si
- the extrema are at different wavenumbers
- less efficient energetic transitions

## Drift current
The current due to the applied electric field $E=\partial_{x}V$ is
$$
\begin{align}
I&=nA\bar{v}e \\
&=(n\mu_{n}+p\mu_{p})EAe
 \end{align}
$$
where $e$ is the $\mathrm{e}^{-}$ charge.

So the applied voltage required to induce that current is
$$
\begin{align}
\int I\,\mathrm{d}x&=\int(n\mu_{n}+p\mu_{p})Ae\,\mathrm{d}V \\ \\
\Rightarrow\quad V&=\frac{I}{e(n\mu_{n}+p\mu_{p})} \frac{L}{A}
 \end{align}
$$
hence the conductivity of the semiconductor is
$$
\sigma=en\bar{\mu}=e(n\mu_{n}+p\mu_{p})
$$
