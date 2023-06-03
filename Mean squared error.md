---
tags: 🌱
alias: MSE
date: 02--May--2023
---

# Mean squared error

Use of training MSE and test MSE may seem to be closely related, but there is no guarantee that the function with lowest training MSE will have the lowest test MSE.
$$MSE = \frac{1}{n}\sum_{i=1}^n(y_i - \hat{f}(x_i))^2$$
## Relation to test [[Prediction]]
Having a small MSE on the training data is not of key interest, rather the test is if $\hat{f}(x_0)$ is approximately $y_0$.


---
Links: 