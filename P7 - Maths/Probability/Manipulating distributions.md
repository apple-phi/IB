## DRVs
Consider a discrete random variable $X$ and a dependent variable $Y= f(X)$ for a function $f:\mathbb{X\to Y}$. In general,
$$
P_{Y}(y)=\sum_{\{ x\mid y=g(x) \}}P_{X}(x)
$$
If $g$ is invertible, then
$$
P_{Y}(y)=P_{X}(g^{-1}(y))
$$
### Example
With $X\sim \operatorname{Geo}(p)$ and $m\in\mathbb{Z^{+}}$, find the PMF of $Y=(X-1) \ \mathrm{mod}\ m$.

Observe that $Y=y$ if $X=m\mathbb{Z}^{+}+y+1$. Hence $\{ x\mid g(x)=y \}=\{ x=rm+y+1 \}_{r\in\mathbb{Z}_{>0}}$ so we conclude that
$$
\begin{align}
P_{Y}(y)&=\sum\limits_{ r=0 }^{ \infty }P_{X}(rm+y+1) \\
&=\sum\limits_{ r=0 }^{ \infty }pq^{rm+y} \\
&= \frac{pq^{y}}{1-q^{m}}
 \end{align}
$$
![[discrete-dist-manipulation.png]]

## CRVs
Consider the CDF of $Y=g(X)$ to be $F_{Y}(y)=\operatorname{\mathbb{P}}[g(X)\leq y]$
For $g$ to be strictly monotonic, we require
$$
\begin{align}
f_{Y=g(x)}(y)&= \frac{f_{X}(x)}{|g'(x)|}
 \end{align}
$$
### Proof
For $g$ to be monotonic, under the required conditions $F_{Y}(y)=\left|\pm F_{X}(x)+C\right|$ for some $C\leq 1$.

> E.g. $C=1$ in the case $F_{y}=\operatorname{\mathbb{P}}[Y\geq y]=1-F_{X}(g^{-1}(y))$ 

Therefore,
$$
\begin{align}
f_{Y}(y) & =f_{X}(x)\left|\frac{\mathrm{d} g^{-1}}{\mathrm{d}y}\right|  \\
&= \frac{f_{X}(x)}{|g'(g^{-1}(y))|}
 \end{align}
$$
## Sums of RVs
Let $X$ and $Y$ be two random variables. We are interested in their sum $S=X+Y$.

We have already seen that
$$
\operatorname{\mathbb{E}}[S]=\operatorname{\mathbb{E}}[X]+\operatorname{\mathbb{E}}[Y]
$$
and it is trivial to show that
$$
\operatorname{Var}[S]=\operatorname{Var}[X]+\operatorname{Var}[Y]+2\operatorname{Cov}[X,Y]
$$
where the covariance $\operatorname{Cov}[X,Y]$ is defined as 
$$
\operatorname{Cov}[X,Y]=\operatorname{\mathbb{E}}[XY]-\operatorname{\mathbb{E}}[X]\operatorname{\mathbb{E}}[Y]
$$
We can also define the correlation coefficient $\rho$ that satisfies $|\rho|<1$
$$
\rho= \frac{\operatorname{Cov}[X,Y]}{\sqrt{ \operatorname{Var}[X]\operatorname{Var}[Y] }}
$$
### The PMF of sums
Let $X$ and $Y$ be two DRV with joint PMF $P_{XY}(x,y)$ and $S=X+Y$. Employing the law of total probability,
$$
P_{S}(s)=\sum_{y\in\mathbb{Y}}P_{S\mid Y}(s\mid y)P_{Y}(y)
$$
where, by definition,
$$
\begin{align}
P_{S\mid Y}(s\mid y) & =\operatorname{\mathbb{P}}[S=s\mid Y=y] \\
&=\operatorname{\mathbb{P}}[X=s-y\mid Y=y] \\
&=P_{X\mid Y}(s-y\mid y)
 \end{align}
$$
Returning to the law of total probability,
$$
\begin{align}
P_{S} & =\sum_{y\in\mathbb{Y}}P_{X\mid Y}(s-y\mid y)P_{Y}(y) \\
&= \sum_{y\in\mathbb{Y}}P_{XY}(s-y,y) \\
&= \sum_{x\in\mathbb{X}}P_{XY}(x,s-x)
 \end{align}
$$
If $X$ and $Y$ are independent, this directly implies that
$$
\begin{align}
P_{S}(s)&=\sum_{x\in\mathbb{X}}P_{X}(x)P_{Y}(s-y) \\
&=P_{X}*P_{Y}
 \end{align}
$$
That is, the summed distribution $P_{X+Y}=P_{X}*P_{Y}$ is the discrete convolution of the distributions of $X$ and $Y$ 

An analogous analysis can be applied to CRVs to show that for continuous $X$ and $Y$ 
$$
f_{X+Y}=f_{X}*f_{Y}
$$

## Distribution transforms
Here we describe two useful transforms for RVs. Their properties make distribution manipulation easier, e.g. to find the distribution describing the sum of independent RVs.

### PGF
For a DRV $X$ with support $\mathbb{X}$, the probability generating function $G_{X}(z)$ defined by
$$
\begin{align}
G_{X}(z)&=\operatorname{\mathbb{E}}[z^{X}] \\
&=\sum_{k\in\mathbb{X}}z^{k}P_{X}(k)
 \end{align}
$$
Under this transform the expectation is
$$
\operatorname{\mathbb{E}}[X]= G_{X}'(1)
$$
and the variance is
$$
\operatorname{Var}[X]=G_{X}''(1)+G_{X}'(1)-{G_{X}'(1)}^{2}
$$
For the sum of independent RVs we know that combined expectations are separable,
$$
\operatorname{\mathbb{E}}[z^{X+Y}]=\operatorname{\mathbb{E}}[z^{X}z^{Y}]=\operatorname{\mathbb{E}}[z^{X}]\operatorname{\mathbb{E}}[z^{Y}]
$$
Hence
$$
G_{X+Y}=G_{X}\times G_{Y}
$$
Or, more generally,
$$
G_{\sum X_{i}}=\prod G_{X_{i}}
$$

### MGF
For a CRV $X$, the moment generating function $g_{X}(s)$ is
$$
\begin{align}
g_{X}(s)&=\operatorname{\mathbb{E}}[e^{sX}] \\
&=\int_{-\infty}^{\infty} e^{sx}f_{X}(x) \, \mathrm{d}x 
 \end{align}
$$
Under this transform, the expectation is
$$
\operatorname{\mathbb{E}}[X]=g_{X}'(0)
$$
and the variance is
$$
\operatorname{Var}[X]=g_{X}''(0)-g_{X}'(0)
$$
Also, just like for the PGF, for independent $X$ and $Y$ 
$$
g_{X+Y}=g_{X}\times g_{Y}
$$
Or, more generally,
$$
g_{\sum X_{i}}=\prod g_{X_{i}}
$$
## Central limit theorem
The above transforms can be applied to show the central limit theorem that repeated summation of random variables of any distribution tends to a normal distribution with $\mu=\operatorname{\mathbb{E}}\left[ \sum X \right]=\sum \mu _i$ and $\sigma^{2}=\operatorname{Var}\left[ \sum X \right]=\sum \sigma_{i}$

In particular,
$$
\lim_{ n \to \infty } \operatorname{Bin}(n,p)=\mathcal{N}(np,npq)
$$
>Experimental noise can be effectively modelled by a Gaussian distribution since it comes from the sum of many independent distributions.
## Multivariate Gaussians
An $n$-dimensional random vector $\mathbf{X}\sim \mathcal{N}(\boldsymbol{\mu},\boldsymbol{\Sigma})$ is normally distributed if
$$
f_{X}(\mathbf{x})= \frac{1}{\sqrt{ (2\pi)^{n}|\boldsymbol{\Sigma}| }}\exp\left( -\frac{1}{2}(\mathbf{x}-\boldsymbol{\mu})^{\dagger}\boldsymbol{\Sigma}^{-1}(\mathbf{x}-\boldsymbol{\mu}) \right)
$$
where $\boldsymbol{\mu}=\operatorname{\mathbb{E}}[\mathbf{X}]$ is the mean vector and $\boldsymbol{\Sigma}$ is the symmetric $n\times n$ covariance matrix such that
$$
\Sigma_{ij}=\operatorname{\mathbb{E}}[(X_{i}-\mu_{i})(X_{j}-\mu_{j})]
$$
>Note that $\Sigma_{i\neq j}=\operatorname{Cov}[X_{i},X_{j}]$ and $\Sigma_{i=j}=\operatorname{Var}[X_{i}]$

The marginals and partial marginals of a multivariate Gaussian are also Gaussian.

The components of $\mathbf{X}$ are mutually independent if $\boldsymbol{\Sigma}$ is diagonal.

The conditional given by 
$$
f_{X_{1}\mid X_{2}=x_{2}}=\mathcal{N}\left( \mu_{1}+\rho \frac{\sigma_{1}}{\sigma_{2}}(x_{2}-\mu_{2}), \left(1-\rho^{2}\right)\sigma_{1}^{2}\right)
$$
is also Gaussian. Multivariate conditionals are also Gaussian.
