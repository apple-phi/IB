#materials
## Summary
- There is an interfacial energetic cost between phases, which can be expressed as a surface energy
- Considering this surface energy in the context of free energy, for a crystal to be stable and grow it must first reach a certain size through random fluctuations
- Homogenous nucleation is difficult to stabilise due to a large critical radius
- Heterogeneous nucleation has the same radius but a low contact angle with a lower stable crystal volume
## Homogenous nucleation
A [[Spontaneous reactions|spontaneously forming]] nucleus within a phase initially develops spherically. The formation [[Spontaneous reactions|reaction feasibility]] depends on the trade-off between the bulk free energy and the surface energy.

Consider a spherical nucleus with bulk free energy per unit volume $\Delta G_v<$ 0 and interfacial surface energy $\gamma>0$,$$G(r)=\underbrace{V(r)}_{\frac{4}{3}\pi r^3}\Delta G_{v}+\underbrace{A(r)}_{4\pi r^2}\gamma$$Then the feasibility of formation requires $\mathrm dG\leq0$. To find the critical spontaneous radius:$$\begin{align*}
\frac{\mathrm{d}G}{\mathrm{d}r}=0&=4\pi r^{2}\Delta G_{v}+8\pi r \gamma\\
&= \Delta G_{v}r+2\gamma\\
\\
\Rightarrow\quad r^{*}&= \frac{2\gamma}{-\Delta G_v}
\end{align*}$$![[homogenous-nucleation.png]]
### Undercooling for nucleation
$\Delta G_{v}$ increases with temperature with $\Delta G_{v}(T_{f})=0$ where $T_{f}$ is freezing temperature, so for a feasible reaction $T<T_{f}$. Let’s find out exactly how much undercooling is required.

A common assumption is that $\Delta H$ and $\Delta S$ are invariant of temperature[^1]. Thus, we can compare $\Delta G_{v}(T)$ to $\Delta G_{v}(T_{f})$,$$\begin{align*}
\Delta G_{v}(T_{f})&=\Delta H_{v}-T_{f}\Delta S_v=0\\
\Rightarrow\quad\Delta S_{v}&= \frac{\Delta H_{v}}{T_{f}}\\
\\
\Delta G_{v}(T)&=\Delta H_{v}-T\Delta S_v\\
&= \Delta H_{v}\left(1-\frac{T}{T_{f}}\right)\\
\\
\Rightarrow\quad r^{*}= \frac{2\gamma}{-\Delta G_v}&= \frac{2\gamma}{-\Delta H_v}\cdot\frac{T_f}{T_{f}-T}
\end{align*}$$Hence, the greater the undercooling $(T_{f}-T)$, the smaller the random fluctuation producing the nucleus needs to be.![[homogenous-undercooling.png]]
### So… is it feasible?
Let’s take the example of ice forming in water. $T_{f}=\pu{273 K }$,$\gamma\approx\pu{0.025 J/m2}$ and $\Delta H_v\approx\pu{333000 J/kg}$. Let’s suppose the maximum undercooling is $\pu{ 10K }$. This gives $r^{*}\approx\pu{4E-6 m}$. Given that water molecules are sized on the order of nano-meters, there must be another mechanism at work for ice to nucleate upon cooling water.

## Heterogeneous nucleation
In reality, large amounts of undercooling is unnecessary for nucleation because defects/impurities in the phase act as nucleation sites which are more energetically favourable.

Consider a solid spherical cap $S$ nucleating on a planar catalyst $C$ within a liquid phase $L$ with bulk free energy per unit volume $\Delta G_v<$ 0 and interfacial surface energies $\gamma_\text{SL},\gamma_\text{CS}, \gamma_\text{CL}>0$. These surface energies are measured in $\pu{J/m^2}=\pu{N/m}$ so exert a force per unit length and we can apply a force balance at their intersection:![[heterogenous-nucleation-geo.png]]$$\gamma_{CL}=\gamma_{CS}+\gamma_{SL}\cos\theta$$Assuming constant surface energies, the cap angle remains constant also, so has a fixed shape. The system free energy is given by$$G(r)=V_{S}(r)\Delta G_{v}+A_{SL}(r)\gamma_{SL}+A_{CS}(r)(\gamma_{CS}-\gamma_{CL})$$Skipping the derivation, the key result is that this has the same critical cap radius as before,$$r^{*}= \frac{2\gamma}{-\Delta G_v}= \frac{2\gamma}{-\Delta H_v}\cdot\frac{T_f}{T_{f}-T}$$However, at the same radius as the homogenous case, with a low contact angle, much fewer atoms are required in the fluctuation producing the nucleus for it to be stable and grow.

[^1]: This isn’t strictly true and can be a dangerous assumption to make, but in this case the contributions of their variation cancel out. Consider the following, under isobaric conditions:$$\begin{align*}
\mathrm{d}G&=\mathrm{d}(U+pV-TS)\\
&=\cancel{\mathrm{d}U+p\mathrm{d}V-T\mathrm{d}S}+V\cancelto{0}{\mathrm{d}p}-S\mathrm{d}T\\
\\
\Rightarrow\quad \frac{\partial G}{\partial T}&=-S
\end{align*}$$So now if we perform a [[Series expansions#The Taylor Series|Taylor Series]] expansion of $\Delta G_v$ around the freezing temperature, $T_{f}$, we get:$$\begin{align*}
\Delta G_v(T_{f}+t)&=\left.\mathrm{e}^{t\cdot\mathop{}\partial_{T}}\Delta G_v\right|_{T=T_{f}}\\
&= \left.(1+t\cdot\partial_{T}+\ldots)\Delta G_v\right|_{T=T_{f}}\\
&= \cancelto{0}{\Delta G_v(T_{f})}+ t\frac{\partial \Delta G_v}{\partial T}+\ldots\\
\\
\Rightarrow\quad \Delta G_v(T)=\Delta H_v-T \Delta S_v&\approx-\Delta S_v(T-T_{f})\\
\Delta H_v&\approx T_{f}\Delta S_v
\end{align*}$$as required.
