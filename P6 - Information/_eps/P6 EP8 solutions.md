## 1.
Using the non-unitary [[Fourier transform]] $F=\left< f\mid e^{ j\omega t } \right>,$
### Convolution
$$
\begin{align}
\mathscr{F}\left\{ f*g \right\} &=\int_{-\infty}^{\infty} e^{ -j\omega t }\int_{-\infty}^{\infty} f(\tau)g(t-\tau) \, \mathrm{d}\tau  \, \mathrm{d}t \\
&=\int_{-\infty}^{\infty} f(\tau)\int_{-\infty}^{\infty} g(t-\tau)e^{ -j\omega t } \, \mathrm{d}t  \, \mathrm{d}\tau \\
&=  \int_{-\infty}^{\infty} f(\tau)\int_{-\infty}^{\infty} g(u)e^{ -j\omega(u+\tau) }\,\mathrm{d}u\,\mathrm{d}\tau \\
&=\int_{-\infty}^{\infty} f(\tau)e^{ -j\omega \tau } \, \mathrm{d}\tau \int_{-\infty}^{\infty} g(u)e^{ -j\omega u } \, \mathrm{d}u \\
&=F(\omega)G(\omega)
\end{align}
$$
### Modulation
$$
\begin{align}
\mathscr{F}\left\{ f\cos(\omega_{0}t) \right\} &= \int_{-\infty}^{\infty} f\cos(\omega_{0}t)e^{ -j\omega t } \, \mathrm{d}t \\
&= \int_{-\infty}^{\infty} f(t)\left( \frac{e^{ j\omega_{0}t }+e^{ -j\omega_{0}t }}{2} \right)e^{ -j\omega t } \, \mathrm{d}t \\
&=\frac{1}{2}\left[ \int_{-\infty}^{\infty}  \,fe^{ -j(\omega+\omega_{0})t }  \mathrm{d}\omega+\int_{-\infty}^{\infty}  \,fe^{ -j(\omega-\omega_{0})t }  \mathrm{d}\omega  \right]  \\
&=\frac{1}{2}\left[ F(\omega-\omega_{0})+F(\omega+\omega_{0}) \right] 
\end{align}
$$
### Parseval’s Theorem

By definition, using bra-ket notation,
$$
\ket{f}=\frac{1}{2\pi}\int \ket{e^{ -j\omega t }}\braket{ e^{-j\omega t} \mid F  } \, \mathrm{d}\omega
$$
Hence,
$$
\begin{align}
\int |f|^{2} \, \mathrm{d}t&= \braket{ f \mid f }  \\
&=\frac{1}{2\pi}\int \braket{ f \mid e^{ -j\omega t } } \braket{ e^{-j\omega t} \mid F  } \, \mathrm{d}\omega \\
&=\frac{1}{2\pi}\int \frac{1}{2\pi}\int \braket{ F \mid e^{ -j\Omega t }  }\bra{e^{ -j\Omega t }}   \, \mathrm{d}\Omega\, \ket{ e^{ -j\omega t } } \braket{ e^{-j\omega t} \mid F  } \, \mathrm{d}\omega  \\
&=\frac{1}{2\pi}\int \bra{F} \int\ket{e^{ -j\Omega t }}\delta(\omega-\Omega)   \, \mathrm{d}\Omega   \braket{e^{ -j\omega t }\mid F} \, \mathrm{d}\omega  \\
&=\frac{1}{2\pi}\int \braket{ F\mid e^{ -j\omega t }  }\braket{ e^{ -j\omega t } \mid F }   \, \mathrm{d}\omega \\
&= \frac{1}{2\pi} \braket{ F \mid F  } 
 \end{align}
$$

## 2.
AM-modulation takes up twice the bandwidth of the original signal, thus the waveband is comprised of
$$
B=2Wn+G(n-1)
$$
where $W$ is the signal bandwidth and $G$ is the required sideband gap. Substituting the required parameters gives 
$$
\lfloor n \rfloor =91
$$
Using a single sideband instead means $2W\mapsto W$ so we get
$$
\lfloor n \rfloor =143
$$
which is 52 extra transmissions.

