## S1
Consider the resistor network per unit area,
$$
E_{b{1}}\overset{\frac{1}{\varepsilon}}\leftrightsquigarrow G_{1}\overset{-1}\leftrightsquigarrow G_{2}\overset{\frac{1}{\varepsilon}}\leftrightsquigarrow E_{b2}
$$
Then the net resistance is
$$
R= \frac{2}{\varepsilon}-1=99
$$
Hence the heat flux is
$$
\begin{align}
\dot{q}_{12}&=R^{-1}\Delta E_{b} \\
&= \left( \frac{2}{\varepsilon}-1 \right)^{-1}\sigma\Delta (T^{4})_{12} \\
&=\pu{ 6.865 Wm^{-2} }
 \end{align}
$$

Then, by potential divider,
$$
\begin{align}
G_{1}&=\sigma T_{1}^{4}-\frac{\dot{q}}{\varepsilon} \\
&=\pu{ 754Wm-2 } \\
G_{2}&=\sigma T_{2}^{4}+\frac{\dot{q}}{\varepsilon} \\
&=\pu{ 761Wm-2 }
 \end{align}
$$
Recalling that $\dot{q}=J-G,$
$$
\begin{align}
J_{1}&=\dot{q}+G_{1}=G_{2} \\
J_{2}&=\dot{q}-G_{2}=G_{1}
\end{align}
$$
If a radiation shield is introduced the resistor network becomes
$$
E_{b{1}}\overset{\frac{1}{\varepsilon}}\leftrightsquigarrow G_{1}\overset{-1}\leftrightsquigarrow G_{s}\overset{\frac{0.2}{\varepsilon}}\leftrightsquigarrow E_{s}\overset{\frac{0.2}{\varepsilon}}\leftrightsquigarrow G_{s}'\overset{-1}\leftrightsquigarrow G_{2}\overset{\frac{1}{\varepsilon}}\leftrightsquigarrow E_{b2}
$$
so the net resistance is
$$
R'= \frac{2.4}{\varepsilon}-2=118
$$
So the fraction reduction in heat transfer is
$$
\begin{align}
1- \frac{\dot{q}'}{\dot{q}}&=1-\frac{R}{R'} \\
&= 1-\frac{99}{118}\\
&= 16\%
 \end{align}
$$

>  **Supo question:** why don’t we just do the resistor network through $G$ like the above? I.e., the other way round from the lectures, with potential difference $(E_{b}-G_{1})$ and using $-f$ instead of $+f.$ It simplifies the algebra so much… If it doesn’t work in all cases, then which cases *does* it work? Hypothesis—works for all questions as long as you don’t have to use given values of $f$ (because the conversion is non-trivial).

## 1.
Conserving radiant flux in the $1\to \mathrm{e}$ direction, noting that for thermal equilibrium, $T_{1}=T_{e}$ and employing reciprocity relationship $A_{e}f_{e_{1}}=A_{1}f_{1e},$
$$
\begin{align}
&&E_{1}A_{1}f_{1e}&=E_{e}A_{e}f_{e{1}}\alpha \\
&\Rightarrow &E_{1}&=E_{e}\alpha \\
&\Rightarrow &\varepsilon\sigma T_{1}^{4}&=\sigma T_{e}^{4}\alpha \\
&\Rightarrow &\varepsilon&=\alpha
\end{align}
$$
## 2.
The resistor network is
$$

E_{b,e}^{\circ}\overset{\frac{1-\varepsilon}{A_{e}\varepsilon}}\leftrightsquigarrow J_{e} \begin{matrix}\overset{- \frac{1}{A_{e}f_{e,0}}}\leftrightsquigarrow  \\
\underset{ -\frac{1}{A_{e}f_{e,r}}-\frac{1}{A_{r}f_{r,0}}}\leftrightsquigarrow
 \end{matrix}\  E^{\circ}_{b,0}
