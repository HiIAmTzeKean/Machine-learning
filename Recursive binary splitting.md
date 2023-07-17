---
tags: 🌱
date: 13--Jun--2023
---

# Recursive binary splitting

More specialised version of a [[Decision tree]]. The predictor $X_j$ and cut point $s$ chosen such that the split $\set{X|X_j\lt s}$ and $\set{X|X_j\ge s}$ leads to the most reduction in [[Residual sum of squares|RSS]].
## Finding optimal model
The optimal model would have the [[Parameter]] j and s such that the equation is minimised
$$RSS = \sum_{i:x_i \in R_1(j,s)} (y_i - \hat y_{R_1})^2 + \sum_{i:x_i \in R_2(j,s)} (y_i - \hat y_{R_2})^2$$
where $R_1(j,s) = \set{X|X_j \le s}$. All possible [[Predictor]] from $X_1, … X_p$ is considered, and some [[Predictor]] $X_j$ is chosen along with the threshold value $s$ that performs the best split. Note how the [[Response]] values are chosen instead to compute the RSS.
## Limitation
The above method can produce good prediction on the [[Training data]] but may [[Overfitting|Overfit]]. the tree might become overly [[Complex]]. A smaller tree (less splits) is more [[Generalisation|Generalise]]able. There is also [[Bias and variance trade-off]], where the fewer splits will lead to lower [[Variance]] and better [[Interpretation]] at the low cost of [[Bias]]. (Note that when there is less split, the data is more likely to fall within a smaller [[Subset]] of regions and thus smaller variance).
### Overcome [[Overfitting]] for binary splitting
1. [[Decision tree split threshold]]
2. [[Tree pruning]]

---
Links: [[Strata]] - [[Binary splitting]]