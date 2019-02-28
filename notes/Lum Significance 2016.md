# To predict and serve?

> Author: Lum et al, 2015
>
> DOI: <https://doi.org/10.1111/j.1740-9713.2016.00960.x>

Contribution: 

- This article is not technically part of the scientific literature, but it offers some examples and modeling to intuitively demonstrate how predictive algorithms based on biased datasets (in this case, police cases) can be very problematic.

Methodology: 

- They generate a synthetic population from the National Survey on Drug Use and Health to map drug use at a local level and compared that to the drug arrests made by the Oakland police department (Figure 1). Very interesting and illustrative.
- They also demonstrate a feedback loop via simulation — where increased policing in a specified area naturally leads to a higher number of crime cases, which then leads to more recommendations to increase policing in that area (Figure 3).

Thoughts:

- The introduction is strongly reminiscent of Minority Report and I'm naively surprised "predictive policing" (profiling someone for a crime before they commit one) actually happened (happens?) in police departments.
- They mention that "PredPol," a vendor of a predictive policing system, self-describes its algorithm as a parsimonious "race-neutral" system. If true, this sort of marketing is obviously hugely misleading and problematic. 
- Overall, this is an illuminating example of what can go wrong if you don't think carefully about the data. In this case, it's maybe not so hard for a statistician to realize that racial profiling is likely being reinforced by the prediction models. But more abstractly, something like this can happen whenever the outcome of interest is predicated on some hidden choices/interventions.