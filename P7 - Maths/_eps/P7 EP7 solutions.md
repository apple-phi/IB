## 1.
Denote the vectors $u, v$ and $u', v'.$ Then they are related by
$$
\begin{align}
u'&=2u-v \\
v'&=v-2u
\end{align}
$$
since $u\neq v,$ and $u'\neq v'$ then both vector spaces have the same dimension so must be equivalent.

## 2.

$$
\begin{align}
\det \begin{bmatrix}
1&-1&3 \\
2&3&1 \\
0&1&-1
\end{bmatrix}&=\begin{vmatrix}
3&1 \\
1 &-1
\end{vmatrix}-2\begin{vmatrix}
-1&3 \\
1&-1
\end{vmatrix} \\
&=-4-2(-2) \\
=0
 \end{align}
$$
Therefore $S$ must be 2D.

The normal vector to $S$ is
$$
\mathbf{n}\propto \begin{bmatrix}
1 \\
2 \\
0
\end{bmatrix}\times \begin{bmatrix}
-1 \\
3 \\
1
\end{bmatrix}
=\begin{bmatrix}
2 \\
-1 \\
5
\end{bmatrix}
$$
The vector $\mathbf{v}=\begin{bmatrix}1&0&1\end{bmatrix}$ lies in $S$ if it is orthogonal to the normal vector.
$$
\begin{bmatrix}
1 \\
0 \\
1
\end{bmatrix}\cdot \mathbf{n}=7\neq 0
$$
Hence it does not lie in $S.$

$T$ is the space spanned by $\mathbf{n}.$

$\mathbf{v}$ lies in $S\cup T.$ The contribution from $T$ is given by
$$
\begin{align}
\mathbf{v}_{T}&=(\mathbf{v}\cdot \mathbf{\hat{n}})\mathbf{\hat{n}} \\
&=\frac{7}{|\mathbf{n}|^{2}}\mathbf{n} \\
&=\frac{7}{30}\mathbf{n} \\
 \end{align}
$$
Then the remainder must lie in $S.$
$$
\begin{align}
\mathbf{v}_{S}&=\mathbf{v}-\mathbf{v}_{T} \\
&=\begin{bmatrix}
1 \\
0 \\
1
\end{bmatrix}-\begin{bmatrix}
\frac{7}{15} \\
-\frac{1}{30} \\
\frac{5}{6}
\end{bmatrix} \\
&=\begin{bmatrix}
\frac{8}{15} \\
\frac{1}{30} \\
\frac{1}{6}
\end{bmatrix}
 \end{align}
$$

## 3.
$\operatorname{rank}A=2.$ Let $A'=\begin{bmatrix}1 &0\\0&0\\0&1\end{bmatrix}$ and the column space of $B=\begin{bmatrix}a&b \\c&d\end{bmatrix}$ be $U.$ Then the column space of $A'B$ is $A'U.$ Hence as long as $U$ is the whole space (which requires $\det B\neq 0$), then $\operatorname{colsp}A=\operatorname{colsp}(A'B).$ Therefore, every $A'B$ satisfies the column space of $A.$

## 4.
By inspection,
$$
C=A\overbrace{ \begin{bmatrix}
0&0&1 \\
1&0&0\\
0&1&0
\end{bmatrix}}^{ P }
$$
Then

$$
\begin{align}
D&=C^{-1}AB \\
&=P ^{-1}A^{-1}AB \\
&=P^{\top}B \\
&=\begin{bmatrix}
0&1&0 \\
0&0&1\\
1&0&0
\end{bmatrix}\begin{bmatrix}
1 &1 \\
2&1 \\
6&2
\end{bmatrix} \\
&=\begin{bmatrix}
2&1 \\
6&2 \\
1&1
\end{bmatrix}
 \end{align}
$$

To satisfy the equation $B=QD,$ $Q=(P^{\top})^{-1}=P.$

>Supo question: the cribs says $Q=P^{\top},$ so what have I done wrong?

## 5.

### (a)
$$
\begin{align}
A&=\begin{bmatrix}
3&1&2 \\
-3&3&1
\end{bmatrix} \\
&=\begin{bmatrix}
1 & 0 \\
-\frac{3}{3} & 1
\end{bmatrix}\begin{bmatrix}
3 & 1 & 2 \\
0  & R'_{1} & R'_{2}
\end{bmatrix} \\
 \\
