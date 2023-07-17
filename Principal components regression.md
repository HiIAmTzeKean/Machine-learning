---
tags: 🌱
alias: PCR
date: 07--Jun--2023
---

# Principal components regression

Constructing the first M [[Principal component]] and using these as a [[Predictor]] in [[Linear regression]] model fitted using [[Least squares]]. The use of [[Principal component]] is the same as choosing [[Linear combination]] that best represent X.
## Idea
- Small number of [[Principal component]] are sufficient to explain the [[Variance]] in data
    - Direction that X show most variation is the direction that is highly associated with Y (the response being predicted)
    - This assumption is generally true, but there are minor exceptions.
- Fitting a [[Least squares]] solution using $Z_1,…Z_M$ instead of $X_1,…X_p$ with $M \ll p$ mitigates [[Overfitting]]
## Challenge
### Similar challenge to [[Linear regression]]
- Increasing the number of [[Principal component]] used in [[Regression]] causes the bias to decrease and the [[Variance]] to increase
    - Creates [[U shaped graph]]
### PCR does not perform [[Feature selection]]
- All M principal components is a [[Linear combination]] of **all p** original features
- PCR might have lesser than p [[Coefficient]] but it is reliant on all p features
- PCR in that sense is more similar to [[Ridge regression]] than [[The lasso]]
### Unsupervised drawback
The [[Unsupervised learning]] of [[Principal component]] chosen does not guarantee that the best linear combination of X is the best for predicting Y too 
### Special case when it reduces to linear regression
Note that when the number of [[Principal component]] equals to number of predictors, then PCR performs like [[Linear regression]]
## Choosing [[Principal component]]
- Use of [[Cross validation]]
    - The model with the lowest [[Cross validation]] error
- Use of [[Standardization]] on [[Predictor]] before generating [[Principal component]]
    - Ensures that variables are on the same scale
    - Without standardization, variables with high variance will play a larger role in [[Principal component]] (absolute value of difference is large, but the deviation from [[Mean]] may not be as large when standardized)
- [[Unsupervised learning]] where the choice of [[Principal component]] depends on X and not Y [[Response]]

---
Links: 