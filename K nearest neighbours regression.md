---
tags: 🌱
date: 16--May--2023
---

# K nearest neighbours regression

Related to [[K nearest neighbours classifier]].
## Approach
1. Given K, and prediction point $x_0$
2. $\mathscr{N}_0 \leftarrow$ Identify K datapoints close to $x_0$
3. $\displaystyle \hat f(x_0) = \frac{1}{K}  \sum_{x_i \in N_0} y_i$ 
## Values of K
### Small K
When K is small, then the number of neighbours used to determine the [[Response]] is less, consequently the model is more [[Flexible model|Flexible]]. There will be less [[Bias]] but higher [[Variance]] since the average is more sensitive to changes in the neighbours chosen.
### Large K
When K is larger, the bias increases and variance decrease since there are more points chosen and the average is more stable. The boundary will be smoother, but these smoothing effect would cause bias in the model by masking some of the structure in $f(X)$

## Question
- What is the difference between [[K nearest neighbours classifier]] and its regression counter part
    - The classifier works by using [[Majority vote approach]] while the regression model uses the average of the responses of the neighbours
    - The classifier produces a [[Qualitative]] output while the regression produces a [[Quantitative]] output

---
Links: 