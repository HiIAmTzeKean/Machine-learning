---
tags: 🌱
date: 03--Jun--2023
---

# Mean of highly correlated quantities has higher variance

Refer to [[Variance sum law#Variance sum law 2]] whereby [[Correlation|Correlated]] variables have higher variance due to the presence of [[Covariance]] not being zero. As for the [[Mean]] being higher, suppose now there are 2 variables X and Y. If both are highly correlated, then X and Y are likely to increase in the same direction, causing the mean to rise together.

## Intuition
![[Pasted image 20230603121527.png]]
When the variables are correlated the possible [[sample space]] is constrained. Looking at fig 5, when X increases, Y must increase as well. Overall the variance of the mean of X+Y is greater as the possible values are more spread out. In contrast, fig 3 shows the case when the variables are not correlated, giving a more [[Gaussian distribution]].
As for Fig 1 and 2, note that the seemingly smaller variance is a result of the negative correlation. Recall the formula $\sigma_{X+Y} = \sigma_X + \sigma_Y \pm 2Cov(X,Y)$, where negative covariance will reduce the combined variance.
## Other references
[Intuitive explanation through dice](https://stats.stackexchange.com/questions/464200/why-highly-correlated-means-higher-variance)

---
Links: 