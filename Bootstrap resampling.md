---
tags:
  - 🌱
  - ComputerScience
  - MachineLearning
date: 24--May--2023
---

# Bootstrap resampling

## Example
Investing money into 2 assets X and Y which are random quantities. A fraction \alpha invested in X and the remaining 1–\alpha into Y. To minimise the total risk ([[Variance]]), $\min(Var(\alpha X + (1-\alpha)Y))$ is computed. (Refer to [[Minimising risk]] on why variance is chosen as the measure)

Apply [[Variance sum law]]
$$\begin{align*}
&\frac{d}{d\alpha}[\alpha^2 \cdot \sigma_X^2 + (1-\alpha)^2 \cdot \sigma_Y^2 + 2\alpha (1-\alpha) Cov(X,Y)] = 0\\
&2\alpha \cdot \sigma_X^2 - 2(1-\alpha)\sigma_Y^2 + 2(1-\alpha) Cov(X,Y) - 2\alpha Cov(X,Y)= 0\\
&\alpha= \frac{\sigma_Y^2 - \sigma_{XY}} {\sigma_X^2 +\sigma_Y^2-2\sigma_{XY}}
\end{align*}$$
to obtain the estimate of $\bar \alpha$, multiple estimates of $\alpha$ must be computed and is denoted as $\hat \alpha$.
$$\bar \alpha = 1/n \sum_{i=1}^n \hat \alpha$$
The [[Standard deviation]] can also be computed. However, to obtain a good estimate, a large number of samples is needed which is not always available.

## Power of bootstrap
Bootstrap repeatedly samples observation from the original data set without generating additional samples.
### Procedure
1. Randomly select m observations from the data set to create a bootstrap data set $Z^{*1}$
2. [[Sampling]] is done with replacement
    1. Same observations can appear twice
3. Multiple bootstrap data set $Z^{*1},...Z^{*B}$ can be created
### Outcome
This [[Resampling method]] is useful when there is limited observations and there is a need to train the model multiple times.

---
Links: [[Bootstrap]]