---
tags: 🌱, TOCHECK
alias: logit
date: 18--May--2023
---

# Log-odds

The log-odds or also known as logit
$$\log(\frac{P(X)}{1-P(X)}) = \beta_0 + \beta_1X$$
## Relation to [[Logistic regression]]
The logistic regression model has a logit linear in X as seen from above.
### [[Logistic regression]] difference to [[Linear regression]]
In [[Linear regression]], $\beta_1$ is the average change a unit increase in X. But in [[Logistic regression]] increasing X by one unit changes the log-odds by $\beta_1$ or equivalently multiplies the odd by $e^{\beta_1}$. Since the relationship with P(X) and X is not a straight line, the amount P(X) changes due to one unit change of X depends on the current value of X. 

---
Links: 