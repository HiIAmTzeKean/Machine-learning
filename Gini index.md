---
tags:
  - 🌱
  - ComputerScience
  - MachineLearning
date: 04--Jul--2023
modified: 19--Dec--2023
---

# Gini index

Measures the inequality in a node or also known as impurity. The higher the gini coefficient the more pure it is.
$$G = \sum_{k=1}^K \hat p_{mk} (1-\hat p_{mk})$$
In this case, we can see that the value of G is bounded by $[0,0.5]$. Related to [[Tree]] and [[Decision tree]]

Here m represents the region and k represents those belonging to the kth class.
## [[RecSys]]
The Gini Index metric measures inequality in recommendation lists. It's a system wide metric, so only its result it will be returned and not those of every user.
The metric is calculated as such:
$$
Gini_{sys} = \frac{\sum_i(2i - n - 1)x_i}{n\cdot\sum_i x_i}
$$

Where:
- $n$ is the total number of distinct items that are being recommended
- $x_i$ is the number of times that the item $i$ has been recommended

A perfectly equal recommender system should recommend every item the same number of times, in which case the Gini index would be equal to 0. The more the recsys is "dis-equal", the more the Gini Index is closer to 1

If the 'top_n' parameter is specified, then the Gini index will measure inequality considering only the first *n* items of every recommendation list of all users

---
Links: 