$$
Hence the net resistance is
$$
R=\frac{1-\varepsilon}{A_{e}\varepsilon}+ \left[ A_{e}f_{e0}+\left( \frac{1}{A_{e}f_{er}}+\frac{1}{A_{r}f_{r0}} \right)^{-1}  \right] ^{-1}
$$
where the areas per unit length are
$$
\begin{align} 
A_{e}&=\pi D_{e}=\frac{3}{40}\pi=0.2356\\
A_{r}&=\frac{1}{2}\pi D_{r}=\frac{\pi}{4}=0.7854\\
\end{align}
$$
By symmetry of the heating element $e$,
$$
f_{er}=f_{e0}=\frac{1}{2}
$$
Conserving radiance from the reflector $r$,
$$
\begin{align}
f_{rr}+f_{re}+f_{r0}&=1 \\ \\
 f_{r0}&=1-f_{rr}-f_{re} \\
&=1-f_{rr}- \frac{A_{e}}{A_{r}}f_{er} \\
&=0.494
 \end{align}
$$
Then the net resistance is
$$
\begin{align}
R&=\frac{1}{A_{e}\varepsilon}+\frac{1}{A_{e}f_{e{0}}} \cdot \frac{1}{1+ \frac{1}{1+ \frac{A_{e}f_{e0}}{A_{r}f_{r0}}}} \\
&=\pu{ 5.856\Omega }
 \end{align}
$$
Then the heat flow is
$$
\dot{Q}_{e0}= \frac{\sigma\Delta(T^{4})_{e0}}{R}=\pu{ 23.6kWm-1 }
$$
Without the reflector, by taking a path through $G_{e}$ we see that
$$
\begin{align}
R'&=\frac{1-\varepsilon}{A_{e}\varepsilon}+\frac{1}{A_{e}f_{e0}}=5.30 \\
\dot{Q}'&=\pu{ 26.3kWm-1 }
 \end{align}
$$
This is an increase of 11%.
## 3.
The remaining view factor estimates would be too large by about 2%.

## 4.
With radiator $c,$ room $r,$ and environment $0,$
$$
\begin{align}
\dot{Q}_{r}&=2\sigma \Delta T^{4}_{cr}=\pu{558.6W} \\
\dot{Q}_{w}&=\underbrace{ 2\sigma\Delta T^{4}_{cw}}_{ \mathrm{incident} }=\underbrace{ \frac{2\Delta T_{0w}}{R}}_{ \mathrm{conducted }}+\underbrace{ 2h\Delta T_{wr}}_{ \mathrm{convected} } \\ \\
\sigma(T^{4}_{c}-T^{4}_{w})&=\frac{T_{w}-T_{0}}{R}+h(T_{w}-T_{r}) \\
T_{w}&=\pu{ 311K } \\
\dot{Q}_{w}&=\pu{333.5W}
 \end{align}
$$
With foil on the wall, there is no conductive heat transfer through it.
$$
\begin{align}
T'_{w}&=\pu{287.6K} \\
\end{align}
$$
Then the reduction in loss rate is
$$
\Delta \dot{Q}_{\mathrm{loss}}=\frac{2\Delta T}{R}=-\pu{117W}
$$
Hence the heat necessary for the room is less.

## 5.

We effectively have a resistor delta network. 

![[P4 EP6 Q5.png]]
Nodes 2 and 3 are insulated, so do not contribute current. Therefore
$$
\begin{align}
J_{2}&=\sigma T_{2}^{4} \\
J_{3}&=\sigma T_{3}^{4}
\end{align}
$$
![[P4 EP6 Q5 part 2.png]]
Conserving current around $J_{1}\to 2\to 3$ gives
$$
J_{1}=\pu{ 11058kWm-2 }
$$
Conserving the current generated in $E_{1}\to J_{1}$ gives
$$
\begin{align}
T_{1}&=\pu{ 6859K } \\
\dot{Q}_{1}&=\pu{5.96W}
 \end{align}
