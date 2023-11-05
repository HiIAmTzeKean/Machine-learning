---
tags:
  - 🌱
  - ComputerScience
  - MachineLearning
date: 12--May--2023
---

# K nearest neighbours
Conditional [[Distribution]] is not always known, but can be estimated. Application of [[Bayes classifier]] can be done by classifying an observation to the highest estimated [[Probability]].

## Procedure
1. K integer selected
2. Observation x_0 selected
3. $N_0 \rightarrow$ KNN identifies K points in training data closest to x_0
4. Estimate conditional probability for class j as fraction of points in N_0
5. $P(Y=j|X=x_0)= \frac{1}{K} \sum_{i \in N_0} I(y_i=j)$
6. Applies [[Bayes classifier]] 
## Lower bound on error rate
Similar to [[Bayes classifier]], in the ideal situation, KNN will achieve a minimum error when the conditional probability is known. 
## Upper bound on error rate
The upper bound is obtained by using a [[Constant classifier]] (If KNN cannot beat this, then it is worst off than guessing a constant label).
### When K=n
Then all data points in the training set is taken to be a neighbour, and the most common class will always be predicted. The algorithm becomes a [[Constant classifier]].
### When K=1
We can show that 1-NN is convergent. When $n \rightarrow \infty$, then $dist(x_{NN}, x_0)=0$, so the nearest neighbour equals to $x_0$.
The [[Error rate]] = probability that $x_{NN}$ not equal to x_0 = probability of drawing two different label =  
$$\epsilon_{NN} = P(y*|x)(1-P(y*|x_{NN})) + (1-P(y*|x))P(y*|x_{NN})$$
where $y*$ is the correct label, x is the test data. This equation tries to find the probability that the prediction of the test data is different from NN. Since probabilities are less than 1, and that when  $n \rightarrow \infty$ then the NN=x, the equation can be reduced to 
$$\begin{align}
&\epsilon_{NN} = P(y*|x)(1-P(y*|x_{NN})) + (1-P(y*|x))P(y*|x_{NN})&\\
&\le (1-P(y*|x_{NN})) + (1-P(y*|x))&\\
&\le 2(1-P(y*|x_{NN}))&\\
&\le 2\epsilon_{bayesOPT}&
\end{align}$$
Recall from [[Bayes classifier]] for the substitution. 

---
Links: [[Non-parametric learning]]
Reference: [website](https://www.cs.cornell.edu/courses/cs4780/2018fa/lectures/lecturenote02_kNN.html)