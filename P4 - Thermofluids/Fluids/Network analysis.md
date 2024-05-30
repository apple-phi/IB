The *stagnation* pressure is the sum of *static* and *dynamic* pressures. The *total* pressure is the combination of *stagnation* pressure with gravitational effects.
$$
\text{total pressure}=\underbrace{ p }_{ \text{static} }+\underbrace{ \frac{1}{2}\rho V^{2} }_{ \text{dynamic} }+\rho gh
$$
It is often useful to refer to pressures in terms of their *heads*—the height difference due to pressure variation.
$$
\begin{align}
\text{total head}&=\frac{\text{total pressure}}{\rho g} \\
&= \frac{p+\frac{1}{2}\rho V^{2}+\rho gh}{\rho g}
\end{align}
$$
>Note: the nomenclature of these terms is *not* unified within the scientific community…

## Loss of total pressure along a pipe
Consider the following uphill flow through constant cross-section:

![[pipe-height-gradient.png|400]]
The pressure drop due to friction coefficient is
$$
\frac{\mathrm{d}P}{\mathrm{d}x}=-\frac{\rho V^{2}}{R}c_{f}
$$
which, in terms of pipe diameter $D$ is
$$
\frac{\mathrm{d}P}{\mathrm{d}x}=-\frac{4c_{f}}{D}\cdot \frac{\rho V^{2}}{2}
$$
>It is common to define a constant $f=4c_{f}$

With constant $D$, $V$ and $\mathrm{Re}$,
$$
\begin{align}
\frac{\Delta P}{L} & =\Delta p+\rho g\Delta h \\
 & =-\frac{\mathrm{d}P}{\mathrm{d}x}
\end{align}
$$
Knowing the bulk velocity is constant:
>tbc

$$
\frac{ d^{2}x }{ dy^{2} }
$$

## Loss of total pressure at pipe discharge

Assume the outlet flow is fast enough that it is uniform, hence there is no streamline curvature so no pressure gradient.
![[flow-outlet.png|300]]
Combining continuity and the SFME gives
$$
\Delta p=\rho V_{2}^{2}\left[ \left( \frac{A_{2}}{A_{3}} \right)^{2}-\frac{A_{2}}{A_{3}}   \right] 
$$
Assuming the changes in $\rho gh$ are negligible, the drop in total pressure becomes
$$
\Delta p_{T,2\to3}=\Delta p_{2\to 3}+\frac{1}{2}\rho V_{2}^{2}\left[ 1- \left( \frac{V_{3}}{V_{2}} \right)^{2}  \right]
$$
Substituting, we have:
$$
\begin{align}
\Delta p_{T,2\to3} & = \frac{1}{2}\rho V_{2}^{2}\left( 1- \frac{A_{2}}{A_{3}} \right)^{2} \\
 & =\frac{1}{2}\rho V_{2}^{2}K
\end{align}
$$
where $K$ is the loss coefficient of the sudden expansion. 
![[loss-coeff.png|400]]
## Loss of total pressure across an orifice plate
![[orifice-plate.png]]
Since the streamlines are *locally* straight between sections 2 and 3, the Bernoulli principle can be applied along these central streamlines.
$$
\begin{align}
\Delta p_{1\to 2} & = \frac{1}{2}\rho V_{1}^{2}\left[ \left( \frac{V_{2}}{V_{1}} \right)^{2}-1 \right] \\
 & = \frac{1}{2}\rho V_{1}^{2}\left[ \left( \frac{A_{1}}{A_{2}} \right)^{2}-1 \right]
\end{align}
$$
The total static pressure change between sections 1 and 3 is
$$
\begin{align}
\Delta p_{1\to 3} & =\Delta p_{1\to 2}+\Delta p_{2\to 3} \\
& = \frac{1}{2}\rho V_{1}^{2}\left( \frac{A_{1}}{A_{2}}-1 \right)^{2} \\
 & =\frac{1}{2}\rho V_{1}^{2}K
\end{align}
$$
Since there is no height variation and $V_{1}=V_{3}$, this is also the change in total pressure.

>Note: less obvious, but if the the height variation was not negligible, the same result still applies!

Applying dimensional analysis to this gives
$$
K=f\left( \underbrace{ \frac{\rho VD}{\mu} }_{ \mathrm{Re} }, \frac{d}{D} \right) 
$$
At very large $\mathrm{Re}>\pu{ E6 }$, the problem becomes *independent* of $\mathrm{Re}$ and $K$ is a function of geometry only.
![[orifice-K.png|300]]
## Changes in total pressure across network components
In general, dimensional analysis shows that the total pressure loss is always of the form
$$
\Delta p_{T}= \frac{1}{2}\rho V_{1}^{2}K
$$
which loses the Reynolds dependence at high $\mathrm{Re}$.

## Mechanical work, pumps and turbines
Because $\Delta p_{T}$ corresponds to a per-volume energy loss,
$$
-\dot{W}_{x,\mathrm{out}}=\frac{\dot{m}\Delta p_{T}}{\rho}+\text{irrev. losses}
$$
### Example

![[network-anal-ex.png]]
Start by writing then changes in total pressure throughout the system:
![[network-anal-orifice-ex-soln.png]]
By mass conservation of an incompressible flow, the volumetric flow rate is
$$
\begin{align}
Q & =\int v_{x} \, dA \\

 & = \frac{\pi d_{A}^{2}}{4} =\frac{\pi d_{B}^{2}}{4}
\end{align}
$$
The total pressure is
$$
p_{T,7}=p_{T,0}+\sum_{i} \Delta p_{T, i}
$$
![[network-anal-ex-solution.png]]
>So the significance of $d$ far outweighs $c_{f}$

