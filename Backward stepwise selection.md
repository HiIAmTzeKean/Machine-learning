---
tags:
  - 🌱
  - ComputerScience
  - MachineLearning
date: 03--Jun--2023
---

# Backward stepwise selection

Begins with the full [[Least squares]] models containing all p predictor and iteratively removes the least useful [[Predictor]] at each step. [[Feature selection]] via removal of the least useful predictor.
## Algorithm
1. Let $M_p$ denote the full model with p predictor
2. For $k=p,p-1,…,1$
    1. $M_{k-1} \leftarrow M_k \text{ least the useful predictor}$
    2. All k predictors will be considered and the measure of least useful is the one which gives the smallest [[Residual sum of squares|RSS]]
3. Select the single best model
## Challenge
- Like [[Forward stepwise selection]], there is no guarantee of yielding the best model since the optimal solution might not be a subset of the previous steps
- Require number of samples n larger than number of variables p
    - Else model cannot be fit. Refer to [[Prediction accuracy]], where there is no [[Unique]] solution
    - If a model cannot be fitted then it is impossible to know which predictor to remove when $p \ge n$

---
Links: 