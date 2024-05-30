## Supervision questions
Please see question 5.
## 1.
### (a)
From first principles, with $\omega_{n}= \frac{2\pi n}{T}$
$$
\begin{align}
c_{n} & = \frac{\left< x\mid e^{jw_{n}t} \right> }{\left< e^{j\omega_{n}t}\mid e^{j\omega_{n}t} \right>  } \\
 & = \frac{1}{T}\int_{0}^{T}e^{-t}e^{-j\omega_{n}t}  \, \mathrm{d}x  \\
 & = \frac{1}{T}\left[ -\frac{e^{-(1+j\omega_{n})t}}{1+j\omega_{n}} \right] _{0}^{T} \\
 & = \frac{1}{T}\left[ \frac{1}{1+j\omega_{n}}- \frac{e^{-T-2\pi nj}}{1+j\omega_{n}} \right]  \\
 & = \frac{1-e^{-T}}{T+j 2\pi n} \\
 \\
\Rightarrow\quad x & =\sum\limits_{ n=-\infty }^{ \infty }\frac{1-e^{-T}}{T+j 2\pi n} e^{j \frac{2n\pi}{T}t}
\end{align}
$$
### (b)
Avoiding integration by parts, with $\omega_{n}=\frac{n\pi}{T}$,
$$
\begin{align}
c_{n} & = \frac{\left< x\mid e^{jw_{n}t} \right> }{\left< e^{j\omega_{n}t}\mid e^{j\omega_{n}t} \right>  }  \\
 & = \frac{1}{2T}\int _{-T}^{T} \frac{t}{T}e^{-j\omega_{n}t} \, \mathrm{d}t \\
 & = \frac{1}{2T^{2}}\int _{-T}^{T}\frac{\partial (e^{-j\omega_{n}t}) }{\partial (-j\omega_{n})} \, \mathrm{d}t  \\
 & = \frac{1}{2T^{2}}\frac{\mathrm{d} }{\mathrm{d}(-j\omega_{n})} \left[ \frac{e^{-j\omega_{n}t}}{-j\omega_{n}} \right] _{t=-T}^{t=+T} \\
 & = \frac{1}{2T^{2}}\frac{\mathrm{d} }{\mathrm{d}(-j\omega_{n})}\left\{ \frac{2\sinh(-j\omega_{n}T)}{-j\omega_{n}} \right\}  \\
 & =\frac{-j\omega_{n}T\cosh(-j\omega_{n}T)-\sinh(-j\omega_{n}T)}{-T^{2}\omega_{n}^{2}} \\
 & = \frac{j\omega_{n}T\cos(\omega_{n}T)-j\sin(\omega_{n}T)}{T^{2}\omega_{n}^{2}} \\
 & = \frac{j\cos (\pi n)}{T\omega_{n}} \\
 & = \frac{j(-1)^{n}}{\pi n} \\
 \\
\Rightarrow\quad x & = \frac{j}{\pi}\sum\limits_{ n=-\infty }^{ \infty } \frac{(-1)^{n}}{n}e^{j \frac{n\pi}{T}t}
\end{align}
$$
### (c)
With $\omega_{n}=\frac{2\pi n}{T}$,
$$
\begin{align}
c_{n} & = \frac{\left< x\mid e^{j\omega_{n}t} \right> }{\left< e^{j\omega_{n}t}\mid e^{j\omega_{n}t} \right> } \\
 & = \frac{1}{T}\int _{-\frac{T}{2}}^{{+\frac{T}{2}}}xe^{-j\omega_{n}t} \, \mathrm{d}t \\
 & = \frac{1}{T}\int _{-\frac{T}{2}}^{{+\frac{T}{2}}}e^{-j\omega_{n}t} \, \mathrm{d}t +  \frac{1}{T}\int _{-\frac{T}{4}}^{{+\frac{T}{4}}}e^{-j\omega_{n}t} \, \mathrm{d}t \\
 & = \frac{j}{T\omega_{n}}\left[ e^{-j\pi n} - e^{j\pi n}+e^{-j \frac{\pi n}{2}} - e^{j \frac{\pi n}{2}}\right]  \\
