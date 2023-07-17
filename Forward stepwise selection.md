---
tags: 🌱
date: 01--Jun--2023
---

# Forward stepwise selection

Reduces the possible [[Search space]] from $2^n$ in [[Best subset selection]] to a smaller space. The idea is to start with the null model then iteratively add the [[Predictor]] with the greatest additional improvement to the model till all predictors are in the model.
[[Feature selection]] via selecting the most useful predictor.
## Algorithm
- $M_0$ denote the null model which contains no predictor
- For k=0,…,p-1
    - Consider all (p-k) models that improve $M_k$ by adding one predictor
    - Take the best of (p-k) models and assign it to $M_{k+1}$
- Select the single best model from $M_0,…M_{k+1}$ using [[Information criteria]]
## Complexity 
- Fitting the null model takes up 1 time step
- For k=0,..,p-1
    - There is $\sum_{k=0}^{p-1} (p-k) = \frac{p(p+1)}{2}$  by [[Arithmetic summation]]
- The model performs much better than [[Best subset selection]] when p=20 with a huge marginal difference
## Challenge
- The choice of the best model via use of RSS or $R^2$ may not be the best
- Guarantee of optimality not certain
    - Similar to [[Greedy algorithm]] once the choice is made in previous steps, the predictor selected will be carried on to the next step
    - X_1 might be optimal for one-variable model, but X_2 and X_3 might be the optimal for a two-variable model. Since X_1 is selected as the first best predictor, the two variable model will contain X_1
## Advantage
- Computationally more feasible than [[Best subset selection]]
- Can be applied to high-dimensional setting with $n<p$
    - Note that only models $M_0,...,M_{n-1}$ have unique solutions
    - Each model is fitted using [[Least squares]] which will not give a unique solution when $p \ge n$. Refer to [[Prediction accuracy]] case 3

---
Links: 