
Estimating the effect of the 2005 change in BCG policy in England: A retrospective cohort study
===============================================================================================

**Background**

In 2005, England changed from universal Bacillus Calmette–Guérin (BCG) vaccination of school-age children to targeted BCG vaccination of high-risk children at birth.

**Methods**

We combined notification data from the Enhanced Tuberculosis Surveillance system, with demographic data from the Labour Force Survey to construct retrospective cohorts of individuals in England relevant to both the universal, and targeted vaccination programmes between Jan 1, 2000 and Dec 31, 2010. For each cohort, we estimated incidence rates over a 5 year follow-up period and used Poisson and Negative Binomial regression models in order to estimate the impact of the change in policy on TB burden.

**Results:**

In the non-UK born, we found evidence for an association between a reduction in incidence rates and the change in BCG policy (school-age IRR: 0.74 (95%CI 0.61, 0.88), neonatal IRR: 0.62 (95%CI 0.44, 0.88)). We found some evidence that the change in BCG policy was associated with a increase in incidence rates in the UK born school-age population (IRR: 1.08 (95%CI 0.97, 1.19)) and weaker evidence of an association with a reduction in incidence rates in UK born neonates (IRR: 0.96 (95%CI 0.82, 1.14)). We found that the change in BCG policy was associated with preventing 385 (95% CI -105, 881) cases in the study population.

**Conclusions**

The change in BCG policy was associated with reduced incidence of TB in the study population. This was largely driven by reductions in the non-UK born. There was a slight increase in those at school-age, who were UK born.

Docker
======

This analysis was developed in a docker container based on the tidyverse docker image. To run the docker image run:

``` bash
docker run -d -p 8787:8787 --name DirectEffBCGPolicyChange -e USER=DirectEffBCGPolicyChange -e PASSWORD=DirectEffBCGPolicyChange seabbs/directeffbcgpolicychange
```

The rstudio client can be found on port :8787 at your local machines ip. The default username:password is DirectEffBCGPolicyChange:DirectEffBCGPolicyChange, set the user with -e USER=username, and the password with - e PASSWORD=newpasswordhere. The default is to save the analysis files into the user directory.

If you have access to the required underlying raw data then the entire analysis can be reproduced from scratch by adding the following to the `docker run` command, with the data saved into `data/tb_data`. The data requirements, and structure, can be found [here](https://www.samabbott.co.uk/tbinenglanddataclean/).

``` bash
--mount type=bind,source=$(pwd)/data/tb_data,target=/home/DirectEffBCGPolicyChange/data/tb_data
```
