---
tags: 🌱
date: 24--May--2023
---

# Linear model selection
## Comparison to [[Least squares]]
An alternative fitting procedure can yield better [[Prediction accuracy]] and [[Model interpretability]].
## Classes of [[Model selection]]
- [[Subset selection]]
    - Identify a subset of p [[Predictor]] related to response and fit a model using [[Least squares]] on the reduced set
- [[Shrinkage methods]]
    - Fitting all p [[Predictor]] but [[Coefficient]] are shrunken towards 0. This process is known as [[Regularisation]] and has the effect of reducing [[Variance]]. Depending on the extent of the shrinkage, some coefficient may become zero allowing this method to perform[[ variable selection]]
- [[Dimension reduction methods]]
    - [[Projection]] of p predictors into M-dimensional subspace, with $M<p$. This is done through computing M different [[Linear combination]]

---
Links: 