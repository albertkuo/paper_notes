# **The Holdout Randomization Test: Principled and Easy Black Box Feature Selection**

> Author: Tansey et al, 2019
>
> DOI: [arXiv:1811.00645v3](https://arxiv.org/abs/1811.00645v3)

Contribution: 

- They propose a method (holdout randomization test) for feature selection for any black box prediction model.

Method: 

- The holdout randomization test (HRT) produces a p-value for each feature. They obtain it by replacing each feature $X_j$ by a null version $\tilde{X}_j$ that is conditionally independent of $Y$ given the other features, and doing this over and over again. 

Thoughts:

- I thought this paper was very interesting. In fact, the reason I read this paper is because the author gave a talk that I liked at our department.
- "Yet in many scientific studies, feature selection is performed heuristically (e.g. using the lasso), without any statistical guarantees or control over the error rate." - :clap: This is relevant to a lot of things I'm doing now.
- They also address (and critique) a lot of the other work that's been done in this area already, which I didn't read too closely,  but I think will be useful for me to revisit.

