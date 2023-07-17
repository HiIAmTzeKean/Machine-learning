---
tags: 🌱
date: 25--May--2023
---

# R square

Also known as coefficient of determination. It is a [[Statistic]] measure of how much the [[Variance]] of the dependent variable is explained by an independent variable.
$$R^2 = (1- \frac{RSS}{TSS})$$
Where [[Residual sum of squares|RSS]] and [[Total sum of squares|TSS]].
## Properties
- $0 \le R^2 \le 1$
    - Small values indicates that the independent variable does not explain most of the variation in the dependent variable.
    - Large values indicate that the independent variable explains most of the variation in the dependent variable
- Linked to [[Correlation]] where R^2 is just the square of the correlation coefficient
## R^2 versus Correlation
The choice of R^2 makes it more intuitive to interpret the statistic. Where R^2 = 0.5 means that the independent variable explains 50% of the variation in the dependent variable.
## Selection of models with varying variables
When deciding which [[Predictor]] to include in a model, $R^2$ performs poorly because it tends to decrease as the number of variables increase.
## Others
---
Links: 