# CMS Provider of Services Files

This repo houses code to import and manage the CMS Provider of Services (POS) files. Data from 1984 through 2019 were downloaded from the National Bureau of Economic Research (NBER) POS data pages, available [here](https://data.nber.org/data/provider-of-services.html). Data after 2019 were downloaded directly from CMS, available [here](https://data.cms.gov/provider-characteristics/hospitals-and-other-facilities/provider-of-services-file-hospital-non-hospital-facilities). Note that I take only the Q4 files from CMS for each year. I downloaded all of the raw data into a separate directory, which are linked to the data folder in this repo (but not tracked). Following NBER naming, the naming convention for all files is "posXXXX.csv", where XXXX denotes the year.

My code file (in `R`) is available [here](data-code/data-combine.R). Please also see Adam Sacarny's repo [here](https://github.com/asacarny/provider-of-services), which provides code to import and clean the POS data in Stata.

Finally, two quick notes on the data:

1. CMS writes: "This data is gathered as part of the CMS Provider Certification process and is updated each time a provider is recertified.  The specific time table for each provider types recertification process does vary." I interpret this to mean that the data may not be fully up to date. 

2. The NBER writes: "The Provider of Services file is a historic file, so only a recent file might be needed." Still, there is perhaps some merit in using individual years of data if we want to attempt to track changes in a hospital's provider number or certification status. As such, I use each individual year of data in this repo.

