## 1.
The Nyquist frequency is $\pu{ 4kHz }.$ At $\pu{ 3kHz }$ sampling there is overlap of $\pu{ 1kHz }$ and at $\pu{ 6kHz }$ sampling there are spectral gaps of $\pu{ 2kHz }.$

## 2.
The spectra are:
- $X(f)=\delta(\pm f+f_{s}+f_{0})$
- $X(f)=\delta(\pm f+f_{s}-f_{0})$
- $X(f)=\delta(\pm f+f_{0})$

When sampled at $f_{s},$ i.e. at intervals of $\frac{1}{f_{s}}$
$$
\begin{align}
x(t)&=a\cos\left(2\pi n \frac{f_{0}}{fs} \right) \quad\forall n\in\mathbb{Z}^{+} \\
X(f)&=a\delta\left( f\pm \frac{f_{0}}{f_{s}}n \right)
 \end{align}
$$
## 3.
By sifting theorem,
$$
\begin{align}
v(t)\delta(t-nT)&=\frac{\mathrm{d} }{\mathrm{d}t} \int  v(t)\delta(t-nT)\, \mathrm{d}t  \\
&=\frac{\mathrm{d} }{\mathrm{d}t} \left\{ v(nT)H(t-nT) \right\}  \\
&=v(nT)\delta(t-nT)
\end{align}
$$
The sampled signal is
$$
v_{s}=T\left\{ v(nT)\delta(t-nT) \right\}\quad\forall n\in\mathbb{Z}
$$
Consider the pulse-broadening circuit with time domain input $x$ and output $y.$ In the time domain, denote $\operatorname{\hat{P}}$ as the linear unitary shift operator such that $\operatorname{\hat{P}}f(x)=f(x-T)$
$$
\begin{align}
y&=\frac{1}{T}\int _{-\infty}^{t}(x-\operatorname{\hat{P}}x) \, \mathrm{d}t  \\
 \end{align}
$$
For the impulse response when $x=\delta(t),$
$$
\begin{align}
y&=\frac{1}{T}\int _{-\infty}^{t}(\delta-\operatorname{\hat{P}}\delta) \, \mathrm{d}t \\
&=\frac{1}{T}\left[ H-\operatorname{\hat{P}}H \right] _{-\infty}^{t} \\
&=\frac{1}{T}\left[ H(t)-H(t-T) \right]  \\
 \end{align}
$$

By linearity, the output signal $w_{s}$ is
$$
\begin{align}
w_{s}&=Tv(nT)\sum y(\delta(t-nT)) \\
&=v(nT)\sum\left[ H(t-nT)-H(t-(n+1)T) \right] 
 \end{align}
$$
This looks like a quantised version of $v.$ 

The transfer function of the circuit is
$$
G(\omega)=\frac{1+e^{j\omega T}}{j\omega T}
$$
Then the sampled spectrum is 
$$
W(\omega)=\frac{1+e^{j\omega T}}{j\omega T}\sum V\left( \omega-\frac{2\pi n}{T} \right)
$$
The ideal reconstruction filter can then be expressed in the spectral domain as a central rectangular pulse of height $\frac{j\omega T}{1+e^{j\omega T}}$ and width $\frac{2\pi}{T}.$

## 4.
The original signal has peaks at $\omega\in\{ 0,\pm\omega_{0},\pm \omega_{2} \}$ so the sampled signal has peaks at
$$
\begin{align}
\omega&\in\{ n\omega_{s},\pm\omega_{0}+n\omega_{s}, \pm 2\omega_{0}+n\omega_{s} \} \\
&\in \left\{ \frac{n\omega_{0}}{1+k}, \pm\frac{n+1+k}{1+k}\omega_{0}, \pm\frac{n+2+2k}{1+k}\omega_{0}\right\} 
 \end{align}
$$
With the applied low-pass filter, the surviving frequencies are
$$
\omega\in\left\{  0, \pm \frac{k}{1+k}\omega_{0}, \pm \frac{2k}{1+k}\omega_{0}  \right\}
$$
So the reconstructed signal is $x_{r}(t)=x\left( \frac{k}{1+k}t \right).$

