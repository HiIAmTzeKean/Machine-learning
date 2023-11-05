---
tags:
  - 🌱
  - ComputerScience
  - MachineLearning
date: 03--Jun--2023
---

# Bias and variance trade-off
## Bias and variance
Increasing the [[Bias]] by using simple algorithms or decreasing the number of [[Predictor]] used through methods like [[Shrinkage methods]] or [[Dimension reduction method]] can reduce the chances of [[Overfitting]] → [[Variance reduction]].

When the bias is too high, the model might [[Underfit]], the model might fail to capture hidden patterns in the data. Overall the trade-off results in a [[Mean squared error]] [[U shaped graph]].
## Dimension of data
![[Prediction accuracy#Relation to Training data]]
## Relation with [[Flexible model]] and [[Model interpretability]]
### Flexibility
As the number of [[Coefficient]] used in models such as [[Linear regression]] increases, the bias will start to decrease as the number of underlying assumptions made decreases. The variance will however increase since the model is now more sensitive to a smaller change in [[Training data]]. This causes the model to be more flexible. Note that the underlying [[Statistic]] behind it is due to the increase in the [[Degree of freedom]], where the model is better fitted to the observation with more independent information.
### Model interpretation
As the model becomes more [[Flexible model]] due to the increase in the number of predictors used, the model becomes harder to interpret. This is due to the model fitting more complex relationships between the [[Predictor]] and [[Response]].
## Bias perspective
[[Validation set approach]] can lead to [[Overestimate test error rate]] since training set used only contains half of the observations. 
- [[Leave one out cross validation]] will give approximately [[Unbiased estimate of test error]] since each [[Training data]] is large at $n-1$
- [[k Fold cross validation]] on the other hand only has $(k-1) \frac{n}{k}$ observation. Hence, from a [[Bias reduction]] standpoint. LOOCV is preferred
## Procedure's variance perspective
- LOOCV has higher variance than k-fold with $k<n$
    - LOOCV averages the output of n fitted models each trained on almost identical observations. The outputs are highly [[Correlation|Correlated]] due to the high overlap in training data for each training set
    - K-fold averages the output of k fitted models. Outputs have less correlation since the overlap between training set is smaller
    - [[Mean of highly correlated quantities has higher variance]]. Refer to variance

---
Links: [[Bias]] - [[Variance]] - [[Estimating test error]]