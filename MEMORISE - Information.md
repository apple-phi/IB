## BPSK
tbc

## Linear systems
### Bode plots
[my.ece.utah.edu/\~ee3110/bodeplot.pdf](https://my.ece.utah.edu/~ee3110/bodeplot.pdf)

### Nyquist stability criterion
For a closed loop system with return ratio $L(s)$ and transfer function
$$
\frac{L(s)}{1+L(s)}
$$
if we know that $L(s)$ is asymptotically stable (all poles in LHP) and its Nyquist contour has no net encirclements of $-1+j0$ then the closed loop system is stable.

If the Nyquist contour of $L(s)$ leaves the point $-1+j0$ entirely on the left, we can assume that the closed loop system is stable, even if $L(s)$ is unstable.

>Unexaminable: more complicated unstable $L(s)$

## Fourier transforms
### Standard transforms
The Fourier transform of a standard unit-height rectangular pulse $\operatorname{rect}(t)$ from $t\in[-1,1]$ centred at the origin is
$$
\operatorname{rect(t)}\leftrightarrow 2
\operatorname{sinc}(\omega)
$$
The Fourier transform of a standard $\operatorname{sinc}$ pulse is then
$$
\operatorname{sinc}(t)\leftrightarrow \pi \operatorname{rect}(\omega)
$$
by duality.

### Properties

Duality
$$
\mathscr{F}\{F(\omega)\}=2\pi f(-\omega)
$$
Time-scaling
$$
f(at)\leftrightarrow \frac{1}{a}F\left( \frac{\omega}{a} \right)
$$
Frequency-scaling
$$
\frac{1}{a}f\left( \frac{t}{a} \right)\leftrightarrow F(a\omega)
$$

Conjugation
$$
\overline{ f(t)}=\overline{ F(-\omega)}
$$

>Others in Databook

## Reconstruction filters
- Windowed $\operatorname{sinc}$—approximates ideal brick-wall filter in the frequency domain
	- But has ringing / edge effects
- Triangular filter—linear interpolation

## Signal modulation
 The carrier frequency is big so the receiver antenna can be small.
 
![[AM-summary.png|400]]
## Amplitude Modulation (AM)
$$
s=(a_{0}+x)c
$$
where $a_{0}>\max|x|$ to avoid phase reversal.

Modulation index
$$
m= \frac{\max|x|}{a_{0}}<1
$$
Bandwidth
$$
B=2W
$$
Power
$$
P= \frac{a_{0}^{2}+P_{x}}{2}
$$

*Rx*: envelope detector
![[am-receiver.png|400]]
On the $+ve$ half-cycle, capacitor charges up to the peak value of $s$. When the input signal falls, the diode becomes reverse-biased and the capacitor discharges slowly through the load $R_{L}.$

![[am-receiver-waveform.png|400]]

## Double Sideband Suppressed Carrier (DSB-SC)
By suppressing the carrier,
$$
s(t)=x(t)\cos(\omega_{c}t)
$$
Bandwidth same as for AM
$$
P=2W
$$
Power lower than $\mathrm{AM}$ since carrier is suppressed
$$
P= \frac{P_{x}}{2}
$$
*Rx*: product modulator (with a copy of the carrier) then low pass filter.
![[DSB-SC-receiver.png|400]]
$$
\begin{align}
s'(t)&=s(t)\cos(\omega_{c}t) \\
&=x(t)\cos ^{2}(\omega_{c}t) \\
&= \frac{x(t)}{2} + \frac{x(t)\cos(2\omega _{c}t)}{2}
\end{align}
$$

## Single Sideband Suppressed Carrier (SSB-SC)
Encoding only the upper sideband saves bandwidth.

Bandwidth half of AM
$$
B=W
$$
Power is half of DSB-SC (quarter of AM)
$$
P= \frac{P_{x}}{4}
$$
Can reconstruct by symmetry.
## Frequency Modulation (FM)
Modulate the instantaneous frequency of the carrier wave
$$
f(t)=f_{c}+k_{f}x(t)
$$
so the instantaneous phase is
$$
\theta(t)=2\pi \int_{0}^{t}f(\tau) \, \mathrm{d}\tau
$$
The modulated FM signal is
$$
s(t)=A_{c}\cos(\theta(t))
$$
Frequency deviation
$$
\Delta f=k_{f}\max_{t} x(t)
$$
Modulation index for a pure tone $x(t)=A\cos(2\pi f_{x}t)$
$$
\begin{align}
\beta&=\frac{\Delta f}{f_{x}} \\
&=\max|\theta-\omega_{c}|
 \end{align}
$$

*Rx*: time-differentiator then envelope detector.

Power only depends on carrier
$$
P= \frac{1}{2}A_{c}^{2}
$$

More robust to noise than $\mathrm{AM}.$ Non-linear.

**Infinite bandwidth!** Effective bandwidth given by Carson’s rule.
$$
\begin{align}
B&=2(f_{x}+\Delta f) \\
&=2(f_{x}+W)
 \end{align}
$$

## Pulse amplitude modulation (PAM)
$$
x_{b}(t)=\sum_{k}X_{k}p(t-kT)
$$
Integer pulse-shifts must be orthonormal $\delta_{ij}$

*Rx*:
- matched-filter demodulation by time-convolution with $p(-t)$
- detection

The average symbol energy for an $M$-point constellation is related to the average bit energy by
$$
E_{s}=\frac{1}{M}\sum_{m}A^{2}_{m}=E_{b}\log_{2}M
$$
since each symbol represents $\log_{2}M$ bits.

Transmission rate
$$
\frac{1}{T}\, \pu{symbols/s}=\frac{\log_{2}M}{T}\,\pu{bits/s}
$$

Signal-to-noise ratio
$$
\mathrm{snr}=\frac{E_{b}}{\sigma^{2}}
$$
## Quadrature amplitude modulation (QAM)

Tx: Passband generated like $\mathrm{PAM}$ but with complex-valued constellation, then up-converted by AM baseband to send both real and imaginary parts orthogonally
$$
\begin{align}
s(t)&=\Re\left\{ x_{b}e^{ j\omega_{c}t } \right\}  \\
&=\sum_{k}p(t-kT)\left[\Re\left\{ X_{b} \right\} \cos(\omega_{c}t)-\Im\left\{ X_{b} \right\} \sin(\omega_{c}t) \right] 
 \end{align}
$$
Rx:
- down-converted by product modulator and filter for each carrier
- demodulated by matched filter time-convolution with $p(-t)$
- detection

Bandwidth same when up- and down- converted
$$
B=2W_{p}
$$

## Hamming Code
$(N,K)=(7,4)$ block code—it carries 4 bits of information in a total of 7 bits. Can error correct one bit.

Put the source block $\{s_{1},s_{2},s_{3},s_{4}\}$ as the overlaps then the parity bits $\{c_{5},c_{6},c_{7}\}$ are such that the parity of each circle is even—there must be an even number of 1s in each circle.

![[hamming-code.png|300]]