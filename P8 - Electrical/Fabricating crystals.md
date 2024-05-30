Silicon forms strong covalent bonds so has a high melting point—difficult to grow.

## Obtaining pure $\mathrm{Si}$
- Start with quartzite $\ce{SiO_{2}}$
$$
\ce{SiC + SiO_{2} -> Si + SiO(g) + CO(g)} 
$$
- Improve the purity by converting to a more easily purifiable intermediate—trichlorosilane $\ce{SiHCl_{3}}$
$$
\ce{Si + 3HCl\rightleftharpoons SiHCl_{3} + H_{2}} 
$$
- Purify the trichlorosilane using fractional distillation then convert back using the reverse reaction.

## Czochralski process

To form a bulk single crystal:
- Melt high-purity $\ce{Si}$ just above its melting point ($\pu{1425\!\degree C}$)
- Dip in a seed crystal and slowly pull it upwards while slowly rotating

### Advantages
- No direct contact between the crystal and the walls

### Disadvantages
- Susceptibility to impurities
	- Oxygen $\ce{O_{2}}$
	- Carbon $\mathrm{C}$
	- Inhomogeneous dopant distribution

>The inhomogeneity of the dopant distribution can be reduced by using a magnetic field (MCz)

### Float zone growth
This is a technique to avoid impurities due to the contact between the walls and the melt. Use a heating element to selectively heat portions of the seed crystal locally so the melt never touches the walls.

## Forming wafers

Once the bulk single crystal is formed:
- The ingot is flattened along the grain (x-ray diffraction to find orientation)
- Then sliced into wafers

>The edges of the wafers are lapped (mutually abraded) using a slurry of $\ce{Al_{2}O_{3}}$ powder in glycerine

The wafer edges are rounded to reduce cracking.

## Epitaxy

Further layers of $\ce{c-SI}$ are grown on the wafers, and the deposited film takes on the same crystal structure and orientation as the underlying substrate crystal.

The feed layers can be applied by:
- a vapour phase
- molecular beam delivery

![[epitaxy.png|600]]

## Doping

While we can easily dope the Czochralski melt or epitaxial feed by mixing in impurities, it is harder to dope a layer that is already formed.

![[doping-mosfet.png|500]]

### Diffusion
One solution is to diffuse the dopants into the bulk. For low (nearly intrinsic) dopant concentrations, we can assume Fick’s Laws. 

So only the desired surface section is doped, use a silicon dioxide $\ce{SiO_{2}}$ mask layer.
- Some lateral diffusion will still occur!

### Ion implantation
One alternative is to ionise dopant atoms then accelerate them into the substrate to be implanted.

>After ionisation, filter out any remaining low charge density atoms

Post-implantation, rapidly anneal the sample to activate the dopants by smoothing our defects and encourage the dopants to bond with the lattice.

The number of implanted dopants at a depth $x$ into the substrate follows a Gaussian distribution:
$$
\operatorname{n}(x)= \frac{Q}{\sqrt{ 2\pi }\sigma}\exp \left\{ -\frac{1}{2}\left( \frac{x-R}{\sigma} \right)^{2}  \right\} 
$$
where $Q$ is the dopant ion flux density, $R$ is the projected range and $\sigma$ is the standard deviation in $R.$


## Thermal oxidation for $\ce{SiO_{2}}$ formation

There’s a trick we can use if we specifically want to form silicon dioxide $\ce{SiO_{2}}$ that gives high quality!

### Dry oxidation

Silicon reacts with oxygen at 700-1250°C:
$$
\ce{Si + O2 -> SiO2}
$$
The high temperature helps diffuse $\ce{O_{2}}$ into the reaction.
### Wet oxidation

We bubble the $\ce{O_{2}}$ through water to introduce steam.
$$
\ce{Si + 2H2O(g) -> SiO2 + 2H2}
$$
These conditions are more favourable and have a faster reaction rate.

# **tbc all of the below!!!**

## PECVD of $\ce{SiO2}$ and $\ce{SiN}$

- Radio frequency plasma enhanced chemical vapor deposition (rf-PECVD) is used1
- $\ce{SiO2}$ is deposited from $\ce{SiH4}$ and $\ce{N2O}$: $\ce{SiH4 + 4N2O -> SiO2 + 2H2O + 4N2}$1
- $\ce{SiN}$ is deposited from $\ce{SiH4}$ and $\ce{NH3}$, with $\ce{N2}$ as a diluent1
- PECVD $\ce{SiN}$ contains 20-25% hydrogen1

## LPCVD of $\ce{SiN}$

- Low pressure chemical vapor deposition (LPCVD) is preferred for $\ce{SiN}$ due to lower stress1
- $\ce{SiN}$ is deposited from $\ce{SiH2Cl2}$ and $\ce{NH3}$ at 800°C and 70 Pa1
- $\ce{SiN}$ stoichiometry can be tuned by adjusting the $\ce{SiH2Cl2}$:$\ce{NH3}$ ratio1
- LPCVD yields conformal, pinhole-free coatings, but is limited by the high temperature1

## Atomic Layer Deposition (ALD)

- ALD allows precise control of thin film stoichiometry and conformality1
- Reactants are introduced and purged in a cyclic manner1
- In thermal ALD, heat decomposes reactants which chemically bond to the surface1
- Plasma-enhanced ALD uses a plasma to assist reactant decomposition for higher growth rates