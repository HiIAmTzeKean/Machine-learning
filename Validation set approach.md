---
tags:
  - 🌱
  - ComputerScience
  - MachineLearning
date: 22--May--2023
---

# Validation set approach

Randomly dividing the observation set into 2 parts. The [[Train data]] and [[Validation set]].
## Usage
Verifying that the goodness of a fit of a model can be done through [[p-value]] or through a validation method.
## Idea
Observations are randomly split into 2 sets of equal size ([[Randomness]]). the model is fitted on the training set and evaluated on the [[validation set]]. [[Mean squared error|MSE]] is computed as a measure of goodness of fit.
### Advantage
- Easy to implement as the splitting is arbitrary
### Disadvantage
- Validation estimate of [[Test error rate]] highly variable depending on which observations are in the training set and those in the validation set
- Only a subset of observations are used to fit the model. Smaller sample size tends to cause models to perform worse, and thus the validation set error rate may tend to [[Overestimate test error rate]].

---
Links: 