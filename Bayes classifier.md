---
tags:
  - ComputerScience
  - MachineLearning
date: 12--May--2023
modified: 29--Oct--2023
---

# Bayes Classifier
[[Test error rate]] minimised on average by assigning each observation the most likely class given the predictor value.
$$P(Y=j|X=x_0)$$
The use of conditional probability to determine the class response belongs to. 

[[Bayes decision boundary]] is learnt from the train data. This will always produces the lowest test error rate called the [[Bayes error rate]]. The overall Bayes error rate is 
$$1-E(\underset{j}{max} P(Y=j|X))$$
Bayes classifier is the gold standard for predicting [[Qualitative]] responses, but conditional [[Distribution]] of Y given X is not always known, and thus computing [[Bayes classifier]] is not possible.
## Proof
By choosing the class with the highest probability that satisfies $\arg \max_y P(y|x_0)$, the error rate for $X=x_0 \equiv 1-max_j(P(Y=j|X=x_0))$. Note that that $max_j(P(Y=j|X=x_0))$ is the probability of correctly classifying the response. Thus, the probability of wrongly classifying a response is $1-P(correct)$.
This occurs when the sample does not have the most likely label.
## Min error rate
It is possible that the error rate is greater than zero. This is because classes can overlap in the true population, and $max_jP(Y=j|X=x_0)<1$ for some values of x_0
## Application
While it cannot be used in practise (due to limited information), it provides information of the lower bound of the [[Error rate]].

---
Links: 