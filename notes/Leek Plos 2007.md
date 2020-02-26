# Capturing Heterogeneity in Gene Expression Studies by Surrogate Variable Analysis

> Author: Leek et al, 2007
>
> DOI: https://doi.org/10.1371/journal.pgen.0030161

Contribution:

* They develop a method, surrogate variable analysis (SVA), to handle batch effects.

Method:

* SVA estimates batch effects from the expression data and constructs surrogate variables for them.
* There are 4 steps to the method:
  1. Decomposition of residual expression matrix into orthogonal vectors, and determine the vectors that represent more variation than would be expected by chance.
  2. Identify subset of genes significantly associated with the significant vectors.
  3. Build a surrogate variable using the expression of that subset of genes
  4. Include surrogate variable in subsequent analysis

Thoughts:

* They provide a link to the [R package](http://www.bioconductor.org/packages/release/bioc/html/sva.html) in the paper. I haven't used the package myself, but it reminds me of why it's so important to provide an R package -- it significantly increases the chance that other people are actually going to use your proposed method.