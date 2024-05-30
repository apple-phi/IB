## The Probability Density Function
The PDF is defined in terms of the CDF $F_{X}(x)=\operatorname{\mathbb{P}}[X\leq x]$
$$
f_{X}(x)=\frac{\mathrm{d} F_{X}}{\mathrm{d}x} 
$$
It is defined such that
$$
\operatorname{\mathbb{P}}[a\leq X<b]=\int_{a}^{b} f_{X} \, \mathrm{d}x 
$$
The support $\mathbb{X}$ of $X$ is typically extended to $\mathbb{R}$ by setting values outside of the domain to be $0$.

## Joint Probability Density Function
For two continuous random variables $X$ and $Y$ with joint CDF $F_{XY}(x,y)=\operatorname{\mathbb{P}}[X\leq x \cap Y\leq x]$, the joint PDF is
$$
f_{XY}(x,y)=\frac{\partial^{2}F_{XY} }{\partial x\partial y} 
$$
In this continuous formulation, marginalisation is stated as
$$
f_{X}=\int_{-\infty}^{\infty} f_{XY} \, \mathrm{d}y 
$$
and Bayes’ rule is
$$
f_{X|Y}(x,y)= \frac{f_{XY}}{f_{Y}}
$$
$X$ and $Y$ are independent if and only if
$$
\begin{align}
f_{XY} & =f_{X}f_{Y} \\
	\iff f_{X|Y} & =f_{X} \\
\iff f_{Y|X} & =f_{Y}
\end{align}
$$
Once again,
$$
\operatorname{\mathbb{E}}[g(X)]=\int_{-\infty}^{\infty} g\cdot f_{X} \, \mathrm{d}x 
$$
In particular, the $n\mathrm{th}$ moment is
$$
\operatorname{\mathbb{E}}[X^{n}]
$$
And the $n\mathrm{th}$ central moment is
$$
\operatorname{\mathbb{E}}[(X-\operatorname{\mathbb{E}}[X])^{n}]
$$
The mean is the first moment and the variance is the second central moment.

## PDF characteristics
- The standard deviation is $\sigma=\sqrt{ \operatorname{Var}[X] }$ 
- The mode is $x$ such that $f_{x}$ is maximised
- The median is $x$ such that $F_{X}=\frac{1}{2}$
- The $n\mathrm{th}$ quartiles are $x$ such that $F_{X}=\frac{n}{4}$
- The skewness is
$$
\frac{\operatorname{\mathbb{E}}[(X-\operatorname{\mathbb{E}}[X])^{3}]}{\sigma^{3}}
$$

## Exponential distribution
Consider $X_{t}\sim \operatorname{Po}(\lambda t)$ which models the number of successes $X_{t}$ during a time interval $t$ with average success rate $\lambda$.

To model the time interval $T$ between arrivals, consider the average time between arrivals in the interval $[t, t+\delta t]$
$$
f_{T}\delta t = \operatorname{\mathbb{P}}[t<T\leq t+\delta t]
$$
>Note that the event $\{ t<T\leq t+\delta t \}$ means:
>- No arrivals occur in the interval $[0,t]$
>- Exactly one arrival occurs between $[t,t+\delta t]$

$$
\begin{align}
f_{T}\delta t & = \operatorname{\mathbb{P}}[X_{t}=0]\times \operatorname{\mathbb{P}}[X_{t}=1] \\
 & = \frac{(\lambda t)^{0}e^{-\lambda t}}{0!}\times\frac{(\lambda \delta t)^{1}e^{-\lambda \delta t}}{1!} \\
 & = \lambda e^{-\lambda t}e^{-\lambda\delta t}\delta t \\
 \\
\Rightarrow\quad f(T) & =\lim_{ \delta t \to 0 } \lambda e^{-\lambda t}e^{-\lambda\delta t} \\
 & =\lambda e^{-\lambda t}
 \end{align}
$$
A CRV $X\sim \operatorname{Exp(\lambda)}$ is modelled by an exponential distribution under the support $\mathbb{X}=[0,\infty)$ if
$$
f_{X}=\lambda e^{-\lambda x}
$$
### Cumulative distribution
$$
F_{X}=1-e^{-\lambda x}
$$
### Expectation
$$
\operatorname{\mathbb{E}}[X]= \frac{1}{\lambda}
$$
### Variance
$$
\operatorname{\mathbb{E}}[X^{2}]= \frac{2}{\lambda^{2}}
$$
### Mode
The maximum value of $f_{X}$ is at $x_{\max}=0$.