R'&=A'-\begin{bmatrix}
-\frac{3}{3}
\end{bmatrix}\otimes \begin{bmatrix}
1 \\
2
\end{bmatrix} \\
&= \begin{bmatrix}
3 & 1
\end{bmatrix}-\begin{bmatrix}
-1 & -2
\end{bmatrix} \\
&=\begin{bmatrix}
4 & 3
\end{bmatrix}\\
 \\
A&=\begin{bmatrix}
1 & 0 \\
-1 & 1
\end{bmatrix}\begin{bmatrix}
3 & 1 & 2 \\
0  & 4 & 3
\end{bmatrix}
 \end{align}
$$
### (b)
$$
\begin{align}
A&=\begin{bmatrix}
2 & 1 \\
6 & 4 \\
-2 & 0
\end{bmatrix} \\
&=\begin{bmatrix}
1 & 0 & 0 \\
\frac{6}{2}  & 1 & 0 \\
-\frac{2}{2} & L'_{31} & 1
\end{bmatrix}\begin{bmatrix}
2 & 1 \\
0  & R'_{11} \\
0 & 0
\end{bmatrix} \\
&=\begin{bmatrix}
1 & 0 & 0 \\
3  & 1 & 0 \\
-1 & 1& 1
\end{bmatrix}\begin{bmatrix}
2 & 1 \\
0  & 1 \\
0 & 0
\end{bmatrix}
 \end{align}
$$

## 6.
$$
\begin{align}
A&=\begin{bmatrix}
-1 & 2 & 0 \\
1 & 1 & 4 \\
2 & -2 & 4
\end{bmatrix} \\
&=\begin{bmatrix}
1 & 0 & 0 \\
-1  & 1 & 0\\
-2  & L'_{21} & 1
\end{bmatrix}\begin{bmatrix}
-1 & 2 & 0 \\
0 & R'_{11} & R'_{12} \\
0 & R'_{21} & R'_{22}
\end{bmatrix} \\
 \\
R'&=A'-\begin{bmatrix}
- 1  \\
-2
\end{bmatrix}\otimes \begin{bmatrix}
2 \\
0
\end{bmatrix} \\
&=\begin{bmatrix}
1 & 4 \\
-2 & 4
\end{bmatrix}-\begin{bmatrix}
-2  & 0\\
-4 & 0
\end{bmatrix} \\
&=\begin{bmatrix}
3 & 4 \\
2 & 4
\end{bmatrix} \\
&=
\end{align}
$$
tbc

## 7.
skip, matlab

## 8.
By recursion and inspection,
$$
\begin{align}
A&=\begin{bmatrix}
1 & 2 & 0 & 1 \\
0 & 1 & 1 & 0 \\
1 & 3 & 1 & 1
\end{bmatrix} \\
&=\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
1 & 1 & 1
\end{bmatrix}\begin{bmatrix}
1 & 2 & 0 & 1 \\
0 & 1 & 1 & 0 \\
 0 & 0 & 0 & 0
\end{bmatrix}
\end{align}
$$
Then solve $Ax=b$ by forward substitution.

## 9.
Find the bases of each fundamental subspace

## 10.
### (a)
$$
\begin{bmatrix}
1 & 0  \\
0 & 0 \\
0 & 1
\end{bmatrix}
$$

### (b)
colsp is line in R3 so rank 1. Nullsp is line in R3, rowsp is orthogonal compl of nullsp so must be plane in R3 with rank 2

since rank(colsp)!=rank(rowsp), contradictory so doesn’t exist

### (c)
rowsp rank 3, colsp rank 4, doesn’t exist

## 11
$$
\begin{align}
\begin{bmatrix}
2 & 2 & 1 & 1 & 0 & 0 \\
3 & 4 & 2 & 0 & 1 & 0 \\
1 & -1 & 1.5 &  0 & 0 & 1
\end{bmatrix} \\
\begin{bmatrix}
1 & 1 & 0.5  & 0.5  & 0 &0 \\

\end{bmatrix}
\end{align}
$$
etc.

unfinished


## 12.
$$

$$

unfinished

## 13.

$P$ is full rank (invertible) so can write $PA\mathbf{x}=P\mathbf{b}.$ Then $PA=LU$ so $LU\mathbf{x}=P\mathbf{b}$ so for $U\mathbf{x}=\mathbf{c},$ find $\mathbf{c}$ but forward subst.

$$
\mathbf{c}=\begin{bmatrix}
2 \\
-1 \\
5 \\
1
\end{bmatrix}
$$

4th component of $\mathbf{c}$ $i$ s0 so it is possible to find a solution to $U\mathbf{x}=\mathbf{c}$

Hence $\mathbf{b} \in \operatorname{colsp}A$

tbc