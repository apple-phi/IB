Useful links:
- [Bra-Ket Notation Trivializes Matrix Multiplication](https://algassert.com/post/1629)
Matrix multiplication is defined as 
$$
\begin{align}
(AB)_{ij}&=\left[\left( \sum\limits_{ i=1 }^{ N }\sum\limits_{ j=1 }^{ N }A_{ij}\ket{i} \bra{j} \right)\left( \sum\limits_{ k=1 }^{ N }\sum\limits_{ l=1 }^{ N }B_{kl}\ket{k} \bra{l} \right)\right]_{ij} \\
&=\sum\limits_{ k=1 }^{ N }A_{ik}B_{kj}
 \end{align}
$$
## Permutation matrix
[Permutation matrix - Wikipedia](https://en.wikipedia.org/wiki/Permutation_matrix)
A permutation matrix that permutes the columns or rows of the matrix it operates on (depending on left or right multiplication).

### Properties
- Binary
- Orthogonal
- a single $1$ per column or row
- every permutation matrix is a permutation of the identity matrix, $P=PI=IP$
- $P ^{-1}=P^{\dagger}$

## LU decomposition
It is possible (and useful) to factorise a matrix $M$ as the product of two matrices:
- $L$, a square lower triangular matrix with $1$s on the leading diagonal
- $U,$ an upper echelon matrix

That is, write
$$
M=LU
$$
This is only possible for matrices which are reducible to row-echelon form without row interchange.

### Motivation

To solve for $\mathbf{x}$ where
$$
M\mathbf{x}=\mathbf{y}
$$
we can start by solving for $U\mathbf{x}$ where
$$
LU\mathbf{x}=\mathbf{y}
$$
and then solve for $\mathbf{x}$ where
$$
U\mathbf{x}=L^{-1}\mathbf{y}
$$
Both these steps are very fast because $L$ and $U$ are both triangular.

### Method

Instead of a full algebraic expansion, a quick(-ish) trick is to write
$$
M=IM
$$
And then apply complementary elementary row operations to $I$ and $M$ respectively to achieve the required form.

A recursive algorithm is given here: [LU decomposition - Wikipedia](https://en.wikipedia.org/wiki/LU_decomposition#Through_recursion)

### Properties
- Any square matrix is (P)LU decomposable if and only if all of its leading principle minors (submatrix determinants) are nonzero

## Partial pivoting
Consider decomposing a 3 by 3 square matrix:
$$
{\begin{bmatrix}m_{11}&m_{12}&m_{13}\\m_{21}&m_{22}&m_{23}\\m_{31}&m_{32}&m_{33}\end{bmatrix}}={\begin{bmatrix}\ell _{11}&0&0\\\ell _{21}&\ell _{22}&0\\\ell _{31}&\ell _{32}&\ell _{33}\end{bmatrix}}{\begin{bmatrix}u_{11}&u_{12}&u_{13}\\0&u_{22}&u_{23}\\0&0&u_{33}\end{bmatrix}}
$$

If $m_{11}=0=\ell_{11}u_{11}$ then continuing the factorisation would involve a division by $0.$ We can solve this problem by pre-multiplying $M$ by a permutation matrix, to instead solve $PM=L'U'.$ 

Then have the decomposition of $M$ as
$$
M=P^{\top}L'U'
$$
In general, pivoting is required if there is a 0 on the leading diagonal, that is, there exists $i$ such that $m_{ii}=0.$

## Further issues
In some cases, the forward / back-substitution algorithms for solving systems of linear equations can be prone to significant floating point error accumulation. These can sometimes be minimised by pivoting.