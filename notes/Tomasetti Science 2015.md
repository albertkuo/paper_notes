# Variation in cancer risk among tissues can be explained by the number of stem cell divisions

> Author: Tomasetti et al, 2015
>
> Link: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3588146/

Contribution: 

* They argue that a major part of the variation in cancer risk between tissue types is due to DNA replication. As expected, there is a strong correlation between the number of stem cell divisions and lifetime cancer risk by tissue type.

Methodology: 

* In Figure 1, since $R=0.80​$, then $R^2 = 0.65​$ and 65% of the variation in cancer risk between tissues can be explained by differences in stem cell divisions. This is a basic statistical fact, but in this context, I see how it can easily be misinterpreted: saying "explained by" sounds causal, but it is not. 
* For Figure 2, they used K-means clustering on "extra risk scores" (ERS), which is probably the most popular clustering method and something I'm almost sure I've used before. They also verified their results with [hierarchical clustering](https://en.wikipedia.org/wiki/Hierarchical_clustering), which I'm not familiar with, but is also some unsupervised clustering algorithm.

Thoughts:

* If carcinogenesis is driven by mutations in stem cells, then it seems obvious that the normal process of DNA replication can cause cancer. The higher the number of stem cell divisions, the more mutations a cell will acquire, and the higher the probability that it develops cancer. They provide evidence that is consistent with this theory. I'm surprised it hasn't been stated before. 
* I can't tell if the ERS is defined as lifetime risk x number of stem cell divisions or lifetime risk / number of stem cell divisions. 
* Not sure if I agree with the interpretation or methodology of clustering in Figure 2. They say R-tumors are mainly due to stochastic effects and D-tumors are mainly due to environmental/hereditary deterministic factors. I think it would've been better to do a ranking of tissues rather than clustering because the ERS is a relative measure. Let $X$ be how much a tissue type's cancer risk is caused by deterministic factors. Suppose $X$ is right-skewed and continuous. How do you group $X$ into two clusters of D-tumors and R-tumors? The cut-off is going to be arbitrary and not really meaningful imo. They actually acknowledge this "continuum" in the supplement, but didn't explain why they decided to cluster anyway... maybe it's for easier interpretation? 