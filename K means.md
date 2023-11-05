---
tags:
  - 🌱
  - ComputerScience
  - MachineLearning
date: 22--Oct--2023
---
# K means

Select number of clusters first
Randomly select data points as centroid
Compute the distance for every point to the centroid
Compute the mean for each cluster
Compute the [[Variance]] of each cluster with respect to its [[Mean]]

## Optimal cluster choice
As the number of clusters increase, the variance within each cluster will decrease. When K=N, the variance becomes 0.

Elbow plot can be used to assess the optimal K value, where the decrease in variance per increase in cluster decreases substantially.

---
Links: [[Cluster analysis]] [[Hierarchical clustering]] [[Euclidean distance]]
