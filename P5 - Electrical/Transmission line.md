Transmission lines consist of at least two conductors:
- an out path
- a return path
separated by a dielectric insulator. There will be some associated capacitance between the two conductors if separated by a gap.

Consider a small length $\delta x$ of a transmission line with impedances $C\delta x$ and $L\delta x.$ Then the equivalent circuit is
![[transmission-line-equiv-circ.png]]

## Telegrapher’s equations
The voltage drop across the inductor comes from its characteristic equation that $\dot{\phi}=-L\dot{I},$
$$
\partial_{x}V=-L\partial_{t}I
$$
The current drop across the capacitor comes from its characteristic equation that $\dot{Q}=-C\dot{V},$
$$
\partial_{x}I=-C\partial_{t}V
$$
In these equations, $L$ and $C$ are taken per unit length.

By differentiating these equations with respect to $x$ and co-substituting, 
$$
\begin{align}
\frac{ \partial^{2}  }{ {\partial x}^{2} }  \begin{bmatrix}
V \\
I
\end{bmatrix}&= LC \frac{ \partial^{2}  }{ {\partial t}^{2} }\begin{bmatrix}
V \\
I
\end{bmatrix}
 \end{align}
$$
This fits the form of a wave equation with wave speed $c=\frac{1}{\sqrt{ LC }}.$

