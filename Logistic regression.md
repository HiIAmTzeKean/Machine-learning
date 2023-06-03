---
tags: 🌱
date: 18--May--2023
---

# Logistic regression
Models the probability that Y belongs to a particular category $P(Y|X)$ using logistic function. Succinctly, learning P(Y|X). 
## Overcoming limitations of linear regression
Logistics regressions attempts to resolve this issue [[Classification over linear regression#Issue with linear regression on binary response]].
Modelling P(X) using a function bounded by \[0,\1] such as a [[Logistic function]] ensures that the prediction is bounded.
## Fitting model with binary response
### Assuming there is only 1 predictor
[[Maximum likelihood]] approach is used. Regardless the value of X, the [[Logistic function]] will produce an S-shaped curve to ensure that the prediction is sensible.
#### Odds
By manipulating the [[Logistic function]]
$$odds=\frac{P(X)}{1-P(X)} = e^{\beta_0 + \beta_1X} \in [0,\infty]$$
the [[Odds]] can be obtained. Small value of odds represent low probability, while higher odds represent higher probability.
#### log-odds/ logit
[[Log-odds]]
#### Estimating [[Coefficient]]
[[Maximum likelihood]] method preferred for statistical properties. The intuition is that the coefficients when substituted should be close to the actual P(X) values.
$$likelihood = \mathscr{l}(\beta_0,\beta_1) = \prod_{i:y_i=1} P(x_i) \prod_{i':y_{i'}=0}(1-P(x_{i'}))$$
Where the likelihood of the parameters is to maximise the expression ([[Likelihood function]]).
### Multiple logistics regression
Extension of the formula is similar to [[Linear regression]].
$$\log(\frac{P(X)}{1-P(X)}) = \beta_0 + \beta_1X_1 +...+\beta_pX_p$$
for p predictors. Similarly, the equation can be rewritten to obtain the [[Logistic function]]
## Conflicting information with single and multiple logistics regression
The coefficient of the [[Dummy variable]] for single regression accounts for the average values of all other [[Predictor]]s. While the [[Coefficient]] of the dummy variable for multiple regression indicates for fixed values of predictors.
## Limitations for >2 response class
[[Linear discriminant analysis]] is a more popular choice compared to other extensions of logistics regression.

---
Links: [[Classification]] - [[Qualitative]]