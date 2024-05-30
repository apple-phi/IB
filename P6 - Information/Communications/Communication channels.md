A channel is the medium used to transmit the signal from transmitter to receiver.
- Introduces attenuation and noise
- So the received signal is a faded and noisy version of what the transmitter sent—this can cause errors

## Modelling a channel
Model them as a linear system with additive noise. The output $y$ given input $x$ and noise addition $n$ through transfer function $h$ satisfies
$$
\begin{align}
y&=h*x+n \\
Y&=HX+N
 \end{align}
$$
If the input is bandlimited to where the transfer function $H(\omega)$ is constant, then
$$
\begin{align}
y&=x+n \\
Y&=X+N
 \end{align}
$$
This is a common model.

## Modelling the noise
The origin of noise $n$ is thermal noise at the Rx due to thermal agitation of electrons.

Model $n$ as independent samples from a normal distribution.
![[additive-gaussian.png]]
## Real-world channels
Mobile wireless channel
- Distortion of the signal by multipath propagation and mobility

Optical fibre channel
- Very large [[bandwidth]], cheap production, low attenuation
- Disperses optical pulses
- Expensive regenerators required

Electrical wire channel
- Twisted pair cables (e.g., Ethernet) have limited [[bandwidth]], high attenuation
- Cheap, used for short distances

