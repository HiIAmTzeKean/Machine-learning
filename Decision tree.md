---
tags:
  - 🌱
  - ComputerScience
  - MachineLearning
date: 12--Jun--2023
---

# Decision tree

Each region is denoted to be a [[Terminal node]] or [[Leaves]] of a tree, $R_i$. The point at which a split is made is denoted as [[Internal node]].  The segment of a tree that connect the nodes are [[Branches]].
## Prediction through [[Stratifying]]
1. The predictor space is divided into J distinct non-overlapping regions ([[Strata]])
2. Any observation that falls into the same region would result in the same prediction. Which is the mean of the [[Response]] values for the training observation in $R_j$
$$\bar x = 1/n \sum_i^n x_i, |R_j|=n$$
### Obtaining optimal model
#### Decision tree RSS equation
![[Residual sum of squares#Decision trees]]
#### Issue with computing RSS
The optimal model would then be the model with regions such that RSS is minimised. However it is computationally infeasible to compute all possible combinations. Refer to [[Bell number]].
Consider a value J such that it is large, then there are many possible combinations in the set to choose from. Instead, a [[Constraint]] can be placed on J to limit the possible [[Search space]].
### Alternative approach
A [[Top down approach]] with [[Greedy algorithm]] taken. This is also known as [[Recursive binary splitting]]. The algorithm begins at the top and splits the tree to the bottom. At each split, a greedy decision is made, the best action taken instead of look ahead.

---
Links: 