&=  \frac{\sin \pi n+\sin \frac{\pi n}{2}}{\pi n}
 \end{align}
$$

### (d)
Once again I decide to avoid integration by parts. With $\omega_{n}=\frac{2\pi n}{T}$
$$
\begin{aligned}
a_{n}&=\frac{\left< x\mid \cos(\omega_{n}t) \right> }{\left< \cos(\omega_{n}t)\mid \cos(\omega_{n}t) \right> }  \\
&= \frac{1}{T}\int _{-\frac{T}{2}}^{{+\frac{T}{2}}}x\cos(\omega_{n}t) \, \mathrm{d}t \\
&= \frac{2}{T}\int _{0}^{\frac{T}{2}}x\cos(\omega_{n}t) \, \mathrm{d}t  \\
&= \frac{6}{T^{2}}\int _{0}^{\frac{T}{3}}t\cos(\omega_{n}t) \, \mathrm{d}t +\frac{2}{T}\int _{\frac{T}{3}}^{\frac{T}{2}}\cos(\omega_{n}t) \, \mathrm{d}t \\
&= \frac{6}{T^{2}}\int _{0}^{\frac{T}{3}}\frac{\partial }{\partial \omega_{n}} \sin(\omega_{n}t) \, \mathrm{d}t  + \frac{2}{T}[\sin(\omega_{n}t)]_{\frac{T}{3}}^\frac{T}{2} \\
&= \frac{6}{T^{2}}\frac{\mathrm{d} }{\mathrm{d}\omega_{n}} \left[ -\frac{\cos(\omega_{n}t)}{\omega_{n}} \right]_{0}^{\frac{T}{3}} + \frac{\sin(\pi n)-\sin\left( \frac{2}{3}\pi n \right)}{\pi n} \\
&=\frac{6}{T^{2}} \frac{\mathrm{d} }{\mathrm{d}\omega_{n}} \left[ \frac{1-\cos\left( \frac{\omega_{n}T}{3} \right)}{\omega_{n}} \right] + \frac{\sin(\pi n)-\sin\left( \frac{2}{3}\pi n \right)}{\pi n}  \\
&= \frac{6}{T^{2}\omega_{n}^{2}} \left[ \frac{T\omega_{n}}{3}\sin\left( \frac{2}{3}\pi n \right)+\cos\left( \frac{2}{3}\pi n \right) -1\right] + \frac{\sin(\pi n)-\sin\left( \frac{2}{3}\pi n \right)}{\pi n} \\
&= \frac{3}{2\pi^{2}n^{2}}\left[ \cos\left( \frac{2}{3}\pi n \right)-1 \right] + \frac{\sin(\pi n)}{\pi n}
\\ \\
\Rightarrow\quad c_{n}&= \frac{a_{n}}{2} \\
 \\
\Rightarrow\quad x&= \sum\limits_{ n=-\infty }^{ \infty }e^{j \frac{{2}\pi n}{T}t}\left\{ \frac{3}{2\pi^{2}n^{2}}\left[ \cos\left( \frac{2}{3}\pi n \right)-1 \right] + \frac{\sin(\pi n)}{\pi n} \right\} 
\end{aligned}
$$

## 2.
$$
\begin{align}
c_{n} & = \frac{\left< x\mid e^{j\omega_{n}t} \right> }{\left< e^{j\omega_{n}t}\mid e^{j\omega_{n}t} \right> } \\
 & = \frac{1}{T}\int _{-\frac{T}{2}}^{{+\frac{T}{2}}}\delta(t)e^{-j\omega_{n}t} \, \mathrm{d}t \\
 & = \frac{1}{T} \\
 \\
