---
tags:
  - 🌱
date: 19--Dec--2023
modified: 19--Dec--2023
---
# Catalog coverage
The Catalog Coverage metric measures in percentage how many distinct items are being recommended in relation to all available items. It's a system wide metric, so only its result it will be returned and not those of every user. It differs from the [[Prediction coverage]] since it allows for different parameters to come into play. If no parameter is passed then it's a simple Prediction Coverage.
The metric is calculated as such:

$$
Catalog Coverage_{sys} = (\frac{|\bigcup_{j=1...N}reclist(u_j)|}{|I|})\cdot100
$$

Where:
- $N$ is the total number of users
- $reclist(u_j)$ is the set of items contained in the recommendation list of user $j$
- $I$ is the set of all available items

The recommendation list of every user ($reclist(u_j)$) can be reduced to the first *n* parameter with the top-n parameter, so that catalog coverage is measured considering only the most highest ranked items.

With the 'k' parameter one could specify the number of users that will be used to calculate catalog coverage: k users will be randomly sampled and their recommendation lists will be used. The formula above becomes:

$$
Catalog Coverage_{sys} = (\frac{|\bigcup_{j=1...k}reclist(u_j)|}{|I|})\cdot100
$$

Where:
- $k$ is the parameter specified

Obviously $k< N$, else simply recommendation lists of all users will be used

Check the 'Beyond Accuracy: Evaluating Recommender Systems  by Coverage and Serendipity' paper and page 13 of the 'Comparison of group recommendation algorithms' paper for more

---
Links:
