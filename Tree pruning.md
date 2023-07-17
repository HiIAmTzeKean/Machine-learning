---
tags: 🌱
date: 28--Jun--2023
---

# Tree pruning
Standard [[Binary splitting]] to obtain a [[Decision tree]] is can cause [[Overfitting]]. While setting a [[Decision tree split threshold]] might help reduce the overfit, there may be good splits that are missed since good splits may come after a bad split.

Instead, a better strategy is to grow a large [[Tree]] and then prune it to obtain a [[Subtree]].  To obtain a good subtree, methods like [[Cross validation]] or [[Validation set approach]] can be done. However, to test each subtree is not feasible and hence [[Cost complexity pruning]] is typically used.
## Algorithm
1. Use [[Recursive binary splitting]] to grow a large tree and stop only when terminal node has fewer than some set number of observations
2. Apply Cost complexity pruning to obtain sequence of best trees as function of $\alpha$
3. Use [[k Fold cross validation]] to choose $\alpha$
    1. Repeat step 1 and 2 on all but the kth fold
    2. Evaluate the [[Mean squared error]] on the kth fold as function of $\alpha$
4. Return subtree from step 2 that correspond to $\alpha$ chosen
### Proof
For each alpha, there is a subtree $T \subset T_0$ such that the equation below is small
$$\sum_{m=1}^{|T|} \sum_{i: x_i \in R_m} {(y_i - \hat y_{R_m}) ^2 + \alpha |T|}$$
- |T| is the number of terminal nodes of T
- R_m is the subset of predictor space corresponding to the mth [[Terminal node]]
- $\hat y_{R_m}$ is predicted response for $R_m$ (prediction of [[Decision tree]] uses the [[Mean]] of the values)
- $\alpha$ controls the trade off between [[Complex|Complexity]] and fit to [[Training data]]
    - When $\alpha = 0, T = T_0$ since the equation only measures the [[Residual sum of squares|RSS]], refer to [[Residual sum of squares#Decision trees]]
    - As alpha increases, the penalty for having more [[Terminal node]] is larger, thus favouring trees with less nodes. This control is similar to [[The lasso]] 

---
Links: 