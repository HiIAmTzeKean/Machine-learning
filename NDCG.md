---
tags:
  - 🌱
date: 19--Dec--2023
aliases:
  - Normalised Discounted Cumulative Gain
modified: 07--Jan--2024
---
# Normalised Discounted Cumulative Gain
> [!info] Designed for situation of non-binary notions of [[Relevance]]
## Idea
Evaluated over some top $k$ results like [[Precision#Precision at K]] 
$$NDCG(Q,k)=\frac{1}{|Q|}\sum^{|Q|}_{j=1}{Z_{kj}} \sum^{k}_{m=1}{\frac{2^{R(j,m)}-1}{\log_2(1+m)}}$$
Where
- $R(j,d)$ be relevant score for document $d$ for query $j$
- $Z_{kj}$ is a [[Normalisation]] factor such that perfect ranking at $k$ for query $j$ is 1
- Queries for $k'<k$ documents retrieved, last summation is done till $k'$
## [[RecSys]]
$$DCG_{u}(scores_{u}) = \sum_{r\in scores_{u}}{\frac{f(r)}{log_x(2 + i)}}$$
Where:
- $scores_{u}$ are the ground truth scores for predicted items, ordered according to the order of said items in the
    ranking for the user $u$
- $f$ is a gain function (linear or exponential, in particular)
- $x$ is the base of the logarithm
- $i$ is the index of the truth score $r$ in the list of scores $scores_{u}$

If $f$ is "linear", then the truth score $r$ is returned as is. Otherwise, in the "exponential" case, the following formula is applied to $r$:
$$
f(r) = 2^{r} - 1
$$
### Single user

$$
NDCG_u(scores_{u}) = \frac{DCG_{u}(scores_{u})}{IDCG_{u}(scores_{u})}
$$

Where:
- $IDCG_{u}$ is the DCG of the ideal ranking for the truth scores

So the basic idea is to compare the actual ranking with the ideal one
### Entire system

$$
NDCG_{sys} = \frac{\sum_{u} NDCG_u}{|U|}
$$

Where:
- $NDCG_u$ is the NDCG calculated for user :math:`u`
- $U$ is the set of all users

The system average excludes NaN values.

---
Links: [Online reference](https://arize.com/blog-course/ndcg/#:~:text=Normalized%20Discounted%20Cumulative%20Gain%20(NDCG)%20is%20a%20measure%20of%20ranking,or%20other%20information%20retrieval%20system.)
