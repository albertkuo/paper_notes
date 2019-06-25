# **Detection and localization of surgically resectable cancers with a multi-analyte blood test**

> Author: Cohen et al, 2018
>
> DOI: 10.1126/science.aar3247

Contribution: 

* They created a blood test to detect the presence and type of 8 common cancers.

Methodology: 

* Most of the methodology is in the supplementary materials.
* Classifying cancer was done using mutations and protein markers. Tissue recognition information was primarily found in the protein markers, since driver gene mutations are not usually tissue-specific.
* For a given mutation in a sample, calculate the mutant allele frequency (MAF) = # of supermutants/# of UIDs. Then normalize the MAF according to how common the MAF is in the normal controls. Compare the MAF to reference distribution of MAF in normals vs cancer in training set. Calculate p-values (how likely you observe something > MAF under each distribution?) and take weighted log ratio of p-values (similar to log-likelihood ratio). The log ratio is called the omega-score. The omega-score used in classification seems to be the maximum omega score over all found mutations.
* For mutations with omega-score > 1, check that they were not also identified in WBC (however, WBC was only available in 23% of cancer patients?), i.e. a result of Clonal Hematopoiesis of Indeterminate Potential. Mutation was excluded if the ratio of max MAF in plasma and max MAF in WBC was < 100. 
* Protein normalization was done by truncation. 
* Forward selection with logistic regression was used to select proteins. Then logistic regression was used for cancer classification.
* Random forest was used for cancer type prediction.

Thoughts:

* They showed that the sensitivity of detection plateaus at 60 amplicons in Figure 1. Increasing the number of amplicons further would thus increase the false-positive rate without substantial improvement to the sensitivity. I think I would've liked to see that trade-off in Figure 1.
* Why was a smaller percentage of pancreatic cancers detected than expected in Figure 1?
* I wonder how much loss in performance (if any) resulted from creating a blood test that detects any of 8 different cancers (as opposed to just 1). 
* They eliminated from consideration any proteins that had a higher median value in normal than cancer samples. Is this due to lab constraints (it's hard to measure low counts)? Isn't it possible that a lower protein count is also a signal for cancer? 