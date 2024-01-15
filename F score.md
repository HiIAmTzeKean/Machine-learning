---
tags:
  - 🌱
date: 18--Dec--2023
modified: 05--Jan--2024
---
# F score
Calculated from [[Precision]] and [[Recall]]. It is the weighted [[Harmonic mean]] of both the metric.
$$F_\beta = \frac{1}{\alpha \frac{1}{P} + (1-\alpha) \frac{1}{R}}=\frac{(\beta^{2}+1)PR}{\beta^{2}P+R}$$
## Properties
- $\max(F)=1$. Perfect precision and recall.
- $\min(F)=0$. When either precision or recall is 0.
- $\alpha \in [0,1]$ and $\beta \in [0,\infty]$
- [[Set-based measure]]
## [[Harmonic mean]] instead of [[Arithmetic mean]]
Note from [[Recall#Properties]] that perfect recall can always be obtained by retrieving all documents. By the same process, a 50% [[Arithmetic mean]] can always be obtained.
The [[Harmonic mean]] is always less than or equal to [[Arithmetic mean]] and [[Geometric mean]], where by its always closer to the minimum of either mean.
## Types of F Score
### Balanced F measure (F1)
When $\alpha=\frac{1}{2}$ or $\beta=1$, we write the F measure as $F_1$
### $\beta>1$
The emphasis is on [[Recall]]
### $\beta<1$
The emphasis is on [[Precision]]

---
Links: [[Precision vs Recall]]
