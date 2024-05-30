## div

In general curvilinear coordinates with $H=\operatorname{diag}\mathbf{h},$ the divergence of a field $\mathbf{F}$ is
$$
\nabla\cdot \mathbf{F}=|H|\begin{bmatrix}
\partial_{1} \\
\partial_{2} \\
\partial_{3}
\end{bmatrix}\cdot\hat{H}\mathbf{F}
$$
>Note that $\hat{H}_{i}=\frac{h_{i}}{\prod h}$

### Cartesian
$$
\nabla\cdot \mathbf{F}=\begin{bmatrix}
\partial_{x} \\
\partial_{y} \\
\partial_{z}
\end{bmatrix}\cdot \mathbf{F}
$$
### Cylindrical polar
The curvilinear scaling factor is $\mathbf{h} = \begin{bmatrix}1&  r & 1\end{bmatrix}$ so
$$
\nabla\cdot \mathbf{F}=\underbrace{ \frac{1}{r}}_{ \prod h }\begin{bmatrix}
\partial_{r} \\
\partial_{\theta} \\
\partial_{z}
\end{bmatrix}\cdot \underbrace{ \begin{bmatrix}
r  \\
 & 1 \\
 &  & r
\end{bmatrix}}_{ \frac{h_{i}}{\prod h} }\mathbf{F}
$$
### Spherical polar
The curvilinear scaling factor is $\mathbf{h} = \begin{bmatrix}1&  r & r\sin\theta\end{bmatrix}$ so
$$
\nabla\cdot \mathbf{F}=\underbrace{ \frac{1}{r^{2}\sin \theta}}_{ \prod h }\begin{bmatrix}
\partial_{r} \\
\partial_{\theta} \\
\partial_{\phi}
\end{bmatrix}\cdot \underbrace{ \begin{bmatrix}
r^{2}\sin\theta  \\
 & r\sin\theta \\
 &  & r
\end{bmatrix}}_{ \frac{h_{i}}{\prod h} }\mathbf{F}
$$

## grad
In general curvilinear coordinates with $H=\operatorname{diag}\mathbf{h},$ the gradient of a field $\mathbf{F}$ is
$$
\operatorname{\nabla}\mathbf{F}=H^{-1}\begin{bmatrix}
\partial_{1} \\
\partial_{2} \\
\partial_{3}
\end{bmatrix}\mathbf{F}
$$
>Note that $H^{-1}_{i}=\frac{1}{h_{i}}$
### Cartesian
$$
\operatorname{\nabla}\mathbf{F}=\begin{bmatrix}
\partial_{x} \\
\partial_{y} \\
\partial_{z}
\end{bmatrix}\mathbf{F}
$$
### Cylindrical polar
The curvilinear scaling factor is $\mathbf{h} = \begin{bmatrix}1&  r & 1\end{bmatrix}$ so
$$
\operatorname{\nabla}\mathbf{F}=\underbrace{ \begin{bmatrix}
1 \\
 & \frac{1}{r}\\
 &  & 1
\end{bmatrix}}_{h_{i}^{-1} }\begin{bmatrix}
\partial_{r} \\
\partial_{\theta} \\
\partial_{z}
\end{bmatrix}\mathbf{F}
$$

### Spherical polar
The curvilinear scaling factor is $\mathbf{h} = \begin{bmatrix}1&  r & r\sin\theta\end{bmatrix}$ so
$$
\operatorname{\nabla}\mathbf{F}=\underbrace{ \begin{bmatrix}
1 \\
 & \frac{1}{r} \\
 &  & \frac{1}{r\sin\theta}
\end{bmatrix}}_{ h_{i}^{-1} }\begin{bmatrix}
\partial_{r} \\
\partial_{\theta} \\
\partial_{\phi}
\end{bmatrix}\mathbf{F}
$$
## curl
In general curvilinear coordinates with $H=\operatorname{diag}\mathbf{h},$ the curl of a field $\mathbf{F}$ is
$$
\nabla\times \mathbf{F}=\hat{H}\begin{bmatrix}
\partial_{1} \\
\partial_{2} \\
\partial_{3}
\end{bmatrix}\times H\mathbf{F}
$$
>Note that $\hat{H}_{i}=\frac{h_{i}}{\prod h}$
### Cartesian
$$
\nabla\times\mathbf{F}=\begin{bmatrix}
\partial_{x} \\
\partial_{y} \\
\partial_{z}
\end{bmatrix}\times\mathbf{F}
$$
### Cylindrical polar
The curvilinear scaling factor is $\mathbf{h} = \begin{bmatrix}1&  r & 1\end{bmatrix}$ so
$$
\nabla\times\mathbf{F}=\underbrace{ \begin{bmatrix}
\frac{1}{r} \\
 &  1 \\
 &  & \frac{1}{r}
\end{bmatrix}}_{ \frac{h_{i}}{\prod h} }\begin{bmatrix}
\partial_{r} \\
\partial_{\theta} \\
\partial_{z}
\end{bmatrix}\times \underbrace{ \begin{bmatrix}
1 \\
 & r \\
 &  & 1
\end{bmatrix}}_{ h_{i} }\mathbf{F}
$$
### Spherical polar
The curvilinear scaling factor is $\mathbf{h} = \begin{bmatrix}1&  r & r\sin\theta\end{bmatrix}$ so
$$
\nabla\times\mathbf{F}=\underbrace{ \begin{bmatrix}
\frac{1}{r^{2}\sin\theta} \\
 &  \frac{1}{r\sin\theta} \\
 &  & \frac{1}{r}
\end{bmatrix}}_{ \frac{h_{i}}{\prod h} }\begin{bmatrix}
\partial_{r} \\
\partial_{\theta} \\
\partial_{z}
\end{bmatrix}\times \underbrace{ \begin{bmatrix}
1 \\
 & r \\
 &  & r\sin\theta
\end{bmatrix}}_{ h_{i} }\mathbf{F}
$$

