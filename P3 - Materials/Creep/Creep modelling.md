Creep is time-dependent plastic deformation which typically occurs at high temperatures in metals.

It produces continued strain under constant stress, which can lead to necking, unwanted elongation, and tensile failure (creep rupture).
![[creep-strain.png]]
It also produces stress relaxation under constant strain, which can lead to bolts slackening over time.
![[creep-stress.png]]
>For crystalline materials, creep becomes significant at about $T=0.5T_{m}$

## Modelling
![[creep-stages.png]]
Steady-state creep dominates creep life so this is what component design usually focuses on minimising.

It is well modelled by a combination of a power law and the [[Rates of reaction|Arrhenius law]],
$$
\dot{\varepsilon}_{ss}\propto\sigma^{n}\exp\left( \frac{Q_{a}}{RT} \right)
$$
To obtain the power law parameters and activation energy, logarithmic plots at constant $T$ or $\sigma$ can be used respectively.

## Creep rupture
Creep failure begins with the [[Nucleation#Heterogeneous nucleation|nucleation]] of voids along grain boundaries, which reduce the cross-sectional area and increase the stress, accelerating the void growth and producing the transition to tertiary creep, then creep rupture.
![[creep-rupture.png|300]]
The time till failure can be empirically modelled by the Monkman-Grant relationship:
$$
\dot{\varepsilon}_{ss}t_{f}=C
$$
Here the material constant $C$ represents a critical strain at failure.

## Creep mechanism maps
The dominant creep mechanism depends on the temperature and the applied stress. This dominant mechanism can be visualised by a creep mechanism map.
![[creep-mechanism-map.png]]
This map can also be used to calculate the local creep exponent for each mechanism, noting that the steady-state Arrhenius power law given above implies that
$$
\begin{align} \\
\dot{\varepsilon}_{ss} & =A\sigma^{n}\exp\left( \frac{Q_{a}}{RT} \right) \\
 \\
\Rightarrow\quad\log\dot{\varepsilon}_{ss}  & =n\log \sigma+C\\
 \\
\Rightarrow\quad\frac{\Delta\log \dot{\varepsilon}_{ss}}{\Delta \log\sigma} & =n
\end{align}
$$
so measuring $\Delta\log \dot{\varepsilon}_{ss}$ and $\Delta\log \sigma$ between points on two nearby strain-rate contours immediately gives $n$
