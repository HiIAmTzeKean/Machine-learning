---
tags: 🌱
date: 01--Jun--2023
---

# Cp
Also known as Mallow's Cp. 
$$C_p = \frac{1}{n} (RSS + 2d \hat \sigma^2)$$
where the fitted model contains d [[Predictor]], $\hat \sigma^2$ is the [[Error term]] for each model response, Cp estimates the test MSE.
## Intuition
- Adding a penalty of $2d\hat \sigma^2$ to training RSS to adjust for the fact that [[Training error rate]] tends to be underestimated
- Penalty increases as $d$ increases, to account for the fact that training RSS decrease as number of predictors increase

---
Links: [[Residual sum of squares|RSS]] - [[Mean squared error]]