## 1.
$y$ and $y'$ are both continuous, but $y^{(n)}$ is not for $n\geq 2$
$$
\begin{align}
y & =x(\pi\pm x) \\
y'&=\pm 2x+\pi \\
y'' & =\pm 2
\end{align}
$$
Hence the coefficients in the series of $y$ vary as $\frac{1}{n^{3}}$. When evaluating, the function is odd so only consider the sine terms for positive $x$
$$
\begin{align}
b_{n} & = \frac{\left< y\mid \sin(nx) \right> }{\left< \sin(nx)\mid \sin(nx) \right> } \\
 & =\frac{2}{\pi}\int_{0}^{\pi}x(\pi-x)\sin(nx)  \, \mathrm{d}x 
\end{align}
$$
Applying tabular integration by parts:

| Sign | D | I |
| ---- | ---- | ---- |
| $+$ | $x(\pi-x)$ | $\sin(nx)$ |
| $-$ | $-2x+\pi$ | $-\frac{1}{n}\cos(nx)$ |
| $+$ | $-2$ | $-\frac{1}{n^{2}}\sin(nx)$ |
| $-$ | $0$ | $\frac{1}{n^{3}}\cos(nx)$ |
$$
\begin{aligned}
b_{n} & =\frac{2}{\pi}\left[ -x(\pi-x) \frac{1}{n}\cos(nx)+(-2x+\pi) \frac{1}{n^{2}}\sin(nx)-\frac{2}{n^{3}}\cos(nx) \right]_{0}^{\pi}  \\
  & =\frac{2}{\pi}\left[ -\cancel{\frac{\pi \sin(n\pi)}{n^{2}}}-\frac{2\cos(n\pi)}{n^{3}}+\frac{2}{n^{3}} \right]  \\
  & =\frac{4}{\pi}\left[ \frac{1-\cos(n\pi)}{n^{3}} \right]  \\
&=\begin{cases}
\begin{align}
&\quad0&&n\in 2\mathbb{Z}^+ \\
&\:\frac{8}{\pi n^{3}}&&n\in (2\mathbb{Z}^{+}-1)
\end{align}
\end{cases}
\end{aligned}
$$
This decreases as $\frac{1}{n^{3}}$, as expected.

## 2. 
Expanding the sinusoid terms as complex exponentials,
$$
\begin{align}
y & = \frac{a_{0}}{2}+ \sum\limits_{ n=1 }^{ \infty }\left[ a_{n}\cos(n\omega_{0}t)+b_{n}\sin(n\omega_{0}t) \right]  \\
& = \frac{a_{0}}{2}+ \sum\limits_{ n=1 }^{ \infty }\left[ \frac{e^{jn\omega_{0}t}+e^{-jn\omega_{0}t}}{2}a_{n}+\frac{e^{jn\omega_{0}t}-e^{-jn\omega_{0}t}}{2j}b_{n} \right]  \\
 & = \frac{a_{0}}{2}+\sum\limits_{ n=1 }^{ \infty }\left[ \frac{a_{n}-jb_{n}}{2}e^{jn\omega_{0}t} +\frac{a_{n}+jb_{n}}{2}e^{-jn\omega_{0}t}\right]  \\
