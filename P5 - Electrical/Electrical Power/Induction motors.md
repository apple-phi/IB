The stator is wound with a balanced 3-phase winding excited by a balanced 3-phase voltage supply, so there is a rotating magnetic field in the air gap.

This magnetic field rotates at $\omega_{s}=\frac{\omega}{p}.$ The rotor is also wound with a balanced 3-phase winding *but with its terminals short circuited*.
![[Induction motor.png]]
Define the slip $s$ as the amount of synchronicity between the rotor and its driving stator,
$$
\begin{align}
s&= \frac{\omega_{s}-\omega_{r}}{\omega_{s}}
 \end{align}
$$
From the rotor reference frame, the stator-driven field is rotating at $\omega_{s}-\omega_{r}.$ Then, in this reference frame
$$
s\omega _{s}=\frac{s\omega}{p}
$$

>The stator and rotor-driven fields have the same number of poles and rotate at the same speed—these conditions necessary for torque production.

At exactly synchronous speed, there is no relative motion of the fields so no torque is produced.

>Because of this, the induction motor is also known as the asynchronous motor.

## Equivalent circuit
It looks like a transformer with a 1:1 turning ratio transformer with its output short-circuited.
![[Induction motor equivalent circuit.png]]
The parameters are:
- $R_{1}$—stator winding resistance
- $X_{1}$—stator leakage reactance
- $R_{2}$—rotor winding resistance
- $X_{2}$—rotor leakage reactance
- $X_{m}$—magnetising reactance
- $R_{0}$—iron loss resistance

The induced EMF per phase in the stationary rotor is
$$
\tilde{E}_{2}=\tilde{I_{2}}(R_{2}+jX_{2})
$$
At rotation with slip $s$, $E_{2}\to sE_{2}$ because $\omega\to s\omega$ and $\mathrm{EMF}\propto\omega.$ Also, $X_{2}\to sX_{2}$ because $\omega\to s\omega.$
$$
\tilde{E}_{2}=\tilde{I_{2}}\left( \frac{R_{2}}{s}+jX_{2} \right)
$$
Then referred to the stator side,
![[stator-side-equiv-circ.png]]

>If $Z_{1}$ is small, then $R_{0}\parallel X_{m}$ can be moved to the terminals
## Finding equivalent circuit parameters
### No-load test for $R_{0}$ and $X_{m}$
No load means there is no slip, so $\frac{R_{2}'}{s}\to \infty.$ We assume that $Z_{1}\ll R_{0}\parallel X_{m}$ so we can use this simplified circuit as our equivalent:
![[no-load-test-induction-motor.png]]

### Locked rotor test for $Z_{1}$ and $Z_{2}'$
Holding the rotor stationary, there is $100\%$ slip, $s=1.$ The magnetising terms $R_{0}$ and $X_{m}$ are negligible compared to the rotor and stator impedances $Z_{1}$ and $Z_{2}$, so we can use this simplified circuit as our equivalent:
![[locked-rotor-test.png]]

## Construction
### Stator
Same as synchronous machine *i.e.*, laminated, carries a balanced three-phase winding.

### Rotor
Rotor winding must produce rotating $B$-field with same number of poles as stator.
- Laminated

The two options are:

#### Wound (slip-ring) rotor
3-phase windings of same pole-number as stator winding. Can be short- circuited, or provided with slip-rings & brushes, so external resistances can be added
![[wound-rotor.png]]

This physical contact has the problem of insulation wearing-away.
#### Cage rotor
Also known as a *Squirrel cage rotor*, this is comprised of 1 conductor per slot. Joined at ends by thick conducting end-rings.

Either:
- Fabricated, or
- Die-cast

##### Fabricated rotor
The conducting copper bars are shorted across the rotor, at a certain skew angle.
![[fabricated-rotor.png]]
##### Die-cast rotor
![[die-cast-rotor.png]]

## Power and torque
$$
P_{i}=3I_{1}^{2}R_{1}+3I_{0}^{2}R_{0}+\frac{3{I_{2}'}^{2}R_{2}'}{s}
$$
The power losses are:
- Iron loss $3I_{0}^{2}R_{0}$ 
- Stator winding loss $3I_{1}^{2}R_{1}$ 
- Rotor winding loss $3I_{2}^{2}R_{2}=3{I_{2}'}^{2}R_{2}'$ 

$$
P_{\mathrm{loss}}=3I_{0}^{2}R_{0}+3I_{1}^{2}R_{1}+3I_{2}^{2}R_{2}
$$
Therefore the output power is
$$
P_{o}=\frac{3(1-s)}{s}{I_{2}'}^{2}R_{2}'
$$
The mechanical power is then $P_{o}=T\omega_{r}=T\omega _s(1-s)$
$$
T= \frac{3}{s\omega_{s}}{I_{2}'}^{2}R_{2}'
$$
Where $T$ is the gross torque. The mechanical loss torque is given by
$$
T_{\mathrm{net}}=T-T_{\mathrm{loss}}
$$

## Variation of torque with speed
If $s<0,$ the machine is a generator. It has negative torque.

If $0<s<1,$ the machine is a motor. It has positive torque.

If $s>1,$ the machine dissipates electrical energy. This only occurs when $\omega_{s}\omega_{r}<0,$ *i.e.*, the rotor and stator have opposite rotation directions!

>This is often used to rapidly stop an induction motor, known as plug-braking.

![[torque-and-slip.png]]

When $s=1,$ the rotor and stator have no relative rotation so produce no torque.
## Maximum torque
We derived above that
$$
T= \frac{3}{s\omega_{s}}{I_{2}'}^{2}R_{2}'
$$
Therefore the maximum torque is given when there are the maximum losses in the $\frac{R_{2}'}{s}$ internal resistance.

## Rotor resistance torque / speed control
Two key results:
- $T_{\max}$ is independent of $R_{2}'$
- $s_{m}\propto R_{2}'$

![[rotor-resistance-torque.png]]

Therefore we can set the angular speed that maximises the torque by setting the rotor resistance.

In wound (slip-ring) motors the extra rotor resistance can be connected via slip-rings. For squirrel cage rotors, you can add extra resistance via specially shaped Boucherot slots to take advantage of the skin effect.

### The skin effect
This skin effect is the tendency of high frequency current to flow at the surface of a conductor, thereby increasing the resistance.

In cage rotors, high frequencies only occur at low speed.

**tbc: make this concise**

At starting the majority of the current flows in the smaller cross-section at the top of the slot, so with a reduced conductor area the resistance is naturally large. At low slips, the current flows over the entire slot area, thus the effective resistance becomes reduced. The result is the torque-speed curve shown in Fig. 10.8, so that maximum torque is achieved over most of the speed range.

![[boucherot-slot.png]]
