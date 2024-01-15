---
tags:
  - 🌱
  - ComputerScience
  - MachineLearning
alias: MSE
date: 02--May--2023
modified: 19--Dec--2023
---

# Mean squared error

Use of training MSE and test MSE may seem to be closely related, but there is no guarantee that the function with lowest training MSE will have the lowest test MSE.
$$MSE = \frac{1}{n}\sum_{i=1}^n(y_i - \hat{f}(x_i))^2$$
## Relation to test [[Prediction]]
Having a small MSE on the training data is not of key interest, rather the test is if $\hat{f}(x_0)$ is approximately $y_0$.
## [[RecSys]]
The MSE (Mean Squared Error) metric is calculated as such for the **single user**:
$$
MSE_u = \sum_{i \in T_u} \frac{(r_{u,i} - \hat{r}_{u,i})^2}{|T_u|}
$$

Where:
- $T_u$ is the *test set* of the user $u$
- $r_{u, i}$ is the actual score give by user $u$ to item $i$
- $\hat{r}_{u, i}$ is the predicted score give by user $u$ to item $i$

And it is calculated as such for the **entire system**:
$$
MSE_{sys} = \sum_{u \in T} \frac{MSE_u}{|T|}
$$
Where:
- $T$ is the *test set*
- $MSE_u$ is the MSE calculated for user $u$

There may be cases in which some items of the *[[Test set]]* of the user could not be predicted (eg. A [[CBRS]] was chosen and items were not present locally)

In those cases the $MSE_u$ formula becomes
$$
MSE_u = \sum_{i \in T_u} \frac{(r_{u,i} - \hat{r}_{u,i})^2}{|T_u| - unk}
$$

Where:
- $unk$ (*unknown*) is the number of items of the *user test set* that could not be predicted

If no items of the user test set has been predicted ($|T_u| - unk = 0$), then:
$$
MSE_u = NaN
$$

---
Links: 