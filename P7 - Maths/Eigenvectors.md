For a symmetric matrix $A$, the eigenvalues are real and the eigenvectors orthogonal. Consider a matrix $A$ with eigenvectors $\mathbf{u}$ and eigenvalues $\lambda_{i}.$ 
$$
AU=U\Lambda
$$
where $U=[\mathbf{u}_{i}]$ and $\Lambda=\operatorname{diag}(\lambda_{i}).$ Then 
$$
A^{k}=(U\Lambda U^{-1})^{k}=U\Lambda^{k}U^{-1}
$$
Given the largest eigenvalue $\lambda_{m}$ for normalised eigenvector $\mathbf{u}_{m}$ then for large $k$ we have
$$
A^{k}\mathbf{x}=\lambda ^{k}_{m}(\mathbf{u}_{m}\cdot\mathbf{x})\mathbf{u}_{m}
$$

## Characteristic polynomial
The characteristic polynomial of a matrix $A$ is
$$
P(\lambda)=\det(A-\lambda I)
$$
whose roots are the eigenvalues of $A.$ By applying Vieta’s formulas we find that
$$
\begin{align}
\operatorname{Tr}A&=\sum\limits_{ i=1 }^{ N }\lambda_{i} \\
\det A&=\prod\limits_{ i=1 }^{ N }\lambda_{i} 
\end{align}
$$
>For singular matrices, at least one of the eigenvalues is 0.
## Diagonal matrices
Given a diagonal matrix $A=\operatorname{diag}(\mathbf{a})$ then the eigenvalues are $\boldsymbol{\lambda}=\mathbf{a}.$

>Eigenvectors of the same eigenvalue describe an eigen-plane. 

## Triangular matrices
Consider a triangular matrix $A$ with leading diagonal $\mathbf{a}.$ Then just like a diagonal matrix, $\boldsymbol{\lambda}=\mathbf{a}.$

## Complex eigenvalues
A complex eigenvalue describes a rotation!

tbc—further research

## Defective matrices
Consider the matrix
$$
\begin{align}
A=\begin{bmatrix}
1 & -1 \\
0 & 1
\end{bmatrix}
 \end{align}
$$
which has eigenvalue $\lambda=1$ with algebraic multiplicity $2.$ This matrix has only one eigenvector, $[1,0]^{\top}.$

Hence the algebraic multiplicity is $2$ but the geometric multiplicity $1.$ We say such mismatches are *defective* and can prove they can only happen for repeated eigenvalues.


## Similar matrices and diagonalisability
When matrices have the same eigenvalues we say they are *similar*. Their eigenvectors have a linear map relationship that can be described as a matrix. 

A matrix which is similar to a diagonal matrix is said to be *diagonalisable*


tbc commutative diagram
```tikz
\usepackage{tikz-cd}
\tikzcdset{scale cd/.style={every label/.append style={scale=#1},
    cells={nodes={scale=#1}}}}
\begin{document}
\begin{tikzcd}[scale cd=4,sep=huge]
    & X \times_Z Y \arrow[r, "p"] \arrow[d, "q"]
    & X \arrow[d, "f"] \\
    & Y \arrow[r, "g"]
    & Z

\end{tikzcd}
\end{document}
```
## When are non-symmetric matrices diagonalisable?
Although we always can’t tell in advance if a matrix is diagonalisable, there are some special cases where we can.
- Any matrix with distinct eigenvalues can be diagonalised

## Computation of eigenvalues
tbc