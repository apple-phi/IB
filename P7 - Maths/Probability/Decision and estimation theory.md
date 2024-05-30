Suppose that the PDF (or PMF) of an RV $X$ is a function $f_{X}(x,\theta)$ that depends on a parameter $\theta$ 

We wish to find the value of $\theta$ from observations of $X$
- If the support of $\theta$ is continuous, we want to estimate it
- If the support of $\theta$ is discrete, we want to decide which value it takes

We define an observation $x$ as a measurement of $X$.

We define the sample as the set of RVs underlying the observations $\mathbf{X}$. These are usually independent and identically distributed (i.i.d.).

The estimate (or decision) is a function $\hat{\theta}(\mathbf{x})$ of all the observations.

The estimator (or decision rule) is the corresponding RV $\hat{\Theta}=\hat{\theta}(\mathbf{X})$

## In Bayesian stats
- The unknown parameter $\theta$ is viewed as the value of the random variable $\Theta$ 
- The distribution of the sample is interpreted as the conditional distribution $f_{\mathbf{X}\mid\Theta}(\mathbf{x}\mid\theta)$
- The *prior* is used to assign a PDF (or PMF) to $\Theta$
- The problem of estimating / deciding $\theta$ is then equivalent to predicting the value $\theta$ takes from $\Theta$ 
Some definitions:
- The prior function $f_{\Theta}(\theta)$
- The likelihood function $f_{\mathbf{X}\mid\Theta}(\mathbf{x}\mid\theta)$
- The posterior function $f_{\Theta \mid \mathbf{X}}(\theta \mid \mathbf{x})$

>The posterior function is obtained from Bayes’ rule.
## Common estimators
### Maximum likelihood (ML) estimator
$$
\hat{\theta}_{\mathrm{ML}}(\mathbf{x})=\arg\max f_{\mathbf{X}\mid\Theta}(\mathbf{x}\mid\theta)
$$
### Maximum *a posteriori* (MAP) estimator
$$
\hat{\theta}_{\mathrm{MAP}}=\arg\max f_{\Theta \mid\mathbf{X}}(\theta \mid \mathbf{x})
$$
If $f_{\Theta}(\theta)$ is constant then ML is equivalent to MAP
### Minimum mean squared error (MMSE)
$$
\begin{align}
\hat{\theta}_{\mathrm{MMSE}}(\mathbf{x})&=\arg\min \operatorname{\mathbb{E}}[(\theta-\Theta )^{2}\mid \mathbf{X}=\mathbf{x}] \\
&= \operatorname{\mathbb{E}}[\Theta \mid \mathbf{X}=\mathbf{x}]
 \end{align}
$$
## Example
We draw $n$ observations of the CRV $X\sim \mathcal{N}(\theta,1)$ from the i.i.d. sample $\mathbf{X}$. We will find the ML estimator.

The likelihood function (by applying *conditional independence*) is
$$
\begin{align}
f_{\mathbf{X}\mid\Theta}(\mathbf{x}\mid\theta)&=\prod_{i=1}^{n}f_{X_{i}\mid\Theta}(x_{i}\mid\theta) \\
&= \frac{1}{\sqrt{ (2\pi)^{n} }}\exp\left( -\frac{1}{2}\sum\limits_{ i=1 }^{ n }(x_{i}-\theta)^{2} \right)
 \end{align}
$$
So maximising the likelihood function is equivalent to minimising $\sum\limits_{ i=1 }^{ n }(x_{i}-\theta)^{2}$ so
$$
\hat{\theta}_{\mathrm{ML}}=\bar{\mathbf{x}}
$$