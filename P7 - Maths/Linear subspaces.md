A subspace $W$ of a vector space $V$ is linear if $W$ is closed over vector addition.

## Properties
- Closure under linear combination
- Inclusion—a subspace cannot lie in any other subspace of lesser dimension. If $\operatorname{dim}U=n$ and $U\subset W$ then $\operatorname{dim}W=n$ if and only if $U\equiv W.$

## Trivial linear subspaces
There are at least two trivial linear subspaces of any vector space:
- The zero vector space, $W=\{ \vec{0} \}=0$
- The entire vector space itself, $W=V$

## The 4 fundamental subspaces
### Column space
The column space of a matrix operation $M$ is the set of all linear combinations of its columns (the space *spanned* by the column vectors).

This is the *image* of $M,$ the set of all nonzero values for $M\mathbf{x}$. It is equivalently the set of all inputs $\mathbf{x}$ such that, for the dual transformation,
$$
\mathbf{x}^{\top}M\neq 0
$$

### Row space
The row space of a matrix operation $M$ is the set of all linear combinations of its rows (the space *spanned* by the row vectors).

This is the set of all inputs $\mathbf{x}$ such that
$$
M\mathbf{x}\neq 0
$$
This is the *coimage* of $M,$ the set of all nonzero values of $M^{\top}\mathbf{x}.$

### Null space (kernel)
Given a linear operation $M,$ its null space (or kernel) $\operatorname{ker}M$ is the set of all inputs $\mathbf{x}$ such that
$$
M\mathbf{x}=0
$$
That is,
$$
\operatorname{ker}M=\{ \mathbf{v}\in V:M\mathbf{v}=0 \}
$$
### Left null space (cokernel)

The left null space (cokernel) of a matrix operation $M$ is the kernel of the transpose,
$$
\operatorname{coker}M=\operatorname{ker}M^{\top}
$$
Equivalently, it is the set of solutions to
$$
\mathbf{x}^{\top}M=0
$$

## Duality

The 4 fundamental subspaces can be split into just two pairs of objects!
- The row space is the dual of the column space
- The left null space is the dual of the null space

This is because a single matrix $M\in\mathbb{R}^{m\times n}$ describes two dual operations. The “right” operation $R=R(\mathbf{x})$ is $\mathbf{x}\mapsto M\mathbf{x}$ and acts on vectors while the “left” operation $L=L(\mathbf{x}^{\top})$ is $\mathbf{x}^{\top}\mapsto \mathbf{x}^{\top}M$ and acts on covectors.

|  | $L(\mathbf{x}^{\top})$ | $R(\mathbf{x})$ |
| ---- | ---- | ---- |
| $\operatorname{image}$ | row space | column space |
| $\operatorname{ker}$ | left null space | null space |

## Orthogonal complements

From the definitions of the 4 fundamental subspaces, we can see directly that for a linear map $M:V\to W,$ we can write two (equivalent) expressions of complementariness.
$$
\begin{cases}
\begin{align}
\operatorname{coim}M\oplus\operatorname{ker}M&=V \\
\operatorname{im}M\oplus\operatorname{coker}M&=W
\end{align}
 \end{cases}
$$
where $\oplus$ is the *direct sum*.

Additionally, by definition of the kernel, for $\mathbf{x}\in\operatorname{ker}M$ to satisfy $M\mathbf{x}=0,$ it must be orthogonal to every row in $M.$ Therefore $\operatorname{coim}M$ and $\operatorname{ker}M$ are not just complements—they are *orthogonal complements*! 

## Rank
Given a matrix $M,$ its rank is the number of linearly independent columns (or rows). This is equivalently the dimension of the column space $C$ and the dimension of the row space $R$.
$$
\operatorname{rank}(M)=\operatorname{rank}(M^{\dagger})=\operatorname{dim }(C)=\operatorname{dim} (R)
$$
The rank can be computed as the number of pivots in the echelon form (which can be found as the number of non-zero rows in the $U$ of [[Matrix multiplication#LU decomposition|LU decomposition]]).

## The rank-nullity theorem
Recall the analysis of [[#Orthogonal complements|orthogonal complements]]. For linear map $M:V\to W$ with column space $C$ and row space $R,$ we previously showed the equivalent statements
$$
\begin{cases}
\begin{align}
R\oplus \operatorname{ker}M&=V \\
C\oplus \operatorname{coker}M&=W
\end{align}
 \end{cases}
$$
Taking dimensions gives the rank-nullity theorem,
$$
\begin{cases}
\begin{align}
\operatorname{rank}M+\operatorname{nul}M&=\operatorname{dim}V \\
\operatorname{rank}M+\operatorname{conul}M&=\operatorname{dim}W
\end{align}
 \end{cases}
$$
This is sometimes called the Fundamental Theorem of Linear Algebra.

