---
tags:
  - 🌱
  - ComputerScience
  - MachineLearning
date: 19--May--2023
---

# Linear discriminant analysis
Model [[Predictor]] X in each [[Response]] Y $P(X|Y)$ and through [[Bayes Theorem]] to obtain $P(Y|X)$. If the distribution are assumed to be normal, the model will be in similar in form to [[Logistic regression]].
## Advantage over [[Logistic regression]]
- When classes well separated, logistic regression model are unstable than linear discriminant analysis
- If n is small and distribution of [[Predictor]] approximately normal, [[Linear discriminant analysis]] is more stable
## Application of Bayes' Theorem
- $\pi_k$ be [[Prior probability]] that randomly chosen observation from kth class
- $f_k(x) \equiv P(X=x|Y=k)$ denote [[Probability density function]] of X coming from kth class
    - $f_k(x)$ will be large if high probability observation in kth class has X=x
$$P_k(X) = P(Y=k|X=x) = \frac{\pi_kf_k(x)}{\sum_{l=1}^K \pi_l f_l(x)}$$

## Method
Assuming only one predictor.
LDA attempts to estimate $f_k(x)$

---
Links: 