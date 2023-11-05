---
tags:
  - 🌱
  - ComputerScience
  - MachineLearning
alias: Flexible
date: 29--May--2023
---

# Flexible model
## Idea
Flexible models allow the model to take on more [[Parameter]]/[[Predictor]] that serves to predict the [[Response]]. This allows the model to better fit to the [[Training data]] and consequently better predict the response.
## Challenge
As the number of predictors used increases, the model becomes increasingly [[Complex]] and the [[Variance]] of the [[Response]] tends to increase. This is because the relationship between the response and predictors are not as clear since there can be [[Synergy effect]] between the predictors. However, as the number of parameters used increase, the [[Bias]] of the model decreases as there is less underlying assumptions in the model. [[Interpretation]] of the model will also be tougher.
Cross a point, the model will [[Overfitting|Overfit]] the training data. The [[Training error rate]] will continue to decrease, but the [[Test error rate]] will start to increase. This can be seen on a graph, where a [[U shaped graph]] for test error can be seen.

![[Bias and variance trade-off#Relation with Flexible model and Model interpretability]]

## Questions
- Does [[Flexible model]] give rise to greater [[Prediction accuracy]] when increase in [[Bias]] is less than decrease in [[Variance]]
- When the [[Training data]] n is huge and the number of [[Predictor]] p is small, is a flexible model preferred?
    - Yes, when n is high and p is small it means there is an abundance of data to fit the model to. A method such as [[Stepwise model selection]] could be used to add predictors to the model
- When p is large, and n is small, is a [[Flexible model]] preferred?
    - No. When $p>n$, then [[Bias and variance trade-off#Dimension of data]], the chances of [[Overfitting]] is high, and there is no unique solution to models that are flexible. A non-flexible model is likely to perform better
- When the relationship between [[Predictor]] and [[Response]] highly non-linear, is a flexible model preferred
    - Yes, inflexible models might not be able to capture the underlying patterns in the data set
- When the variance of the [[Error term]] is high $Var(\epsilon)$
    - Then each observations would vary by a large extent.
- What is the advantage of using more flexible models
    - Able to better fit non-linear data

---
Links: [[Bias]] - [[Variance]] - [[Bias and variance trade-off]] - [[Model interpretability]] - [[U shaped graph]] - [[Parametric learning]]