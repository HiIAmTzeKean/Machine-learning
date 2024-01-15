---
tags:
  - 🌱
date: 19--Dec--2023
modified: 07--Jan--2024
---
# Relevant precision
The R-Precision metric is calculated as such for the **single user**:

$$
R-Precision_u = \frac{tp@R_u}{tp@R_u + fp@R_u}
$$

Where:
- $R$ it's the number of [[Relevance|Relevant]] items for the user *u*
- $tp@R_u$ is the number of items which are in the recommendation list  of the user **cutoff to the first R items** and have a rating >= relevant_threshold in its 'ground truth'
- $tp@R_u$ is the number of items which are in the recommendation list  of the user **cutoff to the first R items** and have a rating < relevant_threshold in its 'ground truth'

And it is calculated as such for the **entire system**, depending if 'macro' average or 'micro' average has been chosen:

$$
Precision@R_{sys} - micro = \frac{\sum_{u \in U} tp@R_u}{\sum_{u \in U} tp@R_u + \sum_{u \in U} fp@R_u}
$$

$$
Precision@R_{sys} - macro = \frac{\sum_{u \in U} R-Precision_u}{|U|}
$$

---
Links: [[Precision]]
