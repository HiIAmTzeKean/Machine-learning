---
tags:
  - 🌱
  - ComputerScience
  - MachineLearning
alias: LOOCV
date: 22--May--2023
---

# Leave one out cross validation

Closely linked to [[Validation set approach]] but instead of splitting the observations in half, only a single observation is used for [[Validation set]] and all other $n-1$ observations are used for [[Training data]].
## Usage
- A single observation is left out and $n-1$ observation used to train the model
- $MSE_1=(y_1 - \hat{y}_1)^2$ is unbiased since (x_1,y_1) not used in training
    - But use of a single point is highly variable
    - This can be mitigated by iterating through all $n$ observations
- $CV_n = \frac{1}{n} \sum_{i=1}^n MSE_i$
## Advantage
- Less bias than [[Validation set approach]] since n-1 observations are used to fit the model as compared to half of the observation pool
    - LOOCS tends to not [[Overestimate test error rate]] as much as [[Validation set]]
- Unlike validation set approach that yields different results when applied repeatedly due to [[Randomness]] in the split, LOOCV will always yield the same results since there is no randomness in the split
## Disadvantage
- High computational cost from fitting n times
    - Can be overcome with [[Linear regression]] as a shortcut to make LOOCV the same as a single model fit
    - $CV_n = \frac{1}{n} \sum_i^n(\frac{y_i-\hat{y}_i}{1-h_i})^2$
    - $\hat{y}_i$ is the fitted value from the [[Least squares]] fit and $h_i$ is the [[Leverage statistic]]
    -  Leverage lies between 1/n and 1 and reflects the amount that an observation influence the fit
    - Residuals for high leverage points are inflated by the right amount for the equity to hold
- High procedure [[Variance]] as the training sets at each step is almost identical
    - $\frac{1}{n} \sum_{i=1}^n MSE_i$ is the averaging of the model output of each training set
    - Output are highly [[Correlation|Correlated]] with each other caused by the huge overlap between training sets

---
Links: [[Mean squared error]] [[Cross validation]]