There are two steps to digitise an analogue signal:
- sampling  (ideally lossless)
- quantisation (lossy)

## Motivation
- Robustness
- Performance
	- Error-correcting codes can correct bit errors that occur in transmission
- Encryption

## Quantisation
Quantisation is always lossy! If $Q(z)$ is the quantised value of $z=x(nT),$ then the quantisation noise is defined as
$$
e(z)=z-Q(z)
$$
If the quantisation step size is $h$ then
$$
e(z)\in\left[ -\frac{h}{2}, \frac{h}{2} \right]
$$
We model the random variable as uniformly distributed in this the range.

Then the noise power is
$$
\begin{align}
N_{Q}=\operatorname{\mathbb{E}}[e_{}^{2}]&=\int_{-\frac{h}{2}}^{\frac{h}{2}} \frac{x^{2}}{h} \, \mathrm{d}x  \\
&=\frac{h^{2}}{12}
 \end{align}
$$

> Supo question: why is $e(z)$ not normally distributed due to CLT?

## Signal to noise ratio
The signal-to-noise ratio is defined as the ratio of signal and noise powers. For a sinusoid signal with signal power $\frac{V^{2}}{2},$ applying an $n$-bit uniform quantizer with $2^{n}$ levels and step size $h= \frac{2V}{2^{n}}$ gives
$$
\mathrm{SNR}= \frac{\frac{V^{2}}{2}}{\frac{h^{2}}{12}}= 3\times 2^{2n-1}
$$

There is a trade-off in the number of bits we decide to use. A larger number of bits means
- smaller step size, better quality quantizer
- but more bits to transmit

## Data rate
For a signal of [[bandwidth]] $W$ sampled at the Nyquist frequency and quantized to $n$ bits, the digitised source will have a bit rate of
$$
R=2Wn
$$
because there are $2W$ samples per second, each encoded in $n$ bits.

>Mobile phones use non-uniform (companding) quantizers which obtain a lower bit rate by employing clever algorithms.