## 3.
Recall that
$$
s= (a_{0}+x)\cos(\omega_{c}t)
$$
When unmodulated, i.e., $x(t)=0,$
$$
s_{0}=a_{0}\cos(\omega_{c}t)
$$
Hence the amplitude and frequency of the given carrier is $\pu{10V}$ and $\pu{9MHz}$ respectively.

The modulation index of the given signal is
$$
\begin{align}
m&= \frac{\max|x|}{a_{0}} \\
&=0.3
\end{align}
$$
The resultant waveform looks like a carrier envelope around a much higher frequency signal wave.

## 4.
$$
\begin{align}
s&=x\cos(\omega_{c}t) \\
v&=x\cos(\omega_{c}t)\cos(\omega_{c}t+\phi) \\
&=x\cos(\omega_{c}t)\left[ \cos(\omega_{c}t)\cos \phi-\sin(\omega_{c}t)\sin \phi \right]  \\
&=x\cos ^{2}(\omega_{c}t)\cos \phi-x\cos(\omega_{c}t)\sin(\omega_{c}t)\sin \phi \\
&=\frac{1+\cos(2\omega_{c}t)}{2}x\cos \phi- \frac{\sin(2\omega_{c}t)}{2}x\sin \phi \\
&\approx \frac{1}{2}x\cos \phi \\
\hat{x}&= x\cos \phi
 \end{align}
$$
When $\phi=\frac{\pi}{2}$ then $\hat{x}=0.$ We cannot compensate for $\phi$ using this rudimentary receiver. 

## 5.
 $$
\begin{align}
y&=(2+bc_{x}+c_{c})^{2} \\
&=4+b^{2}c^{2}_{x}+c^{2}_{c}+4bc_{x}+4c_{c}+2bc_{x}c_{c} \\
f&=4c_{c}+2bc_{x}c_{c} \\
&=(4+2b\cos(2\pi f_{x}t))\cos(2\pi f_{c}t)
\end{align}
$$
This is an $\mathrm{AM}$ signal with a modulation index of
$$
m=\frac{b}{2}
$$
## 6.
$$
\begin{align}
\operatorname{Re}\left\{ A_{c}e^{ j\beta \sin(\omega_{x}t)}e^{ j \omega_{c}t }  \right\} &=A_{c}\operatorname{Re}\left\{ e^{ j(\beta \sin(\omega_{x}t)+\omega_{c}t) } \right\}  \\
&=A_{c}\cos(2\pi f_{c}t+\beta \sin(2\pi f_{x}t)) \\
&=s_{\mathrm{FM}}(t)
 \end{align}
$$
By definition, $\bar{s}$  periodic in $f_{x}.$ The Fourier coefficient of $\bar{s}$ are
$$
\begin{align}
c_{n}&=\frac{1}{2\pi}\braket{ \bar{s} \mid e^{ jn\omega_{x}t }  }^{T}_{-T} \\
&=\frac{1}{2\pi}\int_{-T}^{T} A_{c}e^{ j\beta \sin(\omega_{x}t)}e^{ -jn\omega_{x}t } \, \mathrm{d}t  \\
&=\frac{A_{c}}{2\pi}\int_{-\pi}^{\pi} e^{ j(\beta \sin u-nu ) } \, \mathrm{d}u  \\
&=A_{c}J_{n}(\beta)
 \end{align}
$$
Assume that $J_{n}(\beta)$ is not purely real, then
$$
\begin{align}
0&\neq \operatorname{Im}\{ J_{n}(b) \} \\
&=\frac{A_{c}}{2\pi}\int_{-\pi}^{\pi} \operatorname{Im}\{ e^{ j(\beta \sin u-nu ) } \} \, \mathrm{d}u \\
&=\frac{A_{c}}{2\pi}\int_{-\pi}^{\pi} \sin(\overbrace{ \beta \sin u-nu}^{ \mathrm{odd} })\, \mathrm{d}u \\
&=0
 \end{align}
