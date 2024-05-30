#materials 

The equilibrium [[Phase diagrams|phase diagram]] and the [[Lever rule]] show that phase composition during freezing is not constant during the plastic melting region, but settles on a uniform solid phase composition that matches the alloy composition.

However, in practice, this equilibrium state is not achieved due to insufficient time for diffusion. Instead there is a radial composition gradient within each grain and throughout the bulk.
![[Segregation.png|400]]
A similar process leads to a non-uniform impurity distribution due to much higher impurity solubility in the liquid phase—therefore impurities are rejected to the growing grain boundaries (micro-segregation) and to the casting centre (macro-segregation).

## Consequences
- non-uniform yield strength distribution 
- possible *porosity* through the impurities
- reduced toughness due to stress concentration around sharp impurities

## Solutions
- reduce grain size, e.g., by using [[Casting metals#Inoculants|inoculants]]
- [[High alloy steels|further alloying]] to react with impurities and trap them as salts
- re-homogenisation of the casting by reheating to encourage diffusion

## Modelling homogenisation
Modelling the initial fluctuation distribution as a [[Thermal conduction#Sinusoidal response|sinusoid]] with:
- wavelength of the grain width $d$, 
- mean value $C_{0}$
- Mean-to-peak amplitude $C_{a}$

Then the time response under homogenisation can be approximated as:$$
C(x,t)=C_{0}+(C_{a}-C_{0})\cos\left( \frac{2\pi}{d} \right)\exp\left( -\frac{4\pi^{2}Dt}{d^{2}} \right)
$$This has an exponential time constant of$$\tau= \frac{d^{2}}{4\pi^{2}D} \quad\mathrm{s.t.}\quad D=D_{0}\exp\left( -\frac{Q_{a}}{RT} \right)$$which has a strong temperature dependence and grain size dependence. As temperature increases and grain size decreases, the rate of homogenisation rises.

As before, this small grain size optimal for homogenisation can be achieved by an inoculant dispersion.