This has the general solution of
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
given in terms of the complex phase and amplitude of the forwards and backwards waves ($\overline{ V}$ and $\overline{ I}$.

## Wave speed
Consider a coaxial cable with and inner conductor inner radius $a$ and outer conductor radius $b.$ The intermediate dielectric has absolute permittivity $\varepsilon_{d}$ and absolute permeability $\mu_{d}.$

Its capacitances and inductances per unit length are
$$
\begin{align}
C&=\frac{2\pi\varepsilon_{d}}{\ln\left( \frac{b}{a} \right)} \\
L&= \frac{\mu_{d}}{2\pi}\ln\left( \frac{b}{a} \right)
\end{align}
$$
From the telegrapher’s equations, the wave speed along the transmission line is
$$
c= \frac{1}{\sqrt{ \varepsilon_{d}\mu_{d} }}
$$
which is only a function of the dielectric properties.

>*This expression for $c$ holds in general!*

If the dielectric is a vacuum (or close enough, like air), then $\varepsilon_{d}, \mu_{d}=\varepsilon_{0},\mu_{0},$ then $c_{0}= \frac{1}{\sqrt{ \varepsilon_{0}\mu_{0} }}$ and the wave travels at the speed of light.

## Wavelength
We consider the current to behave like an incompressible fluid. However, this assumption relies on the wavelength to be long relative to the system length.

In high frequency or long transmission lines, this assumption breaks down.

## Lossy transmission lines
Assume the conductors are imperfect and have an internal resistance $R\delta x$ and the dielectric is an imperfect insulator with conductance $G\delta x.$

![[lossy-transmission-lines.png]]

It is useful to define the propagation constant $\gamma,$
$$
\gamma=\sqrt{ (R+j\omega L)(G+j\omega L) }
$$
The general solution to the Telegrapher’s equations becomes
$$
\begin{bmatrix}
V \\
I
\end{bmatrix}=\begin{bmatrix}
\overline{ V} \\
\overline{ I}
\end{bmatrix}_{F}e^{ j(\omega t-\beta x) }e^{ -\alpha x }+\begin{bmatrix}
\overline{ V} \\
\overline{ I}
\end{bmatrix}_{ B}e^{ j(\omega t+\beta x) }e^{ \alpha x }
$$
where $\alpha$ is the attenuation constant.

## Characteristic impedance
Substituting the non-lossy solution into the capacitive Telegrapher’s equation $\partial_{x}I=-C\partial_{t}V,$ we obtain the following after cancellation:
$$
\beta(-\overline{ I}_{F}e^{ -j\beta x }+\overline{ I}_{B}e^{ j\beta x })=-\omega C(\overline{ V}_{F}e^{ -j\beta x }+\overline{ V}_{B}e^{ j\beta x })
$$
Comparing the coefficients of $e^{ -j\beta x }$ and $e^{ j\beta x },$ we get a constant that we will term the characteristic impedance.
$$
Z_{0}\overset{\mathrm{def}}=\frac{\overline{ V}_{F}}{\overline{I}_{F}}=-\frac{\overline{V}_{B}}{\overline{I}_{B}}=\frac{\beta}{\omega C}
$$
However $\beta=\frac{2\pi}{\lambda}$ and $\omega=2\pi f$
$$
\begin{align}\frac
{\omega}{\beta}&=c=\sqrt{ LC } \\
\Rightarrow\quad Z_{0}&=\sqrt{ \frac{L}{C} }
 \end{align}
$$
This is the ratio of voltage and current of a unidirectional wave at any point on a transmission line. For ideal, lossless transmission lines, $Z_{0}$ is always a real number. 

>Although $Z_{0}$ has units of $\Omega,$ it does not dissipate power and $V$ and $I$ are not between the same point. It is the apparent impedance that is seen if you are looking into an infinitely long line at $x=0,$ i.e., $\frac{V(0,t)}{I(0,t)}$

Substitution of $L$ and $C$ for the actual transmission line parameters results in
$$
Z_{0}=\mathfrak{g}\sqrt{ \frac{\mu}{\varepsilon} }
$$
where $\mathfrak{g}$ is a factor arising due to the line geometry.

If the line is lossy then the characteristic impedance gains a frequency dependence as
$$
Z_{0}=\sqrt{ \frac{R+j\omega L}{G+j\omega C} }
$$
## Maximising power transfer
To maximise signal power, we need the load impedance to match the cable impedance,
$$
Z_{l}=Z_{0}
$$
>This is why we standardise coaxial cables and $\mathrm{BNC}$ inputs / outputs in our devices to be either $\pu{ 50\Omega }$ or $\pu{ 75\Omega }.$

## Signal reflection

Suppose there is a load at $x=0$ (which may cause a reflection of the wave) and consider the (attenuated) solutions to the Telegraphers equations here at $x=0$,
$$
\begin{align}
\begin{bmatrix}
V \\
I
\end{bmatrix}&=\begin{bmatrix}
\overline{ V} _{F}+\overline{ V} _{B}\\
\overline{ I}_{F}+\overline{ I}_{B}
\end{bmatrix}e^{ j\omega t } \\
 \\
\Rightarrow\quad Z_{L}&= \frac{\overline{ V} _{F}+\overline{ V} _{B}}{\overline{ I}_{F}+\overline{ I}_{B}} \\
&=  \frac{\overline{ V} _{F}+\overline{ V} _{B}}{ \\
\overline{ V} _{F}-\overline{ V} _{B}} Z_{0} \\
 \\
\Rightarrow\quad \overline{ V} _{B}&=\frac{Z_{L}-Z_{0}}{Z_{L}+Z_{0}}\overline{ V} _{F}
 \end{align}
$$
So we define the voltage reflection coefficient $\rho_{0}$ of this load as
$$
\rho_{L}=\frac{Z_{L}-Z_{0}}{Z_{L}+Z_{0}}
$$
Therefore a proportion $\rho_{L}$ of the forward voltage wave $V_{F}$ is reflected to give a backwards wave which superposes to give a standing wave.
$$
V(x,t)=\overline{ V}_{F}(e^{ -j\beta x }+\rho_{L}e^{ j\beta x })e^{ j\omega t }
$$
![[voltage-standing-wave.png|600]]
We define the voltage standing wave ratio (VSWR) as the ratio of maximum and minimum voltage amplitude,
$$
\mathrm{VSWR}= \frac{1+|\rho_{L}|}{1-|\rho_{L}|}
$$
A reflected wave implies some reflected power. The proportion of reflected power is
$$
r_{p}=\rho_{L}^{2}
$$

### Open-ended circuit
$$
\begin{align}
Z_{L}&=\infty \\
\rho_{L}&=1
 \end{align}
$$
The reflected wave has no phase change. A perfect standing wave $(\mathrm{VSWR}=\infty)$ appears with an antinode at the reflection point.
![[open-ended-circuit.png]]

### Close-ended circuit
$$
\begin{align}
Z_{L}&=0 \\
\rho_{L}&=-1
\end{align}
$$
The reflected wave has a phase change of $\pi.$ A perfect standing wave $(\mathrm{VSWR}=\infty)$ appears with a node at the reflection point.

![[close-ended-circuit.png]]

### Matched load impedance
$$
\begin{align}
Z_{L}&=Z_{0} \\
\rho_{L}&=0
\end{align}
$$
There is no reflected wave—all power is dissipated in the load! This is the ideal case for most scenarios.

## Dealing with an unmatched impedance


tbc rest of electromagnetism lecture 2 