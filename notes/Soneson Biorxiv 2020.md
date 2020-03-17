# **Preprocessing choices affect RNA velocity results for droplet scRNA-seq data**

> Author: Soneson, et al. 2020
>
> DOI: https://doi.org/10.1101/2020.03.13.990069

Contribution: 

- They compare different quantification tools/approaches in terms of the resulting spliced (mRNA) and unspliced (pre-mRNA) counts and downstream analyses, specifically on RNA velocity.

Method: 

- They use 4 public scRNA-seq datasets of reads. Each dataset consists of ~1000 to 3000 cells.
- To define intron sequences, the BUSpaRse package uses either a "separate" or "collapse" approach. In the "separate" approach, introns can overlap with exons, while in the "collapse" approach, introns are defined as the remaining parts that are not in any of the exonic isoforms of a gene. They reimplement both approaches themselves and since they found errors in BUSpaRse, this is what they end up using.
- They build 8 different reference index (Table 2):
  1. (alevin_sep/coll_gtr = salmon-joint-eisaR-separate/collapse) Salmon: spliced transcript and intron index, with genome sequence as decoy
  2. (?? = salmon-spliced) Salmon: spliced transcript as index, with genome sequence as decoy
  3. (alevin_spliced_unspliced_gtr = salmon-spliced-unspliced) Salmon: spliced and unspliced transcript index, with genome sequence as decoy
  4. (alevin_sep/coll_decoy_gtr = salmon-spliced-decoy-eisaR-collapse/separate) Salmon: spliced transcript as index, with genome sequence + intron as decoy
  5. (?? = salmon_introns_decoy) Salmon: intron as index, with genome sequence + transcript as decoy
  6. (kallisto | bus_coll/sep_incl/excl = kallisto-joint-eisaR-collapse/separate) kallisto: spliced transcript and intron as index
  7. (velocyto = cellranger) CellRanger: whole genome
  8. (starsolo/_diff = star) STAR: whole genome
- They use *alevin*to generate counts for the Salmon index, *kallisto | bustools* for kallisto, CellRanger or velocyto for CellRanger, and STARsolo for STAR.

Questions/Thoughts:

* How did people know what the exons/transcript isoforms of a gene were?
* What is a decoy sequence?
* How is the whole genome index different from the spliced transcript index?
* I found the reference index generation/Table 2 to be confusing. Specifically, I was not totally clear what is the difference between unspliced transcript vs intron. Is an unspliced transcript supposed to be exon + intron? If so, how did they define an unspliced transcript? Also, the description preceding Table 2 did not match the order of the table entries, which made it difficult to follow.
* What is the purpose of estimating sequence uniqueness?
* What is the purpose of using alevin (I thought Salmon already gives counts?)?
* It was also confusing trying to match the approaches from Table 2 to Table 3. Some indexes in Table 2 do not seem to appear in Table 3.

