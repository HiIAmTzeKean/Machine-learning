---
tags: 🌱
date: 23--May--2023
---

# k Fold cross validation

The observations are randomly ([[Randomness]]) divided into k groups/folds of approximately equal sizes. The algorithm iterates for each fold, where $fold_i$ treated as the [[Validation set]] and the model is fitted on k-1 folds. The MSE of each fold is computed $MSE_1,MSE_2...MSE_k$ and the overall CV estimate is computed by averaging the values.
$$CV_k = \frac{1}{k}\sum_{i-1}^k MSE_i$$
[[Leave one out cross validation]] is a special case of k fold, where k=n such that there are n folds.
## Advantage
- If $k<n$ then the computational cost is lower than [[Leave one out cross validation|LOOCV]]
    - There is some [[Variability]] but the overall variability is still lover than [[Validation set approach]]
- [[Bias and variance trade-off]]

---
Links: [[Cross validation]] [[Mean squared error]]