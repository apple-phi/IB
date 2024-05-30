## 1.
tbc nonsense question.

## 2.
Let $\Omega=\mathcal{A}+\overline{ \mathcal{A}}$ be the whole sample space, then the second axiom of probability gives the complement rule:
$$
\begin{align}
1&=\operatorname{\mathbb{P}}[\Omega] \\
&=\operatorname{\mathbb{P}}[\mathcal{A}]+\operatorname{\mathbb{P}}[\overline{ \mathcal{A}}]
 \end{align}
$$
Then let $\mathcal{A}=\Omega,\overline{ \mathcal{A}}=\emptyset$ to obtain the impossible event rule:
$$
\begin{align}
\operatorname{\mathbb{P}}[\emptyset]&=1-\operatorname{\mathbb{P}}[\Omega] \\
&=0
\end{align}
$$
If $\mathcal{A}\subseteq \mathcal{B}$ we find that
$$
\begin{align}
\mathcal{B}&=\mathcal{A}+\mathcal{B} \setminus \mathcal{A} \\
\operatorname{\mathbb{P}}[\mathcal{B}]&=\operatorname{\mathbb{P}}[\mathcal{A}]+\operatorname{\mathbb{P}}[\mathcal{B}\setminus \mathcal{A}] \\
\operatorname{\mathbb{P}}[\mathcal{B}]&\geq \operatorname{\mathbb{P}}[\mathcal{A}]
\end{align}
$$

To prove the inclusion-exclusion principle, first consider the mutual exclusivity of $\mathcal{A}$ and $\mathcal{B}\setminus \mathcal{A}.$
$$
\begin{align}
\operatorname{\mathbb{P}}[\mathcal{A}\cup \mathcal{B}]&=\operatorname{\mathbb{P}}[\mathcal{A}\cup(\mathcal{B}\setminus \mathcal{A})] \\
&=\operatorname{\mathbb{P}}[\mathcal{A}]+\operatorname{\mathbb{P}}[\mathcal{B}\setminus \mathcal{A}]
\end{align}
$$
Now also consider the mutual exclusivity of $\mathcal{B}\setminus \mathcal{A}$ and $\mathcal{A}\cap\mathcal{B}.$
$$
\begin{align}
\operatorname{\mathbb{P}}[\mathcal{B}]&=\operatorname{\mathbb{P}}[(\mathcal{B}\setminus \mathcal{A})\cup(\mathcal{A}\cap \mathcal{B})] \\
&=\operatorname{\mathbb{P}}[\mathcal{B}\setminus \mathcal{A}]+\operatorname{\mathbb{P}}[\mathcal{A}\cap \mathcal{B}]
 \end{align}
$$
Subtracting the two equations gives
$$
\operatorname{\mathbb{P}}[\mathcal{A}\cup \mathcal{B}]=\operatorname{\mathbb{P}}[A]+\operatorname{\mathbb{P}}[B]-\operatorname{\mathbb{P}}[\mathcal{B}\cap\mathcal{A}]
$$
as expected.

## 3.
$$
\begin{align}
\operatorname{\mathbb{P}}[A\mid D]&= \frac{\operatorname{\mathbb{P}}[A\cap D]}{\operatorname{\mathbb{P}}[D]} \\
&= \frac{0.78}{0.83}=0.9397 \\ \\
\operatorname{\mathbb{P}}[\bar{D}\mid \bar{A}]&= \frac{\operatorname{\mathbb{P}}[\bar{D}\cap \bar{A}]}{\operatorname{\mathbb{P}}[\bar{A}]} \\
&= \frac{\operatorname{\mathbb{P}}[\bar{A}]+\operatorname{\mathbb{P}}[\bar{D}]-\operatorname{\mathbb{P}}[\bar{A}\cup \bar{D}]}{\operatorname{\mathbb{P}}[\bar{A}]} \\
&= \frac{\operatorname{\mathbb{P}}[\bar{A}]+\operatorname{\mathbb{P}}[\bar{D}]-\operatorname{\mathbb{P}}[\overline{ A\cap D}]}{\operatorname{\mathbb{P}}[\bar{A}]} \\
&=\frac{0.08+0.17-0.22}{0.08} \\
&=\frac{3}{8}
 \end{align}
$$
## 4.
Spot that $\operatorname{\mathbb{E}}[X]=p$ so $\operatorname{g}(\operatorname{\mathbb{E}}[X])=\operatorname{g}\left(p \right).$ Then
$$
\begin{align}
\operatorname{\mathbb{E}}[\operatorname{g}(X)]&=\operatorname{g}(0)(1-p)+\operatorname{g}(1)p \\
&\geq \operatorname{g}(p)=\operatorname{g}(\operatorname{\mathbb{E}}[X])
\end{align}
$$
This is Jensen’s inequality for binary variables. To prove the general case, consider the $\mathrm{DRV}$ $Y$ which has $N$ possible outcomes.
$$
\begin{align}
\operatorname{\mathbb{E}}[\operatorname{g}(Y)]&=\sum\limits_{ n=1 }^{ N }p_{n}\operatorname{g}(y_{n}) \\
&=p_{1}\operatorname{g}(y_{1})+(1-p_{1})\operatorname{g}(\bar{y}_{1}) \\
&\geq \operatorname{g}\left( p_{1}y_{1}+(1-p_{1})\bar{y}_{1} \right) \\
&=\operatorname{g}\left( p_{1}y_{1}+\sum\limits_{ n=2 }^{ N }p_{n}y_{n} \right) \\
&=\operatorname{g}(\operatorname{\mathbb{E}}[Y])
 \end{align}
