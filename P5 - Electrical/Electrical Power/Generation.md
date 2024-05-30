## Features of electrical energy
- No easy means of bulk storage—pumped storage is the only impactful method—so generated power must equal consumed power at all times and instantly react to changes in demand (e.g. by keeping a pooled spinning reserve)
- Supplier has no control over demand variation (except through pricing)—generation must exceed maximum demand
- Future demand predicted to increase greatly
- Environmental factors are considered important
- Security of supply is important—a high degree of interconnection (e.g. National Grid) to avoid bottlenecks requires synchronised generation.

## Basic principles
Generators consist of a *stator* and a *rotor*:
- stator—stationary
- rotor—rotates around bearings when driven by the prime-mover
![[rotor-stator.png|500]]
DC current fed into rotor coils by slip-rings and brushes, which sets up a magnetic field through the path:
1. Rotor core
2. Air gap
3. Stator core
4. Air gap
5. Rotor core

The air gap magnetic flux density varies sinusoidally with $\theta$,
$$
\mathbf{B}(\theta, t)=\widehat{\mathbf{B}}\cos(\omega_{\mathrm{rotor}}t-\theta)
$$
The total flux linked through one coil is
$$
\phi(t)=\iint \mathbf{B}\cdot \,\mathrm{d}\mathbf{A} 
$$
And the total generated EMF through all coils can be found through Faraday’s Law,
$$
\mathrm{EMF} = -N\frac{\mathrm{d}\phi}{\mathrm{d}t}
$$
From this derivation:
- A rotating sinusoidal air gap flux density induces a sinusoidal time varying EMF in the stator coil
- Frequency and magnitude of the EMF are both proportional to the rotor speed $\omega_{r}$
- The EMF phase $\alpha$ is the same as the angular position of the stator coil
## Multiple coil generators
Real generators have many coils evenly distributed throughout the stator.
![[multi-coil-gen.png|500]]
To reduce the maximum current per coil (and limit power loss in heating), connect the coils in series into three phases.
$$
V:=\hat{V}_{a}=\hat{V}_{b}=\hat{V}_{c}
$$
![[three-phase-coils.png|500]]

This also makes the wiring easier.

The maximum output power is
$$
P_{\mathrm{max}}=3VI_{\mathrm{max}}
$$
>Note that the coils cannot be connected in parallel since individual coils have different instantaneous EMFs.

Consider if they were connected to give a single-phase supply:
![[single-phase-gen.png|500]]
Then $\left|\bar{V}_{1\varphi}\right|=2V$ so
$$
\begin{align}
P_{1\varphi,\mathrm{max}} & =2VI_{\mathrm{max}} \\
 & =\frac{2}{3}P_{3\varphi,\mathrm{max}}
\end{align}
$$
The self-interference due to the phases leads to a lower efficiency, even though we’ve modelled the power loss per phase as being the same! 

>On the bright side we only need 2 wires…

Relative to the 3-phase implementation:

| # phases | # wires | power output (%) |
| ---- | ---- | ---- |
| 1 | 2 | 66.7 |
| 2 | 3 | 94.2 |
| 3 | 3 | 100  |
| 4 | 4 | 102 |

## Magnetic field due to stator currents
Consider the flux density due to current in phase $A$. Flux crosses the air gap radially since iron is a very good conductor of magnetic flux. The field pattern is called a 2-pole because the flux density crosses the air gap once in the outward and once in the inward direction.
![[stator-mag-field.png|500]]
If phases $A$, $B$ and $C$ are sequentially excited, the field pattern rotates! This is the physical basis of the rotating magnetic field.

Ampere’s Law shows that the air gap flux density is a square wave of amplitude
$$
B= \frac{\mu_{0}NI}{2g}
$$
Using Fourier analysis of a square wave, it can be approximated as a single sinusoid with
$$
\hat{B}=\frac{2\mu_{0}NI}{\pi g}
$$
Considering the three phases $A$, $B$ and $C$ at angles of $\gamma=0,\pm 120^{\circ}$, by superposing the fields they produce, the net field is
$$
\begin{align}
B(\theta, t) & = \sum B_{i}(\theta, t) \\
 & = \frac{\mu_{0}\hat{I}N}{\pi g}\sum_{\phi\in\left\{  0,\pm \frac{\pi}{3} \right\}}2\cos(\theta+\phi)\cos(\omega t+\phi) \\
