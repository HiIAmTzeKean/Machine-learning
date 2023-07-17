---
tags: 🌱
alias: Predicting
date: 02--May--2023
---

# Prediction
Suppose response Y and different predictors (X_1,X_2…X_n) are such that there is a relationship with Y and X = (X_1,X_2…X_n).
$$Y=f(x) + \epsilon$$
where epsilon is a random [[Error term]] independent of X and has mean zero
## Approximating Y
When some inputs X are available, we want to predict the value Y
$$\hat{Y}=\hat{f}(X)$$
where $\hat{Y} \approx Y$
### Accuracy
$$E(Y-\hat{Y})^2=[f(X)-\hat{f}(X)]^2 + Var(\epsilon)$$
### Reducible error
Using $\hat{f}$ to predict $f$ is not always perfect, by the error can be reduced with by using statistical learning.
#### Cases
- Model does not capture true relationship
- Insufficient features
- [[Overfitting]]
### Irreducible error
Suppose the perfect estimator is learnt $\hat{Y}=f(X)$, the prediction would still have error since $Y=f(x) + \epsilon$ → Y function of [[Error term]] which cannot be predicted by X.

---
Links: 