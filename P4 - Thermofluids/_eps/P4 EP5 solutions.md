## S1.
In order of $\text{breeze block}\to\mathrm{air}\to \mathrm{brick},$ the bulk thermal resistance are
$$
\begin{align}
R_{\theta}&=\frac{1}{k} \frac{l}{A} \\
&=\left[ 0.67^{-1}\frac{0.1}{A}, 0.026^{-1} \frac{0.05}{A},1.32^{-1} \frac{0.1}{A} \right]
\end{align}
$$
Also, the interfacial thermal resistances for the breeze block and brick respectively are
$$
\begin{align}
R_{\theta}&= \frac{1}{hA} \\
&=\frac{9.4^{-1}}{A}, \frac{15.2^{-1}}{A}
 \end{align}
$$
Hence the total thermal resistance is
$$
\begin{align}
\sum R_{\theta}&= \frac{1}{A}\left[ \frac{1}{6.7}+\frac{1}{20\cdot{0}.026} +\frac{1}{13.2}+\frac{1}{9.4}+\frac{1}{15.2}\right]  \\
&\approx\frac{2.3203}{A}
\end{align}
$$
noting that the trapped air is assumed to be not convective. 

Then the heat power loss density is
$$
\dot{q}= \frac{\Delta T}{2.3203}=\pu{ 8.62Wm^{-2} }
$$
The temperature on the outside brick surface is
$$
T_{b,o}=\frac{\dot{q}}{15.2}=\pu{0.567 \degree C}
$$
The temperature on the inside brick surface is
$$
\begin{align}
T_{b,i}&=\dot{q}\left( \frac{1}{15.2}+ \frac{1}{13.2} \right)  \\
&=\pu{1.22\degree C}
 \end{align}
$$
This demonstrates the low thermal resistance of the brick.

## 1.
The thermal resistance per unit length is is
$$
\begin{align}
R_{\theta}&= \frac{1}{2\pi}\left[ \frac{1}{r_{o}h_{o}}+ \frac{1}{\lambda_{o,s}}\ln \frac{r_{s}}{r_{o}}+ \frac{1}{\lambda_{s,i_{1}}}\ln \frac{r_{i_{1}}}{r_s}+\frac{1}{\lambda_{i_{1},i_{2}}}\ln \frac{r_{i_{2}}}{r_{i_{1}}}+\frac{1}{r_{w}h_{w}} \right]  \\
&=
 \end{align}
$$
where the following parameters apply:
$$
\begin{align}

\end{align}
$$

tbc : calc $R$ and finish the question

## 2.
Considering a single unit length of pipe,
$$
\begin{align}
R_{s}&= \frac{1}{hD\pi}=\frac{1}{10\cdot 0.01\pi}
 \end{align}
$$
So the heat loss per unit length is
$$
\dot{Q}=\frac{\Delta T}{R_{s}}=\frac{9}{2}\pi=\pu{14.14Wm^{-1}}
$$
Applying the insulation,
$$
R_{\theta}=\frac{1}{h(D+2t)\pi}+ \frac{1}{2\pi\lambda}\ln \left( \frac{D+2t}{D} \right)
$$
Let $u=D+2t,$ then to find the stationary minimum point in $R$ under constant $D,$
$$
\begin{align}
\frac{\mathrm{d} R_{\theta}}{\mathrm{d}u}=-\frac{1}{h\pi u^{2}}+ \frac{1}{2\pi\lambda u}&=0 \\
\Rightarrow\quad u&=\frac{2\lambda}{h} \\
\Rightarrow\quad t^{*}&=\frac{u-D}{2} \\
&= \pu{ 2.000mm }
 \end{align}
$$
The thickness required for a net reduction in heat transfer satisfies $R_{\theta}=R_{s}$ so
$$
\begin{align}
\frac{1}{hD\pi}&=\frac{1}{h(D+2t)\pi}+\frac{1}{\lambda}\ln \left( \frac{D+2t}{D} \right)  \\
\Rightarrow\quad t^{*}&=\pu{ 5.23mm }
\end{align}
$$
For a pipe of half the diameter, by applying the same analysis the critical thickness is
$$
t^{*}=\pu{ 30.82mm }
$$
Therefore small pipes are probably best off without lagging.

## 3.
The Biot number for a heat characteristic length $l=\frac{V}{A}$ in this spherical case is
$$
\mathrm{Bi}=\frac{hl}{\lambda}=\frac{hd}{6\lambda}=0.083
$$
which is small enough to say there are no thermal gradients in the sphere, justifying the lumped body assumption.

The governing equation is
$$
\rho cV\frac{\mathrm{d} T}{\mathrm{d}t} =-hA\Delta T_{b / \infty}
$$
So the time constant is
$$
\tau=\frac{\rho cV}{hA}=\pu{62.5s}
$$
The time constant is the time to reach $1-\frac{1}{e}$ of the way to equilibrium. Assuming the room temperature to be $\pu{ 25\!\degree C },$ the time to reach a general fraction $\frac{1}{n}$ of the original state is
$$
t_{1 / n }= \tau \ln n
$$
In this case, $\pu{ 85\!\degree C }$ is $\frac{12}{13}$ of the way to $\pu{ 95\!\degree C }$ from $\pu{ 25\!\degree C }$ so the time taken is
$$
t=\tau \ln 13=\pu{160s}
$$
For larger spheres the lumped body analysis is no longer valid. Assuming a unity Fourier number,
$$
\mathrm{Fo}=\frac{\tau}{\left( \frac{L^{2}}{\alpha} \right) }=1
$$
where $L=\frac{V}{A}$ as before and $\alpha=\frac{\lambda}{\rho c}.$ Therefore,
$$
\tau= \frac{L^{2}}{\alpha}=\pu{ 5208s }
$$
## 4.
Conserving energy,
$$
\begin{align}
(\dot{m}c_{p}\Delta T)_\text{oil}+(\dot{m}c_{p}\Delta T)_\text{water}=0
\end{align}
$$
and using $c_{p,\text{water}}=\pu{4.205kJ/kg/K}$ by interpolation,
$$
\Delta T_\text{water}=\pu{ 36.98\!\degree C }
$$
It will also be useful to calculate the heat transfer,
$$
\dot{Q}=\pu{118.2W}
$$

