# **The Holdout Randomization Test: Principled and Easy Black Box Feature Selection**

> Author: Tansey et al, 2019
>
> DOI: [arXiv:1811.00645v3](https://arxiv.org/abs/1811.00645v3)

Contribution: 

- They propose a method (holdout randomization test) for feature selection for any prediction model.

Method: 

- The holdout randomization test (HRT) produces a p-value for each feature. They obtain it by replacing each feature $X_j$ by a null version $\tilde{X}_j$ that is conditionally independent of $Y$ given the other features, and then recalculate the empirical risk on the held out data. They then compare the empirical risk of the null $\tilde{X}_j$ to the empirical risk with the original data $X_j$ to get a test statistic for that feature.
- There are 3 improvements to the basic idea of HRT: 1) how to calibrate the estimated conditional distribution (which I didn't really understand), 2) how to do HRT in a cross-validated manner, and 3) how to speed up computation by caching scores (which I also didn't really understand). Both (1) and (2) appears to improve HRT a lot in terms of power/FDR.

Thoughts:

- I thought this paper was very interesting. In fact, the reason I read this paper is because the author gave a talk at our department that I liked.
- "Yet in many scientific studies, feature selection is performed heuristically (e.g. using the lasso), without any statistical guarantees or control over the error rate." - :clap: 
- They also address (and critique) other work that's been done in this area already.

