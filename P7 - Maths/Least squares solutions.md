See also:
- [Moore–Penrose inverse - Wikipedia](https://en.wikipedia.org/wiki/Moore%E2%80%93Penrose_inverse#Applications)
- [Projection matrix - Wikipedia](https://en.wikipedia.org/wiki/Projection_matrix)

## Least squares
Consider we have a set of coordinates $a_{i}=[x_{i},y_{i}]$ and observe a value $b_{i}$ at each coordinate. Let’s fit these observables to a linear function
$$
b_{i}=Cx_{i}+D
$$
for some $C$ and $D.$ In general, this will give inconsistent solutions for $C$ and $D$ since the observed values will not lie exactly on any linear function, but we can minimise the residuals to get a good fit!

If we have taken $n$ observations, then we can write this as

$$
\begin{align}
\mathbf{r}&=\begin{bmatrix}
x_{1} & y_{1} \\
x_{2} & y_{2} \\
\vdots & \vdots \\
x_{n} & y_{n}
\end{bmatrix}\begin{bmatrix}
C \\
D
\end{bmatrix}
-\mathbf{b} \\
&=A\mathbf{x}-\mathbf{b}
 \end{align}
$$

where we want $C$ and $D$ that minimise $\mathbf{r}^{2}.$

## Gram-Schmidt decomposition
Consider a vector space $V=\{ \mathbf{v}_{1},\mathbf{v}_{2},\dots \}.$ To form an set $Q=\{ \mathbf{q}_{1},\mathbf{q}_{2},\dots \}$ of orthonormal basis vectors for $V$, Gram-Schmidt allows us to generate the basis vectors one at a time. Note that $|Q|\leq |V|.$

$$
\begin{align}
\mathbf{q}_{1}&=\hat{\mathbf{v}}_{1} \\
\mathbf{q}_{n+1}&=\operatorname{normalize}\left( \mathbf{v}_{n+1}-\sum\limits_{ k=1 }^{ n } (\mathbf{q}_{k}\cdot \mathbf{v}_{n})\mathbf{q}_{k}\right)
 \end{align}
$$
You can stop the process when you reach $\mathbf{q}_{n}=0,$ since any further basis vectors will then also be the zero vector.

## $\mathrm{QR}$–decomposition

By applying the Gram-Schmidt process to the column vectors of a matrix $A,$ we can decompose it as
$$
\begin{align}
A&=QR \\
&=\begin{bmatrix}
\mathbf{q}_{0} & \mathbf{q}_{1} & \dots & 
\end{bmatrix}R
 \end{align}

$$
where $R$ is given as

$$
R_{ij}=\sum
$$
tbc


## Applying $\mathrm{QR}$ to least-squares
$$
\begin{align}
0&=A^{\top}A\mathbf{\bar{x}}-A^{\top}\mathbf{b} \\
&=(QR)^{\top}QR\bar{\mathbf{x}}-(QR)^{\top}\mathbf{b} \\
&=R^{\top}\underbrace{ Q^{\top}Q}_{ I }R\mathbf{\bar{x}}-R^{\top}Q^{\top}\mathbf{b}  \\
&=R\bar{\mathbf{x}}-Q^{\top}\mathbf{b}
 \end{align}
$$
## Operation count and robustness of QR
$\mathrm{QR}$ is more costly than $\mathrm{LU}$ for consistent equations but more cost effective for inconsistent equations that need least-squares fitting.

>For large $n$, the Gram-Schmidt process can become ill-conditioned under computation and so is no longer suitable for finding $Q.$

## Projection onto columns space
The projection $\mathbf{b}_{col}$of $\mathbf{b}$ onto $\operatorname{colsp}A$ satisfies
$$
\mathbf{b}_{col}=A(A^{\top}A)^{-1}A^{\top}\mathbf{b}
$$
tbc projection matrix