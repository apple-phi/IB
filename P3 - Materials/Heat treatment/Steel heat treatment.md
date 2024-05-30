#materials 
## Properties
| State | $\sigma_{y}\mathrm{\ /\ MPa}$ | Treatment |
| ---- | ---- | ---- |
| $\alpha+\mathrm{pearlite}$ | 200–450 | normalised |
| $\alpha+\mathrm{bainite}$ | 500–700 | hot quenched |
| $\mathrm{martensite}$ | 1000–3000 | cold quenched |
## Slow-cooling
Consider the normalisation (slow-cooling) of hypo-eutectoid [[Iron-Carbon system|steel]] from austenite to $\alpha$-ferrite and pearlite:$$\boxed{\gamma\rightleftharpoons \gamma+\alpha\rightleftharpoons\alpha+\mathrm{Fe_{3}C}}$$![[steel-hypoeutectoid.png]]
As the ferrite and pearlite phases are rejected from the austenite they tend to nucleate [[Nucleation#Heterogeneous nucleation|heterogeneously]] along and grow perpendicularly to the grain boundaries:

![[steel-normalisation.png]]

The strength range of the result is about 200–450 MPa and increases with the fraction of pearlite due to the hard, brittle cementite in the lamellar pearlite. The fraction of pearlite is set by the alloying composition in the two-phase region by the [[Lever rule]].

## Quenching (rapid-cooling)
This is the [[Transformation diagrams#TTT (Time-Temperature-Transformation)|TTT diagram]] for constant-temperature quenching of 0.4% wt. C hypo-eutectoid steel:![[steel-TTT.png]]
### $\alpha$-ferrite + pearlite
The carbide line marks the transition from ferrite formation to pearlite formation. A quench and hold at high temperatures above the “nose” of the C-curves (but still in the region that eventually forms pearlite) produces a similar microstructure to slow-cooling:
![[steel-high-temp-quench.png|200]]
The position of the carbide line depends on the [[Steel composition and the TTT diagram|steel composition]].
### $\alpha$-ferrite + bainite
At high, non-martensitic temperatures but below the “nose” of the C-curves, the austenite transforms directly to bainite ($\alpha$-ferrite finely dispersed with cementite).$$\gamma\longrightarrow\alpha+\mathrm{Fe_{3}C}$$This bainite nucleates heterogeneously at the austenite grain boundaries by the simultaneous precipitation of $\alpha$-ferrite and cementite into a ferrite matrix proliferated by cementite needles (instead of pearlite).
![[bainite-formation.png|200]]
Bainite has the ideal microstructure for [[Hardening methods#Precipitation hardening|precipitation hardening]]—a fine, uniform dispersion of hard precipitates. Its yield strength is in the range of 500–700 MPa. 
### Martensite
When quenched to a temperature that results in cooling faster than the Critical Cooling Rate, much like in [[Aluminium heat treatment|aluminium cooling]] a metastable phase is formed—in this case martensite.$$\gamma\longrightarrow\alpha'$$This is a supersaturated solid solution of $\mathrm{C}$ in $\mathrm{Fe}$, but unlike in $\mathrm{Al}$ quenching, the supersaturation of the solid solution holds the iron lattice in its austenitic FCC configuration rather than the equilibrium BCC configuration.

To overcome this, martensite has an associated phase transformation where it shears (a diffusion-less process) at near to the speed of sound to conform more closely to the BCC configuration.
![[martensite-shear.png]]
This results in the martensite grain being misaligned with the surrounding austenite.
![[martensite-grain-alignment.png|500]]
Because this process occurs without [[Fick's Laws|diffusion]], it has no cooling rate dependence and the contours showing transformation progress are horizontal.

However, the final temperature dictates the fraction of austenite transformed into martensite. This is because the formation of martensite minimises free energy sufficiently to compensate for the degree of [[Nucleation#Undercooling for nucleation|undercooling]] so further undercooling is required to progress the transformation.
![[martensite-fraction.png]]
The minimum undercooling occurs at the martensite start temperature and all unstable austenite is converted into martensite at the martensite finish temperature. These temperatures depend on the [[Steel composition and the TTT diagram|steel composition]].

Martensite has a very high yield strength (1000–3000 MPa) due to effective [[Hardening methods#Solid solution hardening|solid solution hardening]] which is enhanced by the lattice distortion—many interstitial holes contain oversized carbon atoms. A higher carbon composition increases these effects and makes martensite harder.
![[martensite-hardness.png|500]]

> Martensite is very brittle and its fracture toughness of $<5 \mathrm{\ MPa/\sqrt{ m }}$ is often considered negligible.
## Tempering
Martensite is too brittle to be commonly used as-quenched. Therefore, it is typically tempered at 450–600°C to encourage diffusion.
- This increases fracture toughness
- But decreases yield strength to about 450–800 MPa
$$
\mathrm{martensite}\longrightarrow\alpha+\mathrm{cementite}
$$
Microstructurally, tempering encourages diffusion so the $\mathrm{Fe}$ matrix transforms into its equilibrium BCC state while the supersaturated $\mathrm{C}$ diffuses into $\mathrm{Fe_{3}C}$ cementite precipitates which then coarsen.
![[martensite-tempering.png]]
This coarsening (softening) rate increases with temperature. More coarsening decreases strength.
![[martensite coarsening.png|500]]
The temper temperature also sets the precipitate fraction, as can be seen on the [[Iron-Carbon system]] phase diagram.

The fine dispersion of hard cementite provides excellent precipitation hardening. Tempered martensite has a yield strength 2–3 times greater than if slow-cooled, but with a similar fracture toughness. Therefore, component cross-sections can be decreased, or be designed for higher loads.