## 5.
$$
\begin{align}
f_{m}&\overset{?}=\frac{T}{2\pi}\int_{-\frac{\pi}{T}}^{\frac{\pi}{T}} F_{s}(\omega)e^{jm\omega T} \, \mathrm{d}\omega  \\
&=\frac{T}{2\pi}\int_{-\frac{\pi}{T}}^{\frac{\pi}{T}} \left( \sum\limits_{ n=-\infty }^{ \infty }f_{n}e^{-jn\omega T} \right)e^{jm\omega T} \, \mathrm{d}\omega  \\
&=\sum\limits_{ n=-\infty }^{ \infty }f_{n}\left( \frac{T}{2\pi}\int_{-\frac{\pi}{T}}^{\frac{\pi}{T}} e^{ j\omega T(m-n) } \, \mathrm{d}\omega  \right)  \\
&=\sum\limits_{ n=-\infty }^{ \infty }f_{n}\delta _{mn} \\
&=f_{m}
 \end{align}
$$
## 6.
Applying the [[Discrete Fourier transform|discrete Fourier transform]],
$$
\begin{align}
F_{k}&= \sum\limits_{ n=0 }^{ N-1 }f(nT)e^{-j 2\pi n \frac{k}{N}} \\
&=e^{ 0 }+0+0+e^{ -j \frac{3}{2}\pi k } \\
&=[ 2,1+j,0,1-j ]_{k}
 \end{align}
$$
These values are a positive unit real translation of the 4th roots of unity. In terms of magnitude and phase they are
$$
\mathbf{F}= \begin{bmatrix}
2 \\
\sqrt{ 2 }\angle \frac{\pi}{4} \\
0 \\
\sqrt{ 2 }\angle -\frac{\pi}{4}
\end{bmatrix}
$$
Applying the inverse DFT,
$$
\begin{align}
f_{n}&= \frac{1}{N}\sum\limits_{ k=0 }^{ N-1 }F_{k}e^{ j 2\pi n \frac{k}{N} } \\
&=\frac{1}{4}\sum\limits_{ k=0 }^{ N-1 }F_{k}e^{ j \frac{\pi}{2} n k } \\
&= \frac{1}{4}\mathbf{F}\cdot \left[ 1,j^{n},(-1)^{n},(-j)^{n} \right]  \\
 \\
\mathbf{f}&=\frac{1}{4}\begin{bmatrix}
1 &1 &1 &1 \\
1&j&-1&-j \\
1&-1&1&-1 \\
1&-j&-1&j
\end{bmatrix}\begin{bmatrix}
2 \\
1+j \\
0 \\
1-j
\end{bmatrix}\\
&=\frac{1}{4}\begin{bmatrix}
4 \\
0 \\
0 \\
4
\end{bmatrix} \\
&=[1,0,0,1]^{\dagger}
 \end{align}
$$
Considering the reversed, conjugated DFT,
$$
\begin{align}
F^{*}_{-k}&= \sum\limits_{ n=0 }^{ N-1 }f(nT)\overline{e^{-j 2\pi n \frac{(-k)}{N}} } \\
&=\sum\limits_{ n=0 }^{ N-1 }f(nT)e^{-j 2\pi n \frac{k}{N}}  \\
&=F_{k}
 \end{align}
$$
Considering the shifted DFT $F_{k+N},$
$$
\begin{align}
F_{k+N}&= \sum\limits_{ n=0 }^{ N-1 }f(nT)e^{-j 2\pi n \frac{k+N}{N}}  \\
&= \sum\limits_{ n=0 }^{ N-1 }f(nT)e^{-j 2\pi n \frac{k}{N}} e^{ -j2\pi n} \\
&= \sum\limits_{ n=0 }^{ N-1 }f(nT)e^{-j 2\pi n \frac{k}{N}}  \\
&=F_{k}
 \end{align}
$$
## 7.
For a sampling frequency $f=\frac{1}{T}$ and with component $k$ corresponding to a frequency $f_{k}=\frac{k}{N}f_{s},$
$$
\begin{align}
F_{k}&= \sum\limits_{ n=0 }^{ N-1 }e^{-nT}e^{-j 2\pi n \frac{k}{N}}  \\
&= \frac{1-\left( e^{ -T-j 2\pi \frac{k}{N} } \right)^{N}}{1-e^{ -T-j 2\pi \frac{k}{N} }} \\
&=\frac{1- e^{ -NT}}{1-e^{ -T-j 2\pi \frac{k}{N} }} 
 \end{align}
$$