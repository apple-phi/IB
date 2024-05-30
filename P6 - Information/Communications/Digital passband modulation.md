Recall that the $\mathrm{PAM}$ signal carrying the information symbols $X_{n}$ is
$$
x_{b}(t)=\sum\limits_{ n }^{  }X_{n}p(t-nT)
$$
But most channels are passband—we can only transmit our signal over a fixed frequency band centred around a carrier frequency $f_{c}.$

How do we convert the $\mathrm{PAM}$ signal to passband?

## Baseband to passband
The most natural thing is to modulate the amplitude of a high-frequency carrier with $x_{b},$
$$
\begin{align}
x(t)&=x_{b}(t)\cos(\omega_{c}t)
 \end{align}
$$
This is a digital analogue of DSB-SC modulation. 

> When the pulse signal is rectangular, this signal is sometimes known as Amplitude Shift Keying (ASK).

## Demodulation at the Rx
First we apply the standard DSB-SC demodulation scheme.
![[PAM-demod.png]]
This gives an expression in terms of the baseband noise $n_{b}$
$$
\begin{align}
y_{b}&=x_{b}+n_{b} \\
&=n_{b}+\sum\limits_{ n }^{  }X_{n}p(t-nT)
 \end{align}
$$
Then we apply standard $\mathrm{PAM}$ demodulation by passing $y_{b}$ through a matched filter and sampling at integer times.

![[passband-PAM-step-demod.png]]

## Quadrature amplitude modulation
As with analogue signals, DSB-SC uses double the [[bandwidth]] of the original signal—not very efficient! 

But in digital signals we don’t need to resort to SSB-SC! We can make the information symbols complex-valued!.

The baseband waveform is again
$$
x_{b}(t)=\sum\limits_{ k }X_{k}p(t-kT)
$$
where now $X_{k}\subset \mathbb{C}.$ So $x_{b}$ is now complex although we still need to transmit only a real signal.
$$
\begin{align}
x_{t}(t)&=\operatorname{Re}\left[ x_{b}(t)e^{ j\omega_{c} t} \right]  \\
&=\operatorname{Re}[x_{b}]\cos(\omega_{c}t)-\operatorname{Im}[x_{b}]\sin(\omega_{c}t) \\
&=\sum\limits_{ k }^{   }p(t-kT)|X_{k}|\cos(\omega_{c}t+\phi _{k})
 \end{align}
$$
where $|X_{k}|$ and $\phi_{k}$ denote the magnitude and phase of the complex symbol $X_{k}.$

Intuitively we can understand this as
- $\mathrm{QAM}$ having two carriers
	- $\cos$ carries $\operatorname{Re}[X_{k}]$
	- $\sin$ carries $\operatorname{Im}[X_{k}]$
- In $\mathrm{QAM}$ the information symbol modulated both the amplitude *and phase* of the carrier.

>Recall that in $\mathrm{PAM}$ that $\operatorname{Im}[X_{k}]=0$

### $\mathrm{QAM}$ properties
Just like $\mathrm{PAM},$ the [[bandwidth]] is $2W.$ However we are using it to transmit information more efficiently.
$$
\begin{align}
\mathrm{rate}&= \frac{1}{T}\ \pu{QAM symbols/s} \\
&= \frac{\log_{2}M}{T}\ \pu{bits/s}
 \end{align}
$$
>$\mathrm{QAM}$ is the modulation scheme used in 4G LTE.
### Common $\mathrm{QAM}$ constellations
Many common $\mathrm{QAM}$ constellations are Phase-Shift Keying ($\mathrm{PSK}$) and have constant $|X_{k}|.$
![[QAM-constellations.png]]
>In a constellation with $M$ symbols, each symbol corresponds to $\log_{2}M\ \pu{bits}$

The average energies of some of these are
![[QAM-av-energies.png]]

For all $\mathrm{PSK}$ constellations, the average symbol energy is $E_{s}=A^{2}.$

>Average energy per bit is $E_{b}=\frac{E_{s}}{\log_{2}M}$

The energy per symbol is important because it is proportional to the power requirement.

## Demodulating $\mathrm{QAM}$ 
In $\mathrm{PAM}$ we needed a product modulator and a low pass filter. In $\mathrm{QAM}$ we now need two product modulators, one for $\cos$ and one for $\sin$ (and we still need the low pass filter).

![[QAM-demod.png]]
After down-converting we have
$$
\begin{align}
y^{r}(t)&=n^{r}(t)+\sum\limits_{ k }^{  }X_{k}^{r}p(t-kT) \\
y^{i}(t)&=n^{i}(t)+\sum\limits_{ k }^{  }X_{k}^{i}p(t-kT)
\end{align}
$$
where superscripts $^{r}$ and $^{i}$ denote the real and imaginary parts respectively. Then we apply the same matched-filter demodulation as for $\mathrm{PAM}.$

![[QAM-matched-filter.png]]
Then the sampled outputs are
$$
\begin{align}
Y^{r}_{m}&=X_{m}^{r}+N^{r} \\
Y^{i}_{m}&=X_{m}^{i}+N^{i}
\end{align}
$$
We then have to look past the noise and decide the $X_{m}$ from the $Y_{m}.$ The optimal detection rule assuming equal probabilities of constellation symbols is the maximum-likelihood detector
$$
\hat{X}=\underset{x\in\mathbb{X}}{\arg\max}f(Y\mid x)
$$
where the conditional distribution of $Y=(Y^{r},Y^{i})$ given $x=(x^{r},x^{i})$ is
$$
f(Y\mid x)=\frac{1}{2\pi\sigma^{2}}\exp \left\{ - \frac{(Y^{r}-x^{r})^{2}+(Y^{i}-x^{i})^{2}}{2\sigma^{2}} \right\} 
$$
so the optimal detector is 
$$
\begin{align}
\hat{X}&=\underset{x\in\mathbb{X}}{\arg\min}\left\{ (Y^{r}-x^{r})^{2}+(Y^{i}-x^{i})^{2} \right\}  \\
&=\underset{x\in\mathbb{X}}{\arg\min}|Y-x|^{2}
 \end{align}
$$
This is just choosing the $x$ that is closest to the observed $Y.$ For example the decision regions for 8-$\mathrm{PSK}$ is
![[8-PSK-decision.png]]
The probability of error $P_{e}$ satisfies
- $P_{e}$ is a $\mathcal{Q}$-function depending on $\frac{d}{\sigma}$ where $d$ is the separation between adjacent constellation points
- $P_{e}$ decays exponentially with $\left( \frac{d}{\sigma} \right)^{2}$

If we increase the size of a constellation are constant average energy per symbol $E_{s}$:
- higher transmission rate (more information per symbol)
- lower $d$ to keep $E_{s}$ constant so $P_{e}$ increases (bad)!