\Rightarrow\quad x&=\sum\limits_{ n=-\infty }^{ \infty } \frac{1}{T}e^{-j\omega_{n}t}
\end{align}
$$
## 3.
$$
\begin{align}
c_{n} & = \frac{\left< x\mid e^{j\omega_{n}t} \right> }{\left< e^{j\omega_{n}t}\mid e^{j\omega_{n}t} \right> } \\
 & = \frac{1}{T}\int _{0}^{T}E\exp\left( -\frac{5+j2\pi n}{T}t \right)\, \mathrm{d}t \\
 & = \frac{E}{5+j2\pi n}\left[ -\exp\left( -\frac{5+j2\pi n}{T}t \right)\, \right] _{0}^{T} \\
&= \frac{ 1-e^{-5}}{5+j2\pi n}E \\
 \\
c_{0}&= \frac{ 1-e^{-5}}{5}E  \\
\sqrt{ a_{1}^{2}+b_{1}^{2} }=2|c_{1}|&= \frac{ 2(1-e^{-5})}{\sqrt{ 25+4\pi^{2} }}E 
 \end{align}
$$
Considering current in the RC circuit,
$$
\begin{align}
\frac{v_{i}-v_{o}}{R} & =C\frac{\mathrm{d} v_{o}}{\mathrm{d}t} \\
V_{i}-V_{0}&=RCj\omega V_{o} \\
V_{0}&= \frac{V_{i}}{1+j\omega RC} \\
 \end{align}
$$
For a DC signal with amplitude $V_{i}= \frac{1-e^{-5}}{5}E$ and frequency $\omega=0$
$$
V_{o} = V_{i}
$$
For a sinusoidal signal of amplitude $V_{i}=\frac{ 2(1-e^{-5})}{\sqrt{ 25+4\pi^{2} }}E$ and frequency $\frac{2\pi}{RC}$
$$
\begin{align}
V_{o}&=\frac{\frac{ 2(1-e^{-5})}{\sqrt{ 25+4\pi^{2} }}E}{1+j 2\pi} \\
 \\
\Rightarrow\quad |V_{o}| & = \frac{ 2(1-e^{-5})}{\sqrt{ 25+4\pi^{2} }\sqrt{ 1+4\pi^{2} }}E \\
&\approx0.0389E
 \end{align}
$$

## 4.

### (a)
$$
\begin{align}
\mathscr{F}\{f(t-t_{0})\}  & = \int _{-\infty}^{+\infty} f(t-t_{0})e^{-j\omega t}\, \mathrm{d}t \\
 & = \int _{-\infty}^{+\infty} f(u)e^{-j\omega u}e^{-jwt_{0}}\, \mathrm{d}u \\
&=e^{-j\omega t_{0}}F
\end{align}
$$
### (b)
$$
\begin{align}
\mathscr{F}^{-1}\left\{ \frac{\mathrm{d} F}{\mathrm{d}\omega}  \right\} &= \frac{1}{2\pi}\int _{-\infty}^{+\infty}  \frac{\mathrm{d} F}{\mathrm{d}\omega} e^{j\omega t}\, \mathrm{d}\omega  \\
&=\frac{1}{2\pi}\int_{-\infty}^{\infty}e^{j\omega t}\int_{-\infty}^{\infty} \frac{\partial}{\partial\omega}(fe^{-j\omega t}) \, \mathrm{d}t  \, \mathrm{d}\omega \\
&=\frac{1}{2\pi}\int_{-\infty}^{\infty} (-jtF)e^{j\omega t} \, \mathrm{d}\omega \\
&= -jt\mathscr{F}^{-1}\{F\} \\
&= -jtf
 \end{align}
$$
### (c)
The trick is to recall that $\delta(x)= \mathscr{F}^{-1}\{1\}$
$$
\begin{align}
\frac{1}{2\pi}\int_{-\infty}^{\infty} |F|^{2} \, \mathrm{d}\omega &= \frac{1}{2\pi}\int_{-\infty}^{\infty}FF^{*} \mathrm{d}\omega \\
&=\frac{1}{2\pi}\int_{-\infty}^{\infty} \left( \int_{-\infty}^{\infty} f(t)e^{j\omega t} \, \mathrm{d}t \right)  \left( \int_{-\infty}^{\infty} f^{*}(\tau)e^{-j\omega \tau} \, \mathrm{d}\tau \right) \, \mathrm{d}\omega \\

