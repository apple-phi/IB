## Active Matrix Displays
Consists of:
- Pixel control [[transistors]] (i.e. TFTs)
- A light-emitting material (e.g., LEDs)
- External drivers

![[active-matrix-display-arch.png]]

## Light modulators
### Liquid crystal displays

Liquid [[crystals]] are a phase of matter between liquid and crystal—rod-shaped and about $\pu{25Å}$ long. Two kins: nematic (threadlike) and smectic (soap-like in slip planes).

Nematic LCs twist to follow the orientation of polarised light, which can be controlled with applied electric fields.

![[LCD.png|300]]

![[display-anatomy.png]]

### E-ink
Lots of microcapsules filled with black and white pigment particles of opposite charges. By applying an electric field, the charges attract or repel to either show black or white on the top.
![[e-ink.png|400]]

### LEDs

By forward-biasing the diode, the potential barrier lowers so recombination occurs by mutual diffusion of holes and $\mathrm{e}^{-}.$ This releases light.

![[leds-semiconductor.png|350]]

## Pixel circuits
### Voltage-regulated
Used for LCDs or E-ink. $\mathrm{TFT}$ used as a switch, biased in linear operation (to act like a resistor whose resistance is set by the gate).
![[v-pix-circ.png|400]]
The small-signal resistance of the $\mathrm{TFT}$ in linear operation is
$$
R_{\mathrm{TFT}}=\frac{\mathrm{d} V_{ds}}{\mathrm{d}I_{ds}} \approx \frac{1}{\mu C_{ox} \frac{W}{L}(V_{gs}-V_{T})}
$$
so the $\mathrm{RC}$ time constant is
$$
\tau=R_{\mathrm{TFT}}C_{s}
$$
### Current-regulated
Used for $\mathrm{LED}$ displays. Use two $\mathrm{TFT}$s, one as a switch (linear bias, resistor-like) and the other as a current source (in saturation mode). 
![[current-pix-circ.png|300]]
Since T2 is in saturation mode,
$$
V_{gs}=V_{\mathrm{data}}
$$
hence the current is
$$
I_{ds}= \frac{1}{2}\mu C_{ox} \frac{W}{L}(V_{gs}-V_{T})^{2}
$$
