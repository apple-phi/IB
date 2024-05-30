We can factorise any matrix into a rotation, followed by a rescaling, followed by another rotation. This is a generalisation of the eigendecomposition of a square normal matrix with orthonormal eigenbasis to any matrix.

$$
A=\hat{Q}\Sigma Q^{\top}
$$

where $Q$ is orthonormal.

tbc draw commutative diagram 

Consider the square, symmetric matrix $A^{\top}A.$ It is therefore diagonalisable and the [[eigenvectors]] can be chosen to be orthonormal. so
$$
A^{\top}AQ=A\Lambda
$$
where $Q$ is an orthonormal matrix whose columns are the [[eigenvectors]] of $A^{\top}A$ and $\Lambda=\boldsymbol{\lambda}I$ is the tbc

We also know that there will be $\operatorname{rank}A$ non-zero eigenvalues. 

Define the singular values of $A$ as the square roots of the non-singular eigenvalues.
$$
\sigma_{i}=\sqrt{ \lambda_{i} }\qquad 1\leq i\leq \operatorname{rank}A
$$
Define a norm of $A$ as the magnitude of the largest singular value,
$$
\lVert A \rVert =\max|\sigma|
$$

Now lets generalise the idea of an eigenvalue. tbc 

We have $\hat{\mathbf{q}}_{1}, \hat{\mathbf{q}}_{2},\dots,\hat{\mathbf{q}}_{\operatorname{rank}A}$ orthonormal [[eigenvectors]] of $AA^{\top}$ and we can complete this set by adding $\hat{\mathbf{q}}_{\operatorname{rank}(A)+1},\dots,\hat{\mathbf{q}}_{m}$ which are [[eigenvectors]] corresponding to eignevalue zero for $AA^{\top}.$ These are all orthogonal to the $\hat{\mathbf{q}}_{1}, \hat{\mathbf{q}}_{2},\dots,\hat{\mathbf{q}}_{\operatorname{rank}A}$ set and can be chosen as orthonormal basis vectors.

$$
AA^{\top}=QAQ^{\top}
$$