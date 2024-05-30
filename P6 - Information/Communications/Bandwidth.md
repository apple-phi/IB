## Energy
The energy of a signal $x$ with spectrum $X$ is defined as 
$$
E_{x}=\left< x\mid x \right> = \left< X\mid X \right> 
$$
assuming the spectrum is generated by a unitary transform.

We define the energy spectral density as
$$
\frac{\mathrm{d} E_{x}}{\mathrm{d}f} = |X(f)|^{2}
$$
By definition, this is the energy of the signal in the infinitesimal frequency band $[f,f+\delta f].$

## Power
The signal power is the energy normalised by the time duration of the signal,
$$
P_{x}= \frac{1}{T}\left< x\mid x \right> 
$$
For an infinite duration signal, we take the power to be from the limit as $T\to \infty$

## Bandwidth
The bandwidth of a signal is roughly the range of frequencies over which its spectrum is non-zero.

For real signals, it is typical to measure the bandwidth as the range of *positive* frequencies because $|X(\omega)|$ is an even function.

>For real signals, $X(-\omega)=X^{*}(\omega)$

However, many real signals are time-limited, not frequency limited. Consider the case where $x$ is a rectangular pulse. Then the spectrum is a $\operatorname{sinc}(\omega)$ function.

![[rect-spectrum.png]]

So under the above definition, this signal has infinite bandwidth. Other more practical definitions of bandwidth include:
- 90% bandwidth—the range of frequencies which contain 90% of the energy of the spectrum
- 3 dB bandwidth—the range of frequencies which contain 50% of the energy of the spectrum
- Null-to-null bandwidth—the width of the “main lobe” of the spectrum

Bandwidth is a measure of the extent of significant spectral content of the signal.

Bandwidth is a scarce resource. Wired channels like telephone lines and USB cables also act as filters due to their physical properties. Therefore transmitted signals need to be bandlimited.

>In both wired and wireless communication, need good Tx + Rx designs that make optimal use of available bandwidth 
### Low-pass signal
A low-pass (baseband) signal has its spectrum centred around $\omega=0.$

![[low-pass-filter.png]]

### Passband signal
A signal is said to be *passband* if its spectral content is centred around $\pm f_{c}$ where $f_{c}>0.$

![[passband-signal.png]]