## 1D case
- Apply smoothing by convolution with the Gaussian kernel $\operatorname{g(x)}$
$$
\operatorname{g}(x)= \frac{1}{\sqrt{ 2\pi }\sigma}\exp\left( - \frac{1}{2} \frac{x^{2}}{\sigma^{2}} \right)
$$
- Mark edges at the maximum and minimum gradients of the smoothed image

>The amount of smoothing applied is a trade-off between accuracy and noise.

>Note that the exponential coefficient is just a scaling factor and does not affect the gradients.

### Optimisations
- Naively, both the smoothing and differentiation steps are performed using convolutions (expensive)
- However, by employing the derivative theorem of convolution:
$$
\begin{align}
\frac{\partial }{\partial x} f_{\mathrm{smooth}} &=\frac{\partial }{\partial x} \left\{ f*\operatorname{g} \right\}   \\
&=f*\frac{\partial \operatorname{g}}{\partial x} 
 \end{align}
$$
which only requires one convolution.

> Finding the locations of maximum and minimum gradients of the smoothed function can be effectively calculated by finding the roots of the second derivative $\partial_{xx}f_{\mathrm{smooth}},$ for example with the Laplacian filter

$$
D^{2}_{x} =\begin{bmatrix}
1&-2&1
\end{bmatrix}
$$


## 2D case

This extends naturally to $n$ dimensions.

- The smoothed image is found by convolution with the Gaussian kernel $\operatorname{g}(\mathbf{x})$

$$
\operatorname{g}(\mathbf{x})= \frac{1}{(2\pi)^{n/2}\sqrt{ |\Sigma| }}\exp \left\{ -\frac{1}{2}\mathbf{x}\cdot\Sigma ^{-1}\mathbf{x} \right\} 
$$
>Note that the exponential coefficient will not affect the gradients and can be ignored. For rotationally symmetric Gaussians this then simplifies to a more intuitive extension of the 1D case.

$$
\operatorname{g}(\mathbf{x})\propto \exp\left( - \frac{1}{2} \frac{\mathbf{x}\cdot \mathbf{x}}{\sigma^{2}} \right)
$$

Now the maxima and minima gradients can be calculated. There are two main approaches.

### Marr-Hildreth detector (isotropic)

Like the 1D case, just find the roots of $f_{\mathrm{smooth}}.$ This can be done for example with the five-point stencil Laplacian filter:
$$
\mathbf{D}^{2}_{xy}=\begin{bmatrix}
0&1&0 \\
1&-4&1 \\
0&1&0
\end{bmatrix}
$$

### Canny detector (directional)

Consider the gradients of the smoothed image $\mathbf{f}_{\mathrm{smooth}},$
$$
\begin{align}
\nabla f_{\mathrm{smooth}}&=\nabla \left\{ f*\operatorname{g} \right\}  \\
&=f*\nabla \operatorname{g}
 \end{align}
$$
This encodes the strength and direction of the gradients at each point.

1-pixel edgel (edge element) curves are generated from the points on $\nabla f_{\mathrm{smooth}}$ that are local maxima in the gradient direction.

Edgels are then discarded by thresholding (specifically hysteresis thresholding, but that’s outside the scope of the course).


## Implementing convolutions

- Kernels are typically truncated to remove samples less than $\frac{1}{1000}$ of the peak kernel value. 

- Multidimensional convolutions can be decomposed into iterative convolutions along each dimension.
$$
f*\operatorname{g}(x,y)=f*\operatorname{g}_{x}*\operatorname{g}_{y}$$

- One common differentiation kernel is the Sobel operator

$$
\begin{align}
D_{x} &=\begin{bmatrix}
+1&0&-1 \\
+2&0&-2 \\
+1&0&-1
\end{bmatrix} \\
 \\
D_{y} &=\begin{bmatrix}
+1&+2&+1 \\
0&0&0 \\
-1&-2&-1
\end{bmatrix}
 \end{align}
$$
which in 1D would just be $D=\begin{bmatrix}1&0&-1\end{bmatrix}.$ This is a 1st order approximation.

>There is a curious relationship between the kernel entries for the $n\mathrm{th}$ derivative and the Pascal’s triangle entries at the $n\mathrm{th}$ row. 
