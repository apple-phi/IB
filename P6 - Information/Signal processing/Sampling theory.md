Consider a function $f$ sampled at intervals of $T$ such that we obtain the values of $f(x\in T\mathbb{Z})$.

If we measure of $T$ that are
-  Too large—we have insufficient data to reconstruct the signal. This can lead to aliasing.
- Too small—we preserve noise in the output

## The sampling theorem
Representing the discrete sampling of a continuous signal $f$ as multiplication with a function $g$ composed of a train of $\delta$ functions at intervals of $T$,
$$
\begin{align}
g=\frac{1}{T}\sum\limits_{ n=-\infty }^{ \infty } e^{-j\omega_{n}t}
 \end{align}
$$
Taking the [[Fourier transform]] of the sampled signal $f_{s}=f\cdot g$,
$$
\begin{align}
F_{s}=\mathscr{F}\{f\cdot g\}&= \frac{1}{T}\sum\limits_{ n=-\infty }^{ \infty }fe^{-j\omega_{n}t} \\
&= \frac{1}{T}\sum\limits_{ n=-\infty }^{ \infty }F(\omega-n\omega_{0})
 \end{align}
$$
Consider a signal with frequency band $[0,\omega_{\max}]$. Then $F_{s}$ will have peaks of width $2\omega_{\max}$ centred at each integer multiple of the sampling frequency $n\omega_{n}$. Aliasing occurs when the peaks overlap.

The maximum $\omega_{\max}$ before aliasing is $\frac{\omega_{0}}{2}$ so the Nyquist (optimum) sampling frequency is $\omega_{0}=2\omega_{\max}$.

>For perfect signal reconstruction, the sampling frequency must be at least double the maximum signal frequency. 

![[nyquist-frequency.png|600]]
## Discrete-time Fourier Transform (DTFT)
The [[Fourier transform]] of the sampled signal can alternatively be written as
$$
F_{s} = \sum\limits_{ n=-\infty }^{ \infty }f(nT)e^{-j\omega_{n}t}
$$

## Ideal reconstruction filter
For perfect reconstruction, the frequency domain representation of the ideal filter $h_{r}$ applied by convolution in the time domain is
$$
\begin{align}
H_{r} (\omega)&= \begin{cases}
\begin{aligned}
&T &&\omega\in[-\omega_{\max}, +\omega_{\max}] \\
&0 &&\mathrm{otherwise}
\end{aligned}
\end{cases} \\
 \\
h_{r}(t)&=\frac{\omega_{max}T}{\pi}\operatorname{sinc}(\omega_{max}t)
 \end{align}
$$
This filter selects the fundamental peak from the spectrum of $F_{s}$

At the Nyquist frequency this is then
$$
h_{r}(t)=\operatorname{sinc}\left( \frac{\omega_{0}}{2}t \right)
$$
So, applying the convolution filter,
$$
\begin{align}
f(t)&=h_{r}*f_{s} \\
&= \operatorname{sinc}\left( \frac{\omega_{0}}{2}t \right)*\sum\limits_{ n=-\infty }^{ \infty }f(nT)\delta(t-nT) \\
&=\sum\limits_{ n=-\infty }^{ \infty }f(nT)\operatorname{sinc}\left[ \frac{\pi}{T}(t-nT) \right] 
 \end{align}
$$
by sifting theorem. So the original signal $f$ can be perfectly reconstructed as a discrete (but infinite!) summation.

## Practical considerations
- Must determine the maximum frequency desired to preserve before sampling
- To avoid aliasing of noise, apply low-pass filter first
- Can’t implement the ideal reconstruction filter in practice, a frequency step change will be gradual in practice, so must allow a little extra signal [[bandwidth]] to account for this.
