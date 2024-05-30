## 1.
$$
\begin{align}
F[\mathrm{MT^{-2}}]&=\operatorname{f}(h_{1}[L],h_{2}[L],V_{1}[LT^{-1}],g[LT^{-2}],\rho[ML^{-3}])  \\
\frac{F}{\frac{1}{2}\rho V_{1}^{2}h_{1}}\left[ \cancel{\mathrm{\frac{MT^{-2}}{ML^{-3}(LT^{-1})^{2}L}} }\right]&= \operatorname{f}\left( \frac{h_{1}}{h_{2}}, \frac{h_{2}}{h_{2}}, \frac{V_{1}^{2}}{gh_{1}}\left[ \mathrm{\frac{(LT^{-1})^{2}}{LT^{-2}L}} \right], \frac{g}{g}, \frac{\rho}{\rho} \right) \\
\frac{F}{\frac{1}{2}\rho V_{1}^{2}h_{1}}&=\operatorname{f}\left( \frac{h_{1}}{h_{2}},\mathrm{Fr} \right)
\end{align}
$$
$V_{2}$ is dependent on $V_{1}$, $h_{1}$ and $h_{2}$ by continuity.
$$
\begin{align}
\mathrm{Fr}^{2}&=\frac{V_{1}^{2}}{gh_{1}} \\
&\propto \frac{\frac{1}{2}\rho V_{1}^{2}}{\rho gh_{1}} \\
&= \frac{1}{2}\mathrm{Fr}^{2}
\end{align}
$$
Consider $F\sim \frac{1}{2}\rho V_{1}^{2}+\rho gh_{1} \overset{\mathrm{Fr\to \infty}}{=} \frac{1}{2}\rho V_{1}^{2}$. Then $\underset{\mathrm{Fr}\to \infty}{F}=\operatorname{f}(\rho, V_{1})$ and is independent of $\mathrm{Fr}$.

At low $\mathrm{Fr}$, we have $\frac{1}{2}\rho V_{1}^{2}\ll \rho gh_{1}$ then
$$
\begin{align}
\frac{F}{\frac{1}{2}\rho V_{1}^{2}h_{1}}&=\frac{ \frac{1}{2}\rho V_{1}^{2}+\rho gh_{1}}{\frac{1}{2}\rho V_{1}^{2}h_{1}} \\
&\approx \frac{\rho gh_{1}}{\frac{1}{2}\rho V_{1}^{2}h_{1}} \\
&= \mathrm{Fr}^{-2}
\end{align}
$$
Considering the specific example, employing continuity we have $h_{1}V_{1}=h_{2}V_{2}$. The change of momentum is
$$
\begin{align}
\Delta p & =\rho h_{2}V_{2}^{2}-\rho h_{1}V_{1}^{2} \\
&=\rho \left( \frac{h_{1}^{2}V_{1}^{2}}{h_{2}}-h_{1}V_{1}^{2} \right)  \\
&=\rho h_{1}V_{1}^{2}\left( \frac{h_{1}}{h_{2}}-1 \right)
 \end{align}
$$
The net force forwards per unit width due to pressure is
$$
\begin{align}
\sum ph&= \int_{h_{2}}^{h_{1}}\rho gh \, \mathrm{d}h  \\
&= \left[ \frac{\rho gh^{2}}{2} \right]_{h_{2}}^{h_{1}} \\
&= \frac{\rho g}{2}\left(h_{1}^{2}-h_{2}^{2}  \right)  \\
 \end{align}
$$
Then the total net force on the sluice gate per unit width is
$$
\begin{align}
F&=\sum \phi- \Delta p \\
&=\frac{\rho g}{2}(h_{1}^{2}-h_{2}^{2})+\rho h_{1}V_{1}^{2}\left( 1-\frac{h_{1}}{h_{2}} \right)
 \end{align}
$$
Under variable fluid input, the above two terms are proportional to $\rho gh_{1}$ and $\frac{1}{2}\rho V_{1}^{2}$ respectively, hence the limiting cases under the previous assumption for $F$ still hold.

## 2.
From the given ratio, 
$$
w_{m}=\frac{w_{r}}{15}=\frac{4}{3}
$$
By dynamic similarity, the Froude number is the same for both model and reality, so
$$
\begin{aligned}
\mathrm{Fr}=\frac{V}{\sqrt{ gz }}\propto \frac{V_{m}}{\sqrt{ w_{m} }}&=\frac{V_{r}}{\sqrt{ w_{r} }}
\\
\\
\Rightarrow\quad \frac{V_{m}}{V_{r}}&=\sqrt{ \frac{w_{m}}{w_{r}} }\\
&=\frac{1}{\sqrt{ 15 }}
\\ \\
\Rightarrow\quad Q_{m}&=V_{m}A_{m}\\
&=\frac{V_{m}A_{m}}{V_{r}A_{r}} Q_{r}\\
&=\frac{1}{\sqrt{ 15 }}\cdot \frac{1}{15^{2}}\cdot125\\
&=\pu{ 0.143m^{3}s^{-1} }
 \end{aligned}
