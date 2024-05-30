## Power and energy
Define the energy content of a signal $f$ as 
$$
\begin{align}
E & =\int^\infty_{\infty} |f(t)|^{2} \, \mathrm{d}t  \\
& =\lim_{ T \to \infty } \int^{+\frac{T}{2}}_{-\frac{T}{2}} |f(t)|^{2} \, \mathrm{d}t 
\end{align}
$$
Similarly, the average power content is
$$
P= \lim_{ T \to \infty } \frac{1}{T}\int^{+\frac{T}{2}}_{-\frac{T}{2}} |f(t)|^{2} \, \mathrm{d}t 
$$

>The magnitude is used instead of the function value itself to preserve useful properties.

When the signal is periodic you only need to consider a single time period.

## Delta functions
Consider a regular pulse $f(\varepsilon,t)$ of unit area and width $\varepsilon$. The $\delta$ function is defined as the limit
$$
\delta(t)=\lim_{ \varepsilon \to \infty } f(\varepsilon,t)
$$
It can also be defined as the limiting case of other functions, e.g. the normal distribution and also
$$\frac{1}{\pi}{\mathrm{sinc(\varepsilon x)}}=\frac{1}{\pi}\frac{\sin(\varepsilon x)}{ \varepsilon x}$$
which again has unit area. Hence,
$$
\pi \cdot\delta(t)=\lim_{ \varepsilon \to \infty } \mathrm{sinc}(\varepsilon t)
$$
which is a useful result for many improper integrals.
### Sifting theorem
$$
f(a)= \int_{-\infty}^\infty f(t)\delta(t-a) \, \mathrm{d}t 
$$
#### Proof
Switching the limits and using the properties of the even $\delta$ function,
$$
\begin{align}
 & \qquad\int_{-\infty}^\infty f(t)\delta(t-a) \, \mathrm{d}t  \\
 & =\int_{-\infty}^\infty f(a)\delta(t-a) \, \mathrm{d}t  \\
 & =f(a)\int_{-\infty}^\infty \delta(t-a) \, \mathrm{d}t  \\
 & =f(a)
\end{align}
$$
