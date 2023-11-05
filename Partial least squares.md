---
tags:
  - 🌱
  - ComputerScience
  - MachineLearning
alias: PLS
date: 05--Jun--2023
---

# Partial least squares

[[Supervised learning]] alternative compared to [[Principal components regression|PCR]]. Is also a [[Dimension reduction method]]
## Overcoming challenge of PCR
![[Principal components regression#Unsupervised drawback]]
M [[Linear combination]] of original features are still identified, but the [[Principal component]] that is chosen will approximate both [[Predictor]] X and [[Response]] Y.
## Idea
- [[Standardisation]] of p [[Predictor]]
- Set each $\phi$ equal to the [[Coefficient]] from [[Simple linear regression]]
    - [[Coefficient proportional to correlation]] between Y and X
    - If Y highly correlated to X, then $\phi$ will be higher
    - This places more weight onto [[Predictor]] strongly related
    - This sets the first [[Principal component]], $Z_1$
- The subsequent [[Principal component]] is chosen via
    - Adjusting each variable for Z_1 by [[Regression|Regressing]] each variable on Z_1 and taking the [[Residual]]
    - The residual can be interpreted as the remaining information that has not been explained by the first [[Principal component]]
    - The next [[Principal component]] computed using [[Orthogonal|Orthogonalized]] data
- Once M components are identified, fit using [[Least squares]]
### Selecting M
[[Cross validation]] is used to selected the M number of principal component
## Use case
- [[Chemometrics]]
- [[Digitized spectrometry signals]]
## Performance
Generally does not perform any better than [[Ridge regression]] or [[Principal components regression]] even though there is use of additional information.
## Challenge
[[Supervised learning]] can reduce [[Bias]] but can increase [[Variance]].

---
Links: [[Correlation]] - [[Coefficient]]