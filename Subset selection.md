---
tags: 🌱
date: 25--May--2023
---

# Subset selection
- [[Best subset selection]]
- [[Stepwise model selection]]
## Idea
Performing [[Feature selection]] on a set of [[Predictor]] to derive a model with a subset of predictors that best model the response. Choosing the best algorithm depends on the time complexity and also the model that results in the smallest number of predictors chosen to minimise [[Overfitting]].
## Questions
- When performing [[Best subset selection]], [[Forward stepwise selection]], [[Backward stepwise selection]], which of the 3 models will have the smallest [[Training error rate]] and consequently smallest training [[Residual sum of squares]]
- Following up from previous question, which will have smallest [[Test error rate]]
- The [[Predictor]] in a k-variable model identified by [[Forward stepwise selection]] is a subset of the predictors in its (K+1) step
- The predictor for a k-variable model identified by [[Backward stepwise selection]] is a subset of the predictors in its (K+1) step
- The predictor in the k-variable model identified by [[Forward stepwise selection]] is a subset of the predictor in the K+1 variable model identified by [[Backward stepwise selection]]
    - In essence, the question is asking if there is a connection between the forward stepwise and backward stepwise method


---
Links: 