& = \frac{\mu_{0}\hat{I}N}{\pi g}\sum_{\phi\in\left\{  0,\pm \frac{\pi}{3} \right\}}\left[ \cos(\omega t-\theta)+\cos(\omega t+\theta+\phi) \right]  \\
 & = \frac{3\mu_{0}\hat{I}N}{\pi g}\cos(\omega t-\theta)
 \end{align}
$$

Balanced 3-phase currents in balanced 3-phase windings produce a rotating magnetic field!

## Multi-pole windings
Two coils per phase gives a four pole field. 
![[2-pole-field.png|500]]
$p$ coils per phase gives a $2p$ pole field.

The rotating field is then given by
$$
B(\theta,t)=\hat{B}\cos(\omega t-p\theta)
$$
Consider a point on the wave that moves an angular distance $\Delta\theta$ in time $\Delta t$,
$$
\begin{align}
\hat{B}\cos(\omega t-p\theta) & =\hat{B}\cos(\omega t+\omega\Delta t- p\theta-p\Delta t) \\
0 & =\omega\Delta t-p\Delta t \\ \\
\Rightarrow\quad \frac{\mathrm{d} \theta}{\mathrm{d}t}  & =\frac{\omega}{p}
 \end{align}
$$
Hence the *synchronous speed* is $\dot{\theta}=\frac{\omega}{p}$

## Conditions for steady torque production

For steady torque, the rotor must rotate in synchronism with the stator field, and the rotor and stator must possess the same number of poles.

### Pole number condition
The rotor and stator-driven fields must have the same number of poles. This is so each rotor pole can pair up with a corresponding  stator pole during each phase of the rotation.

![[rotor-stator-torque.png|500]]

### Synchronous speed condition 
The rotor speed must be equal to the speed of the stator-driven field,
$$
\omega_{r}=\frac{\omega}{p_{s}}
$$
If this were not the case, then the direction of torque would flip, e.g. in the case where a rotor passes a stator pole but the slip rings haven’t caused swapped the field direction yet.
![[synch-speed.png|500]]

At this synchronous speed, the torque $T$ is
$$
T=K\hat{B}_{s}\hat{B}_{r}\sin\alpha
$$

## The equivalent circuit
The rotor, stator-driven and total air gap fields can be shown on a space phasor diagram.

![[space-phasor-rotor-stator.png|500]]

The time phase of induced EMF equals space phase of the inducing magnetic field. The magnitude of induced EMF is proportional to the magnitude of the inducing field.

At the ideal stator winding,
$$
E_{t}=V
$$
Since the stator consists of inductive coils,
$$
E_{s}\propto B_{s}\propto I=jX_{s}I
$$
where $X_{s}$ is the *synchronous reactance*.

$E_{r}$ is the excitation voltage—the EMF induced by the rotor-driven field.

>We *assume* that $E_{r}$ is proportional to the rotor field current excitation.
$$
\begin{align}
\overline{ E}_{t} & =\overline{ E}_{r}+\overline{ E}_{s} \\ \\
\Rightarrow\quad \overline{ V} & =\overline{ E}+j\bar{I}X_{s}
 \end{align}
$$
This equation directly leads to the equivalent circuit.
![[rotor-stator-equiv-circuit.png|600]]
## Generator convention
Most synchronous machines operate as generators so it is convenient to make power flowing out of the terminals positive, contrary to the standard EE convention.

## Operation modes
### Stand-alone operation
A single generator supplies a single 3-phase load. This occurs in a limited set of situations, usually when connection to the national grid is too expensive.

### Parallel operation
When connected to the massive national grid, no individual generator in the network has a significant impact on the terminal voltage. This is known as an *infinite bus*.

## Variation of torque with load angle
As before, 
$$
T=K\hat{B_{r}}\hat{B}_{s}\sin\alpha
$$
Applying the sine rule,
$$
\begin{align}
\hat{B}_{s}\sin\alpha & =\hat{B}_{t}\sin\delta \\
 \\
\Rightarrow\quad T&=K\hat{B}_{r}\hat{B}_{t}\sin\delta
 \end{align}
