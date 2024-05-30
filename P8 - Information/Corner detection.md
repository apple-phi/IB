[[Edge detection]] is insufficient in some cases, e.g. when analysing image motion. This is the *aperture problem*.

![[Aperture_problem_animated.gif]]
>*Which direction is the image moving?*

So we need to detect corners to detect the direction of motion.

## Correlation
A useful operator is the cross-correlation of two functions. It is defined as
$$
\begin{align}
f\star g &=  \overline{ f(-t)}*g \\
&=\int_{\mathbb{R}} \overline{ f(-\tau)}\,g(t-\tau) \, \mathrm{d}\tau \\
&=\int_{\mathbb{R}} \overline{ f(\tau)}\,g(t+\tau) \, \mathrm{d}\tau 
 \end{align}
$$
There is only commutativity $f\star g=g\star f$ $\iff$ both $f$ and $g$ are Hermitian, i.e. $f(t)=\overline{ f(-t)}.$ This implies that in this case, the cross-correlation is identical to convolution.

## Algorithm
Start with the smoothed image $S=f_{\mathrm{smooth}}.$ Then the changes in intensity in direction $\mathbf{\hat{n}}$ is
$$
\begin{align}
S_{n}&=\mathbf{\hat{n}}\cdot\nabla S \\
S_{n}^{2}&=\mathbf{\hat{n}}^{\top}\nabla S\nabla S^{\top}\mathbf{\hat{n}} \\
 \end{align}
$$
Note that the self-outer product of the gradient $\nabla S\nabla S^{\top}$ is an approximation to the Hessian matrix.

[terminology - Name for outer product of gradient approximation of Hessian - Cross Validated](https://stats.stackexchange.com/a/122152)

$\nabla S\nabla S^{\top}$ encodes information about how changes in $S$ propagate in different directions relative to each other. The diagonal elements represent the squared rate of change of $S$ in the principal directions; the off-diagonal elements encode the interaction between these directional changes

tbc [[eigenvectors]]