&= \int_{-\infty}^{\infty}\int_{-\infty}^{\infty}f(t)f^{*}(\tau)\left( \frac{1}{2\pi}\int_{-\infty}^{\infty}e^{j\omega(t-\tau)}\,\mathrm{d}\omega \right) \mathrm{d}t\,\mathrm{d}\tau \\
&= \int_{-\infty}^{\infty}\int_{-\infty}^{\infty}f(t)f^{*}(\tau)\delta(t-\tau)\,\mathrm{d}\tau\,\mathrm{d} t \\
&= \int_{-\infty}^{\infty} f(t)f^{*}(t) \, \mathrm{d}t  \\
&= \int_{-\infty}^{\infty}|f|^{2} \, \mathrm{d}t 
 \end{align}
$$
This approach can be extended to general $\left< f(t)\mid g^{*}(t)  \right>$ by substituting $F^{*}=G^{*}$

### (d)
$$
\begin{align}
\mathscr{F}^{-1}\{f(\omega)\} &= \frac{1}{2\pi}\int_{-\infty}^{\infty} f\left( \omega\right)e^{-j\omega (-t)} \, \mathrm{d}\omega \\
&=\frac{1}{2\pi}F(-t)
 \end{align}
$$
## 5.
Let $u=\frac{t}{T}$ then
$$
\begin{align}
X(\omega)&=\left< x\mid e^{j\omega t} \right>  \\
&= \int _{-\frac{T}{4}}^{\frac{T}{4}}\cos\left( \frac{2\pi t}{T} \right)e^{-j\omega t}  \, \mathrm{d}t \\
&=\frac{1}{2}\int ^{\frac{1}{4}}_{-\frac{1}{4}} (e^{j2\pi u}+e^{-j2\pi u})e^{-j\omega Tu}\, \mathrm{d}u \\
&= \frac{1}{2}\left[ \left( \frac{e^{j2\pi u}}{j(2\pi-\omega T)}-\frac{e^{-j2\pi u}}{j(2\pi+\omega T)} \right)e^{-j\omega Tu} \right] ^{\frac{1}{4}}_{-\frac{1}{4}} \\
&=\frac{1}{2j}\left[ \frac{2\pi \left( e^{j2\pi u}-e^{-j 2\pi u} \right)+\omega T\cancel{(e^{j 2\pi u}+e^{-j 2\pi u})} }{4\pi^{2}-\omega^{2}T^{2}}e^{-j\omega Tu} \right]  ^{\frac{1}{4}}_{-\frac{1}{4}} \\
&= \frac{2\pi}{4\pi^{2}-\omega^{2}T^{2}} \left[ \sin(2\pi u)e^{-j\omega Tu} \right] ^{\frac{1}{4}}_{-\frac{1}{4}} \\
&=\frac{2\pi}{4\pi^{2}-\omega^{2}T^{2}}\left( e^{-j \frac{\omega T}{4}}+e^{j \frac{\omega T}{4}} \right) \\
&= \frac{4\pi \cos\left( \frac{\omega T}{4} \right)}{4\pi^{2}-\omega^{2}T^{2}}
\end{align}
$$
By linearity, the Fourier transform of the triple half-cosine pulse is
$$
\begin{align}
Y(\omega)&=\mathscr{F}\left\{ x(t)+x\left( t+\frac{T}{2} \right)+x\left( t-\frac{T}{2} \right) \right\} \\
&=X(\omega)\left(1+e^{j\frac{\omega T}{2}}+e^{-j\frac{\omega T}{2}}\right) \\
&=  \frac{4\pi }{4\pi^{2}-\omega^{2}T^{2}}\cos\left( \frac{\omega T}{4} \right)\left( 1+2\cos\left( \frac{\omega T}{2} \right) \right)
 \end{align}
