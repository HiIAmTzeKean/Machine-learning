---
tags: 🌱
date: 03--Jun--2023
---

# BIC

[[Bayesian]] information criteria
Derived from Bayesian view point
$$BIC = \frac{1}{n}(RSS + \log(n)d\hat \sigma^2)$$
## Intuition
- Similar to the other [[Information criteria]] estimates, BIC takes on small values for models with small [[Test error rate]]
## Differences to [[Cp]] and [[AIC]]
The constant term used in Cp and AIC is replaced with $\log(n)$ instead. $\log(n) > 2$ for $n \gt 7$, thus a greater penalty by BIC for models that have more variables. This causes [[BIC]] to choose smaller models. 

---
Links: 