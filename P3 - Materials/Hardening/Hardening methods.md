#materials 
## Precipitation hardening
For small precipitates, yield stress is inversely proportional to obstacle separation:$$\boxed{\sigma_{y}\propto \frac{1}{d}}$$![[precip-shear.png|400]]
As the precipitate grows, the yield stress trades-off against the obstacle’s ability to resist being bypassed due to its size:$$\boxed{\sigma_{y}\propto \sqrt{ r }}$$![[dislocation-pinning.png|500]]
Coarsening (tendency for small precipitates to morph into larger, more spaced-out precipitates due to surface energy penalty) sets the trade-off between the resistance to line bypass and precipitate shearing.
 ![[precip-bypass-shear.png|300]]
See [[Aluminium heat treatment#Ageing]] for how this coarsening affects choices in material processing

## Solid solution hardening
tbc

## Grain boundary hardening
Yield strength increases as grain size decreases
$$
\sigma_{y}=\frac{A}{\sqrt{ d }}+B
$$

## Work hardening
Yield strength increases as dislocation density $\rho_{d}$ increases (as the dislocation spacing $s$ decreases). As in precipitation-hardening, the dislocations pin each other so
$$
\begin{align}
\sigma_{y} & \propto \frac{1}{s}\quad\mathrm{s.t.}\quad s^{2}=\rho_{d} \\
& \propto \sqrt{ \rho_{d} }
\end{align}
$$
A realistic model of the work hardening stress-strain curve is a power-law relationship,$$
\sigma=A\varepsilon^{B}
$$![[work-hardening-power-law.png]]