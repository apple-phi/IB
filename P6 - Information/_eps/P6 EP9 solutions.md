## 1.
The first few multiples of $\frac{1}{16}$ are
$$
\begin{align}
&0,& 0.0625,\qquad& 0.125,&0.1875,\qquad&0.25,&0.3125,\qquad&0.375,&0.4375 \\
&0.5,&0.5625,\qquad&0.625,&0.6875,\qquad&0.75,&0.8125,\qquad&0.875,&0.9375
 \end{align}
$$
The first signal has values $[0, 0.2781, 0.5290, 0.7281, 0.8560, 0.9000]$ so the $\mathrm{DAC}$ output is $\mathbf{r}=[0,0.25,0.5,0.75,0.875, 0.875]$ which has mean squared error
$$
\frac{1}{6}\sum\limits_{ n=1 }^{ 6 }r_{n}^{2}=\pu{5.16E-4V}
$$
The second signal has tbc

## 2.
Consider the pulse $\operatorname{p}(t)=\frac{1}{\sqrt{ T }}\operatorname{sinc}\left( \frac{\pi}{T}t \right).$ With the given definition $\phi_{k}=\operatorname{p}(t-kT),$ by employing Parseval’s theorem,
$$
\begin{align}
\braket{ \phi_{\ell} \mid \phi_{m}}&= \frac{1}{2\pi}\braket{ \Phi_{\ell} \mid \Phi_{m} } \\
&=\frac{1}{2\pi} \int_{-\infty}^{\infty} \Phi_{\ell}\overline{ \Phi_{m}} \, \mathrm{d}\omega  \\
&= \frac{1}{2\pi}\int_{-\infty}^{\infty} e^{ j\omega T(m-\ell) }P(\omega)\overline{ P(\omega)} \, \mathrm{d}\omega
 \end{align}
$$
where $P(\omega)=\sqrt{ T }\operatorname{rect\left( \frac{T}{2\pi}\omega  \right)}$ so
$$
\begin{align}
\braket{ \phi_{\ell} \mid \phi_{m}}&= \frac{1}{2\pi}\int_{-\infty}^{\infty} T\operatorname{rect^{2}}\left( \frac{T}{2\pi}\omega \right)e^{ j\omega T(m-\ell) }\, \mathrm{d}\omega \\
&= \frac{1}{2\pi}\int_{-\frac{\pi}{T}}^{\frac{\pi}{T}} Te^{ j\omega T(m-\ell) } \, \mathrm{d}\omega \\
&= \delta_{m\ell}
 \end{align}
$$
## 3.
Choose the nearest symbol, so
$$
\hat{X}=\begin{cases}
\begin{matrix}
-3A \\
-A \\
A \\
3A
\end{matrix}\qquad\begin{align}
&\text{if }Y<-2A \\
&\text{if }-2A\leq Y<0 \\
&\text{if }0\leq Y<2A \\
&\text{if }Y\geq2A
\end{align}
\end{cases}
$$
The probability of error when $X=-3A$ is
$$
\begin{align}
\operatorname{\mathbb{P}}[\hat{X}\neq-3A\mid X=-3A]&=\operatorname{\mathbb{P}}[Y>-2A\mid X=-3A] \\
&=\operatorname{\mathbb{P}}[-3A+N>-2A\mid X=-3A] \\
&=\operatorname{\mathbb{P}}[N>A] \\
&=\operatorname{\mathbb{P}}\left[ \frac{N}{\sigma}> \frac{A}{\sigma} \right] \\
&=\mathcal{Q}\left( \frac{A}{\sigma} \right)
 \end{align}
$$
Similarly, when the transmitted signal is $-A$ the probability of error is $2\mathcal{Q}\left( \frac{A}{\sigma} \right)$ so the total probability of error given all symbols are equally likely is
$$
P_{e}=\frac{1}{4}\sum P=\frac{3}{2}\mathcal{Q}\left( \frac{A}{\sigma} \right)
$$
The average energy per symbol is
$$
\begin{align}
E_{s}&= \frac{1}{4}\left[ (-3A)^{2}+(-A)^{2}+A^{2}+(3A^{2}) \right]  \\
&=5A^{2}
 \end{align}
