---
tags: 🌱
date: 16--May--2023
---

# Additive assumption linear regression
## Assumption
Changes in [[Predictor]] X on [[Response]] Y is independent of the values of the other predictors.
## Unrealistic assumption
Different [[Predictor]] can interact with each other, and produce different effects known as a [[Synergy effect]] or [[Interaction effect]]
## Removing additive assumption
Introduction of a variable called an [[Interaction term]]. Given the original [[Linear regression]] equation, which only factors the [[Main effect]]
$$Y = \beta_0 + \beta_1X_1 + \beta_2X_2 +\epsilon$$
the inclusion of an interaction term will result in a model
$$Y = \beta_0 + \beta_1X_1 + \beta_2X_2 + \beta_3X_1X_2+\epsilon$$
Where the change in X_1 or X_2 will affect how the the predictor will affect the response. Thus, relaxing the assumption of how the predictors interact with each other.
### Importance of interaction term
Based on the [[Hierarchical principle]], if the interaction term has a small p-value (and hence included in the model), then the main effects (the [[Predictor]]) must be included regardless of their p-values.

---
Links: