We will study a digital modulation technique called Pulse Amplitude Modulation and analyse its performance over an Additive White Gaussian Noise channel.

This has two basic components:
- A constellation
- A pulse shape

## The symbol constellation
The set of values (real or complex) the bits (or bit sequences) are mapped to is called the constellation. A constellation with $N$ symbols represents $\log_{2}N$ bits.

## The pulse shape
The second component is a unit-energy *baseband* waveform denoted $p(t)$ called the pulse shape. The characteristic time of the pulse is called the symbol time.

A sequence of constellation symbols $X_{0}, X_{1},\dots,X_{n}$ is used to generate a baseband signal as a superposition of the pulses, 
$$
x(t)=\sum\limits_{ n }^{  }X_{n}p(t-nT)
$$
Hence we have the steps to achieve the following conversion:
$$
\dots011101010 \longrightarrow X_{0}, X_{1},\dots,X_{n}\longrightarrow x(t)
$$
## Transmission rate
Consider a signal modulated using a rectangular pulse shape such that the characteristic pulse time $T$ corresponds to the rectangular window length. Then the transmission rate is
$$
\mathrm{rate}=\pu{\frac{1}{T} symbols/s}=\pu{\frac{\log_{2}N}{T} bits/s}
$$
## Pulse shape choice
$p(t)$ is chosen to satisfy the following objectives:
- It should quickly rise and decay in time to avoid symbol overlap
- It should have a small [[bandwidth]] since the [[bandwidth]] of $x(t)$ is the same as that of $p(t)$
- The decoding of a noisy signal should be reliable and in the absence of noise the transmission should be lossless

## Orthonormality of pulse shifts
To achieve reliable decoding, the orthonormal shift property is imposed. Let $p_{n}=p(t-nT),$ then we impose
$$
\delta_{nm}=\left< p_{n}\mid p_{m} \right>
$$
where $\delta$ is the Kronecker delta.

This property is satisfied by e.g. the $\operatorname{rect}$ and $\operatorname{sinc}$ pulses. In the case of the $\operatorname{rect}$ function this requirement satisfied because there is no temporal overlap between symbol encodings.

## The trade-off between time decay and [[bandwidth]]
We stated above that we want a pulse with fast decay and small [[bandwidth]]. But these properties oppose each other!

Consider the $\operatorname{sinc}$ function—it is perfectly band-limited to $W=\frac{1}{2T}$ but decays slowly in time as $p\sim \frac{1}{|t|}.$

Conversely, the $\operatorname{rect}$ function is perfectly time-limited to the interval $[-\frac{T}{2}, \frac{T}{2})$ but decays slowly in frequency as $P \sim \frac{1}{|\omega|}$ with a main lobe [[bandwidth]] of $\frac{1}{T}.$

In practice, this trade-off is balanced by choosing the pulse shape to be a root-raised cosine in the frequency domain. 

![[root-raised-cos.png]]
This has a [[bandwidth]] slightly larger than $\frac{1}{2T}$ and decays in time as $|p|\sim \frac{1}{t^{2}}.$

