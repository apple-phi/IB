## Basics
Any function $f$ periodic in the interval $[-\pi,\pi]$ can be expressed as
$$
f(t)= \frac{\bar{f}}{2}+ \sum\limits_{ n=1 }^{\infty }\left( a_{n}\cos(nt)+b_{n}\sin(nt) \right) 
$$
Where $a_{n}$ and $b_{n}$ are the normalised inner products of $f$ with $\cos(nt)$ and $\sin(nt)$.
$$
\begin{cases}
\begin{align}
a_{n}  & = \frac{1}{\pi}\langle f\mid\cos nt \rangle\\
b_{n}  & = \frac{1}{\pi}\langle f\mid\sin nt \rangle
\end{align}
\end{cases}
$$
>Note that the factor of $\pi$ is due to the normalisation by $\pi=\left< \cos nt \,| \cos nt \right> =\left< \sin nt \,| \sin nt \right>$ over the $2\pi$ time period.

## Complex Fourier series
$$
f(t)= \sum\limits_{ n=1 }^{ \infty }c_{n}e^{ -jnt }
$$
with coefficients
$$
c_{n}=\frac{1}{2\pi}\langle f\mid e^{ jnt }\rangle
$$
Once again the $2\pi$ term comes from normalisation by
$$
\begin{align}
\left< e^{jnt}\mid e^{jnt} \right>  & =\int_{-\pi}^{+\pi} e^{jnt}\cdot e^{-jnt} \, \mathrm{d}t  \\
 & =\int_{-\pi}^{+\pi}  \mathrm{d}t  \\
 & =2\pi
\end{align}
$$
Note that 
$$
c_{n}= \frac{a_{n}-b_{n}j}{2}
$$
and conversely,
$$
\begin{cases}
\begin{align}
a_{n} & =c_{n}^{*}+c_{n}=2\operatorname{Re}(c_{n})\\
b_{n}& =c_{n}^{*}-c_{n}=2\operatorname{Im}(\mathbf{c}_{n}) 
\end{align}
\end{cases}
$$

Signals with a period $T$ can be expressed as a Fourier series by a change of scale. Trivially, because all coefficients would be similarly scaled, their relationship *stays the same.*

Linear transformations of the function distribute among the Fourier decomposition terms.

### Proof of equivalence
$$
\begin{align}
c_{n} & =\frac{\left< f\mid e^{jnt} \right>}{\left< e^{jnt}\mid e^{jnt} \right> } \\
 & =\frac{1}{2\pi}\int_{-\pi}^{+\pi} f\cdot e^{-jnt} \, \mathrm{d}t \\
 & =\frac{1}{2}\int_{-\pi}^{+\pi} \left[ \frac{f\cdot\cos(nt)}{\pi} -\frac{f\cdot j\sin(nt)}{\pi} \right]\, \mathrm{d}x  \\
 & =\frac{1}{2}(a_{n}-b_{n}j)
\end{align}
$$


