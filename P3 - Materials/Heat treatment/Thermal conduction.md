#materials 

Heat diffusion can be modelled analogously to [[Fick's Laws|diffusion]].
## Fourier’s Law
This is analogous to [[Fick's Laws#Fick’s First Law|Fick’s first law]]. Defining $\mathbf{q}$ as the heat flux density and $\lambda$ as the thermal conductivity,
$$\mathbf{q}=-\lambda\nabla T$$
## Heat equation
This is analogous to [[Fick's Laws#Fick’s Second Law|Fick’s second law]] and applies to isotropic materials. With $\rho$ as the material density and $c$ as the specific heat capacity:$$\frac{\partial T}{\partial t}=\frac{\lambda}{\rho c}\nabla ^2T$$It is common to write this with $a=\frac{\lambda}{\rho c}$ to obtain the standard form:
$$
\frac{\partial T}{\partial t}=a\nabla ^2T
$$
>*Proof*. Conserving energy:
>$$
\begin{align*}
\iiint_{V} \rho c\frac{\partial T}{\partial t}\mathrm{d}^{3}\mathbf{r}&= -\iint_{S}\mathbf{q}\cdot \mathrm{d}\mathbf{S}\\
&= -\iiint_{V}\nabla \cdot\mathbf{q}\,\mathrm{d}^{3}\mathbf{r}
\end{align*}$$
>For this equation to hold for _every_ possible volume V, it is necessary (and sufficient) for the integrands to be equal everywhere.
>$$\begin{align}
\rho c\frac{\partial T}{\partial t} & =-\nabla \cdot \mathbf{q} \\
 \\
\Rightarrow\quad\frac{\partial T}{\partial t} & =\frac{\lambda}{\rho c}\nabla ^2T
\end{align}$$
## Standard solutions
Consider the 1D case:
$$
\frac{\partial T}{\partial t}=a \frac{\partial^2 T}{{\partial x}^2}
$$
### Impulse response
The response to a delta function at the origin is
$$
T(x, t)= \frac{1}{2\sqrt{ \pi at }}\exp\left(- \frac{x^{2}}{4at} \right)
$$
which is a normal distribution with $\sigma=\sqrt{ 2at }$
$$
T(x)\sim \mathcal{N}(0, \sigma^{2}=2at)
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
]
\addplot3[
	surf,
	samples=17,
	y domain=-1:1,
	domain=0.1:1,
]
{1/(2*sqrt(3.14*x))*exp(-y^2/(4*x))};
\end{axis}
\end{tikzpicture}
\end{document}
```
### Step response
The response to a unit step function at the origin is the integral with respect to $x$ of the impulse response:
$$
\begin{align}
T(x, t)  & = \int \mathcal{N}(0, \sigma^{2}) \, \mathrm{d}x  \\
 & = \frac{1}{2} + \frac{1}{2}\mathrm{erf}\left( \frac{x}{\sqrt{ 2 }\sigma} \right) \\
 & =\frac{1}{2} + \frac{1}{2}\mathrm{erf}\left( \frac{x}{2\sqrt{ at }} \right)
\end{align}
$$
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
]
\addplot3[
	surf,
	samples=17,
	y domain=-1:1,
	domain=0.05:1,
]
{0.5+0.5*erf(y/(2*sqrt(x))};
\end{axis}
\end{tikzpicture}
\end{document}
```
However, in the restricted case where $x>0$, due to the antisymmetric nature of $\mathrm{erf}(x)$, the solution is:
$$
\begin{align} \\
T(x, t) & =\mathrm{erf}\left( \frac{x}{\sqrt{ 2 }\sigma} \right) \\
 & =\mathrm{erf}\left( \frac{x}{2\sqrt{ at }} \right)
\end{align}
$$
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
]
\addplot3[
	surf,
	samples=17,
	y domain=0:1,
	domain=0.05:1,
]
{erf(y/(2*sqrt(x))};
\end{axis}
\end{tikzpicture}
\end{document}
```
In this case, the width between $x=0$ and the diffusing step grows on the order of $\sqrt{ at }$

Consider the case with a non-zero fixed origin temperature:
$$T(x=0)=T_{0}$$
The resulting distribution is rescaled to a linear interpolation with factor $\mathrm{erf}\left( \frac{x}{2\sqrt{ at}} \right)$between $T_{0}$ and the initial step temperature $T_{s}$
$$
T(x,t)=T_{0}+(T_{s}-T_{0})\,\mathrm{erf}\left( \frac{x}{2\sqrt{ at} }\right)
$$
### Sinusoidal response 
Consider a sinusoidal initial temperature distribution with amplitude $T_{a}$ and frequency $\omega$$$
T(x, t=0)=T_{a}\sin(\omega x)
$$Under the 1D heat equation, this has the solution of $$
T(x,t)=A\sin(\omega x)\exp(-\omega^{2}at)
$$which, similarly to the step response, can be rescaled for a non-zero fixed origin temperature $T_{0}$ using linear interpolation with parameter $\sin(\omega x)\exp(-\omega^{2}at)$
$$
T(x,t)=T_{0}+(T_{a}-T_{0})\sin(\omega x)\exp(-\omega^{2}at )
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
]
\addplot3[
	surf,
	samples=17,
	y domain=-1:1,
	domain=0.1:1,
]
{1+sin(deg(3.14159*y))*exp(-(2*3.14159)^2*0.1*x)};
\end{axis}
\end{tikzpicture}
\end{document}
```

This result is invariant of a phase change in the function generating the sinusoid.

>*Proof.* Take a trial solution of the form $$
T(x,t)=f(t)\cdot T_{a}\sin(\omega x)+T_{0}
$$for which $$\begin{cases}
\begin{align}
T(x, 0) & =T_{0}+(T_{a}-T_{0})\sin(\omega x) \\
T(0, t) & =T_{0}
\end{align}
\end{cases}$$The former applies because it is only the surplus $T-T_{0}$ heat that diffuses. Now, under the 1D heat equation we obtain $$
\frac{\mathrm{d}f}{\mathrm{d}t}+a\omega^2f=0 
$$which has auxiliary equation $$
\begin{align}
\lambda+ a\omega^2 & =0 \\
 \\
\Rightarrow\quad f(t) & =A\exp(-a\omega^{2}\cdot t) \\
 \\
\Rightarrow\quad T(x,t) & =A\exp(-\omega^{2}at) \cdot T_{a}\sin(\omega x)+T_{0}
\end{align}
$$Applying the boundary condition for $t=0$$$
\begin{align}
A & =T_{a}-T_{0} \\
 \\
\Rightarrow\quad T(x,t) & =T_{0}+(T_{a}-T_{0})\sin(\omega x)\exp(-\omega^{2}at )
\end{align}
$$