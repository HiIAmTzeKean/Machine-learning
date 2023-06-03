---
tags: 🌱
date: 01--Jun--2023
---

# Stepwise model selection

Stepwise methods tend to more feasible compared to [[Best subset selection]] by restricting the possible [[Search space]].
## Types of stepwise selection
- [[Forward stepwise selection]]
- [[Backward stepwise selection]]
## Hybrid method
### Limitation of forward and backward stepwise selection solution
Solution of next step is a subset of previous step. The true optimal solution for subsequent steps may, however
1. Contain a predictor previously eliminated ([[Backward stepwise selection]])
2. Not contain a predictor previously chosen ([[Forward stepwise selection]])
The way to obtain predictors that give rise to the optimal model at each step is to test all possible combinations which incurs $2^n$ cost.
### Overcoming limitation
Allow the model to remove variables to that no longer provide improvement to model fit. Computational advantage of stepwise preserved, and now closely mimics best subset selection.

---
Links: [[Model selection]]