$$
## 6.
Assume the sun is a black body. Applying Stefan’s Law $E_{b}^{\circ}=\sigma T^{4}$ and combining the remaining power at the Earth’s radius with the intercepting Earth $\mathrm{CSA}$ gives $\pu{ 1.74E17W }$ intercepted. Our energy consumption for comparison is $\pu{1.5E15W}.$


## 7.
Both exhaust and the air are composed of $\sim 80\%\,\ce{N_{2}}$ so it is safe to assume they will have roughly the same properties.
$$
\begin{align}
\rho&=\frac{p}{RT}=\frac{\pu{1E5}}{287\times873}=\pu{ 0.4kgm-3 } \\
u&= \frac{\dot{m}}{\rho \pi r_{e}^{2}}=\pu{12.7ms-2} \\
\mathrm{Re}&=\frac{\rho ud_{t}}{\mu}=\frac{0.4\times12.7\times \pu{ 1.6E-3 }}{\pu{39E-6}}=209
\end{align}
$$
We are given that
$$
\begin{align}
\mathrm{Nu}_{d}&\triangleq \frac{hd_{t}}{\lambda}=0.9\mathrm{Re}_{d}^{0.4} \\
h&=\frac{0.9\lambda\mathrm{Re}_{d}^{0.4}}{d_{t}}= \frac{0.9\times 0.061 \times 209^{0.4}}{\pu{ 1.6E-3 }}=\pu{291Wm-2K-1}
 \end{align}
$$

Assuming all surface are black, then the convection to the thermocouple balances the radiation emitted from the thermocouple. Per unit area,

$$
\begin{align}
h\Delta T_{e / t}&=\sigma \Delta (T^{4})_{t / w} \\
\Rightarrow\quad 291\times(873-T_{t})&=\sigma(T^{4}_{t}-T_{w}^{4})
 \end{align}
$$
With $T_{w}=\pu{ 298K },$ we find that $T_{t}=\pu{ 796K}$ while when $T_{w}=\pu{773K}$ we find that $T_{t}=\pu{844K}.$ Since the actual exhaust temperature is $T_{e}=\pu{873K}$ this is a noticeable error.

At “only” a $\pu{5\!\degree C}$ error at $T_{w}=\pu{298K}$, we require $T_{t}=T_{e}-5=\pu{868K}$ so
$$
h'= \frac{\sigma(868^{4}-298^{4})}{5}=\pu{6348Wm-2K-1}
$$
From the $\mathrm{Re}\mapsto \mathrm{Nu}$ relationship we are given we know that
$$
\begin{align}
h&\propto d_{t}^{-0.6} \\
\Rightarrow\quad \frac{h}{h'}&=\left( \frac{d'_{t}}{d_{t}} \right)^{0.6}
 \end{align}
$$
Hence the required diameter is
$$
d'_{t}=d_{t}\log_{0.6} \frac{h}{h'}=\pu{9.66mm}
$$

> **Supo question:** this is very different answer from the cribs…! **Answer:** basic algebra mistake, there shouldn’t be any logarithms in the solution!

$$
\mathrm{Bi}=\frac{hl_{c}}{\lambda_{t}}
$$
where the characteristic length is given as
$$
l_{c}= \frac{V}{A}= \frac{\pi r^{2}L}{2\pi rL}=\frac{r}{2}=\frac{d}{4}
$$
For $d_{t}=\pu{1.6mm},$ $\mathrm{Bi}=0.0073$ so a lumped heat capacity analysis is valid. The time constant is
$$
\tau_{c}=\frac{\rho_{t}c_{t}l_{c}}{h}=\pu{5.5s}
$$

For $d_{t}'=\pu{0.01mm},$ $\mathrm{Bi}=0.001$ so the lumped heat capacity analysis $s$ even more valid! The new time constant for this case is $\tau_{c}'=\pu{1.6ms}$