---
tags: 🌱
date: 04--May--2023
---

# Overfitting

When there is a monotone decrease in training [[Mean squared error|MSE]] but a U-shape in test MSE. This is a property of [[Statistical learning]] that is always true regardless of **data set** or **statistical method** used.
## Reasons for increase in test MSE
- Model is picking up patterns caused by random chance rather than the unknown function f
    - The supposed patterns learnt do not exist in test data which causes prediction to be off
## Solution
- [[Cross validation]]
---
Links: 