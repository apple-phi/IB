Bayes’ rule:
$$
\mathbb{P}[\mathcal{A}|\mathcal{B}]= \frac{\mathbb{P}{[\mathcal{A}\cap \mathcal{B}]}}{\mathbb{P}[\mathcal{B}]}
$$
Hence the Law of Total Probability follows:
$$
\mathbb{P}[\mathcal{A}]=\mathbb{P}[\mathcal{A}|\mathcal{B}]\cdot\mathbb{P}[\mathcal{B}]+\mathbb{P}[\mathcal{A}|\overline{\mathcal{B}}]\cdot\mathbb{P}[\overline{\mathcal{B}}]
$$
More generally, for a set of *pairwise incompatible* events with $\Omega=\bigcup \mathcal{B}_{i}$
$$
\mathbb{P}[\mathcal{A}]=\sum\mathbb{P}[\mathcal{A}|\mathcal{B}_{i}]\cdot \mathbb{P}[\mathcal{B}_{i}]
$$

### Inverting conditional probabilities
Using Bayes’ rule:
$$
\begin{align}
\mathbb{P}[\mathcal{A\cap B}] & =\mathbb{P}[\mathcal{B\cap A}] \\
\mathbb{P}[\mathcal{A|B}]\cdot \mathbb{P}[\mathcal{B}] & =\mathbb{P}[\mathcal{B|A}]\cdot \mathbb{P}[\mathcal{A}] \\
 \\
\Rightarrow\quad \frac{\mathbb{P}[\mathcal{A| B}]}{\mathbb{P}[\mathcal{B|A}]} & = \frac{\mathbb{P}[\mathcal{A}]}{\mathbb{P}[\mathcal{B}]}
\end{align}
$$

### Independence
This property of a statistic is true if the probability of one sub-result does not change the probability of another, i.e.
$$
\begin{align}
\mathbb{P}[\mathcal{A}|\mathcal{B}] & =\mathbb{P}[\mathcal{A}] \\ \\
\Rightarrow\quad \mathbb{P}[\mathcal{A\cap B}] & =\mathbb{P}[\mathcal{A}]\times \mathbb{P}[\mathcal{B}]
\end{align}
$$