$$
Since the operating time is the ratio of control volume (which scales by $\frac{1}{15^{3}}$) and $Q$ (which scales as above),
$$
\begin{align}
t_{m}&=\frac{\frac{1}{15^{3}}}{\frac{1}{\sqrt{ 15}  } \frac{1}{15^{2}}}t_{r} \\
&=  \pu{ 6.20hours }
\end{align}
$$
## 3.
Under constant Froude number,
$$
\begin{align}
\mathrm{Fr}=\frac{V}{\sqrt{ gz }}\propto \frac{V_{m}}{\sqrt{ L_{m} }}&= \frac{V_{s}}{\sqrt{ L_{s} }} \\
V_{m}&=V_{s}\sqrt{ \frac{L_{m}}{L_{s}} } \\
 &=7\sqrt{ \frac{1}{20} } \\
&=\pu{ 1.565m/s }
\end{align}
$$
Given that $C_\text{total}'=\frac{D'}{\frac{1}{2}\rho {V'}^{2}L'^{2}}=0.001$
$$
C_\text{total}=\underbrace{ C_\text{wave}}_{ \propto \mathrm{Fr} }+\underbrace{ C_\text{form}}_{ \propto \mathrm{Re}^{-0.2} }
$$
### Supervision question:
We have two unknowns: the coefficients of wave and form drag on the model. I’m not sure how the cribs get their values for this.

Answer: didn’t read that the wave drag is half the total drag for the model.

## 4.
The top of the fountain is in equilibrium with the atmosphere. The streamlines are all at the same constant static pressure. 

Consider a central streamline, by Bernoulli we have
$$
\begin{align}
0&=\cancel{\Delta p}+\rho g\Delta h+\frac{1}{2}\rho\Delta \left(V^{2}\right) \\

 \end{align}
$$
The drop in total pressure is
$$
\begin{align}
-\Delta P&=-\rho g\Delta h-\int \frac{\mathrm{d} P_{f}}{\mathrm{d}x}  \, \mathrm{d}x  \\
&=-\rho g\Delta h+\frac{\rho V^{2}}{R}c_{f}L \\
&=-\rho g\Delta h\left( 1+\frac{2c_{f}L}{R} \right) \\
&= \pu{ 539550Pa }
 \end{align}
$$
The power required for this is
$$
\begin{align}
\dot{E}&=-A\Delta P\cdot V \\
&=-\pi R^{2}\Delta P \cdot \sqrt{ 2g\Delta h } \\
&= \pu{ 10493W }
 \end{align}
$$
With the new supply pipe, the pump outlet velocity is $V'=\frac{V}{4}$ by continuity so 
$$
\begin{align}
-\Delta P'
&=-\rho g\Delta h+\frac{\rho {V'}^{2}}{R'}c_{f}L \\
&=-\rho g\Delta h\left( 1+\frac{2c_{f}L}{16R'} \right) \\
&= \pu{ 64378Pa }
 \end{align}
$$
and the new pump power is
$$
\begin{align}
\dot{E}'&=-A'\Delta P'\cdot V' \\
&=-\pi {R'}^{2}\Delta P' \cdot \frac{\sqrt{ 2g\Delta h }}{4} \\
&= \pu{ 1251W }
 \end{align}
$$
>Note that also $\text{pump power}=Q\Delta P$

The mechanical energy loss in the pipe for given $Q=AV$ is
$$
\begin{align}
-\dot{W}_{x,\mathrm{out}}&=Q\Delta p_{f} \\
&\propto \frac{ QV^{2}}{R} \\
&\propto \frac{AV^{3}}{R} \\
&\propto \frac{d^{2}\left( \frac{1}{d^{2}} \right)^{3}}{d} \\
&\propto \frac{1}{d^{5}}
 \end{align}
$$
The exit loss at the nozzle is negligible because the well-defined water-air interface inhibits turbulent fluid mixing.

## 5.
$$
\begin{align}
\Delta p_\text{c}&=\frac{\rho}{2}\sum u^{2}K \\
&=\pu{ 2388.84Pa }
 \end{align}
$$
## 6.
Consider the pressure of the lower reservoir relative to the high reservoirs. The high reservoirs have equivalent central streamlines, hence by Bernoulli’s equation,
$$
\begin{align}
\rho g\Delta h_{2 / 1}+\overbrace{ \frac{1}{2}\rho V_{2}^{2}}^{ \text{exit loss} }+\overbrace{ \frac{\rho V_{2}^{2}f_{2}L_{2}}{2d_{2}}}^{ \text{pipe loss} } & =\rho g\Delta h_{3 / 1}+\frac{1}{2}\rho V_{3}^{2}+\frac{\rho V_{3}^{2}f_{3}L_{3}}{2d_{3}} \\
 \\
\Rightarrow\quad V_{2}^{2}&= \frac{\left( 1+f_{3} \frac{L_{3}}{d_{3}} \right)V_{3}^{2}-2g\Delta y_{2 / 3}}{1+f_{2} \frac{L_{2}}{d_{2}}}
 \end{align}
$$
Using the above, when $Q_{3}=A_{3}V_{3}=\pu{ 0.115m^{3}/s }$, we get that $V_{2}=\pu{ 1.647 m^{3}/s }$, so the total flow rate is
$$
Q_{1}=A_{2}V_{2}+Q_{3}=\pu{ 0.144 m^{3}/s }
$$
Consider the total inlet pump pressure relative to the datum,
$$
\Delta P_{p / 1}=-\frac{\rho V_{1}^{2}f_{1}L_{1}}{2d_{1}}=\pu{ 124503Pa }
$$
We know that
$$
\begin{align}
Q_{1}&=0.144 \\
Q_{2}&=0.0291 \\
Q_{3}&=0.155
\end{align}
$$
and using the Bernoulli equation from part (a)
$$
\Delta P_{2 / 1}=\pu{ 464646Pa }
$$
Then the power required to drive the total pressure increase across the pump is
$$
\begin{align}
Q_{1}\Delta P_{p}&=Q_{2}\Delta P_{2 / 1}+Q_{3}\Delta P_{3 / 1}-Q_{1}\Delta P_{p /1}  \\
&=Q_{1}(\Delta P_{2 /1}-\Delta P_{p / 1}) \\
&= \pu{ 84851W }
 \end{align}
$$
with $\Delta P_{p} = \pu{ 589249Pa }$

### Supervision question
These final two values are slightly wrong… why?

## 7.
By continuity, 
$$
\begin{align}
hV+3hV&=2hV_{b} \\
 
\Rightarrow\quad V_{b}&=2V
 \end{align}
$$
The mechanical power input per unit cross-section is
$$
\dot{E}_{i}=\frac{1}{2}(\rho dhV)V^{2}+\frac{1}{2}(3\rho dhV)(3V)^{2}=14\rho dhV^{3}
$$
The mechanical power output per unit cross-section is
$$
\dot{E}_{o}=\frac{1}{2}(4\rho dhV)(2V)^{2}=12\rho dhV^{3}
$$
So the net power loss is $2\rho dhV^{3}$

## 8.

## 9.
Outside the boundary layer the velocity profile is constant. Within the boundary layer, $\frac{\partial v_{x}}{\partial y}\ll \frac{\partial v_{x}}{\partial x}$ so the velocity profile at a given $x$ coordinate is almost constant. By Bernoulli’s principle, the static pressure is therefore approximately uniform. 

Consider a streamline that has height $h_{0}$ at the start of the boundary layer when $\delta=0$ and increases in height by $\Delta h$ downstream. Within the boundary layer we have
$$
v_{x}= \frac{V}{2}\left[ \frac{3y}{\delta}-\left( \frac{y}{\delta} \right) ^{3} \right] 
$$
By continuity,
$$
\begin{align}
\rho Vh_{0}&=\rho V(h-\delta)+\int_{0}^{\delta}\rho v_{x}  \, \mathrm{d}y  \\
&= \rho V(h-\delta)+\frac{5V\rho\delta}{8} \\
 \\
\Rightarrow\quad \Delta h&=\frac{3\delta}{8} \\
 \end{align}
$$
Drag force on the upper plate per unit width is
$$
\begin{align}
F&=\int _{0}^{x}\tau_{w} \, \mathrm{d}x  \\
&=\int _{0}^{x}\mu \frac{\partial v_{x}}{\partial y}  \, \mathrm{d}x =\int _{0}^{\delta}\rho v_{x}(V-v_{x}) \, \mathrm{d}y  \\
 \end{align}
$$
by force balance.
**tbc**

## 10.
At low $\mathrm{Re}$ the viscous forces dominate so the cylinder is lower drag due to a lower surface contact area.
**tbc**

## 11.
At low Reynold’s number,
$$
\mathrm{drag}\sim \tau A=\mu \frac{\partial v_{x}}{\partial y}A\approx \frac{\mu V}{L}A 
$$
The drag coefficient varies as
$$
\begin{align}
C_{D} & =\frac{\mathrm{drag}}{\frac{1}{2}\rho V^{2}A} \\
&\sim \frac{\frac{\mu V}{L}}{\rho V^{2}} \\
&=\frac{\mu}{\rho VL} \\
&= \frac{1}{\mathrm{Re}}
 \end{align}
$$
**tbc**