### Median
$$
Q_{\frac{1}{2}}= \frac{\ln2}{\lambda}
$$
### $n\mathrm{th}$ quartile
$$
Q_{\frac{n}{4}}=\frac{-\ln\left( 1-\frac{n}{4} \right)}{\lambda}
$$
### Skewness
$$
\frac{\operatorname{\mathbb{E}}[(X-\operatorname{\mathbb{E}}[X])^{3}]}{\sigma^{3}}=2
$$

## The Gaussian distribution
A CRV $X\sim \mathcal{N}(\mu,\sigma^{2})$ is normally distributed with mean $\mu$ and variance $\sigma^{2}$ under continuous infinite support  $\mathbb{X=R}$ if
$$
f_{X}= \frac{1}{\sqrt{ 2\pi \sigma^{2}}}\exp\left\{ - \frac{(x-\mu)^{2}}{2\sigma^{2}} \right\}
$$
### Standard Gaussian
$$
\begin{align}
Z & \sim \mathcal{N}(0,1) \\
 \\
\Rightarrow\quad \mu+\sigma Z & \sim \mathcal{N}(\mu,\sigma^{2})
 \end{align}
$$
### Standard cumulative distribution
The CDF of $Z\sim \mathcal{N}(0,1)$ is
$$
\begin{align}
\phi(z) = F_{Z}(z) & = \frac{1}{\sqrt{ 2\pi }}\int _{-\infty}^{z}e^{- \frac{x^{2}}2{}} \, \mathrm{d}x \\
 & =\frac{1}{2}+\frac{1}{2}\operatorname{erf}\left( \frac{z}{\sqrt{ 2 }} \right)
 \end{align}
$$
### Expectation
$$
\operatorname{\mathbb{E}}[X]=\mu
$$
### Variance
$$
\operatorname{Var}[X]=\sigma^{2}
$$
### Mode
$$
x_{\max}=\mu
$$
### Median
$$
Q_{\frac{1}{2}}=\mu
$$
### Quartile
Find from $Z$-distribution rescaling.

### Skewness
The distribution is symmetric and has no skew.

### Confidence interval
Under multiple independent tests, the $p\%$ confidence interval is the mean-centred interval in which $p\%$ of test values lie.

## Beta distribution
Suppose we observe that $k$ of $n$ Bernoulli trials are successes. What is the PDF of the Bernoulli parameter $p$ given this observation?

![[beta-dist.png]]

Under the Binomial distribution,
$$
P_{k|p}(k|p)= {n \choose k}p^{k}q^{n-k}
$$
Under Bayes rule,
$$
\begin{align}
f_{p|k}(p|k)  & = \frac{P_{k|p}f_{p}}{\int _{0}^{1} P_{k|p}f_{p}\, \mathrm{d}p }
\end{align}
$$
We take the *prior* that before any observations, all values of $p\in[0,1]$ are equally likely, i.e. $f_{p}(p)=1$ 

Then eventually we find that
$$
\begin{align}
f_{p|k}(p|k) = (n+1){n \choose k}p^{k}q^{n-k}
\end{align}
$$
A random variable $X\sim \operatorname{Beta}(\alpha,\beta)$ under continuous finite support $\mathbb{X}=[0,1]$ is said to be Beta distributed with shape parameters $\alpha,\beta>0$ if
$$
f_{X} = \frac{\Gamma(\alpha +\beta)}{\Gamma(\alpha)\Gamma(\beta)}x^{\alpha-1}(1-x)^{\beta-1}
$$
where the Gamma function is defined as
$$
\Gamma(x+1)=\int _{0}^{\infty}t^{x}e^{-t} \, \mathrm{d}t 
$$
### Expectation
$$
\operatorname{\mathbb{E}}[X]=\frac{\alpha}{\alpha+\beta}
$$
### Variance
$$
\operatorname{Var}[X]= \frac{\alpha\beta}{(\alpha+\beta)^{2}(\alpha+\beta+1)}
$$

### Mode
$$
x_{\max}= \frac{\alpha-1}{\alpha+\beta-2}
$$

### Skewness
$$
\frac{\operatorname{\mathbb{E}}[(X-\operatorname{\mathbb{E}}[X])^{3}]}{\sigma^{3}}= \frac{2(\beta- \alpha)\sqrt{ \alpha+\beta+1 }}{(\alpha+\beta+2)\sqrt{ \alpha \beta }}
$$

>Note that there are no closed-form expressions for the quartiles.


