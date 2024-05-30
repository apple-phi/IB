#materials 
## Thick plate
For thermal diffusion during time $t$ through a plate of constant width $L$ with a fixed (typically colder) boundary temperature $T_{0}$, this process can be approximated as 1D heat flow along a bar of infinite length for cases when the length far exceeds the characteristic length of the diffusion:$$L \gg \sqrt{ at }$$Therefore the general result can be approximated as a linear interpolation between the boundary temperature and the asymptotic temperature by parameter $\mathrm{erf}\left( \frac{x}{2\sqrt{ at }} \right)$
$$T(x,t)=T_{0}+(T_{1}-T_{0})\,\mathrm{erf}\left( \frac{x}{2\sqrt{ at }} \right)$$
as given [[Thermal conduction#Step response|here]].
```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\makeatletter
\pgfmathdeclarefunction{erf}{1}{%
  \begingroup
    \pgfmathparse{#1 > 0 ? 1 : -1}%
    \edef\sign{\pgfmathresult}%
    \pgfmathparse{abs(#1)}%
    \edef\x{\pgfmathresult}%
    \pgfmathparse{1/(1+0.3275911*\x)}%
    \edef\t{\pgfmathresult}%
    \pgfmathparse{%
      1 - (((((1.061405429*\t -1.453152027)*\t) + 1.421413741)*\t 
      -0.284496736)*\t + 0.254829592)*\t*exp(-(\x*\x))}%
    \edef\y{\pgfmathresult}%
    \pgfmathparse{(\sign)*\y}%
    \pgfmath@smuggleone\pgfmathresult%
  \endgroup
}
\makeatother
\begin{document}
\begin{tikzpicture}
\begin{axis}[
colormap/viridis,
xlabel=$t$,
ylabel=$x$,
zlabel=$T$,
view={50}{30},
]
\addplot3[
	surf,
	samples=21,
	y domain=0:1,
	domain=0.025:1,
	shader=flat
]
{erf(y/(2*sqrt(x))};
\end{axis}
\end{tikzpicture}
\end{document}
```

The cooling rate can be obtained using the identity
$$\frac{\mathrm{d}}{\mathrm{d}x}\left\{\mathrm{erf(x)}\right\}=\frac{2}{\sqrt{ \pi }}\exp(-x^{2})$$
Then, let $z=\frac{x}{2\sqrt{ at }}$ so
$$
\begin{align}
\frac{\partial T}{\partial t} & =\frac{\partial T}{\partial z}\frac{\partial z}{\partial t} \\
 & =(T_{1}-T_{0})\cdot \frac{2}{\sqrt{ \pi }}\exp(-z^{2})\cdot -\frac{xt^{-1.5}}{4\sqrt{ a }} \\
 & = \frac{(T_{0}-T_{1})xt^{-1.5}}{2\sqrt{ \pi a }}\exp\left( -\frac{x^{2}}{4at} \right)
\end{align}
$$
```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\begin{document}
\begin{tikzpicture}
\begin{axis}[
colormap/viridis,
xlabel=$t$,
ylabel=$x$,
zlabel=$-\frac{\partial T}{\partial t}$,
view={50}{30},
z buffer=auto
]
\addplot3[
	surf,
	samples=21,
	y domain=0:0.7,
	domain=0.1:0.5,
	shader=flat,
]
{1*y*x^(-1.5)*1/(2*sqrt(pi*0.1))*exp(-y^2/(4*0.1*x))};
\end{axis}
\end{tikzpicture}
\end{document}
```

This demonstrates that the plate cools fastest near its cold edge, as expected.
## Finite-width plate
For the case where the width of the plate is on the order of the characteristic diffusion distance,
$$
L\sim \sqrt{ at }
$$
the situation is more complex and the initial temperature distribution can be modelled as a square wave which can be solved using a Fourier series approach.

The square wave parameters are:
- wavelength $2L$ (considering a half-wavelength to represent the hot plate)
- mean value $T_{0}$
- mean-to-peak amplitude $(T_{1}-T_{0})$

Hence the initial conditions can be formulated as:
$$
T(x, 0)=T_{0}+(T_{1}-T_{0})\sum_{n\in \left(2\mathbb{Z}^{+}-1\right)} \frac{4}{n\pi}\sin\left( \frac{n\pi x}{L} \right)
$$
Recall the [[Thermal conduction#Sinusoidal response|standard solution]] for a sinusoid response. Then the square wave response is:
$$
T(x, t)=T_{0}+(T_{1}-T_{0})\sum_{n\in \left(2\mathbb{Z}^{+}-1\right)} \frac{4}{n\pi}\sin\left( \frac{n\pi x}{L} \right)\exp\left( -\frac{n^{2}\pi^{2}at}{L^{2}} \right)
$$
```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\begin{document}
\begin{tikzpicture}
\begin{axis}[
colormap/viridis,
xlabel=$t$,
ylabel=$x$,
zlabel=$T$,
view={50}{30},
z buffer=auto
]
\addplot3[
	surf,
	samples=20,
	y domain=0:1,
	domain=0.05:1,
	shader=flat,
]
{1+1*4/pi*(1/1*sin(deg(1*pi*y))*exp(-(1^2)*pi^2*0.1*x)+1/3*sin(deg(3*pi*y))*exp(-(3^2)*pi^2*0.1*x)+1/5*sin(deg(5*pi*y))*exp(-(5^2)*pi^2*0.1*x)+1/7*sin(deg(7*pi*y))*exp(-(7^2)*pi^2*0.1*x)+1/9*sin(deg(9*pi*y))*exp(-(9^2)*pi^2*0.1*x)};
\end{axis}
\end{tikzpicture}
\end{document}
```

Each mode’s exponential time constant varies as $$
\tau_{n} \propto \frac{L^{2}}{n^{2}a}
$$so reducing plate width has a significant effect on cooling rate. Also, because higher modes decay much faster, the solution for small $t$ can be approximated by just the first term:
$$
T(x, t)\approx T_{0}+(T_{1}-T_{0})\cdot \frac{4}{\pi}\sin\left( \frac{\pi x}{L} \right)\exp\left( -\frac{\pi^{2}at}{L^{2}} \right)
$$