## Matched-filter demodulation
Assume our modulated signal is transmitted over a baseband channel $y=x+n.$
![[baseband-noise.png]]
We will take advantage of the [[#Orthonormality of pulse shifts|orthonormal shift property]] to elegantly demodulate the noisy signal.

We pass the received signal $y$ through a matched filter with impulse response $h(t)=p(-t).$ Then the filter output is
$$
\begin{align}
r(t)&=y*h \\
&=x*h +y*h\\
&=\int_{-\infty}^{\infty} x(\tau)h(\tau-t) \, \mathrm{d}\tau +n*h \\
&=n*h+\sum_{n}X_{n}\int_{-\infty}^{\infty} p(\tau-nT)p(\tau-t) \, \mathrm{d}\tau \\
&=n*h+\sum_{n}X_{n}g(t-nT)
 \end{align}
$$
where $g$ is defined as
$$
g(t)=\int_{-\infty}^{\infty} p(u+t)p(u) \, \mathrm{d}u  
$$
If the output $r(t)$ is sampled at $t=mT$ then
$$
\begin{align}
r(mT)&=n*h\bigg|_{t=mT}+\sum_{n}X_{n}\delta_{nm} \\
Y_{m}&=N_{m}+X_{m}
 \end{align}
$$
which is a lossless reconstruction of the initial $X_{n}$ for $n=0.$

The noise $N_{m}$ can be modelled as independent and identically distributed samples of a Gaussian random variable with zero mean.

## Visualising the transmitted signal and filter output
The right panel shows the transmitted PAM signal $\sum_{k}X_{k}p(t-kT)$ and the left panel shows its individual components.

![[PAM-signal.png]]

The corresponding matched filter output is
![[matched-filter-output.png]]

## Detection for binary PAM
Consider a binary constellation
$$
X_{m}\in\{ -A,A \}
$$
This is also known as binary phase shift keying.

Observe that
$$
\begin{cases}
\begin{aligned}
Y&=A+N &\text{if }X&=A\\
Y&=-A+N &\text{if }X&=-A
\end{aligned}
 \end{cases}
$$
Hence the PDFs of the possible states is
$$
\begin{cases}
\begin{align}
f(Y\mid X=A)&\sim \mathcal{N}(A, \sigma^{2}) \\
f(Y\mid X=-A)&\sim \mathcal{N}(-A, \sigma^{2})
\end{align}
 \end{cases}
$$
Let $\hat{X}$ denote the decoded symbol. When the symbols $A$ and $-A$ are equally likely, the optimal detection rule is to simply choose the most likely symbol:
$$
\begin{cases}
\begin{aligned}
\hat{X}&=A &\text{if }f(Y\mid X=A)\geq f(Y\mid X-A)\\
\hat{X}&=-A &\text{if }f(Y\mid X=-A)\geq f(Y\mid X=A)
\end{aligned}
 \end{cases}
$$
This is a maximum-likelihood decoder, a type of maximum a posteriori (MAP) detection.

The detection rule can be written compactly in the general case as 
$$
\hat{X}=\arg \max_{x\in\mathbb{X}}f(Y\mid X=x)
$$
In the considered binary Gaussian case,
$$
\begin{aligned}
\hat{X}&=\arg\max_{x\in\{ A,-A \}} \frac{1}{\sqrt{ 2\pi\sigma^{2} }}\exp\left\{ -\frac{(Y-x)^{2}}{2\sigma^{2}} \right\} \\
&=\arg\min_{x\in\{ A,-A \}}(Y-x)^{2} \\
&=\begin{cases}
\begin{aligned}
\hat{X}&=A &\text{if }Y\geq 0\\
\hat{X}&=-A &\text{if }Y<0
\end{aligned}
 \end{cases}
 \end{aligned}
$$

This result generalises to the rule *“Choose the constellation symbol closest to the output Y”*
$$
\hat{X}=\arg\min_{x\in\mathbb{X}}\,(Y-x)^{2}
$$
## Decision regions
The detection rule partitions the space of $Y\subset \mathbb{R}$ into decision regions. For binary PAM,
![[binary-PAM-decision-region.png]]

## Probability of detection error
Again consider binary PAM. The detector makes an error when $X=A\cap Y<0$ or when $X=-A\cap Y>0.$

Then the probability of detection error is
$$
\begin{align}
P_{e}&=\operatorname{\mathbb{P}}[\hat{X}\neq X] \\
&=\operatorname{\mathbb{P}}[X=-A]\operatorname{\mathbb{P}}[\hat{X}=A\mid X=-A]+\operatorname{\mathbb{P}}[X=A]\operatorname{\mathbb{P}}[\hat{X}=-A\mid X=A] \\
&=\frac{1}{2}\operatorname{\mathbb{P}}[\hat{X}=A\mid X=-A]+\frac{1}{2}\operatorname{\mathbb{P}}[\hat{X}=-A\mid X=A] \\
&= \frac{1}{2}\operatorname{\mathbb{P}}[N>A]+\frac{1}{2}\operatorname{\mathbb{P}}[N<-A] \\
&=\operatorname{\mathbb{P}}\left[|N|>A\right]
 \end{align}
$$
Applying the symmetry of Gaussian noise gives
$$
P_{e}=\operatorname{\mathbb{P}}\left[ \frac{N}{\sigma}> \frac{A}{\sigma} \right]
$$
where the noise is scaled to be distributed according to the standard normal,
$$
\frac{N}{\sigma}\sim \mathcal{Z}=\mathcal{N}(0,1)
$$
Define a complement to the standard normal $\mathcal{Q}=1-\mathcal{Z},$
$$
\mathcal{Q}(x)=\int_{x}^{\infty} \frac{1}{\sqrt{ 2\pi }} e^{ -\frac{1}{2}u^{2} } \, \mathrm{d}u 
$$
Then the probability of detection error is
$$
P_{e}=\mathcal{Q}\left( \frac{A}{\sigma} \right)=\mathcal{Q}\left( \sqrt{ \frac{E_{s}}{\sigma^{2}} } \right)
$$
where $E_{s}=E_{b}$ is the average energy per symbol in the constellation. For an $M$-point constellation, the average energy per symbol is 
$$
E_{s}=E_{b}\log_{2}M
$$
We define the quantity $\frac{E_{b}}{\sigma^{2}}$ as the signal-to-noise ratio of the transmission scheme.

![[Pe-vs-snr-binary-PAM.png]]

## Error probability vs transmit power

tbc


## Power of $\mathrm{PAM}$ signal
tbc