$$
This is a contradiction of the assumption, therefore $J_{n}(\beta)$ is entirely real and can therefore be written as
$$
J_{n}(\beta)=\frac{A_{c}}{2\pi}\int_{-\pi}^{\pi} \cos({ \beta \sin u-nu}^{  })\, \mathrm{d}u 
$$
From the first part of the question,
$$
\begin{align}
s_{\mathrm{FM}}(t)&=\operatorname{Re}\left\{ e^{ j\omega_{c}t }\sum\limits_{ n=-\infty }^{ \infty }A_{c}J_{n}(\beta)e^{ jn\omega_{x}t } \right\}  \\
&=A_{c}\sum\limits_{ n=-\infty }^{ \infty }J_{n}(\beta)\operatorname{Re}\left\{ e^{ j(\omega_{c}+n\omega_{x})t } \right\}  \\
&=A_{c}\sum\limits_{ n=-\infty }^{ \infty }J_{n}(\beta)\cos(2\pi t(f_{c}+nf_{x}))
 \end{align}
$$
Taking the Fourier transform gives
$$
S_{\mathrm{FM}}(f)=\frac{A_{c}}{2}\sum\limits_{ n=-\infty }^{ \infty }J_{n}(\beta)\left[ \delta(f-f_{c}-nf_{x})+\delta(f+f_{c}+nf_{x}) \right] 
$$
## 7.

Recall that the modulation index $\beta$ is
$$
\beta=\frac{\Delta f}{f_{x}}=\frac{k_{f}a_{x}}{f_{x}}
$$
and that Carson’s rule gives
$$
B\approx 2(f_{x}+\Delta f)
$$
Then the modulation indices for each case are
$$
\beta=10,1,7.5
$$
while the required bandwidths are
$$
B=\pu{110kHz},\pu{40kHz},\pu{ 240kHz }
$$
## 8.
$$
\begin{align}
\pu{200Hz} \\
\pu{6800Hz} \\
\pu{32kHz} \\
\pu{11MHz}
\end{align}
$$
Adding an extra 20% gives
$$
\begin{align}
\pu{240Hz} \\
\pu{8160Hz} \\
\pu{38.4kHz }\\
\pu{13.2MHz}
\end{align}
$$
The bit rate is given by $\mathrm{rate}=fN,$ so
$$
\begin{align}
\pu{2880bit/s} \\
\pu{81600bit/s} \\
\pu{614.4kbit/s} \\
\pu{105.6Mbit/s}
\end{align}
$$
## 9.
In an ideal quantizer with $N$ levels, the step size $h$ is
$$
h= \frac{\operatorname{range}V}{2^{N}}
$$
while the mean square quantisation noise is given by
$$
\begin{align}
V^{2}_{n,\mathrm{rms}}&=\frac{1}{h}\int_{-\frac{h}{2}}^{\frac{h}{2}} x^{2} \, \mathrm{d}x  \\
V_{n,\mathrm{rms}}&=\frac{h}{\sqrt{ 12 }}
 \end{align}
$$
Which for (a) is $\pu{ 11.3mV }$ and for (b) is $\pu{ 1.41mV }.$

Treating the input signals as sinusoids gives
$$
V_\mathrm{s,rms}=\frac{V_{\mathrm{peak}}}{\sqrt{ 2 }}
$$
so we have
$$
\begin{align}
\mathrm{snr}_{a}&=20\log_{10} \frac{V_\mathrm{s,rms}}{V_{\mathrm{noise}}}=\pu{49.9dB} \\
\mathrm{snr}_{b}&=20\log_{10} \frac{V_\mathrm{s,rms}}{V_{\mathrm{noise}}}=\pu{ 74.0dB }
 \end{align}
$$
Assuming the signals have the peak value at $2\sqrt{ 2 }$ times the $\mathrm{RMS}$ value gives
$$
\begin{align}
\mathrm{snr}_{a}&=20\log_{10} \frac{V_\mathrm{s,rms}}{V_{\mathrm{noise}}}=\pu{43.9dB} \\
\mathrm{snr}_{b}&=20\log_{10} \frac{V_\mathrm{s,rms}}{V_{\mathrm{noise}}}=\pu{ 68.0dB }
 \end{align}
$$
For square waves, we cannot model noise the same wave because the noise is no longer normally distributed (it is square-distributed).