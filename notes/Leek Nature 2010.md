# Tackling the widespread and critical impact of batch effects in high-throughput data

> Author: Leek et al, 2010
>
> DOI: https://doi.org/10.1038/nrg2825

Contribution:

* They summarize what batch effects are and how to handle them.

Notes:

* "Batch effects are sub-groups of measurements that have qualitatively different behavior across conditions and are unrelated to the biological or scientific variables in a study."
* Processing groups (same protocol) and dates are often the only surrogates available for other sources of variation
* Batch effects may be confounded with the outcome of interest (bias); even if they are not, they will increase variability and decrease power
* To handle batch effect, first identify and quantify batch effects with PCA or hierarchical clustering
* Then if it looks like all batch effects are captured by measured variables, these variables (e.g. time) can be incorporated with in the model (e.g. ComBat)
* If it looks like not all batch effects can be explained by time, then use a method like SVA

Thoughts:

* I actually already read this paper 2 years ago, but I think I have more appreciation for its usefulness now.