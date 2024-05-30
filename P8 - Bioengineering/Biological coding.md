## Information

For a $\mathrm{DRV}$ $X,$ the measure of surprise to a specific value of $X=x$  that occurs with probability $p$ is
$$
\operatorname{h}(x)=\log \frac{1}{p}
$$
The total entropy of $X$ is
$$
\operatorname{H}[X]=\operatorname{\mathbb{E}}[\operatorname{h}(X)]=\sum_{x\in \mathbb{X}} p_{x}\log \frac{1}{p_{x}}
$$

The distribution that maximises the uncertainty is the uniform distribution.

## Mutual information

The mutual information between $X$ and $Y$ is the reduction in entropy in one due to knowing the other.

$$
\begin{align}
\operatorname{M}_{XY}&=\operatorname{H}[X]-\operatorname{H}[X\mid Y] \\
&=\operatorname{H}[Y]-\operatorname{H}[Y\mid X] \\
&=\sum P_{X Y}\log \frac{P_{XY}}{P_{X}P_{Y}} 
 \end{align}
$$

This is symmetric, non-negative

This is the special case of the Kullback-Leibler divergence,
$$
D_{KL}(P\mathrel{||}Q)=
$$



tbc

## Efficient coding

Maximise $I_{r,s}$ given control of $\operatorname{P}(r\mid s).$

![[efficient-coding.png]]

## Maximum entropy for a single neuron

Find $P_{r}(r)$ that maximises $H_{r}(r),$ subject to the boundary conditions.

Assume:
- $\operatorname{P}(r\mid s)\to\delta(r-f(s))$
-  $H_{r\mid s}\to0$ 

where $f(s)$ is the monotonically increasing tuning curve, s.t.
$$
\begin{align}
P_{r}(r)&= \frac{P_{s}(s)}{|f'(s)|}
 \end{align}
$$
### Example
Consider the case that $r$ is subject to the constraint $|r|\leq r_{\max}.$ It turns out that under these conditions, the maximum entropy distribution is the uniform distribution $P_{r}= \frac{1}{r_{\max}}.$

Then by definition of $f(s)$ we have 
$$
\begin{align}
f(s)&=r_{\max}P_{s}(s) \\
&=r_{\max}\int_{\mathbb{S}}P_{s}(s')  \, \mathrm{d}s' 
 \end{align}
$$
That is, the tuning curve is proportional to the stimulus CDF.

![[histogram-equalisation.png|400]]

## Whitening in the retina

Assume $f(s)$ is a linear filter that is translation-invariant across the visual field (so different retinal cells can use the same filter

**tbc I don’t understand what’s going on**