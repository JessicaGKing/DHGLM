
# Fitting a multi-way DHGLM 

Jessica G. King (1,2), Joel L. Pick (1), Jarrod D. Hadfield (1)

1. Institute of Ecology and Evolution, University of Edinburgh, Edinburgh, UK
2. Present address: CE3C & CHANGE, University of Lisbon, Lisbon, Portugal

## Description

In this project, we provide code for the model implemented in King, Pick & Hadfield (2025) *Quantifying the correlation between variance components: an extension to the double-hierarchical generalised linear model*, Methods in Ecology and Evolution.

In this model, hereon referred to as "multi-way DHGLM", the correlation between variance components can be estimated directly from data, as opposed to methods that estimate correlations between estimates of variance components.

The multi-way DHGLM can be envisaged as a series of standard linear mixed models applied to subsets (groups) of the data. For each group, a single set of random effects (subgroup effects) are fitted, leading to a subgroup variance and a residual variance. The linear mixed models are linked in two ways: group means (the intercepts of the standard linear mixed models) are treated as random over groups, and the pair of variances for each group (residual and subgroup) are assumed to be drawn from a bivariate log-normal distribution over groups, the parameters of which are estimated. We also provide a function for simulating data under this model assuming a balanced design, and then fit the model to data generated using this function. 


## Contents

*DHGLM.Rmd* - Here, we provide a complete workflow for implenting a multi-way DHGLM to data. This workbook includes code to:
1. implement a multi-way DHGLM (Stan code),
2. simulate data (R code),
3. fit data to multi-way DHGLM (R code).

The multi-way DHGlM can be modified where appropriate, given the question and data at hand. For instance, additional fixed and random  effects can be included and variance components can be added to the covariance structure.

*sim_power.Rdata* - Simulated data for the power analysis implemented in DHLGM.Rmd




