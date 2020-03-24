# **Preprocessing choices affect RNA velocity results for droplet scRNA-seq data**

> Author: Soneson, et al. 2020
>
> DOI: https://doi.org/10.1101/2020.03.13.990069

Contribution: 

- They compare different quantification tools/approaches in terms of the resulting spliced (mRNA) and unspliced (pre-mRNA) counts and downstream analyses, specifically on RNA velocity.

Method: 

- They use 4 public scRNA-seq datasets of reads (or UMIs?). Each dataset consists of ~1000 to 3000 cells.
- They compare 4 different quantification tools: velocyto, kallisto | bustools, STARsolo, and alevin (Salmon). 
- They compare different definitions of exonic and intronic regions, namely whether to use a "separate" or "collapse" approach. In the "separate" approach, every exonic transcript is considered separately when extracting intronic regions, so the introns can overlap with exons, while in the "collapse" approach, introns are defined as the remaining parts that are not in any of the exonic isoforms of a gene. A flanking sequence of length L - 1 (or some variants) is added to each side of the intron to account for reads mapping across exon/intron boundaries. 
- They compare different reference indices (Table 2):
  1. (alevin_sep/coll_gtr = salmon-joint-eisaR-separate/collapse) Salmon: spliced transcript and intron index, with genome sequence as decoy
  2. (?? = salmon-spliced) Salmon: spliced transcript as index, with genome sequence as decoy
  3. (alevin_spliced_unspliced_gtr = salmon-spliced-unspliced) Salmon: spliced and unspliced transcript index, with genome sequence as decoy
  4. (alevin_sep/coll_decoy_gtr = salmon-spliced-decoy-eisaR-collapse/separate) Salmon: spliced transcript as index, with genome sequence + intron as decoy
  5. (alevin_sep/coll_decoy_gtr = salmon_introns_decoy) Salmon: intron as index, with genome sequence + spliced transcript as decoy
  6. (kallisto | bus_coll/sep_incl/excl = kallisto-joint-eisaR-collapse/separate) kallisto: spliced transcript and intron as index
  7. (velocyto = cellranger) CellRanger: whole genome
  8. (starsolo/_diff = star) STAR: whole genome
- They use *alevin*to generate counts for the Salmon index, *kallisto | bustools* for kallisto, CellRanger or velocyto for CellRanger, and STARsolo for STAR.

Questions/Thoughts:

* How did people know what the exons/transcript isoforms of a gene were?
* What is the "complete genome sequence" used as a decoy sequence?
* What is the whole genome index and how is it different from the spliced transcript index (Table 2)?
* I found the reference index generation/Table 2 to be confusing. Specifically, I was not totally clear what is the difference between unspliced transcript vs intron. Is an unspliced transcript supposed to be exon + intron? If so, how did they define an unspliced transcript? Also, the description preceding Table 2 did not match the order of the table entries, which made it difficult to follow.
* What is the purpose of estimating sequence uniqueness? [A: Figure 1].
* What is the purpose of using alevin (I thought Salmon already gives counts?)?
* It was also confusing trying to match the approaches from Table 2 to Table 3. 
* How did they obtain UMI counts? I was under the impression that the datasets were reads.

