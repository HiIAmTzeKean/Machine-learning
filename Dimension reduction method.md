---
tags:
  - 🌱
  - ComputerScience
  - MachineLearning
date: 05--Jun--2023
---

# Dimension reduction method

[[Transform]] [[Predictor]]s and fitting a [[Least squares]] model on these variables.
## Formulation
Suppose now there are p [[Predictor]] and transformation is performed on X using a scalar $\phi$. Let $Z_i$ be a [[Linear combination]] of  $X_1,…X_p$, for $Z_1,...Z_M$. This step aims to reduce the dimension of the number of features to fit from p to M.
$$Z_m = \sum_{j=1}^p {\phi_{jm}X_i}$$
$Z_1 = \sum_{j=1}^p {\phi_{j1}X_i} = \phi_{11}X_1 + ... + \phi_{p1}X_p$

Then $Z_1,…Z_M$ can be substituted for $X_1,…X_p$ where $M \lt p$ and $\theta_i$ represents the coefficient for the [[Linear regression]] model. n represents the number of observations in the [[Training data]]. Note the notation $z_{im}$ is used since the response $y_i$ is being predicted by that specific data point.
$$y_i = \theta_0 + \sum_{m=1}^M {\theta_m z_{im} + \epsilon_i},\quad i=1,...n$$
$y_1 = \theta_0 + \sum_{m=1}^M {\theta_m z_{1m} + \epsilon_1}, i=1$
### Dimension reduction
$$ \sum_{m=1}^M {\theta_m z_{im}} = \sum_{m=1}^M {\theta_m} \sum_{j=1}^p {\phi_{jm} x_{ij}} = \sum_{j=1}^p \sum_{m=1}^M {\theta_m \phi_{jm} x_{ij}} = \sum_{j=1}^p {\beta_j x_{ij}}$$
We note that the variables $\theta, \phi, \beta$ are constants and thus not affected by the change in training data point used. Hence the lack of the subscript *i* notation.

The problem of [[Linear regression]] is reduced from p+1 [[Coefficient]]s (inclusive of the intersect) to M+1 [[Coefficient]]s
#### bias coefficient
There is now a constraint on $\beta$ since they must take the form of $\sum_{m=1}^M {\theta_m \phi_{jm}}$. The constraint can bias the [[Coefficient]] estimate.
- When $p \gg n$ training points
    - then $M \ll p$ reduces the [[Variance]] of the coefficients
    - $M=p$ with all $Z_m$ linearly independent poses no constrains. No dimension reduction happens (since p variables are still used) and the problem is equivalent to [[Least squares]] on p predictors.

#### Visual interpretation
![[Drawing 2023-06-08 12.50.14.excalidraw]]

---
Links: 