& =\sum\limits_{ n=-\infty }^{ -1 }\left[ \frac{a_{-n}+jb_{-n}}{2}e^{jn\omega_{0}t}\right] +\frac{a_{0}}{2}+\sum\limits_{ n=1 }^{ \infty }\left[ \frac{a_{n}-jb_{n}}{2}e^{jn\omega_{0}t}\right]
\end{align}
$$
### The key insight
The $a_{n}$ terms are formed from an inner product with the even function $\cos(nt)$, thus
$$a_{n}=a_{-n}$$ while the $b_{n}$ are formed from an inner product with an odd function $\sin(nt)$ so
$$b_{n}=-b_{-n}$$
Hence, by defining $c_{n}= \frac{a_{n}-jb_{n}}{2}=c^{*}_{-n}$ we have
$$
\begin{align}
y& =\sum\limits_{ n=-\infty }^{ -1 }\left[ \frac{a_{n}-jb_{n}}{2}e^{jn\omega_{0}t}\right] +\frac{a_{0}}{2}+\sum\limits_{ n=1 }^{ \infty }\left[ \frac{a_{n}-jb_{n}}{2}e^{jn\omega_{0}t}\right] \\
 & =\sum\limits_{ n=-\infty }^{ -1 }\left[ c_{n}e^{jn\omega_{0}t}\right] +c_{0}+\sum\limits_{ n=1 }^{ \infty }\left[ c_{n}e^{jn\omega_{0}t}\right]  \\
 & =\sum\limits_{ n=-\infty }^{ \infty }c_{n}e^{jn\omega_{0}t}
\end{align}
$$
## 3.
By definition of $c_{n}$
$$
\begin{align}
c_{n} & = \left.\frac{ \left< y\mid \exp\left( \frac{2\pi nt}{T}i \right) \right>}{\left< \exp\left( \frac{2\pi nt}{T}i \right)\mid\exp\left( \frac{2\pi nt}{T}i \right) \right> }\right|_{t\in[0,T], n\in\mathbb{Z^{+}}} \\
 & =\frac{1}{T}\int_{0}^{T} y\exp\left( -\frac{2\pi nt}{T}i \right) \, \mathrm{d}t  \\
& =\frac{1}{T}\int_{0}^{\frac{T}{2}} \exp(-\alpha t)\exp\left( -\frac{2\pi nt}{T}i \right) \, \mathrm{d}t \\
 & = \frac{1}{T}\left[ \frac{-1}{\frac{2\pi ni}{T}+\alpha}\exp\left\{  -\left( \frac{2\pi ni}{T}+\alpha \right)t \right\} \right]_{0}^{\frac{T}{2} } \\
 & = \frac{-1}{2\pi ni+\alpha T}\left[ \exp \left(- \pi ni-\frac{\alpha T}{2} \right)-1 \right]  \\
 & = \frac{1-\exp \left(- \pi ni-\frac{\alpha T}{2} \right)}{2\pi ni+\alpha T}
\end{align}
$$
Expanding $c_{n}$ into its real and imaginary parts,
$$
\begin{align}
c_{n}& = \frac{1-\exp \left(-\frac{\alpha T}{2} \right)\left[ \cos (n\pi)-i\cancel{\sin(n\pi)} \right] }{\alpha^{2}T^{2}+4\pi^{2}n^{2}}(\alpha T-2\pi ni) \\
 & = \frac{1-\exp\left( -\frac{\alpha T}{2} \right)\cos(n\pi)}{\alpha^{2}T^{2}+4\pi^{2}n^{2}}(\alpha T-2\pi ni) \\
 \\
	a_{n} & =2\operatorname{Re}(c_{n}) \\
&=\boxed{ \frac{2\alpha T-2\alpha T\exp\left( -\frac{\alpha T}{2} \right)\cos(n\pi)}{\alpha^{2}T^{2}+4\pi^{2}n^{2}}} \\
 \\
	b_{n}  & =2\operatorname{Im}(c_{n}) \\
 & =\boxed{ \frac{4\pi n-4\pi n\exp\left( -\frac{\alpha T}{2} \right)\cos(n\pi)}{\alpha^{2}T^{2}+4\pi^{2}n^{2}}}
\end{align}
$$
## 4. 
The given square wave is an odd function, so we only need to consider the sine terms.
$$
\begin{align}
b_{n} & = \left. \frac{\left< f\mid \sin(n\omega_{0}t) \right> }{\left< \sin(n\omega_{0}t)\mid \sin(n\omega_{0}t) \right> } \right|_{t\in[0,T], n\in\mathbb{Z^{+}}} \\
 & =\frac{2}{T}\int _{0}^{T}f\sin(n\omega_{0}t) \, \mathrm{d}t \\
 &=\frac{4}{T}\int _{0}^{\frac{T}{2}}\sin(n\omega_{0}t) \, \mathrm{d}t \\
 & = \left.\frac{-4\cos(n\omega_{0}t)}{n\omega_{0}T}\right|_{0}^{\frac{T}{2}} \\
 & = \frac{2-2\cos(n\pi)}{n\pi} \\
 & = \left. \frac{4}{n\pi} \right|_{n\in (2\mathbb{Z^{+}}-1)}
