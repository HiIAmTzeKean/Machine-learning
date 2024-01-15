---
tags:
  - 🌱
date: 19--Dec--2023
modified: 01--Jan--2024
---
# Median Absolute difference
The MAE (Mean Absolute Error) metric is calculated as such for the **single user**:

$$
MAE_u = \sum_{i \in T_u} \frac{|r_{u,i} - \hat{r}_{u,i}|}{|T_u|}
$$
Where:
- $T_u$ is the *test set* of the user $u$
- $r_{u, i}$ is the actual score give by user $u$ to item $i$
- $\hat{r}_{u, i}$ is the predicted score give by user $u$ to item $i$

And it is calculated as such for the **entire system**:
$$
MAE_{sys} = \sum_{u \in T} \frac{MAE_u}{|T|}
$$

Where:
- $T$ is the *test set*
- $MAE_u$ is the MAE calculated for user $u$

There may be cases in which some items of the *test set* of the user could not be predicted (eg. A CBRS was chosen and items were not present locally, a methodology different than *TestRatings* was chosen).

In those cases the $MAE_u$ formula becomes
$$
MAE_u = \sum_{i \in T_u} \frac{|r_{u,i} - \hat{r}_{u,i}|}{|T_u| - unk}
$$

Where:
- $unk$ (*unknown*) is the number of items of the *user test set* that could not be predicted

If no items of the user [[Test set]] has been predicted ($|T_u| - unk = 0$), then:

$$
MAE_u = NaN
$$

---
Links:
