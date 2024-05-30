## 1.
For the mean, let $u= \frac{1}{2}\frac{x^{2}}{s^{2}},\ \mathrm{d}x=\frac{s}{2}\sqrt{ \frac{2}{u} }\,\mathrm{d}u,$ then
$$
\begin{align}
\operatorname{\mathbb{E}}[X]&= \int_{0}^{\infty} \frac{x^{2}}{s^{2}}e^{ -\frac{1}{2} \frac{x^{2}}{s^{2}} } \, \mathrm{d}x \\
&= \int_{0}^{\infty}2u \frac{s}{2}\sqrt{ \frac{2}{u} }e^{ -u }  \, \mathrm{d}u \\
&=\sqrt{ 2 }s \operatorname{\Gamma}\left( \frac{3}{2} \right) \\
&=\sqrt{ 2 }s\cdot \frac{1}{2} \operatorname{\Gamma}\left( \frac{1}{2} \right) \\
&=s \sqrt{ \frac{\pi}{2} }
\end{align}
$$
For the variance, making the same substitution $u=\frac{1}{2} \frac{x^{2}}{s^{2}}$ with $\mathrm{d}u=\frac{x}{s^{2}}\,\mathrm{d}x$ we have
$$
\begin{align}
\operatorname{\mathbb{E}}[X^{2}]-\operatorname{\mathbb{E}}[X]^{2}&= \int_{0}^{\infty} \frac{x^{3}}{s^{2}}e^{- \frac{1}{2}\frac{x^{2}}{s^{2}} }  \, \mathrm{d}x -\operatorname{\mathbb{E}}[X]^{2} \\
&=\int_{0}^{\infty} 2us^{2}e^{ -u } \, \mathrm{d}u -\operatorname{\mathbb{E}}[X]^{2}\\
&=2s^{2}\operatorname{\Gamma}(2)-\operatorname{\mathbb{E}}[X]^{2} \\
&=s^{2}\left( 2-\frac{\pi}{2} \right)
 \end{align}
$$
Then the standard deviation is
$$
\sigma=s\sqrt{ 2-\frac{\pi}{2} }
$$
The mode is $\arg \max f_{X}(x)$ and is satisfied by
$$
\begin{align}
0&=\partial_{x}f_{X} \\
&\propto -\frac{x^{2}}{s^{2}}e^{ - \frac{1}{2}\frac{x^{2}}{s^{2}} }+e^{ - \frac{1}{2}\frac{x^{2}}{s^{2}} } \\
\Rightarrow\quad \arg \max f_{X}(x)&=s
 \end{align}
$$
The quartiles are given by
$$
\begin{align}
\frac{n}{4}&=\int_{0}^{q_{_{n}}} \frac{x}{s^{2}}e^{ -\frac{1}{2}\frac{x^{2}}{s^{2}} } \, \mathrm{d}x \\
&=\left[ -e^{ -\frac{1}{2}\frac{x^{2}}{s^{2}} } \right] _{0}^{q_{n}} \\
&=1- e^{ -\frac{1}{2}\frac{q_{n}^{2}}{s^{2}} } \\
\Rightarrow\quad q_{n}&= s\sqrt{ -2\ln\left( 1-\frac{n}{4} \right) }
 \end{align}
$$
so the interquartile range is
$$
\begin{align}
\mathrm{IQR}&=q_{3}-q_{1} \\
&=s\sqrt{ 2\ln 4 }-s\sqrt{ 2\ln \frac{4}{3} } \\
&\approx0.907s
 \end{align}
$$
The skewness is the third standardised moment,
$$
\begin{align}
\tilde{\mu}_{3}&= \frac{\mu_{3}}{\sigma ^{3}} \\
&=\frac{1}{\sigma^{3}}\operatorname{\mathbb{E}}\left[ (X-\mu)^{3}\right]  \\
&=\frac{\operatorname{\mathbb{E}}[X^{3}]-3\mu\operatorname{\mathbb{E}}[X^{2}]+3\mu^{2}\operatorname{\mathbb{E}}[X]-\mu^{3}}{\sigma^{3}} \\
&= \frac{\operatorname{\mathbb{E}}[X^{3}]-3\mu\sigma^{2}-\mu^{3}}{\sigma^{3}}
\end{align}
$$
where $\operatorname{\mathbb{E}}[X^{3}]$ is given by making the same substitution $u=\frac{1}{2} \frac{x^{2}}{s^{2}}$ as before with $\mathrm{d}u=s^{2}x\,\mathrm{d}x\Leftrightarrow\mathrm{d}x=\frac{s}{\sqrt{ 2u }}\mathrm{d}u$
$$
\begin{align}
\operatorname{\mathbb{E}}[X^{3}]&=\int_{0}^{\infty} \frac{x^{4}}{s^{2}}e^{ -\frac{1}{2}\frac{x^{2}}{s^{2}} } \, \mathrm{d}x  \\
&=\int_{0}^{\infty} 4s^{2}u^{2}e^{ - \\
u }\cdot \frac{s}{\sqrt{ 2u }} \, \mathrm{d}u \\
&= \frac{4}{\sqrt{ 2 }}s^{3}\operatorname{\Gamma}\left( \frac{5}{2} \right) \\
&=\frac{4}{\sqrt{ 2 }}s^{3} \frac{3}{2}\cdot \frac{1}{2}\operatorname{\Gamma}\left( \frac{1}{2} \right) \\
&=3s^{3}\sqrt{ \frac{\pi}{2} } \\
&=3s^{2}\mu
 \end{align}
$$
so the skewness is
$$
\begin{align}
\tilde{\mu}_{3}&= \frac{3s^{3}\sqrt{ \frac{\pi}{2} }-3s^{3}\sqrt{ \frac{\pi}{2} }\left( 2-\frac{\pi}{2} \right)-\frac{\pi}{2}s^{3}\sqrt{ \frac{\pi}{2} }}{s^{3}\left( 2-\frac{\pi}{2} \right)\sqrt{ 2-\frac{\pi}{2} }} \\
&=\frac{3-3\left( 2-\frac{\pi}{2} \right)-\frac{\pi}{2}}{\left( 2-\frac{\pi}{2} \right)^{\frac{3}{2}}}\sqrt{ \frac{\pi}{2} } \\
&=\frac{\pi-3}{\left( 2-\frac{\pi}{2} \right)^{\frac{3}{2}}}\sqrt{ \frac{\pi}{2} }  \\
&\approx 0.63
 \end{align}
$$
which notably is invariant of $s.$

## 2.
Define the ball angle $X$ over a domain $\mathbb{X}=\left[ -\frac{\pi}{2}, \frac{\pi}{2} \right]$ s.t. $f_{X}= \frac{1}{\pi}.$ Then the expected change in momentum is
$$
\begin{align}
\operatorname{\mathbb{E}}[\Delta p]&=2\operatorname{\mathbb{E}}[mv\cos(X)] \\
&=2\int_{\mathbb{X}} \frac{mv}{\pi}\cos x  \, \mathrm{d}x  \\
&=\frac{4mv}{\pi} \\
&=\pu{-0.0127kg/s}
 \end{align}
$$
so the net momentum change per unit second in the direction that the ball ends up heading is
$$
F=-\dot{n}\operatorname{\mathbb{E}}[\Delta p]=\pu{0.127N}
$$
## 3.
For a $\mathrm{DRV}$ $X$ over a domain $\mathbb{X}=\mathbb{N}_{0},$
$$
\begin{align}
\operatorname{\mathbb{E}}[X]&=\sum\limits_{ x=0 }^{ \infty }xP_{X}(x) \\
&\geq \sum\limits_{x=t}^{\infty}xP_{X}(x) \\
&\geq \sum\limits_{x=t}^{\infty}tP_{X}(x) \\
&=t\sum\limits_{x=t}^{\infty}P_{X}(x) \\
&=t\operatorname{\mathbb{P}}[X\geq t]
 \end{align}
$$
This is Markov’s inequality. 

Now let $Y=(X-\operatorname{\mathbb{E}}[X])^{2}$ therefore
$$
\begin{align}
t^{2}\operatorname{\mathbb{P}}[Y^{2}\geq t^{2}]&=t^{2}\operatorname{\mathbb{P}}[\lVert X-\operatorname{\mathbb{E}}[X] \rVert \geq t] \\
&\leq \operatorname{\mathbb{E}}[Y^{2}] \\
&=\sigma^{2}-\operatorname{\mathbb{E}}[X]^{2} \\
&\leq\sigma^{2} \\
\Rightarrow\quad \operatorname{\mathbb{P}}[\lVert X-\operatorname{\mathbb{E}}[X] \rVert \geq t]&\leq \frac{\sigma^{2}}{t^{2}}
 \end{align}
$$

Now let $t=k\sigma$ then
$$
\operatorname{\mathbb{P}}[\lVert X-\operatorname{\mathbb{E}}[X] \rVert \geq k\sigma]\leq \frac{1}{k^{2}}
$$
Then the probability of an observation of $X$ being within $k\sigma$ of the mean is
$$
\operatorname{\mathbb{P}}[\lVert X-\mu \rVert\leq k\sigma ]\geq 1-\frac{1}{k^{2}}
$$
This is Chebyshev’s inequality. So a lower bound on the probability of $X$ being within two standard deviations of the mean is $\frac{3}{4}.$ 

Applying Markov’ inequality to the distribution $X\sim T,$ from the given information about $T$ we can say that
$$
\operatorname{\mathbb{P}}[T\geq2]\leq \frac{\operatorname{\mathbb{E}}[T]}{2}=\frac{1}{4}
$$
Applying Chebyshev’s inequality to $T$ gives
$$
\operatorname{\mathbb{P}}[\lVert T-\operatorname{\mathbb{E}}[T] \rVert \leq2.5\sigma]\geq 1-\frac{1}{2.5^{2}}=0.84
$$
For the case of the data [[transmission line]] with $X\sim \mathcal{B}(n,0.2),$ Markov’s inequality places the upper bound
$$
\operatorname{\mathbb{P}}[X\geq 4] \leq \frac{\operatorname{\mathbb{E}}[X]}{4}= \frac{np}{4}=0.5
$$
while, noting that $\operatorname{\mathbb{E}}[X\mid n=10]=2,$ Chebyshev’s inequality places the bound
$$
\operatorname{\mathbb{P}}[\lVert X-2 \rVert\geq 2 ]=\operatorname{\mathbb{P}}[X=0]+\operatorname{\mathbb{P}}[X\geq 4]\leq \frac{npq}{2^{2}}=0.4
$$
Since $\operatorname{\mathbb{P}}[X=0]=q^{n},$ the Chebyshev upper bound is
$$
\operatorname{\mathbb{P}}[X\geq 4]\leq 0.4-0.8^{10}=0.293
$$
We can calculate this quantity exactly as 
$$
\begin{align}
\operatorname{\mathbb{P}}[X\geq 4]&=\sum\limits_{ n=4 }^{ N }{N \choose n}p^{n}q^{N-n} \\
&=0.121
 \end{align}
$$
Similarly, for $n=1000,$ the Markov upper bound for $\operatorname{\mathbb{P}}[X\geq 4]$ is again $\frac{1}{2}$ while the Chebyshev upper bound is $0.004.$

## 4.
tbc just calculator work

## 5.
The $\mathrm{MGF}$ is given for an exponential distribution with $\lambda>0$ by
$$
\begin{align}
\operatorname{g}(s)&=\operatorname{\mathbb{E}}[e^{sX}] \\
&=\int_{0}^{\infty} e^{sx}\lambda e^{-\lambda x} \, \mathrm{d}x  \\
&=\left[\frac{\lambda}{s-\lambda}e^{ (s-\lambda)x }  \right] _{0}^{\infty} \\
&= \frac{\lambda}{\lambda-s}
 \end{align}
$$
Then its expectation and variance are
$$
\begin{align}
\operatorname{\mathbb{E}}[X]&=\operatorname{g}'(0)=\lambda(\lambda-\cancel{s})^{-2}=\frac{1}{\lambda} \\
\operatorname{Var}[X]&=\operatorname{g''(0)}-\operatorname{\mathbb{E}}[X]=2\lambda(\lambda-\cancel{s})^{-3}-\operatorname{\mathbb{E}}[X]=\frac{1}{\lambda^{2}}
\end{align}
$$
so we have the relation $\operatorname{Var}[X]=\operatorname{\mathbb{E}}[X]^{2}.$ For the Poisson distribution, we instead have $\operatorname{\mathbb{E}}[X]=\operatorname{Var}[X].$ Since this is the case for the sample data, the sample population appears to be Poisson distributed.

Look again! cf actual calc. and dimensional analysis.

# 6.
Consider the $\mathrm{PGF}$s of $X_{1}\sim \operatorname{Po}(\lambda_{1})$ and $X_{2}\sim \operatorname{Po}(\lambda_{2}).$ If $X_{1}+X_{2}\sim \operatorname{Po}(\lambda_{1}+\lambda_{2})$ then 
$$
\begin{align}
\operatorname{g_{1+2}}&=\operatorname{g_{1}}\times \operatorname{g_{2}} \\
&=e^{ \lambda_{1}(z-1) }\times e^{ \lambda_{2}(z-1) } \\
&=e^{ (\lambda_{1}+\lambda_{2})(z-1) } \\
&=\operatorname{g}_{1+2}
 \end{align}
$$
Modelling the emissions,
$$
\begin{align}
\operatorname{\mathbb{P}}[X_{1}+X_{2}=x]&=\frac{\lambda ^{x}}{x!}e^{ -\lambda } \\
&= \frac{10^{2}}{2!}e^{ -10 } \\
&=0.00227
 \end{align}
$$
For part (c), we can use a Skellam distribution (which will involve a modified Bessel function), or compute directly as
$$
\begin{align}
\operatorname{\mathbb{P}}[X_{1}=2X_{2}]&=\sum\limits_{ x=1 }^{ \infty }\operatorname{\mathbb{P}}[X_{1}=2x]\operatorname{\mathbb{P}}\left[ X_{2}=x \right] \\
&=\sum\limits_{ x=1 }^{ \infty } \frac{\lambda_{1}^{2x}}{(2x)!}e^{ -\lambda_{1} }\frac{\lambda_{2}^{x}}{x!}e^{ -\lambda_{2} } \\
&=0.025
\end{align}
$$
Given that $Z=3X_{1}-2X_{2},$ we can see that
$$
\begin{align}
\operatorname{\mathbb{E}}[Z]&=3\operatorname{\mathbb{E}}[X_{1}]-2\operatorname{\mathbb{E}}[X_{2}]=0 \\
\operatorname{Var}[Z]&=3^{2}\operatorname{Var}[X_{1}]+2^{2}\operatorname{Var}[X_{2}] =60
\end{align}
$$
## 7.
Consider the $\mathrm{MGF}$s of $X$ and $Y.$ Finding the $\mathrm{MGF}$ of $Z=X-Y$ gives
$$
\begin{align}
\operatorname{g}_{z}&=\operatorname{g}_{x}\operatorname{g}_{(-y)} \\
&=\exp\left( s\mu_{1}+\frac{1}{2}s^{2}\sigma^{2}_{1} \right)\exp\left( -s\mu_{2}+\frac{1}{2}s^{2}\sigma_{2}^{2} \right) \\
&=\exp\left( s(\mu_{1}-\mu_{2})+\frac{1}{2}s^{2}(\sigma_{1}^{2}+\sigma_{2}^{2}) \right)
 \end{align}
$$
which is the $\mathrm{MGF}$ of $\mathcal{N}(\mu_{1}-\mu_{2},\sigma_{1}^{2}+\sigma_{2}^{2})$ as expected.

tbc tedious calculation

## 8.
From the matrix relationship we can see that
$$
\begin{align}
Y_{1}&=X_{1} \\
Y_{2}&=X_{1}+\frac{1}{2}X_{2}=\mathcal{N}\left( \mu_{1}+\frac{1}{2}\mu_{2} ,\sigma_{1}^{2}+\frac{1}{4}\sigma_{2}^{2}\right)
\end{align}
$$
The desired probability is
$$
\begin{align}
\operatorname{\mathbb{P}}[Y_{2}\leq y_{2}\mid Y_{1}=y_{1}]&=\operatorname{\mathbb{P}}\left[ y_{1}+\frac{1}{2}X_{2}\leq y_{2} \right] \\
&=\operatorname{\mathbb{P}}[X_{2}\leq 2(y_{2}-y_{1})]
 \end{align}
$$
Hence the conditional density is
$$
\begin{align}
f_{Y_{2}\mid Y_{1}}(y_{2}\mid y_{1})&= \frac{\mathrm{d}F_{Y_{2}\mid Y_{1}} }{\mathrm{d}y_{2}}  \\
&=\frac{\mathrm{d} F_{X_{2}}(2(y_{2}-y_{1}))}{\mathrm{d}y_{2}}  \\
&=2f_{X_{2}}(2(y_{2}-y_{1})) \\
&=\frac{1}{\sqrt{ 2\pi } \frac{\sigma_{2}}{2}}\exp \left\{ -\left( \frac{y_{2}- \left( y_{1}+\frac{\mu_{2}}{2} \right)}{\sqrt{ 2 } \frac{\sigma_{2}}{2}} \right)^{2} \right\} 
 \end{align}$$
 That is, $Y_{2}\mid Y_{1}\sim \mathcal{N}\left( y_{1}+\frac{1}{2}\mu_{2}, \frac{1}{4}\sigma_{2}^{2}\right).$ Now the joint density is
$$
\begin{align}
f_{Y_{1},Y_{2}}(y_{1},y_{2})&=f_{Y_{2}\mid Y_{1}}(y_{2}\mid y_{1})\,f_{Y_{1}}(y_{1}) \\
&=\frac{1}{2\pi  \frac{\sigma_{1}\sigma_{2}}{2}}\exp \left\{ -\left( \frac{y_{2}- \left( y_{1}+\frac{\mu_{2}}{2} \right)}{\sqrt{ 2 } \frac{\sigma_{2}}{2}} \right)^{2} \right\} \exp \left\{ -\frac{(y_{1}-\mu_{1})^{2}}{2\sigma_{1}^{2}} \right\} 
 \end{align}
$$
Separately, the covariance matrix $\Sigma$ given by $\Sigma_{ij}=\operatorname{Cov}[X_{i},X_{j}]=\operatorname{\mathbb{E}}[X_{i}X_{j}]-\operatorname{\mathbb{E}}[X_{i}]\operatorname{\mathbb{E}}[X_{j}]$ is
$$
\Sigma=\begin{bmatrix}
\sigma_{1}^{2} & \sigma_{1}^{2} \\
\sigma_{1}^{2} & \sigma_{1}^{2}+\frac{1}{4}\sigma_{2}^{2}
\end{bmatrix}
$$
Testing at $\mu_{1}=\mu_{2}=0$ and $\sigma_{1}=\sigma_{2}=1,$
$$
\begin{align}
\Sigma&=\begin{bmatrix}
1 & 1 \\
1 & \frac{5}{4}
\end{bmatrix} \\
\Sigma ^{-1}&=4\begin{bmatrix}
\frac{5}{4} & -1 \\
-1 & 1
\end{bmatrix}
\end{align}
$$
So the alternate expression for the joint density
$$
\begin{align}
f_{X}(\mathbf{x})&= \frac{1}{\sqrt{ (2\pi)^{2}|\boldsymbol{\Sigma}| }}\exp\left( -\frac{1}{2}(\mathbf{x}-\boldsymbol{\mu})^{\dagger}\boldsymbol{\Sigma}^{-1}(\mathbf{x}-\boldsymbol{\mu}) \right) \\
&=\frac{1}{\pi}\exp \left\{ -2(y_{2}-y_{1})^{2} \right\} \exp \left\{ -\frac{1}{2}y_{1}^{2} \right\} 
 \end{align}
$$
which is consistent with the previous expression. 

If $\mathbf{x}$ is Gaussian then $A\mathbf{x}$ is also Gaussian, but the entries of $A\mathbf{x}$ are generally not independent.

## 9.
$$
\begin{align}
\mathcal{H}_{0}&:X\sim \operatorname{Po}(10) \\
\mathcal{H_{1}}&:X\nsim\operatorname{Po}(10)
\end{align}
$$
Under $\mathcal{H}_{0},$
$$
\operatorname{\mathbb{P}}[X\leq 4]=\sum\limits_{ x=1 }^{ 4 } \frac{10^{x}}{x!}e^{ -10 }=0.0292072881472<5\%
$$
so reject the null hypothesis. Only the second statement of the two given is true.