\end{align}
$$
This immediately gives the required Fourier Series representation.
$$
\begin{align}
c_{n} & = \frac{\cancel{a_{n}}-jb_{n}}{2} \\
& = -j\frac{2}{n\pi}\cos(n\pi)
\end{align}
$$
Or, directly,
$$
\begin{align}
c_{n} & = \frac{1}{T}\int _{0}^{T}fe^{ -jn\omega_{0}t } \, \mathrm{d}t  \\
 & =\frac{1}{T}\left[ \int _{0}^{\frac{T}{2}}e^{ -jn\omega_{0}t } \, \mathrm{d}t-\int _{\frac{T}{2}}^{T}e^{ -jn\omega_{0}t } \, \mathrm{d}t   \right]  \\
 & =\frac{1}{T}\left[ -\frac{\exp(-jn\omega_{0}t)}{jn\omega_{0}} \right]_{0}^{\frac{T}{2}}+\frac{1}{T}\left[ \frac{\exp(-jn\omega_{0}t)}{jn\omega_{0}} \right]_{\frac{T}{2}}^{T}  \\
 & =\frac{\cos(0)-\cos(n\pi)+\cos(2n\pi)-\cos(n\pi)}{jn\omega_{0}T} \\
& = \frac{2-2\cos(n\pi)}{n\pi} \\
 & = \left. \frac{4}{n\pi} \right|_{n\in (2\mathbb{Z^{+}}-1)}
\end{align}
$$
as before.

## 5.
By inspection, this is a time-shift backwards by $a=\frac{T}{4}$. Let $u=t+a$, then
$$
\begin{align}
f_{2}(t) & =f(u) \\
 & =\sum\limits_{ n=-\infty }^{ \infty }c_{n}\exp\left(  \frac{j2\pi nu}{T}  \right) \\
& =\sum\limits_{ n=-\infty }^{ \infty }c_{n}\exp\left(  \frac{j2\pi na}{T}  \right)\exp\left(  \frac{j2\pi nt}{T}  \right) \\
 & =\sum\limits_{ n=-\infty }^{ \infty }c_{n}d_{n}\exp\left(  \frac{j2\pi nt}{T}  \right)
\end{align}
$$
## 6.
Only the 1st, 2nd and 3rd derivates are continuous.
$$
\begin{align}
c_{n}' & = \frac{j 2\pi n}{T}c_{n} \\
 & =\frac{j 2\pi (-1)^{n}}{Tn^{3}} \\
 \\
c_{n}'' & = \left( \frac{j 2\pi n}{T} \right)^{2}c_{n} \\
 & = \frac{2\pi (-1)^{n+1}}{T^{2}n^{2}} \\
 \\
c_{n}^{(-1)} & = \left( \frac{j 2\pi n}{T} \right)^{-1}c_{n} \\
 & = \frac{jT(-1)^{n+1}}{2\pi  n^{5}}
\end{align}
$$
$c_{0}^{(-1)}$ depends on the constant of integration.

## 7.
$$
\begin{align}
f*g & =\int _{0}^{t} f(t-\tau)g(\tau)\, \mathrm{d}\tau  \\
 & =\int _{0}^{t} (t-\tau)e^{ -\alpha \tau }\, \mathrm{d}\tau  \\
\end{align}
$$
Applying tabular integration by parts:

