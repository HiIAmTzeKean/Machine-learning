---
tags: 🌱
date: 25--May--2023
---

# Best subset selection

Fit a separate [[least squares]] [[regression]] for each possible combination of p predictors.
## Complexity
$O(2^p)$ time complexity
## Algorithm
1. Let M_0 denote null model which contains no [[Predictor]]. Thus, the model predicts only the sample mean for any observation
2. For k=1,…p
    1. Fit $p \choose k$ model that contains k predictor
    2. Pick the best model, denoted as M_k. The best can be measured using the smallest [[Residual sum of squares]] or largest [[R square]]
3. Select a single best model from $M_0,...M_p$
## Considerations
[[Residual sum of squares|RSS]] decreases monotonically as the number of [[Predictor]] used increases. As a result, [[R square]] increases monotonically. The choice of highest [[R square]] is not always accurate since it reflects only low [[Training error rate]].
## Application to [[Classification]] models
The same method can be done for [[Logistic regression]], but instead of using RSS to measure the goodness of the model, [[Deviance]] is used instead.
## Choice of best
- Use of [[Information criteria]]
## Limitations
- Computationally not feasible for large values of p
- When p is large, algorithm also suffers from statistical problem
    - Large search space increase chance of fitting a model well on [[Training data]] but might have poor [[Prediction accuracy]].
    - Leads to [[Overfitting]] and high [[Variance]] of [[Coefficient]] estimate.
---
Links: [[Subset selection]]