$$
Similarly, for the sine pulse,
$$
\begin{align}
Z(\omega)&=x\left( t-\frac{T}{4} \right) - x\left( t+\frac{T}{4} \right) \\
&=X(\omega)\left( e^{-j \frac{\omega T}{4}}-e^{j \frac{\omega T}{4}} \right)  \\
&=-\frac{8\pi j }{4\pi^{2}-\omega^{2}T^{2}}\cos\left( \frac{\omega T}{4} \right)\sin\left( \frac{\omega T}{4} \right) \\
&=-\frac{4\pi j \sin\left( \frac{\omega T}{2} \right)}{4\pi^{2}-\omega^{2}T^{2}}
 \end{align}
$$

### Question for supervision
The cribs do this for the triple half-cosine pulse, which I don’t understand,
![[P6EPQ5crib.png]]
When I graphed this in Desmos, it didn’t show equality…

## 6.
$$
\begin{align}
F(\omega)&=\left< f\mid e^{j\omega t} \right>  \\
&=\int_{-\frac{T}{2}}^{\frac{T}{2}}Ve^{j\omega t}  \, \mathrm{d}t  \\
&= \frac{V}{j\omega}\left[ e^{j\omega t} \right] _{-\frac{T}{2}}^{ \frac{T}{2}} \\
&= \frac{2v}{\omega}\sin\left( \frac{\omega T}{2} \right) \\
&= vT\operatorname{sinc}\left( \frac{\omega T}{2} \right)
\end{align}
$$
Then, by linearity,
$$
\begin{align}
G(\omega)&= \mathscr{F}\left\{ f(t)-\frac{1}{2}f\left( 2t+\frac{3T}{2} \right)-\frac{1}{2}f\left( 2t-\frac{3T}{2} \right) \right\} \\
&= F(\omega)- \frac{1}{2}F\left( \frac{\omega}{2} \right)\cos\left( \frac{3T}{4} \right) \\
&=vT\left[ \operatorname{sinc} \left( \frac{\omega T}{2} \right)-\frac{1}{2}\operatorname{sinc}\left( \frac{\omega T}{4} \right) \cos\left( \frac{3T}{4} \right)\right]
 \end{align}
$$
## 7.
With $x(t)=\sum\limits_{ n=-\infty }^{ \infty }x_{n}e^{-j\omega_{n} t}$ and $y^{*}(t)=\sum\limits_{ n=-\infty }^{ \infty }y^{*}_{n}e^{j\omega_{m} t}$ where $\omega_{k}=\frac{2\pi k}{T}$, we have
$$
\begin{align}
\frac{1}{T}\int _{0}^{T}x(t)y^{*}(t) \, \mathrm{d}t&= \frac{1}{T}\int _{0}^{T} \left( \sum\limits_{ n=-\infty }^{ \infty }x_{n}e^{-j\omega_{0}n t} \right)\left( \sum\limits_{ m=-\infty }^{ \infty }y^{*}_{m}e^{j\omega_{0}m t} \right) \, \mathrm{d}t  \\
&= \sum\limits_{ n=-\infty }^{ \infty }\sum\limits_{ m=-\infty }^{ \infty }x_{n}y^{*}_{m}\left( \frac{1}{T}\int _{0}^{T} e^{-j\omega_{0}(m-n)t}\, \mathrm{d}t \right) \\
&= \sum\limits_{ n=-\infty }^{ \infty }\sum\limits_{ m=-\infty }^{ \infty }x_{n}y^{*}_{m}\delta_{nm} \\
&= \sum\limits_{ n=-\infty }^{ \infty }x_{n}y^{*}_{n}
 \end{align}
$$
where $\delta _{ij}$ is the Kronecker delta. 

## 8.
The input energy is
$$
\begin{align}
E_{i}&=\left< X\mid X \right>  \\
&= \int _{-\infty}^{\infty} \,\frac{1}{1+\omega^{2}T_{1}^{2}} \mathrm{d}\omega \\
&= \left[ \frac{1}{T_{1}}\arctan(T_{1}\omega) \right]_{-\infty}^{\infty} \\
&= \frac{2}{T_{1}}
 \end{align}
