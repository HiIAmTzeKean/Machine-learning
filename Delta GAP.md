---
tags:
  - 🌱
date: 19--Dec--2023
modified: 19--Dec--2023
---
# Delta GAP
The Delta GAP (Group Average popularity) metric lets you compare the average popularity "requested" by one or multiple groups of users and the average popularity "obtained" with the recommendation given by the recsys. It's a system wise metric and results of every group will be returned.

It is calculated as such:

$$
\Delta GAP = \frac{recs_GAP - profile_GAP}{profile_GAP}
$$

Users are split into groups based on the *user_groups* parameter, which contains names of the groups as keys, and percentage of how many user must contain a group as values. For example:
`user_groups = {'popular_users': 0.3, 'medium_popular_users': 0.2, 'low_popular_users': 0.5}`

Every user will be inserted in a group based on how many popular items the user has rated (in relation to the percentage of users we specified as value in the dictionary):
* users with many popular items will be inserted into the first group
* users with niche items rated will be inserted into one of the last groups.

In general users are grouped by $Popularity\_ratio$ in a descending order. $Popularity\_ratio$ for a single user $u$ is defined as:
$$
Popularity\_ratio_u = n\_most\_popular\_items\_rated_u / n\_items\_rated_u
$$

The *most popular items* are the first `pop_percentage`% items of all items ordered in a descending order by popularity.

The popularity of an item is defined as the number of times it is rated in the `original_ratings` parameter divided by the total number of users in the `original_ratings`.

It can happen that for a particular user of a group no recommendation are available: in that case it will be skipped and it won't be considered in the $\Delta GAP$ computation of its group. In case no user of a group has recs available, a warning will be printed and the whole group won't be considered.

---
Links:
