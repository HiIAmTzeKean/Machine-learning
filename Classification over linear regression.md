---
tags: 🌱
date: 18--May--2023
---

# Classification over linear regression

[[Problems with linear regression]] also include [[Linear regression]] being inappropriate in dealing with qualitative response.
## Illustration
Given 3 [[Qualitative]] responses, [[Encoding]] each response with an index value can be a possible approach.
$$Y = \begin{cases}
1 & \text{if } X_1\\
2 & \text{if } X_2\\
3 & \text{if } X_3
\end{cases}$$
but this encoding implies
1. Ordering of outcome matters
2. Difference between X_1 and X_2 is the same as the difference between X_2 and X_3

Each different encoding will create different linear models and thus different predictions. Even if the response has natural ordering like {good, fine, bad}, the gap between the response would also have to be similar. In general there is no natural way to convert [[Qualitative]] to [[Quantitative]].
## Binary response
In the case of 2 responses, [[Linear regression]] can work since the [[Dummy variable]] approach can be applied. Even if the encoding was swapped, the regression would still have the same predictions.
### Issue with linear regression on binary response
The estimates can like outside the \[0,1\] interval.
$$P(X) = \beta_0 + \beta_1X$$
Then depending on \beta_0, when the X is small and if the graph intercepts the x-axis, P(X) becomes negative. For large values of X, the graph will exceed 1. 
### Issue with dummy variable approach
Cannot extend to more than 2 levels.

---
Links: [[Classification]]