$$
## 5.

The entropy of $X$ is defined as the expectation of the information,
$$
\operatorname{\mathbb{H}}[X]=\operatorname{\mathbb{E}}[-\log_{2}P_{X}]
$$
For the first case, 
$$
\begin{align}
\operatorname{\mathbb{H}}[X]&=\sum\limits_{ n=1 }^{ 3 }p_{n}\log_{2} \frac{1}{p_{n}} \\
&=\frac{3}{8}\log_{2} \frac{8}{3}+ \frac{3}{8}\log_{2} \frac{8}{3}+ \frac{2}{8}\log \frac{8}{2} \\
&=\pu{1.561bits}
 \end{align}
$$
Following the change $X\mapsto X',$ there is only one week with 1 supervision and the rest have 2 supervisions,
$$
\begin{align}
\operatorname{\mathbb{H}}[X']&=\frac{1}{8}\log_{2}8+ \frac{7}{8}\log_{2} \frac{8}{7} \\
&=\pu{0.5436bits}
 \end{align}
$$
For the uniform distribution $Y$ of $\mathrm{IB}$ students, we have $p= \frac{1}{16}$ so
$$
\begin{align}
\operatorname{\mathbb{H}}[Y]&=\sum\limits_{ n=0 }^{ 15 } p\log_{2} \frac{1}{p} \\
&=\log_{2}16 \\
&=\pu{4bits}
 \end{align}
$$
## 6.
$$
\begin{align}
X&\sim \mathcal{B}(5,0.85) \\
\operatorname{\mathbb{P}}[X\leq 3]&=0.16479
 \end{align}
$$
For the new test, we require
$$
\begin{align}
(1-p)^{5}&=1-0.16479 \\
p&=0.03537
\end{align}
$$
## 7.
$$
\begin{align}
A&\sim \operatorname{Po}(2) \\
\operatorname{\mathbb{P}}[A=0]&=0.1353 \\
 \\
B&\sim \operatorname{Po}(4) \\
\operatorname{\mathbb{P}}[B=0]&=\operatorname{\mathbb{P}}[A=0]^{2}=0.1832 
 \end{align}
$$
If the cabs are equidistant in time, then their arrival is certain so the probability of them not arriving is zero.

With the original $A\sim \operatorname{Po}(2),$
$$
\begin{align}
\operatorname{\mathbb{P}}[A\geq 2]&=1-\operatorname{\mathbb{P}}[A\leq 1] \\
&=0.5940
 \end{align}
$$
## 8.
$$
\begin{align}
X&\sim \mathcal{N}(1830,460^{2}) \\
\operatorname{\mathbb{P}}[X>2750]&=1-\operatorname{\mathbb{P}}[X\leq 2750] \\
&=0.02275
 \end{align}
$$
## 9.
$$
\begin{align}
R&\sim \mathcal{N}(501,3^{2}) \\
\operatorname{\mathbb{P}}[R<498\cup R>508]&=1-\operatorname{\mathbb{P}}[498<R<508] \\
&=0.1685
\end{align}
$$
To minimise the wastage, adjust the mean to be centred in between the rejection regions, $\mu'= \frac{498+508}{2}=503.$
$$
\begin{align}
R'&\sim \mathcal{N}(503,3^{2}) \\
\operatorname{\mathbb{P}}[R'<498\cup R'>508]&=1-\operatorname{\mathbb{P}}[498<R'<508] \\
&=0.09558
 \end{align}
$$
To halve the wasted proportion for an adjusted distribution $R^{*}\sim \mathcal{N}(501,\sigma^{2}),$ we require
$$
\begin{align}
p_{l}\triangleq\operatorname{\mathbb{P}}[R^{*}<498]&= \frac{1}{2}\operatorname{\mathbb{P}}[R<498]=0.07933 \\
p_{u}\triangleq\operatorname{\mathbb{P}}[R^{*}<508]&=1-\frac{1}{2}\operatorname{\mathbb{P}}[R>508]=0.9951
\end{align}
$$
We will consider $p_{u}$ to be negligibly close to 1. Now consider the standard normal $Z \sim \mathcal{N}(0,1).$ 
$$
\begin{align}
\operatorname{\mathbb{P}}[Z<z]&=p \\
z_{l}&= -1.4096= \frac{498-501}{\sigma}\\
\sigma&\approx2.12
 \end{align}
$$
