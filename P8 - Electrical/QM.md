De Broglie
$$
\lambda=\frac{h}{p}
$$
Wave-vector
$$
k=\frac{2\pi}{\lambda}
$$
Momentum
$$
p=mv=\hbar k
$$
Photon energy
$$
E=hf=\hbar\omega
$$
where $\hbar$ is the reduced Planck’s constant.

## Wave functions

Wave-function $\psi$  describes all measurable parameters. $\braket{ \psi \mid  \psi}$ is the probability of finding the object within the domain of that inner product.

Momentum operator
$$
\operatorname{\hat{p}}=\frac{\hbar}{i}\frac{\partial }{\partial x} 
$$
Energy operator
$$
\operatorname{\hat{E}}=-\frac{\hbar}{i}\frac{\partial }{\partial t} 
$$
### Example
Consider the plane wave $\psi \propto e^{ i(kx-\omega t) },$ then by applying the momentum operator we obtain the De Broglie relationship.
$$
\begin{align}
\operatorname{\hat{p}}\psi&= \frac{\hbar}{i} \frac{\partial \psi}{\partial x}  \\
&=\hbar k\psi \\
&= \frac{h}{\lambda}\psi
\end{align}
$$

## Schrödinger's equation

For momentum operator $\operatorname{\hat{p}},$ potential operator $\operatorname{\hat{V}}$ and energy operator $\operatorname{\hat{E}},$ by conserving energy, the time independent Schrödinger's equation is
$$
\begin{align}
\underbrace{ \left( - \frac{1}{2} \frac{\operatorname{\hat{p}}^{2}}{m} \right)\psi}_{ \text{kinetic energy} }+\underbrace{ \operatorname{\hat{V}}\psi}_{ \text{potential energy} }&=\underbrace{ \operatorname{\hat{E}}\psi}_{ \text{total energy} } \\ \\
\Rightarrow\quad  - \frac{1}{2} \frac{\hbar^{2}}{m}\frac{ \partial^{2} \psi}{ {\partial x}^{2} } + \operatorname{\hat{V}}\psi&= -\frac{\hbar}{i}\frac{\partial \psi}{\partial t}
\end{align}
$$

>When a wave encounters a discontinuity in potential, it will scatter or reflect.

### Example

In this example the incident wave of amplitude $A_{1}$ matches the reflected wave of amplitude $B_{1}$ to produce a standing wave.

Reflection probability 
$$
R = \left| \frac{B_{1}}{A_{1}} \right| ^{2}
$$

Transmission probability 
$$
T=1-R
$$

![[wave-function-discontinuity.png|500]]


### Heisenberg’s uncertainty principle

Trade-off between accuracy in measurements of position and momentum.

$$
\Delta p\Delta x\geq\frac{\hbar}{2}
$$
