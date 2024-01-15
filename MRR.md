---
tags:
  - 🌱
date: 19--Dec--2023
aliases:
  - Mean Reciprocal Rank
modified: 12--Jan--2024
---
# MRR
The MRR (Mean Reciprocal Rank) metric is a system wide metric, so only its result will be returned and not those of every user.
MRR is calculated as such:
$$MRR_{sys} = \frac{1}{|Q|}\cdot\sum_{i=1}^{|Q|}\frac{1}{rank(i)}$$
Where:
- $Q$ is the set of recommendation lists
- $rank(i)$ is the position of the first [[Relevance|relevant]] item in the i-th recommendation list

The MRR metric needs to discern relevant items from the not relevant ones: in order to do that, one could pass a custom `relevant_threshold` parameter that will be applied to every user, so that if a rating of an item is >= relevant_threshold, then it's relevant, otherwise it's not.
If no `relevant_threshold` parameter is passed then, for every user, its mean rating score will be used

---
Links:
