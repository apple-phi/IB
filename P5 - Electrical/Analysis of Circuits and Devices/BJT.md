A Bipolar-Junction Transistor (BJT) allows a small current to regulate a larger current. This contrasts with a FET (which allows a small *voltage* to regulate a large current).

## Small signal analysis
$$
\begin{align}
\mathrm{d} I_{c}  & = \mathrm{d} I_{c}(I_{B}, V_{\mathrm{CE}}) \\
 & = \underbrace{ \left. \frac{ \partial I_{C} }{ \partial I_{B} }  \right|_{V_{\mathrm{CE}}}}_{ h_{fe} }\delta I_{B} +\underbrace{ \left. \frac{ \partial I_{C} }{ \partial V_{\mathrm{CE}} }  \right|_{I_{B}} }_{ h_{oe} }\delta V_{\mathrm{CE}} \\
 \\
\Rightarrow\quad i_{c} & =h_{fe}i_{b}+h_{oe}v_{ce}
\end{align}
$$
![[BJT.png]]The reverse voltage transfer ratio, $h_{re}$ is usually negligible.

>Note that $h_{oe}$ is a value given as a *conductance*.

### Input resistance
Apply a test current $i_{b}$ into the Base with an open circuit output and measure the total resistance of $h_{ie}$ in parallel with any external resistors setting the operating point.

Measure the output voltage produced by the current source amplifier to find the overall gain.

### Output resistance
Short-circuit the input then solve for the resistance across the output terminals.

>In many cases, the short-circuit results in $v_{be}=i_{b}=i_{b}h_{fe}=0$



