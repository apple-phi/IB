## Bernoulli distribution
A binary DRV $X$ with discrete finite support $\mathbb{X}=\{ 0,1 \}$ has a Bernoulli distribution $X\sim \operatorname{Ber}(p)$ with parameter $p$ if
$$
P_{X}(k)=\begin{cases}
\begin{aligned}
&p &&\mathrm{if}\  k=1\\
&1-p &&\mathrm{if}\ k=0\\
&0 &&\mathrm{otherwise}
\end{aligned}
\end{cases}
$$

### Expectation
$$
\mathbb{E}[X]=p
$$
### Variance
$$
\operatorname{Var}[X]=p(1-p)=pq
$$
### Entropy
$$
\mathbb{H}[X]=\mathcal{H}_{2}(p)=-p\log_{2}p-q\log_{2}q
$$

>Note: $\mathcal{H}_{2}$ is known as the *binary entropy function*, which is maximised at $p=\frac{1}{2}$, as per our intuition.

## Geometric distribution
The geometric distribution $X\sim \mathrm{Geo}(p)$ of a DRV $X$ with discrete infinite support $\mathbb{X}=\mathbb{Z^{+}}$ which distributes the first success after $k$ trials of success probability $p$ is
$$
P_{X}(k)=q^{k-1}p
$$
### Cumulative probability
$$
\operatorname{\mathbb{P}}[x\leq X]=1-q^{k}
$$
### Expectation
$$
\begin{align}
\operatorname{\mathbb{E}}[X] & =\sum\limits_{ k=1 }^{ \infty }kpq^{k-1} \\
 & =p\frac{\mathrm{d}}{\mathrm{d}q}\sum\limits_{ k=1 }^{ \infty }q^{k} \\
 & =p\frac{\mathrm{d}}{\mathrm{d}q}\left( \frac{q}{1-q} \right) \\
&=\frac{1}{p}
\end{align}
$$
### Variance
$$
\begin{align}
\operatorname{Var}[X]&=\operatorname{\mathbb{E}}[(X-)]
\end{align}
$$
$$
\begin{align}
\operatorname{Var}[X]&= \sum\limits_{ k=1 }^{\infty }(q^{k-1}p-\operatorname{\mathbb{E}}[X])^{2} \\
&=\sum\limits_{ k=1 }^{\infty }\left( q^{2k-2}p^{2}+\frac{1}{p^{2}} -2q^{k-1}\right) \\
&=\frac{p^{2}}{1-q^{2}} -\frac{2}{1-q}+\sum\limits_{ k=1 }^{ \infty } \frac{1}{p^{2}} \\
&=\frac{p^{2}-2(1+q)}{1-q^{2}}+\sum\limits_{ k=1 }^{ \infty } \frac{1}{p^{2}} \\
&=
\end{align}
$$
tbc
## Binomial distribution
tbc

## Poisson distribution

Given a success density of $\lambda$ successes per unit interval, the number of successes $X$ in the interval is distributed as $X\sim \operatorname{Po}(\lambda)$. The support of $X$ is discrete finite $\mathbb{X}=\mathbb{Z}_{\geq 0}$
$$
P_{X}(k)= \frac{\lambda^{k}e^{-\lambda}}{k!}
$$
### Proof from Binomial distribution
The number of successes $X$ in a subdivided unit internal follows a binomial distribution with $n$ trials and expected value $\lambda$ where $n$ is the number of subdivisions of the interval.
$$X\sim \lim_{ n \to \infty } \mathrm{B}\left( n, \frac{\lambda}{n} \right)$$
Hence the PMF is
$$
\begin{align}
P_{X}(k) & =\lim_{ n \to \infty } {n\choose k}\left( \frac{\lambda}{n} \right)^{k}\left( 1-\frac{\lambda}{n} \right)^{n-k}
\end{align}
$$
Using the result that
$$
\lim_{ n \to \infty }  \frac{1}{n^{k}}{n\choose k} = \frac{1}{k!}
$$
we obtain
$$
\begin{align}
P_{X}(k) & =\lim_{ n \to \infty } \frac{\lambda^{k}}{k!}\left( 1-\frac{\lambda}{n} \right)^{n-k} \\
 & = \frac{\lambda^{k}}{k!}\lim_{ n \to \infty }  \left( 1-\frac{\lambda}{n} \right)^{n} \\
 & =\frac{\lambda^{k}}{k!}e^{\lambda}
\end{align}
$$
In general,
$$
\mathrm{B}(n, p) \overset{n\to \infty}\longrightarrow\operatorname{Po}(np)
$$
### Expectation
$$
\operatorname{\mathbb{E}}[X]=\lambda
$$
### Variance
$$
\operatorname{Var}[X]=\lambda
$$

### Entropy
No closed form, but increases with $\lambda$ 
$$
\mathbb{H}[X]\overset{\lambda\gg 1}{\approx}\log_{2}\sqrt{ 2\pi e\lambda }
$$
