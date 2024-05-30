
## Non-unitary formulation
### Fourier transform
The Fourier Transform is given by
$$
\begin{align}
F(\omega) =\mathscr{F}\{f(t)\}& =\braket{ f(t)\, |\, e^{j\omega t} } \\
 & =  \int _{-\infty}^{\infty}f(t)e^{ -j\omega t } \, \mathrm{d}t 
\end{align}
$$
### The inverse Fourier transform
$$
\begin{align}
f(t) & =\braket{ F(\omega)\, |\, e^{-j\omega t} } \\
 & =\frac{1}{2\pi }\int_{-\infty}^{\infty} F(\omega )e^{ jwt } \, \mathrm{d}\omega 
\end{align}
$$

## Properties
### Linearity
$$
\mathscr{F}\{f+g\}=\mathscr{F}{f} + \mathscr{F}{g}
$$
### Time-scaling
$$
\mathscr{F}\{f(at)\}=\frac{1}{a}F\left( \frac{w}{a} \right)
$$
### Time-shifting
$$
\mathscr{F}\{f(t+h)\}=e^{ jwh }\mathscr{F}\{f\}
$$
Note the similarity with the [[Series expansions#The shift operator|shift operator]].

### Frequency shift / modulation
$$
\mathscr{F}\{e^{ jwh}f\}=F(w+h)
$$
Again note the similarity with the [[Series expansions#The shift operator|shift operator]].
### Differentiation 
The Fourier transform of the derivative of a function $f$ can be simply expressed in terms of the original $f$.
$$
\mathscr{F}\left\{ \frac{\mathrm{d}^{n}f}{{\mathrm{d}t}^{n}}\right\} = (jw)^{n}\mathscr{F}\{f\}
$$
### Conjugation
$$
\mathscr{F}\{f(t)^{*}\}=F(-w)^{*}
$$

### Heisenberg-Gabor principle
If a function $f$ has time duration $T$ and its Fourier transform $F$ has frequency [[bandwidth]] $B$ then
$$
T\cdot B\geq 1
$$
### Duality theorem
Given a function $F$ that is already the Fourier transform of another function $f$, then its non-unitary Fourier transform $\mathscr{F}\{F(t)\}$ can be simply expressed in terms of $f$.
$$
\mathscr{F\{F\{}f(t)\}\}=\mathscr{F}\{F(t)\}=2\pi f(-w)
$$

### Convolution Theorem
$$
\mathscr{F}\{f*g\}=F\cdot G
$$
### Multiplication theorem
$$
\mathscr{F}\{f\cdot g\}= \frac{1}{2\pi}F*G
$$
### Parseval’s Theorem
The unitary Fourier transform is energy conserving, and the non-unitary Fourier transform is still well-behaved.
$$
\begin{align}
\left< f\mid f \right> & =\frac{1}{2\pi}\left< F\mid F \right>  
\end{align}
$$
Or, equivalently,
$$
\int _{-\infty}^{+\infty}|f|^{2} \, \mathrm{d}x =\frac{1}{2\pi}\int _{-\infty}^{+\infty}|F|^{2} \, \mathrm{d}\omega 
$$
## Similarity with the Laplace transform
Compare the definitions:
$$
\begin{align}
(\mathcal{L}f)(s) & = \left< f\mid e^{st} \right>_{0}^{\infty}   \\
&=\int_{0}^{\infty} f(t)e^{-st} \, \mathrm{d}t \\
 \\
(\mathscr{F}f)(\omega) &= \left< f\mid e^{j\omega t} \right>_{-\infty}^{+\infty}  \\
& =\int_{-\infty}^{+\infty} f(t)e^{-j\omega t} \, \mathrm{d}t
\end{align}
$$
So for functions defined to be $0$ for negative inputs, i.e.
$$f(x\ni x<0)=0$$
the two transforms are equivalent by the substitution $s=j\omega$

### Which one to choose?
- Laplace transform is better suited for solving problems with boundary conditions at $t=0$
- Fourier transform is better suited to steady state analysis