$$
![[variation-torque-load-angle.png|500]]
Constant $V$ under the infinite bus $\implies$ also constant $\hat{B}_{t}$ and constant excitation means that $E$ is fixed hence $\hat{B}_{r}$ is also fixed. Therefore,
$$
T\propto \sin\delta
$$
where $\delta$ is known as the load angle.
![[load-angle.png|600]]
## Control of real power
With the prime-mover coupled to the generator and both rotating at synchronous speed without mechanical power transfer, the phase location is $[\delta,T]=[0,0]$

With the prime-mover exerting an accelerating torque on the generator then the load angle $\delta$ increases such that the generator electromagnetic torque balances the prime-mover torque until the rotation stabilises again at $\omega_{s}$

The maximum generator torque occurs at $[T,\delta]=\left[ T_{\max}, \frac{\pi}{2} \right]$. In the dangerous case $\delta> \frac{\pi}{2}$ the generator *loses synchronism* and accelerates out of sync, which reduces its torque, accelerating it even faster.

Suppose a load is coupled to the synchronous machine which applies a braking torque to balance this. Thus the machine behaves like a motor with $\delta<0$. In this case losing synchronism is less dangerous because the result is only the total stop of the machine.

## Power and torque
As before the output power is
$$
P_{\mathrm{out}}=3VI\cos \varphi
$$
This balances the input power
$$
P_{\mathrm{in}}=T\omega_{s}
$$
So the required torque is
$$
T= \frac{3VI\cos \varphi}{\omega _{s}}
$$
Now consider this general phasor diagram:
![[phasor-diag-generator.png|600]]
$$
E\sin\delta=X_{s}I\cos \varphi
$$
Therefore the torque in terms of $\delta$ is
$$
T= \frac{3VE}{\omega_{s}X_{s}}\sin\delta
$$
Under constant $V$ and $E$,
$$
T\propto \sin\delta
$$
as before.

## Control of reactive power
Recall that 
$$
P=T\omega_{s}=\frac{{3VE\sin\delta}}{X_{s}}
$$
Under constant $E\sin\delta,$ the end point of the $\tilde{E}$ phasor is free to move horizontally so that $\delta$ can account for reactive power.
![[control-of-vars.png|600]]
Higher $E$ means $\delta$ decreases so the current lags voltage and the *over-excited* machine supplies $\pu{VARs}.$

Lower $E$ means $\delta$ increases so the current leads voltage and the *under-excited* machine absorbs $\pu{ VARs}$.

Thus controlling $E$ enables control of reactive power. So synchronous machines can be used as synchronous compensators to correct the power factor.

## Generator construction
- Stators laminated to prevent eddy currents
- Rotor rectified by either
	- slip rings & brushes
	- AC generator and rectifier
- Rotor does not need to be laminated—constant magnetic field
### Cylindrical rotor
For high-speed machines, 2 or 4 pole generators are used, with long, thin rotors to minimise centrifugal stress.
### Salient-pole rotor
Low-speed machines such as hydro-turbines use 30+ poles, manufactured by joining separately-wound poles to the rotor core.

Stator windings are water cooled to remove heat. Stator and rotor also gas cooled.

## Generator VA rating
Generator is current limited by heating of stator coils due to resistance, voltage limited by flux (iron losses) and insulation considerations.
$$
\text{VA rating}=S_{\max}=3V_{ph}I_{ph}
$$
## Operating chart
After scaling the sides of the phasor diagram by $\frac{3V}{X_{s}}$ the resulting diagram shows the generator operating limitations.
![[op-chart.png|600]]
$$
\begin{align}
P&=3VI\cdot\mathbf{i} \\
&=3VI\cos \varphi \\
 \\
Q&=3VI\cdot\mathbf{j} \\
&=3VI\sin \varphi  \\
 \\
S&=|\mathrm{OP}| \\
&=3VI
 \end{align}
$$
We can draw limiting lines for the various parameters. 
- Vertical position of $P$ is constrained by the prime-mover limit
- $S$ is constrained by the rated VA of the generator—the stator-heating limit
- Length $|\mathrm{AP}|=\frac{3|\mathrm{VE}|}{X_{s}}$ is limited by the maximum excitation EMF, $E_{\max}$—the rotor-heating limit
- The safe load angle is constrained by a practical stability limit
![[op-chart-limits.png|600]]
![[op-chart-another.png|600]]
