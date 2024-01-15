---
tags:
  - 🌱
date: 18--Dec--2023
modified: 06--Jan--2024
aliases:
  - MAP
  - Mean average precision at K
---
# Mean average precision
>[!question] Evaluates how [[Relevance|relevant]] the list of recommended items are.

Single-figure of measure of quality across [[Recall]] levels with good discrimination and stability.
$$MAP(Q) = \frac{1}{|Q|}\sum_{j=1}^{|Q|}{\frac{1}{m_{j}}\sum_{k=1}^{m_{j}}{Precision(R_{jk})}}=\frac{1}{|Q|}\sum_{j=1}^{|Q|}{AP_{j}}$$
where [[Precision#System Macro|AP]] is the average of the sum of precision at each level ($\frac{\sum{P_1,P_2...}}{K}$)
## Properties
- Single information need, AP approximate area under uninterpolated [[Precision-recall curve]] (before [[Interpolated precision]] is applied)
- MAP is roughly average area under the [[Precision-recall curve]] for a set of queries
## [[RecSys]]
### Formula
The $MAP$ metric (*Mean average Precision*) is a ranking metric computed by first calculating the $AP$ (*Average Precision*) for each user and then taking its mean.

The $AP$ is calculated as such for the single user:

$$
AP_u = \frac{1}{m_u}\sum_{i=1}^{N_u}P(i)\cdot rel(i)
$$

Where:
- $m_u$ is the number of relevant items for the user $u$
- $N_u$ is the number of recommended items for the user $u$
- $P(i)$ is the precision computed at cutoff $i$
- $rel(i)$ is an indicator variable that says whether the i-th item is relevant ($rel(i)=1$) or not ($rel(i)=0$)

After computing the $AP$ for each user, we can compute the $MAP$ for the whole system:

$$
MAP_{sys} = \frac{1}{|U|}\sum_{u}AP_u
$$

---
Links:
