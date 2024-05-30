## Motivation
Given values sampled at interval $T$ from a function $f$, the discrete-time [[Fourier transform]] (DTFT) shows how to determine frequency content:
$$
\begin{align}
F_{s}(\omega) &= \sum\limits_{ n=-\infty }^{ \infty}f(nT)e^{-jn\omega T} \\
& =\frac{1}{T}\sum\limits_{ n=-\infty }^{ \infty }F(\omega-n\omega_{0})
 \end{align}
$$
But it is impractical:
- We don’t have sufficient data points
- $F_{s}(\omega)$ is defined over the support $\mathbb{\Omega}=[-\infty,\infty]$ but we can’t store an infinite amount of frequencies!

The discrete [[Fourier transform]] is a way to overcome these practical difficulties.

## Definition
Sample only at discrete times $t=0, T, 2T, \dots (N-1)T$, then
$$
F_{s}(\omega)\approx\sum\limits_{ n=0 }^{ N-1}f(nT)e^{-jn\omega T}
$$
Calculate the spectrum only at corresponding discrete frequencies $\omega=0, \frac{\omega_{0}}{N}, \frac{2\omega_{0}}{N}, \dots, \frac{(N-1)\omega}{N}$ such that
$$
F_{s}\left( \frac{k\omega_{0}}{N} \right)=\sum_{n=0}^{N-1}f(nT)e^{-j 2\pi n \frac{k}{N}}
$$
Then the DFT is
$$
\begin{align}
F_{k} & =F_{s}\left( \frac{k\omega_{0}}{N} \right) \\
&=\sum_{n=0}^{N-1}f(nT)e^{-j 2\pi n \frac{k}{N}}
 \end{align}
$$
Where $F_{k}$ is the complex number representing the frequency and phase of the sinusoidal component of $f$ with frequency $\omega=\frac{2\pi k}{N}$

Some properties of the DFT:
- $N$-periodic
- $F_{k}^{*}=F_{N-k}$
- the naïve implementation is $O(n^{2})$
- Scaled energy conservation (Parseval’s Theorem)
- the boundaries of the sample window introduce spurious frequency components, which can be minimised by signal windowing

This is commonly calculated as the Fast [[Fourier Transform]], which imposes the restriction the $N$ is a power of 2 and has $O(n\log n)$. Other fast implementations exist, e.g. for powers of 4,

## The inverse DFT
Analogously to the continuous inverse [[Fourier transform]], 
$$
f_{n}=\frac{1}{N}\sum_{k=0}^{N-1}F_{k}e^{j 2\pi n \frac{k}{N}}
$$
