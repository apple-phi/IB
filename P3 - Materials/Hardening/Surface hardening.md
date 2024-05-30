#materials 
## Motivation
In many contexts (e.g., machinery), it is insufficient to do bulk [[Steel heat treatment|steel heat treatment]] due to extremely high surface stresses. Therefore it is useful to do additional, case-hardening treatments that harden the surface without reducing the bulk strength or toughness.

## Carburising
This immerses steel in a carbon-rich atmosphere (e.g. molten cyanide salts) prior to heat treatment.

The carbon diffuses into the surface, increasing its [[Hardenability|hardenability]] (ability to form martensite) and the also the hardness of the martensite itself.

![[carburizing.png]]

This can be modelled by a linear interpolation with parameter $\mathrm{erf}\left( \frac{x}{2\sqrt{ Dt }} \right)$ from a fixed surface carbon concentration to the bulk carbon concentration, as derived [[Thermal conduction#Step response|here]]. This gives the highest carbon flux at the surface, as expected.
$$
C(x,t)=C_{s}+(C_{0}-C_{s})\,\mathrm{erf}\left( \frac{x}{2\sqrt{ Dt }} \right)
$$
```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\makeatletter
\pgfmathdeclarefunction{erf}{1}{%
  \begingroup
    \pgfmathparse{#1 > 0 ? 1 : -1}%
    \edef\sign{\pgfmathresult}%
    \pgfmathparse{abs(#1)}%
    \edef\x{\pgfmathresult}%
    \pgfmathparse{1/(1+0.3275911*\x)}%
    \edef\t{\pgfmathresult}%
    \pgfmathparse{%
      1 - (((((1.061405429*\t -1.453152027)*\t) + 1.421413741)*\t 
      -0.284496736)*\t + 0.254829592)*\t*exp(-(\x*\x))}%
    \edef\y{\pgfmathresult}%
    \pgfmathparse{(\sign)*\y}%
    \pgfmath@smuggleone\pgfmathresult%
  \endgroup
}
\makeatother
\begin{document}
\begin{tikzpicture}
\begin{axis}[
colormap/viridis,
xlabel=$x$,
ylabel=$t$,
zlabel=$T$,
view={50}{30},
]
\addplot3[
	surf,
	samples=17,
	domain=0:1,
	y domain=0.02:0.3,
	shader=faceted
]
{2-erf(x/(2*sqrt(y))};
\end{axis}
\end{tikzpicture}
\end{document}
```

We can use this solution to calculate the time required for a particular *case depth*, which can be measured using a benchmark minimum carbon concentration $C_{\mathrm{min}}$  at a fixed coordinate $x_{\mathrm{min}}$$$
C_{\mathrm{min}}=C_{s}+(C_{0}-C_{s})\,\mathrm{erf}\left( \frac{x}{2\sqrt{ Dt }} \right)
$$In this context, $C_{0}$ is the bulk carbon concentration and $C_{s}$ is the carbon concentration at the austenite upper solubility limit (at which there is the maximum amount of carbon in solid solution).
![[solubility-range.png|500]]
Hence after calculating the diffusion coefficient using the [[Rates of reaction|Arrhenius law]], the time required to achieve $C_{\mathrm{min}}$ at depth $x_{\mathrm{min}}$

>A similar technique is *nitriding*, which uses a nitrogen context (e.g. nitrate salts) instead of carbon.

## Transformation hardening
This imposes a localised heat source to the material surface to austenise it before quickly quenching the surface again to form a martensite case.

- The surface heating may come from a traversing flame, laser, electron gun, or high frequency induction coils to induce eddy currents
- Air cooling may be sufficient for martensite formation or water quenching may also be used