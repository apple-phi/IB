Modulation is the process by which some characteristic of a carrier wave is varied in accordance with an information bearing signal.

A common carrier is a sinusoidal wave. We are allotted a certain [[bandwidth]] centred at the carrier frequency to carry our information signal. 

>The carrier frequency is usually large because it allows the receiver antenna to be small.

## Amplitude modulation (AM)
Given a signal $x$ and carrier signal $c=\cos(2\pi f_{c}t),$ the modulated signal is
$$
s=(a_{0}+x)c
$$
where $a_{0}>\max|x|.$ This constraint is imposed to avoid phase reversals (change of sign in $x$) in the signal, since this inhibits signal reconstruction.

![[phase-reversal.png|600]]

The modulation index of the amplitude modulated signal is defined as
$$
m= \frac{\max|x|}{a_{0}}<1
$$

## AM receiver
![[am-receiver.png]]
On the $+ve$ half-cycle of the input signal $s,$ the capacitor rapidly charges up to the peak value $s_\text{peak}.$

When the input signal falls, the diode becomes reverse-biased and the capacitor discharges slowly through the load $R_{L}.$

![[am-receiver-waveform.png]]

## AM spectrum
Consider the spectrum of $s$
$$
\begin{align}
S&=\mathscr{F}\{(a_{0}+x)c\} \\
&=\frac{a_{0}}{2}[\delta(f+ f_{c})+\delta(f-f_{c})]+\frac{1}{2}[X(f+f_{c})+X(f-f_{c})] \\
&=a_{0}\delta(f\pm f_{c})+\frac{1}{2}[X(f+f_{c})+X(f-f_{c})]
 \end{align}
$$

![[AM-modulation-spectrum.png]]

## AM properties
### Bandwidth
The AM signal is passband with [[bandwidth]] $2W$ where $W$ is the one-sided [[bandwidth]] of the baseband signal.

### Power
The power of an AM signal is given by
$$
P_{\mathrm{AM}}= \frac{a_{0}^{2}+P_{x}}{2}
$$
*Proof:*
$$
\begin{align}
P_{\mathrm{AM}}&=\lim_{ t \to \infty }  \frac{1}{T}\int _{0}^{T}(a_{0}+x)^{2}\cos ^{2}(\omega_{c}t) \, \mathrm{d}t \\
&= \lim_{ t \to \infty }  \frac{1}{T}\int_{0}^{T} \frac{(a_{0}+x)^{2}}{2}{[1+\cos(2\omega_{c}t)]} \, \mathrm{d}t \\
&= \frac{a_{0}+P_{x}}{2}+\lim_{ t \to \infty }  \frac{1}{T}\int_{0}^{T} \frac{(a_{0}+x)^{2}}{2}{\cos(2\omega_{c}t)} \, \mathrm{d}t \\
 \end{align}
$$
Applying squeeze theorem, we can see that 
$$
\operatorname{O}(T)> \operatorname{O}\left( \int_{0}^{T} \frac{(a_{0}+x)^{2}}{2}{\cos(2\omega_{c}t)} \, \mathrm{d}t \right) 
$$
Hence the limit tends to $0.$

## Double sideband suppressed carrier
The presence of the $a_{0}$ makes envelop detection possible, but requires an extra power of $\frac{a_{0}^{2}}{2}$ to generate.

If we only transmit the sidebands and suppress the carrier, we can remove this extra power requirement.

The transmitted DSB-SC waveform is
$$
s(t)=x(t)\cos(\omega_{c}t)
$$

![[dsb-sc.png]]
### DSB-SC receiver
Due to the phase reversals, envelop detection cannot be used.

![[DSB-SC-receiver.png]]

The first step of multiplying the received signal by another $\cos(\omega_{c}t)$ term gives 
$$
\begin{align}
s'(t)&=s(t)\cos(\omega_{c}t) \\
&=x(t)\cos ^{2}(\omega_{c}t) \\
&= \underbrace{ \frac{x(t)}{2}}_{ \text{low freq.} }+ \underbrace{ \frac{x(t)\cos(2\omega _{c}t)}{2}}_{ \text{high freq.} }
 \end{align}
$$
The second step of using a high-frequency low-pass filter then recovers the pure low-frequency term.

### DSB-SC properties
$$
\begin{align}
s(t)&=x(t)\cos(2\pi f_{c}t) \\
S(f)&=\frac{1}{2}[X(f+f_{c})+X(f-f_{c})]
\end{align}
$$
- The [[bandwidth]] $B_{s}=2W$ is the same as for amplitude modulation.
- The power is $P_{s}=\frac{P_{x}}{2}$ is lower than for amplitude modulation.
- Less signal power required, but a more complex receiver required.

We assumed that receiver can generate a frequency $f_{c}$ sinusoid that is synchronised perfectly in phase and frequency with transmitter’s carrier. 

## Single sideband suppressed carrier

