Deformation-processed metals are known as *wrought*. They must be sufficiently *ductile* to strain without failing. These deformation processes are typically done in compression to avoid the risk of necking and tensile failure.

## Motivation
- More flexibility in alloy choice than in [[Casting alloys|casting]]
- Lower energy consumption (high temperatures not needed)
- Better surface finish
- Better dimensional accuracy

## Cold-working
- The grains change shape and become anisotropic
- [[Hardening methods|Work hardening]] occurs

Work hardening is useful to increase strength, but it risks fracture and also needs higher and higher forces throughout each subsequent deformation step.

To make processes with many steps or large strains possible, we need to increase the ductility periodically, e.g., by annealing.

## Annealing
The material is heated to reverse the effects of work hardening:
- lower yield strength
- higher ductility

By selecting the optimal annealing times, the material parameters can be maintained according to the manufacturing requirements and consumer specifications.
![[when-to-anneal.png|400]]
The microstructural changes during annealing are driven by the stored elastic energy due to the increased dislocation density. During plastic deformation, the ~5% of energy that is not lost as heat is stored as dislocations that induce elastic strain in the surrounding lattice. Annealing allows this elastic strain to relax.

### Recovery mechanism
One microstructural annealing method is for dislocations to rearrange into a configuration that minimises elastic lattice strain. Recovery only results in a small drop in dislocation density and strength, and requires a minimum annealing temperature of
$$
T_{\mathrm{min}}\approx 0.1T_{\mathrm{freezing}}
$$
This occurs by:
- Dislocations of opposite orientation can annihilate
![[dislocation-annihilation.png|200]]
- Dislocations of similar orientations can align and form sub-grains
![[dislocation-subgrains.png]]
### Recrystallisation mechanism
Another annealing mechanism is to nucleate new grains and replace the old distorted grains. This is a much more significant microstructural rearrangement so requires a higher minimum annealing temperature of$$
T_{\mathrm{min}}\approx 0.3T_{\mathrm{freezing}}
$$but results in a decrease in dislocation density by a factor of about $10^{4}$. This large drop in $\rho_{d}$ corresponds to a large drop in $\sigma_{y}$

![[annealing-recrystallisation.png]]
The driving force of this grain nucleation is the dislocation strain energy. So, with higher initial bulk plastic strain there will be more dislocations and so more stored elastic energy in the lattice. Hence, more work hardening corresponds to smaller nucleated grains (lower bounded by the original grain size).
![[recrystallisation-grain-size.png|600]]

> There is a critical amount of work hardening required for there to be enough stored energy to overcome the nucleus surface energy and [[Nucleation|nucleate]] new grains.

If held at high temperatures after recrystallisation, the grains will grow by interdiffusion, thermodynamically driven to reduce the surface area to volume ratio.

## Hot-working
In practice, the issues caused by cold-working are avoided by deforming the material while hot instead.

This has several benefits:
- stays ductile since strength kept low
- lower tool forces required
- a single step can give larger strains
- no need for separate [[Steel heat treatment|heat treatment]] since already hot

