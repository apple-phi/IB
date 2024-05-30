We define the $p$-value of a result as the probability $p$ of obtaining a result at least as extreme, given $\mathcal{H}_{0}$ is true.

A result is statistically significant and $\mathcal{H}_{0}$ is rejected if $p\leq\alpha$ where $\alpha$ is the significant level.

>This is *reductio ad absurdum*. 

Also see Lucas’s old A-level notes at [Hypothesis testing Flashcards | Quizlet](https://quizlet.com/gb/577268476/hypothesis-testing-flash-cards) 
## Recipe
1. Assume $\mathcal{H}_{0}$ and state $\mathcal{H}_{1}$
2. State whether the test is one- or two-sided
3. Find $p$
4. Compare $p$ to $\alpha$ 
5. If $p\leq\alpha$, the test statistic is significant so reject $\mathcal{H}_{0}$
6. If $p>\alpha$, the test statistic is not significant so accept $\mathcal{H}_{0}$

## Remarks
A common abuse of statistics is to assign $p$ to the probability of $\mathcal{H}_{0}$. It may be unintuitive but it should be obvious that
$$
\operatorname{\mathbb{P}}[\mathbf{x}\mid \mathcal{H}_{0}]\neq \operatorname{\mathbb{P}}[\mathcal{H}_{0}\mid \mathbf{x}]\neq \operatorname{\mathbb{P}}[\mathcal{H}_{0}]
$$
>This has led to some dramatic miscarriages of justice…

Finding the probability of the alternative hypothesis doesn’t carry a lot of information about the validity of $\mathcal{H}_{0}$