Let’s see how to save [[bandwidth]] too! Since $x(t)$ is real, we encode the same information if we only transmit the upper sideband.

![[ssb-sc.png]]

- The [[bandwidth]] is $B=W,$ half of that of AM or DSB-SC!
- The power is $P= \frac{P_{x}}{4},$ half of DSB-SC

## Amplitude modulation summary

![[AM-summary.png]]

## Frequency modulation

In FM we modulate the instantaneous frequency of the carrier wave.

 The modulated signal $f(t)$ is varied linearly with $x(t),$
$$
f(t)=f_{c}+k_{f}x(t)
$$
Hence the instantaneous phase is given by
$$
\begin{align}
\theta(t)&=2\pi \int_{0}^{t}f(\tau) \, \mathrm{d}\tau  \\
&=\omega_{c}t+2\pi k_{f}\int_{0}^{t}x(\tau) \, \mathrm{d}\tau 
 \end{align}
$$
The modulated FM signal is then
$$
\begin{align}
s(t)&=A_{c}\cos(\theta(t)) \\
&=A_{c}\cos \left( \omega_{c}t+2\pi k_{f} \int_{0}^{t}x(\tau) \, \mathrm{d}\tau \right) 
 \end{align}
$$
where $A_{c}$ is the carrier amplitude and $k_{f}$ is the frequency-sensitivity factor.

## FM demodulation
To recover the original signal $x(t)$ from the modulated signal $s(t),$ we can take the time derivative.
$$
\dot{s}=-A_{c}(k_{f}x(t)+\omega_{c})\sin \left( \omega_{c}t+2\pi k_{f}\int_{0}^{t}x(\tau) \, \mathrm{d}\tau  \right) 
$$
I.e., the derivative is a passband signal with amplitude modulation by $[f_{c}+k_{f}x(t)]$

If $f_{c}$ is large enough we can recover $x(t)$ by envelop detection of $\dot{s}.$

Hence the FM demodulator needs to be a differentiator and an envelope detector.

## FM properties
- The power is invariant of $x(t)$ and is $\frac{A^{2}_{c}}{2}$
- Non-linear: $\operatorname{FM}\left\{ x+y \right\}\neq\operatorname{FM}\{x\}+\operatorname{FM} \{y\}$
- More robust to noise than AM 
- Higher bandwidth than AM 

## FM modulation of a pure tone
Consider the $\mathrm{FM}$ modulation of a pure tone $x(t)=a_{x}\cos(\omega_{x}t).$ Then the frequency and phase under $\mathrm{FM}$ modulation is
$$
\begin{align}
f(t)&=f_{c}+k_{f}a_{x}\cos(\omega_{x}t) \\
\theta(t)&=\omega_{c}t+\frac{k_{f}{a_{x}}}{f_{x}}\sin(\omega_{x}t)
\end{align}
$$
Define $\Delta f=k_{f}a_{x},$ the frequency deviation. It is a maximum deviation of the carrier frequency $f(t)$ from $f_{c}.$

Define $\beta=\frac{\Delta f}{f_{x}},$ the modulation index. It is the maximum deviation of the carrier phase from $\omega_{c}t.$

Then the $\mathrm{FM}$ signal is
$$
s(t)=A_{c}\cos(\omega_{c}t+\beta \sin(\omega _{x}t))
$$
This has the frequency spectrum of
$$
S(f)=\frac{A_{c}}{2}\sum\limits_{ n=-\infty }^{ \infty }J_{n}(\beta)[\delta(f-f_{c}-nf_{x})+\delta(f+f_{c}+nf_{x}]
$$
where $J_{n}$ is the $n$th order Bessel function of the first kind.
$$
J_{n}(\beta)= \frac{1}{2\pi}\int_{-\pi}^{\pi} e^{ j(\beta \sin u-nu) } \, \mathrm{d}u 
$$

![[Bessel-func-first-kind.png]]
## Pure tone example
![[FM-mod-pure-tone.png]]
## Bandwidth of an FM signal

Even when $x(t)$ has a single frequency $f_{x},$ the spectrum of the $\mathrm{FM}$ wave is still quite complicated.
- There is a carrier component at $f_{c}$ and components located symmetrically on either side of $f_{c}$
- The absolute bandwidth is infinite but the side components at $f_{c}\pm nf_{x}$ are negligible for large $n.$

### Carson’s rule
For the *effective* bandwidth of $\mathrm{FM}$ signals:
- The bandwidth of an $\mathrm{FM}$ signal generated by modulating a single tone is
$$
\begin{align}
B&\approx 2(f_{x}+\Delta f) \\
&=2\Delta f\left( 1+\frac{1}{\beta} \right)
 \end{align}
$$
- The [[bandwidth]] of an $\mathrm{FM}$ signal generated by modulating a general signal $x(t)$ with [[bandwidth]] $W$ is
$$
B=2(W+\Delta f)
$$
## Summary

tbc