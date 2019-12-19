# **Feature Selection and Dimension Reduction for Single Cell RNA-Seq based on a Multinomial Model**

> Author: Townes et al, 2019
>
> DOI: http://dx.doi.org/10.1101/574574

Contribution: 

- Current normalization techniques induce variability and distort data. They propose a multinomial model for UMI (unique molecular identifiers) data.

Methodology: 

- Replace normal null model with multinomial null model
- GLM-PCA (generalized principal component analysis), and a fast approximation for GLM-PCA using deviance residuals
- Feature selection by deviance using raw UMI counts

Thoughts:

- The generalized-PCA was pretty interesting, since I didn't know of its existence before. 
- The background section was very helpful for me to read, as someone new to the field. It discusses the typical steps in scRNA-Seq data analysis, what's problematic about the methods currently used, and why these problems exist based on how the history of how these methods were developed.