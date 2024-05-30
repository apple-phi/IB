A discrete random variable $X$ is a function of the outcomes of a random experiment, $X : \Omega\to \mathbb{X}$, that takes a discrete set of scalar values forming $\mathbb{X}\subseteq \mathbb{R}$ where $\mathbb{X}$ is known as the *support* or the *alphabet* of $X$.

The *probability mass function (PMF)* of a DRV is the function
$$
\begin{align}
P_{X} & :\mathbb{X}\to [0,1] \\ \\
P_{X}(x) & =\mathbb{P}[X=x]
\end{align}
$$
Note that the events $X=a$ and $X=b$ are disjoint if $a\neq b$ so
$$
\sum_{x \in \mathbb{X}}P_{X}(x)=1
$$
For $x\not\in\mathbb{X}$, we can set $P_{X}(x)=0$ because $[X=x]=\emptyset$.

The cumulative distribution function (CDF) is
$$
F_{X}(x)=\mathbb{P}[X\leq x]=\sum_{\xi\leq x}P_{X}(\xi)
$$
Note that
- The CDF is non-decreasing, $F_{X}(a)\leq F_{X}(b)$
- $\displaystyle\lim_{ x \to -\infty }F_{X}(x)=0$ and $\lim_{ x \to +\infty }F_{X}(x)=1$ 
- $\mathbb{P}[a<X\leq b]=F_{X}(b)-F_{X}(a)$

## Multivariate PMFs
For two random variable $X:\Omega\to \mathbb{X}$ and $Y:\Omega\to \mathbb{Y}$ defined on the same sample space, we define the *joint probability probability mass function* as
$$
\begin{align}
P_{XY} & :\mathbb{X}\times \mathbb{Y}\to [0,1] \\
 \\
P_{XY}(x,y) & =\mathbb{P}[X=x\cap Y=y]
\end{align}
$$
Then [[conditional probability]] is
$$
\begin{align}
P_{X|Y} & :\mathbb{X}\times \mathbb{Y}\to [0,1] \\ \\
P_{X|Y}(x,y) & = \frac{P_{XY}(x,y)}{P_{Y}(y)}
\end{align}
$$
The law of total probability is
$$
P_{X}(x)=\sum_{y\in\mathbb{Y}}P_{XY}(x,y)
$$
and is also known as marginalisation.

Bayes’ rule is
$$
P_{Y|X}(y|x)= \frac{P_{X|Y}(x|y)\,P_{Y}(y)}{P_{X}(x)}
$$

Two random variables $X$ and $Y$ are independent $\iff$ all the events corresponding to values of $X$ are independent of all the events corresponding to values of $Y$:
$$
\begin{align}
P_{XY}(x,y) & =\mathbb{P}[X=x\cap Y=y] \\
 & =\mathbb{P}[X=x]\times \mathbb{P}[Y=y] \\
  & =P_{X}(x)\cdot P_{Y}(y) \\
	 & =\forall x,y\in\mathbb{X}\times \mathbb{Y}
\end{align}
$$
For more than two random variables, we can define the joint multivariate PMF as
$$
P_{X_{1},X_{2},\dots X_{n}}(x_{1}, x_{2}, \dots x_{n})
$$
The variables are mutually independent if 
$$
\begin{align}
P_{X_{1},X_{2},\dots X_{n}}(x_{1}, x_{2}, \dots x_{n})&=P_{X_{1}}(x_{1})\,P_{X_{2}}(x_{2})\,\dots P_{X_{n}}(x_{n}) \\ \\
&\:\,\forall x_{1},x_{2},x_{n}\in\mathbb{X}_{1}\times \mathbb{X}_{2}\times\dots \mathbb{X}_{n}
\end{align}
$$
For more than two variables, this is different from pairwise independence, which only requires that
$$
P_{X_{i}X_{j}}(x_{i}, x_{j})=P_{X_{i}}(x_{i})\,P_{X_{j}}(x_{j}) \qquad\forall x_{i},x_{j}\in\mathbb{X}_{i}\times \mathbb{X}_{j}
$$

## XOR gate
Consider two identically distributed independent binary DRVs $X$ and $Y$ with $P_{X}=P_{Y}$ such that
$$
P_{X}(x)=\begin{cases}
\begin{aligned}
&\frac{1}{2} &x\in\{ 0,1 \}\\
&\:0 & \mathrm{otherwise}
\end{aligned}
\end{cases}
$$
A third DRV $Z$ is defined as
$$
Z=X\oplus Y
$$
By considering the joint distribution of $X$, $Y$ and $Z$, we can show that they are pairwise independent but not mutually independent.

## Expectation
The expectation is the “centre of mass-weighted” of the distribution,
$$
\mathbb{E}[X]=\sum_{x\in\mathbb{X}}xP_{X}(x)
$$
More generally, we can define the expectation of any function of any number of random variables:
$$
\mathbb{E}[g(X)]=\sum_{x_{\mathbb{X}}}g(x)P_{X}(x)
$$
Note that expectation is linear,
$$
\mathbb{E}[aX+bY]=a\operatorname{\mathbb{E}}[X]+b \operatorname{\mathbb{E}}[Y]
$$
For two independent random variables $X$ and $Y$ 
$$
\mathbb{E}[X\times Y] = \operatorname{\mathbb{E}}[X]\cdot\operatorname{\mathbb{E}}[Y]
$$
If this property holds, $X$ and $Y$ are said to be *uncorrelated*

>Note that $X$ and $Y$ being uncorrelated does not imply independence.

## Variance

The expectation can be used to further characterise a probability function by calculating its central moment. The $n\mathrm{th}$ central moment is
$$
\mathbb{E}[(X-\mathbb{E}[X])^{n}]
$$
Some common central moments are:
- 2nd—the variance:$$\begin{align}
\operatorname{Var}[X]&=\mathbb{E}[(X-\mathbb{E}[X])^{2}] \\
&=\mathbb{E}[X^{2}]-{\mathbb{E}[X]}^{2}
\end{align}$$
- 3rd—a measure of the asymmetry
- 4th—a measure of the tailed-ness

## Entropy

The information content of a random variable $X$ is
$$
I_{X}(x)=-\log_{2}P_{X}(x)
$$
And the entropy in bits is the average of the information content,
$$
\begin{align}
\mathbb{H}[X] & =\mathbb{E}[I_{X}]  \\
& = \sum_{x\in\mathbb{X}}I_{X}(x)P_{X}(x)
\end{align}
$$
