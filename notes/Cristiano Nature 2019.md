# **Detection and localization of surgically resectable cancers with a multi-analyte blood test**

> Author: Cristiano et al, 2018
>
> DOI: https://doi.org/10.1038/s41586-019-1272-6

Contribution: 

- They use differences in fragmentation profiles of cell-free DNA to detect patients with cancer.

Methodology: 

- They use whole genome sequencing of cfDNA at 1-2x coverage for about 200 cancer and 200 healthy individuals.
- They adjust for [biases due to GC content](http://statistics.berkeley.edu/tech-reports/804) using a locally weighted smoother (loess).
- They use gradient tree boosting to predict cancer — the features included fragment size and coverage characteristics, chromosomal arm copy number changes, and mitochondrial copy number changes. Importantly, fragment coverage characteristics alone performed as well using all features (AUC = 0.94), suggesting that they are the major contributor to the classifier.

Thoughts:

- I had trouble understanding what the fragmentation features (fragment size and coverage) were exactly, likely due to my nascent knowledge of the field. Fragment size seems to refer to the ratio of small cfDNA fragments to larger cfDNA fragments within 504 windows of 5 Mb. Fragment coverage, I assume, means either the proportion or count of a window that was read in a cfDNA fragment.