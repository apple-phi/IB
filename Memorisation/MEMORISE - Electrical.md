## Electronics

## GBP
First-order circuits conserve their gain-bandwidth product (GBP).

For voltage amplifiers, feedback by transfer function $B$ increases input impedance by factor $1+AB$ and decreases output impedance by factor $1+AB.$

Power amplification
$$
\eta^{*}= \frac{P_{AC}}{P_{DC}}
$$
where the $\mathrm{DC}$ power out is considered to be the supply voltage $\times$ the average current (even though this has no physical meaning…).

### Miller transformation
An impedance $Z$ connected over an inverting amplifier $v_{0}=-Av_{i}$ can be transformed to two impedances:
- From the input to the ground of $\frac{Z}{1+A}$
- From the output to the ground of $\frac{Z}{1+A^{-1}}$


## 3-phase systems

Infinite bus—fixed frequency and voltage, even if a single generator fails.

### Star and delta connections
| Phase quantity | Star $\star$                   | Delta $\Delta$                  |
| -------------- | ------------------------------ | ------------------------------- |
| Voltage        | $V_{\mathrm{line}} /\sqrt{3 }$ | $V_{\mathrm{line}}$             |
| Current        | $I_{\mathrm{line}}$            | $I_{\mathrm{line}} /\sqrt{ 3 }$ |
$$
\begin{align}
P & =\sqrt{ 3 }V_{\ell}I_{\ell}\cos \varphi &=&3V_{p}I_{p}\cos\varphi\\
Q & =\sqrt{ 3 }V_{\ell}I_{\ell}\sin \varphi&=&3V_{p}I_{p}\sin \varphi \\
\mathbf{S} & =\sqrt{ 3 }V_{\ell}I_{\ell}^{*}&=&3V_{p}I_{p}^{*}
\end{align}
$$
### Fault analysis
We need to determine fault current levels to specify breaker $\mathrm{VA}$ ratings
$$
\text{VA rating}=\sqrt{ 3 }\left( VI \right)_\text{nominal} 
$$

### Synchronous machine
$$
\overline{ E}=\overline{ V}+j\overline{ I}X_{s}
$$

## Waves
Skin depth
$$
\delta=\frac{1}{\alpha}
$$

Characteristic impedance
$$
\eta=\left| \frac{\mathbf{E}}{\mathbf{H}} \right| =\sqrt{ \frac{\mu}{\varepsilon} }
$$
Poynting vector
$$
\mathbf{N}=\mathbf{E}\times \mathbf{H}
$$
Time-averaged power per unit area
$$
|\overline{ \mathbf{N}}|=\frac{1}{2}\mathbf{E}\times \mathbf{H}^{*}
$$
At interfaces:
- the normal components of $\mathbf{D}$ and $\mathbf{B}$ are conserved
- the tangential components of $\mathbf{E}$ and $\mathbf{H}$ are conserved

Choosing the orientation of the system so the electric field is perpendicular to the incident plane,
$$
\begin{align}
E_{t}&=E_{i}+E_{r} \\
H_{t}\cos\theta_{2}&=H_{i}\cos\theta_{1}-H_{r}\cos\theta_{1}
\end{align}
$$
so using $\eta=\frac{E}{H},$ we get relationships for $(E_{t})_{\perp}$ and $(E_{r})_{\perp}$ in terms of the values of $\eta$ and $\cos\theta.$ We can use a similar approach with the system oriented so instead the magnetic field is perpendicular to the incident plane to get relationships for $(E_{t})_{\parallel}$ and $(E_{r})_{\parallel}.$

Brewster angle $\theta_B$ for full plane polarisation
$$
(E_{r})_{\parallel}=0
$$
Snell’s Law
$$
n_{1}\sin\theta_{1}=n_{2}\sin\theta_{2}
$$
Quarter wave matching
$$
\frac{\eta}{\eta_{1}}=\frac{\eta_{1}}{\eta_{2}}
$$
## Transmission lines (DB)
Wave speed
$$
c= \frac{1}{\sqrt{ \varepsilon \mu }}=\frac{1}{\sqrt{ LC }}
$$
Characteristic impedance
$$
\begin{align}
Z_{0}&=\mathfrak{g}\sqrt{ \frac{\mu}{\varepsilon} } \\
&=\frac{\overline{ V}_{F}}{\overline{I}_{F}}=-\frac{\overline{V}_{B}}{\overline{I}_{B}}=\frac{\beta}{\omega C} \\
&=\sqrt{ \frac{L}{C} }=\sqrt{ \frac{R+j\omega L}{G+j\omega C} }
 \end{align}