| Sign | D | I |
| ---- | ---- | ---- |
| $+$ | $t-\tau$ | $e^{-\alpha \tau}$ |
| $-$ | $-1$ | $-\frac{1}{\alpha}e^{ -\alpha \tau }$ |
| $+$ | $0$ | $\frac{1}{\alpha^{2}}e^{ -\alpha \tau }$ |

$$
\begin{align}
f*g  & = \left[ \frac{\tau-t+\alpha^{-1}}{\alpha} e^{ -\alpha \tau }\right] _{\tau=0}^{\tau=t} \\
 & =\frac{e^{ -\alpha t }}{\alpha^{2}}- \frac{1}{\alpha^{2}}+\frac{t}{\alpha} 
\end{align}
$$

## 8.
Prove that convolution is associative. Let $u=t-\tau$, then
$$
\begin{align}
f*g&=\int_{t_{0}}^{t}f(\tau)g(t-\tau)  \, \mathrm{d}\tau   \\
& =\int_{t_{0}}^{t}f(t-u)g(u) \, \mathrm{d}(u+t)  \\
 & =\int_{t_{0}}^{t}f(t-u)g(u)\,\mathrm{d}u \\
 & =g*f
\end{align}
$$
## 9.
The different forms of the convolution come from the piecewise nature of the functions being convolved.
$$
\begin{align}
f(t) & =H(t)-H(t-T) \\
g(t) & = e^{-\alpha t}H(t)
\end{align}
$$
where $H(t)$ is the Heaviside step function.
```tikz
\begin{document}    
\begin{tikzpicture}
  \draw[->] (-1, 0) -- (13, 0) node[right] {$t$};
  \draw[->] (0, -1) -- (0, 13) node[above] {$y$};
  \draw[scale=10, domain=0:1, smooth, variable=\x, blue] plot ({\x}, {1});
  \draw[scale=10, domain=0:1, smooth, variable=\y, blue] plot ({1}, {\y});
  \draw[scale=10, domain=0:1.2, smooth, variable=\x, red] plot ({\x}, {exp(\x-1.5)});
  \node[label={left:$1$}] at (0,10) {};
  \node[label={left:$e^{-at}$}] at (0,2.2313016) {};
  \node[label={below:$T$}] at (10,0) {};
  \node[blue,right] at (11,12) {$y=1$};   
  \node[red,right] at (11,12.5) {$y=e^{\alpha (\tau-t)}$};
\end{tikzpicture}
\end{document}
```

Converting to the Laplace domain,
$$
\begin{align}
F(s) & = \frac{1-e^{-sT}}{s} \\
G(s)& = \frac{1}{s+\alpha}
\end{align}
$$
Applying the convolution theorem,
$$
\begin{aligned}
\mathcal{L}\{f*g\}  & = F\cdot G \\
 & =\frac{1-e^{-sT}}{s(s+\alpha)} \\
 & =(1-e^{-sT})\left( \frac{\alpha^{-1}}{s}- \frac{\alpha^{-1}}{s+\alpha} \right) \\
 & =\frac{\alpha^{-1}}{s}-\frac{\alpha^{-1} e^{-sT}}{s}-\frac{\alpha^{-1}}{s+\alpha}+\frac{\alpha^{-1} e^{-sT}}{s+\alpha} \\
 \\
	\Rightarrow\quad f*g&=\frac{1}{\alpha} H(t)-\frac{1}{\alpha} H(t-T)-\frac{1}{\alpha}e^{-\alpha t}H(t) + \frac{1}{\alpha}e^{-\alpha(t-T)}H(t-T) \\
 & =\frac{1}{\alpha}H(t)\left[ 1-e^{-\alpha t} \right] +\frac{1}{\alpha}H(t-T)\left[ e^{\alpha(T-t)}-1 \right]  \\
\\
&= \left\{\begin{matrix}
&0 &&t<0\\
&\frac{1-e^{\alpha t}}{\alpha} &&0\leq t\leq T\\
&\frac{e^{-\alpha t}(e^{\alpha T}-1)}{\alpha} &&t>T
\end{matrix}\right.
\end{aligned}
$$