$$
which per bit given the $\log_{2}4=\pu{2bits}$ required is
$$
E_{b}=\frac{5}{2}A^{2}
$$
Hence the total probability of error can be written as
$$
P_{e}= \frac{3}{2}\mathcal{Q}\left( \sqrt{ \frac{2E_{b}}{5\sigma^{2}} } \right)
$$

## 4.
$\mathcal{C}_{2}$ must be a rotation of $\mathcal{C}_{1}$ so $\mathcal{C}_{2}=\sqrt{ 2 }\{ 1\pm j, -1\pm j \}.$ Given the sequence $[p_{3},p_{1},p_{4},p_{2}],$ under $\mathcal{C}_{1}$ the sequence of $x_{b}$ values is $[-1,1,j,-j]$ whereas under $\mathcal{C}_{2}$ its sequence is $\sqrt{ 2 }[-1-j,1+j,-1+j,1-j].$

See this linked section for [[Digital passband modulation#Demodulating $ mathrm{QAM}$|demodulating QAM]]. 

## 5.
Consider the Fourier transform $X_{b}(\omega)$ of $x_{b}(t).$ If $x_{b}$ is real then spectrum symmetry imposes $X_{b}(-\omega)=\overline{ X_{b}(\omega)}$ hence we require $|X_{b}|$ to be an even function. From its graph we can see this is not the case so $x_{b}$ must be complex.

By employing the conjugation property $\mathscr{F}\{\overline{ x(t)}\}=\overline{ X(-\omega)},$
$$
\begin{align}
x&=\operatorname{Re}\left\{ x_{b}e^{ j\omega_{c}t } \right\}  \\
&= \frac{x_{b}e^{ j\omega_{c}t }+\overline{ x_{b}e^{ j\omega_{c}t }}}{2} \\
X(f)&=\frac{1}{2}\left[ X_{b}(f-f_{c})+\overline{ X_{b}}(-f-f_{c}) \right] 
 \end{align}
$$
hence $X(-f)=\overline{ X(f)}$ as expected since $x(t)$ is real.


## 6.
The bit flips are distributed as $X\sim \mathcal{B}(5,\varepsilon)$ so
$$
P_{e}=\operatorname{\mathbb{P}}[X\geq 3]=\sum\limits_{ n=3 }^{ 5 }{5\choose n}\varepsilon ^{n}(1-\varepsilon)^{5-n}
$$
The rate of the code is $\frac{1}{n}=\frac{1}{5}.$

By applying Hamming parity we have the codeword $[1,1,0,0,0,1,1].$ When two bits are flipped the wrong codeword is found as $[1,0,1,0,0,1,0].$ This is because Hamming codes can only error correct a single bit.

The error probability of the Hamming code requires two or more flipped bits,
$$
P_{e}'=\sum\limits_{ n=2 }^{ 7 }{7\choose n}\varepsilon ^{n}(1-\varepsilon)^{7-n}
$$
tbc Hamming codes
## 7.
**FDMA** multiplexes the users in frequency. Each user is assigned a bandwidth $B_{u}=\frac{B}{K}$ and it is modulated to a carrier such that there are no overlaps among the spectrum of adjacent users. Each user transmits with power $P.$

**TDMA** multiplexes the users in the time domain. Each user is assigned a given time slot of duration $T_{u}=\frac{T_{f}}{K}$ , where $T_{f}$ is the duration of a frame, and each time it transmits, it uses the whole bandwidth $B$ with power $KP$ to keep an average power of $P.$

**CDMA** multiplexes the users assigning different signatures to different users. Each user transmits using the whole bandwidth $B$ over the whole duration of the frame $T_{f}$ with power $P.$ Signatures should be orthogonal to enable recovery of the transmitted data by each user.

If a user transmits at a rate
$$
R=\frac{1}{T}=\pu{200kbit/s}
$$
then the first sidelobe bandwidth is $B_{u}=\frac{4}{T}$ so the number of users possible is
$$
N=\frac{B}{B_{u}}=25
$$
To show orthogonality we need to show that $\braket{ c_{i} \mid  c_{j}}=0$ for all pairs of users.