$$
The output energy is
$$
\begin{align}
E_{o}&= \left< HX\mid HX \right>  \\
&= \int_{-\infty}^{\infty} \frac{1}{(1+\omega^{2}T^{2})(1+\omega^{2}T_{1}^{2})} \, \mathrm{d}\omega \\
&= \int_{-\infty}^{\infty} \frac{1}{T^{2}-T_{1}^{2}}\left( \frac{T^{2}}{1+\omega^{2}T^{2}}-\frac{T_{1}^{2}}{1+\omega^{2}T_{1}^{2}} \right) \, \mathrm{d}\omega  \\
&= \frac{1}{T^{2}-T_{1}^{2}}\left [T\arctan(\omega T) -T_{1}\arctan(\omega T_{1}^{2}) \right] _{-\infty}^{\infty} \\
&=\frac{2(T-T_{1})}{T^{2}-T_{1}^{2}} \\
&= \frac{2}{T+T_{1}}
 \end{align}
$$
We require $\frac{E_{o}}{E_{i}}=\frac{3}{4}$ hence
$$
\begin{align}
\frac{T}{T+T_{1}}&=\frac{3}{4} \\
 \\
\Rightarrow\quad \frac{T_{1}}{T}&=\frac{1}{3}
 \end{align}
$$
## 9.
This question uses the unitary Fourier transform, hence
$$
\begin{align}
E_{F}=E_{f} & = 2\int_{0}^{1} (1-f)^{2}\, \mathrm{d}f  \\
&= 2\int_{0}^{1} (f^{2}-2f+1 )\, \mathrm{d}x  \\
&=2\left[ \frac{f^{3}}{3}-f^{2}+f\right]_{f=1} \\
&=\frac{2}{3}
 \end{align}
$$
We require that $\left< F|F \right>_{f\in[-f_{1},f_{1}]}=\frac{1}{3}$ so using the previous result we have
$$
\begin{align}
\left<F|F \right>_{f\in[-f_{1},f_{1}]}= 2\left[ \frac{f_{1}^{3}}{3}-f_{1}^{2}+f_{1} \right] &=\frac{1}{3}
 \end{align}
$$
By calculator we have only $f_{1}=\pu{ 0.206 Hz }$ for $f\in\mathbb{R}$

## 10.
Applying the half-cosine transform from the data-book,
$$
\begin{aligned}
X_{p}(\omega)&=\int_{-\frac{T}{2}}^{\frac{T}{2}}\cos (pt) e^{-j\omega t} \, \mathrm{d}t  \\
&= \int_{-\frac{T}{2}}^{\frac{T}{2}} \frac{1}{2}\left(e^{jt(p-\omega)} +e^{-jt(p+\omega)}  \right)\, \mathrm{d}t \\
&=\frac{1}{2}\left[\frac{e^{jt(p-\omega)}}{j(p-\omega)} -\frac{e^{-jt(p+\omega)}}{j(p+\omega)}  \right]_{-\frac{T}{2}}^{\frac{T}{2}} \\
&= \frac{\sin\left( \frac{T}{2}(p-\omega) \right)}{p-\omega}+ \frac{\sin\left( \frac{T}{2}(p+\omega) \right)}{p+\omega} \\
 \\
\Rightarrow\quad X(\omega)&=X_{p}+X_{q} \\
&= 
\frac{T}{2}\operatorname{sinc}\left( \frac{T}{2}(\omega-p) \right)+\frac{T}{2}\operatorname{sinc}\left( \frac{T}{2}(\omega+p) \right)\\
&\quad+\  \frac{T}{2}\operatorname{sinc}\left( \frac{T}{2}(\omega-q) \right)+\frac{T}{2}\operatorname{sinc}\left( \frac{T}{2}(\omega+q) \right)

 \end{aligned}
$$
As $T$ increases, the oscillations in $X$ become faster so the peaks are sharper and more resolvable.

The spectrum is a set of superposed $\operatorname{sinc}$ functions centred at $\omega=\pm p, \pm q$ with angular frequency $\frac{T}{2}$ and amplitude $\frac{T}{2}$.


