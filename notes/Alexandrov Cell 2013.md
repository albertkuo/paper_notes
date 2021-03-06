# Deciphering Signatures of Mutational Processes Operative in Human Cancer

> Author: Alexandrov et al, 2013
>
> DOI: [10.1016/j.celrep.2012.12.008](https://dx.doi.org/10.1016%2Fj.celrep.2012.12.008)

I started off reading [Signatures of mutational processes in human cancer](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3776390/), was trying to figure out their methodology, then realized I should probably be reading this paper instead. In "Signatures," they characterized 21 genome-wide mutational signatures through association with age, known mutational processes, and mutagenic characteristics (e.g. if it's on a transcribed strand, insertions/deletions, etc.).

Contribution:

* They develop an approach to identify mutational processes/signatures.

Method:

* They use nonnegative matrix factorization (NMF) to identify signatures from the resulting mixture of mutations.
* They chose the number of mutational processes N based on the lowest reconstruction error on bootstrapped data and signature reproducibility.

Thoughts:

* I am not familiar with methods for "blind source separation" problems (e.g. NMF), so this was interesting to read. Intuitively, NMF feels similar to PCA.