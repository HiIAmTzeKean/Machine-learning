---
tags: 🌱
date: 09--Jun--2023
---

# High dimension data
Traditional [[Statistical learning]] for [[Regression]] and [[Classification]] are intended for [[Low dimension data]]. 
With the advent of [[Big data]], the number of [[Predictor]]s available become extremely large, while the cost of obtaining [[Training data]] become increasingly costly. These data are known as high dimensional.
## Limitations of classical approach
[[Linear regression]] is not suited for such data especially when $p > n$. This can be seen from [[Bias and variance trade-off#Dimension of data]] where [[Overfitting]] is likely to occur.
[[Least squares]] is too [[Flexible model|Flexible]] and fits the data perfectly. As the number of observations continue to decrease, the [[Mean squared error|MSE]] of test set will increase since [[Variance]] of estimate will increase as the model becomes more flexible.
Use of [[R square]] and [[Training data]] MSE is insufficient since these statistic will give misleading results. [[Cp]], [[AIC]], [[Adjusted R square]] and [[BIC]] are also not appropriate as estimating $\sigma^2$ becomes difficult.
### Overcoming limitations
Less [[Flexible model]] like [[Forward stepwise selection]], [[Ridge regression]], [[The lasso]] and [[Principal components regression]] are useful as it avoids overfitting thorough using a less flexible approach.
## Impact to [[Prediction accuracy]]
1. [[Shrinkage methods|Regularisation]] is important in resolving [[High dimension data]] problems
2. The choice of [[Parameter]] is important
3. [[Test error rate]] increases as [[Dimension]] increase (more [[Predictor]] used) unless the additional dimensions added are [[Correlation|Correlated]] with the [[Response]]
    1. Also known as [[Curse of dimensionality]]
## Interpreting results
With relation to [[Multiple linear regression]], where variables are tested for [[Correlation]], performing such a check in high dimensional setting is tougher. Any variable in the model can be written as a [[Linear combination]] of other variables.  Thus, it is difficult to identify true variables that predict the outcome. The best that can be done is to estimate the important [[Predictor]] by assigning a large [[Coefficient]].
### [[Error rate]]
Model fit can also be tricky especially when $p>n$, with reference to [[Prediction accuracy#When $p>n$]].

---
Links: [[Bias and variance trade-off]]