Heat exchanger effectiveness is defined by the ratio of actual heat exchange and optimum (counter-flow) heat exchange.
$$
\begin{align}
\varepsilon&= \frac{(\dot{m}c_{p}\Delta T)_{\mathrm{oil}}}{(\dot{m}c_{p})_{\mathrm{min}}\Delta T_{\text{hot in / cold in}}}
 \end{align}
$$
Here, oil is the minimum $\dot{m}c_{p}$ fluid so
$$
\varepsilon=67\%
$$
Per unit length, the net wall resistance assuming no internal wall temperature gradient is
$$
\begin{align}
R&= \frac{1}{2\pi r_{i}h_{i}}+\frac{1}{2\pi r_{o}h_{o}}=\frac{1}{2\pi r_{i}h_\text{net}}  \\
\Rightarrow\quad h_{\mathrm{net}}&=\pu{ 1264Wm^{-2}K^{-1} }
 \end{align}
$$
The logarithmic mean temperature difference is
$$
\begin{align}
\tau&= \frac{\Delta(\Delta T)}{\ln(r_{\Delta T})}
 \end{align}
$$
where $\Delta T_{2}=T_{h,o}-T_{c,i}$ and $\Delta T_{1}=T_{h,i}-T_{c,o}.$ Therefore its value is
$$
\tau=\pu{ 87.2\!\degree C }
$$
The length of tubing required is
$$
L= \frac{\dot{Q}}{2\pi r_{i}h_{net}\tau}=\pu{27.3m}
$$
## 5.
$$
\begin{align}
R&=\frac{1}{2\pi}\left[ \frac{1}{r_{i}h_{i}}+\frac{1}{\lambda}\ln \frac{r_{o}}{r_{i}}+\frac{1}{r_{o}h_{o}} \right] =\frac{1}{2\pi r_{i}U} \\
 \\
\Rightarrow\quad U&=\pu{5994Wm^{-2}K^{-1}}
 \end{align}
$$
Consider a small element of tube and apply heat balance,
$$
\dot{m}c_{p}\frac{\mathrm{d} T}{\mathrm{d}x}=-d\pi (T-T_{s}) 
$$
Then the solution will be a linear interpolation of $T_{in}\to T_{s}$ with parameter $\exp(-\lambda x)$ where the rate constant is
$$
\lambda=\frac{d\pi}{\dot{m}c_{p}}
$$
by inspection.

In the tube, water enters as a saturated liquid and leaves as dry saturated vapour, so the heat absorbed per unit mass is $h_{fg}.$ By energy balance along the tube,
$$
\begin{align}
\dot{m}_{s}h_{fg}&=\dot{m}\Delta T \\
\Rightarrow\quad \dot{m}_{s}&=\frac{\dot{m}\Delta T}{h_{fg}} \\
&=\pu{0.219kg/s}
 \end{align}
$$
Using the constants for $h_{fg}$ and $T_{s}$ at $\pu{ 80bar }.$

## 6.
The Reynold’s analogy gives
$$
\begin{align}
\mathrm{St}&=\frac{c_{f}}{2} \\
&=\frac{h}{\rho vc_{p}}
\end{align}
$$
where $c_{f}=\frac{\tau}{\frac{1}{2}\rho v^{2}}=0.01.$ Then the film temperature is
$$
T_{f}=\overline{T}=\frac{T_{w}+T_{\infty}}{2}=\pu{ 25\!\degree C }
$$
Interpolating the data-book,
$$
\begin{aligned}
\frac{RT}{p}&=v=0.844\\
\Rightarrow\rho&=1.185\\ \\
c_{p}&=1012.5 \\
\mathrm{Pr}&=0.715 \\
\mathrm{St}&=0.005 \\
\\
\Rightarrow\quad h&=\mathrm{St}\rho vc_{p}=\pu{ 60Wm^{-2}K^{-1} } \\
\Rightarrow\quad \dot{q}&=h\Delta T=\pu{ 2400Wm^{-2} }
 \end{aligned}
$$
If $\mathrm{Pr}\neq 1,$ then $\mathrm{St}=\frac{c_{f}}{2}\mathrm{Pr}^{-\frac{2}{3}}$ from the lecture notes. This corresponds to a 25% increase.

## 7
By dimensional analysis,
$$
\mathrm{
Nu=f(Re, Pr)
}
$$
tbc
## 8.
We expect different correlations for laminar and turbulent boundary layers. $\mathrm{Gr\sim Re}$ for natural convection (it is the max velocity in boundary layer), therefore we expect the state of the boundary layer to depend on $\mathrm{Gr}.$

tbc

## 9.

tbc

