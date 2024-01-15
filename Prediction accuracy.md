---
tags:
  - 🌱
  - ComputerScience
  - MachineLearning
date: 25--May--2023
---

# Prediction accuracy
The true relationship between the [[Response]] and [[Predictor]] is approximately [[Linear]] such that the [[Least squares]] estimate will be a low bias. 
## Relation to [[Train data]]
### When $n \gg p$
If $n \gg p$, where n is number of observations and p is the number of predictors, then the estimate will tend to have low [[Variance]]. 
### When $n>p$
If $n>p$ by a small margin, then there can be a lot of [[Variability]] in the least squares fit. [[Overfitting]] can occur.
### When $p>n$
If $p>n$ then variance is infinite, it doesn't make sense to use [[Least squares]] method
#### Loss of [[Unique]] solution
In the case of [[Linear regression]], the model is said to be [[Overdetermined]]. Since there are more equations than the unknown variables ([[Coefficient]]), then there will not be any [[Unique]] solution. The [[Coefficient]] estimates will result in a perfect fit to the data such that the [[Residual]]s are zero.
#### [[Overfitting]]
The model will fit the training data closely since there is too many [[Degree of freedom]]. [[Noise]] in the data would be fitted in the process.
#### [[High dimension data]]
*Never* use [[Residual sum of squares]], [[p-value]], [[R square]] or traditional [[Statistic]] method for [[Training error rate]] since [[Overfitting]] might occur and inaccurate values might be obtained. For example, when $p>n, R^2 =1$.
Instead, [[Test error rate]] should be reported based on these [[Statistic]] or [[Cross validation]] to be used.
## Question
- What is the link between accuracy with [[Bias]] and [[Variance]]

---
Links: 