$$

>$Z_{0}$ does not dissipate power for non-lossy lines (unless $R,G\neq 0$). It is the apparent impedance looking down an infinite line.

Propagation constant
$$
\gamma=\alpha+j\beta=\sqrt{ (R+j\omega L)(G+j\omega C) }
$$
where $\alpha$ is the attenuation constant and $\beta=\frac{2\pi}{\lambda}$ is the phase constant.
### Reflection
Voltage reflection coefficient
$$
\rho= \frac{Z_{l}-Z_{0}}{Z_{l}+Z_{0}}\leq1
$$
Standing wave by superposition
$$
V=\overline{ V}_{F}(e^{ -j\beta x}+\rho e^{ j\beta x })e^{ j\omega t }
$$
Voltage standing wave ratio ($\infty$ for perfect standing waves)
$$
\mathrm{VSWR}= \frac{1+|\rho|}{1-|\rho|}\geq1
$$
Input impedance of a line of length $L$ connected before a load $Z_{L}.$
$$
\boxed{ \frac{Z_{\mathrm{in}}}{Z_{0}}=\frac{Z_{L}+jZ_{0}\tan \beta L}{Z_{0}+jZ_{L}\tan \beta L}}
$$
When $L=\frac{\lambda}{4}\iff\beta=\frac{\pi}{2},$ this becomes $\frac{Z_{\mathrm{in}}}{Z_{0}}=\frac{Z_{0}}{Z_{L}},$ hence by appropriately choosing a line to satisfy this $Z_{0},$ we can create matched impedances on *both* ends!

| Configuration | $Z_{L}$    | $\frac{Z_{\mathrm{in}}}{Z_{0}}$ | $\rho$ | $\Delta\theta$ |
| ------------- | ---------- | ------------------------------- | ------ | -------------- |
| Open          | $$\infty$$ | $$\frac{1}{j\tan \beta L}$$     | $$+1$$ | $$0$$          |
| Closed        | $$0$$      | $$j\tan \beta L$$               | $$-1$$ | $$\pi$$        |
| Matched       | $$Z_{0}$$  | $$1$$                           | $$0$$  | $$0$$          |

Fraction of reflected power
$$
r=\rho^{2}
$$
### Telegrapher’s equations
$$
\begin{align}
\partial_{x}V&=-L\partial_{t}I \\
\partial_{x}I&=-C\partial_{t}V
\end{align}
$$
Co-substituting and differentiating leads to a wave equation with wave speed $c=\frac{1}{\sqrt{ LC }},$
$$
\begin{align}
\partial^{2}_{x}  \begin{bmatrix}
V \\
I
\end{bmatrix}&= LC \partial^{2}_{t}\begin{bmatrix}
V \\
I
\end{bmatrix}
 \end{align}
$$
General solution
$$
\begin{bmatrix}
V \\
I
\end{bmatrix}=\begin{bmatrix}
\overline{ V} \\
\overline{ I}
\end{bmatrix}_{F}e^{ j(\omega t-\beta x) }+\begin{bmatrix}
\overline{ V} \\
\overline{ I}
\end{bmatrix}_{ B}e^{ j(\omega t+\beta x) }
$$
where $\overline{ V}_{F}, \overline{ I}_{F}, \overline{ V}_{B}, \overline{ I}_{B}$ are all complex-valued.

### Coaxial cables
$$
\begin{align}
C&=\frac{2\pi\varepsilon}{\ln\left( \frac{b}{a} \right)} \\
L&= \frac{\mu}{2\pi}\ln\left( \frac{b}{a} \right)
\end{align}
$$

## Scribbles

Is this valid? For sinusoidal $V_{F}$ and $I_{F},$ using Telegraphers’ equations,
$$
\begin{align}
\frac{\partial }{\partial x} \begin{bmatrix}
V_{F} \\
I_{F}
\end{bmatrix}&\propto\begin{bmatrix}
L\cdot I_{F} \\
C\cdot V_{F}
\end{bmatrix} \\ \\
\Rightarrow\quad Z_{0}&=\frac{\mathrm{d} V_{F}}{\mathrm{d}I_{F}}=\frac{\frac{\partial V_{F}}{\partial x} }{\frac{\partial I_{F}}{\partial x} } = \frac{L}{C}\overbrace{  \frac{V_{F}}{I_{F}}}^{ Z_{0} } \\
&=\sqrt{ \frac{L}{C} }
\end{align}
$$
>No it’s not valid (I think it can be adjusted to be valid though).

Use the $\beta$ method instead.

