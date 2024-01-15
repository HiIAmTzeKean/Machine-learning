---
tags:
  - 🌱
date: 18--Dec--2023
modified: 25--Dec--2023
---
# Cosine similarity
Makes use of [[Vector]] point in space and to calculate the angle between the vectors.
$$\frac{\sum^{n}_{i=1}A_iB_{i}}{\sqrt{\sum^{n}_{i=1}{A_{i}^{2}}}\sqrt{\sum^{n}_{i=1}{B_{i}^{2}}}}$$
Note that [[Cosine similarity]] is defined from dot product where
$$
\begin{align}
\overrightarrow q \cdot \overrightarrow d &= |\overrightarrow q| \cdot |\overrightarrow d| \cos(\overrightarrow q,\overrightarrow d)\\
\cos(\overrightarrow q,\overrightarrow d) &= \frac{\overrightarrow q \cdot \overrightarrow d}{|\overrightarrow q| \cdot |\overrightarrow d|}
\end{align}$$
Thus, by definition cosine similarity use the unit vector to compute the angle between vectors.
## Properties
- Is 0 when both [[Vector]] are [[Orthogonal]] to each other
- Is 1 when both [[Vector]] lie on the same line

---
Links:
