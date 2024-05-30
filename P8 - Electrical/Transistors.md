## Poisson’s equation
For electrostatic potential $\phi,$ s.t. $E=-\nabla \phi,$ from Gauss’s Law $\nabla\cdot E=\frac{\rho}{\varepsilon}$ we immediately have
$$
\nabla^{2}\phi= -\frac{\rho}{\varepsilon}
$$
Semiconductor charge density is related to the charge carrier number density by
$$
\begin{align}
\rho&=e(N_{D}+p-N_{A}-n) \\
&\approx e(N_{D}-N_{A})
 \end{align}
$$

## MOSFETs

A gate controls the resistance of the channel between terminals. 

### Depletion mode
Normally in the $\mathrm{ON}$ state, achieved by doping the channel semiconductor.

E.g., an $n$-channel $\mathrm{MOSFET}$ is $n$-type doped, resulting in excess $\mathrm{e}^{-}.$ Application of a negative gate voltage repels the $\mathrm{e}^{-}$ to create a depletion region.

The converse is true for the $p$-channel depletion mode MOSFET.

### Enhancement mode
Normally in the $\mathrm{OFF}$ state, achieved with either a $\mathrm{PNP}$ or $\mathrm{NPN}$ junction. This creates a central depletion region. When the gate voltage is applied, charge carriers are generated.

tbc inversion mode of operation.


## $\mathrm{MOSFET}$ transit time
At low electric fields, 
$$
v_{d}=\mu E
$$
At high fields, the velocity saturates s.t. $v_{d}\leq v_{s}.$

$$I_{s}=\frac{Q}{t}=\frac{\rho wDL}{t}=qN_{D}wv_{s}$$


## Thin-film transistors (TFTs)

Similar behaviour to enhancement-mode $\mathrm{MOSFET}$s but with a different construction. At $V_{gs}=0,$ there is no channel. At $V_{gs}>0,$ there is a conductive channel of $\mathrm{e}^{-}$ between the source and drain.

The channel potential $U=U(y)$ (with the $y$-direction going from source to drain) can be imagined as a sheet of $\mathrm{e}^{-}$ of cross-sectional area $A.$

$$
\frac{I_{ds}}{A}=\rho v_{d}=\rho \mu E=\rho \mu \frac{ \partial U }{ \partial y } 
$$
Given capacitance per unit area $c,$

tbc

When $V_{ds}<V_{gs}-V_{T},$ the transistor behaves in linear operation like a resistor. For $V_{ds}\geq V_{gs}-V_{T},$ the channel pinches-off and is saturated at a constant $I_{ds}.$

## MESFETs
$\mathrm{MESFET}$s—metal semiconductor field effect transistors have no insulator between the gate and the semiconductor. At their boundary, contacts which are either:

- Ohmic—$\mathrm{GS}$  junction behaves like a resistor
- Schottky—diode-like contact. Depletion region at the interface.

$\mathrm{MESFET}$s are used for high frequency operations.

## Materials

Common materials:

- $\mathrm{Si}$—general purpose, abundant, easy to make defect-free high purity wafers
- $\mathrm{GaAs}$—used at high-frequencies, takes advantage of the [[Semiconductors#E-$k$ diagram|Gunn effect]], used in MESFETs (which target high-frequency applications). But [[crystals]] quite defective.
- $\mathrm{GaN}$—used at high-voltages, has wide band-gap, high breakdown voltage.


>$\mathrm{GaN}$ is also used to make blue / $\mathrm{UV}$ LEDs—c.f. Veritasium video