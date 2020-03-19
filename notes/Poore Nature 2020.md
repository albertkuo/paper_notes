# ****Microbiome analyses of blood and tissues suggest cancer diagnostic approach****

> Author: Poore, et al. 2020
>
> DOI: https://doi.org/10.1038/s41586-020-2095-1

Contribution: 

- They found microbial signatures in tissue and blood that can discriminate cancer status.

Method: 

- They use TCGA sequencing data and used those classified to be non-human (bacteria, archaea, or viruses). This was 2.5% of total reads.
- They trained a stochastic gradient descent boosting algorithm to discriminate between one cancer type versus others, and normal versus tumor.
- They validate that the microbial signatures generated for each tissue seemed to make sense.
- They also use WGS data from TCGA blood samples and applied "our ML strategies."

Thoughts:

- Contamination seems to be a big focus and concern of the paper. I guess the belief is that a lot of the measured microbial DNA could be external, rather than from the sample itself.
- It sounds like there were 2 sets of predictions made: one using sequencing reads of the tumor (Fig. 1) and one using microbial DNA in the blood (Fig. 3). But I couldn't easily tell how these 2 approaches were supposed to compare or possibly integrate.

