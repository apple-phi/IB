There are two main kinds of statistics:
- Frequentist—considers the long-run frequency in a repeatable experiment
- Bayesian—considers un-repeatable situations (e.g. probability of ice caps melting by 2100), so a subjective prior belief is required

Some definitions:
- Experiment—repeatable procedure with well-defined outcomes
- Sample space—the set of all possible outcomes, $\Omega$
- Event—a *subset* of the sample space, $\mathcal{A}\subseteq\Omega$

The probability $\mathbb{P}$ is a measure space satisfying
$$
\begin{cases}
\begin{align}
\mathbb{P}[\mathcal{A}]&\in\mathbb{R}^{+} \\
\mathbb{P}[\Omega]&=1 \\
\mathbb{P}[\mathcal{A}\cup \mathcal{B}]&=\mathbb{P}[\mathcal{A}]+\mathbb{P}[\mathcal{B}]\quad\text{if}\quad\mathcal{A}\cap \mathcal{B}=\emptyset
\end{align}
\end{cases}
$$

From these axioms, the following can be derived:
$$
\begin{align}
\mathcal{A}\subseteq \mathcal{B} & \Rightarrow\mathbb{P}[\mathcal{A}]  \leq \mathbb{P}[\mathcal{B}] \\
\mathbb{P}[\emptyset] & =0 \\
\mathbb{P}[\overline{\mathcal{A}}]  & =1-\mathbb{P}[\mathcal{A}] \\
0 & \leq \mathbb{P}[\mathcal{A}\in\Omega]\leq 1 \\
\mathbb{P}[A\cup B] & =P[A]+P[B]-P[A\cap B] \\
P[A\cap B] & +P[A\cap\overline B]  =P[A]
\end{align}
$$

A consequence of the additivity axiom is
$$
P[A]=\sum_{\omega\in\mathcal{A}}\mathbb{P}[\omega]
$$
where $\omega\in\Omega$ are the disjoint individual outcomes (atomic event) of the experiment.

### De Morgan’s Theorems
$$
\begin{cases}
\begin{align}
\overline{A\cap B} & =\overline A \cup \overline B \\
\overline{A\cup B} & =\overline A \cap \overline B
\end{align}
\end{cases}
$$
