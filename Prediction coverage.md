---
tags:
  - 🌱
date: 19--Dec--2023
modified: 19--Dec--2023
---
# Prediction coverage
The Prediction Coverage metric measures in percentage how many distinct items are being recommended in relation to all available items. It's a system wise metric, so only its result it will be returned and not those of every user.
The metric is calculated as such:
$$
Prediction Coverage_{sys} = (\frac{|I_p|}{|I|})\cdot100
$$

Where:
- $I$ is the set of all available items
- $I_p$ is the set of recommended items

Check the 'Beyond Accuracy: Evaluating Recommender Systems by Coverage and Serendipity' paper for more

---
Links: [[Coverage]]
