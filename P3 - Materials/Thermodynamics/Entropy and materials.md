#materials
## Microstates
To quantify entropy, we discretise the possible system states and use the following relation between entropy $S$ and the number of microstates $\Omega$: $$S=k_{B}\ln\Omega$$where $k_B$ is the Boltzmann constant:$$k_B=1.380649\times10^{-23}\mathrm{J/K}$$The use of the logarithm is to ensure that entropy is extensive—combining two systems gives a system where the number of microstates is the product (not the sum) of the number of microstates in the components.

## Entropy of mixing
The number of unique ways to combine two components of $n_a$ and $n_b$ atoms respectively where individual atoms within each component are indistinguishable is given by:$$\Omega={n\choose n_a}=\frac{n!}{n_a!\cdot n_b!}$$where $n=n_a+n_b$. Therefore the change of entropy upon mixing is $$\Delta S=k_b\ln\left(\frac{n!}{n_a!\cdot n_b!}\right)$$However, this challenges the assumption of extensibility of $S$, which implies:$$S\propto n$$We can use Stirling’s approximation,$$\ln(x!)\approx x\ln x-x$$ for large $x$ to investigate this further. For large $n$, with constant $\frac{n_{a}}{n}$ and $\frac{n_{b}}{n}$,
$$
\begin{align*}
\ln\Omega&\approx n\ln n-n-\left(n_a\ln n_{a}-n_{a}+n_{b}\ln n_{b}-n_{b}\right)\\
&=\underbrace{n}_{n_a+n_{b}}\ln n-n_{a}\ln n_{a}-n_{b}\ln n_{b}\\
&= -n_{a}\ln\left( \frac{n_{a}}{n}\right)-n_{b}\ln\left(\frac{n_{b}}{n}\right)\\
&= -n\left[\frac{n_{a}}{n}\ln\left( \frac{n_{a}}{n}\right)+ \frac{n_{b}}{n} \ln\left(\frac{n_{b}}{n}\right)\right]\\
&\propto n\\\\
\Rightarrow\quad\Delta S&= k_b\ln\Omega\\
&\approx k_{b}\cdot n
\end{align*}
$$
Hence extensibility holds on a macroscopic level.
## Entropy of an ideal gas
Consider an ideal gas trapped in a piston. From the first and second [[Laws of Thermodynamics|laws of thermodynamics]]: $$T\mathrm{d}S=\cancel{\mathrm{d}U}+p\mathrm{d}V$$We know $\mathrm{d}U=0$ because a change in volume does not change the internal energy of an ideal gas. To solve this expression, it is useful to have an expression for $\frac{\partial S}{\partial V}$.

Let’s begin from the expression of entropy in terms of microstates. In an ideal gas, particles do not interact, so their velocities are independent of their positions. Thus,$$\Omega=\Omega_{p}\cdot\Omega_{v}=\Omega_{p}(V)\cdot\Omega_{v}(T)
$$with $\Omega_p$ being only a function of volume and $\Omega_v$ being only a function of temperature. Hence,$$
\begin{align*}
S&=k_{B}\ln\left(\Omega_{p}\cdot\Omega_{v}\right)\\
&= k_B\left[\ln \Omega_{p}(V)+\ln \Omega_v(T)\right]\\\\
\Rightarrow\quad\frac{\partial S}{\partial V}&= \frac{k_B}{\Omega_{p}}\frac{\partial \Omega_p}{\partial V}
\end{align*}
$$Assuming particle positions do not constrain each other, and the number of microstates of a single particle scales with the bounding volume,$$\Omega_{}p\propto V^{n}$$Hence,$$
\begin{align*}
\frac{\partial S}{\partial V}&= \frac{k_B}{V^n}\frac{\partial V^n}{\partial V}\\
&= \frac{k_B}{V^{n}}\cdot nV^{n-1}\\
&= \frac{k_{b}n}{V}\\
\end{align*}
$$Using $T\mathrm{d}S=p\mathrm{d}V$ from above,$$\begin{align*}
\frac{p}{T}&= \frac{\partial S}{\partial V}\\
&= \frac{k_{b}n}{V}\\
\\
\Rightarrow\quad pV = nk_{B}T
\end{align*}
$$This is also commonly and equivalently written as $$pV=NRT$$ where $R=\mathcal{N}_{A}k_{B}$ and $N=\frac{n}{\mathcal{N}_{A}}$.
## Equipartition Theorem
Each quadratic degree of freedom (i.e., has an associated energy proportional to $v^2$) contributes $\frac{1}{2}k_{B}T$ to the average molecular energy of the ideal gas.

Hence, the internal energy of an ideal gas of $N$ monatomic particles is$$U=\frac{3}{2}Nk_{B}T$$
