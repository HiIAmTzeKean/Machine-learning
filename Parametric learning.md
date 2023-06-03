---
tags: 🌱
date: 02--May--2023
---

# Parametric learning
Reducing the problem of estimating $f$ down to estimating a set of parameters
## Approach
Two-step model-based approach
1. Assumption of functional form made
    1. Such as the form being a linear model ([[Linear regression]])
2. A procedure that uses training data to fit the model executed
    1. A common method is using [[Least squares]]
## Advantage
- Estimating only a small set of [[Coefficient]] 
    - [[Test statistic]] can be performed easily
## Limitation
- The model that we choose in step 1 may not match the true form of f
    - Resolution of this issue can be done with [[Flexible model]]
    - This might lead to [[Overfitting]] if not careful
    - [[K nearest neighbours]]
---
Links: 