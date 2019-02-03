## Test environments
* MS Windows Server 2008, 64 bit, R "release", "devel" (winbuilder)
* MS Windows 10 Enterprise, 64 bit, R v3.5.2 (RStudio Desktop)
* Ubuntu 14.05.5 LTS, 64 bit, R 3.5.2 (Travis CI)

## R CMD check results
In all environments, the test results were: 0 errors | 0 warnings | 0 note 

## Downstream dependencies
We have checked downstream dependencies of vortexR using devtools::revdep_check().
Results: No errors or warnings found.

## License
The maintainer of this package, Carlo Pacioni, is an author on both papers 
which generated the data included here. 
Carlo has the written permission of all of his co-authors to make the data 
included here available in this form (as R package) under the chosen license (GPL-3).

## Reason for release as CRAN package
This package serves as an auxiliary data package for our main package vortexR.
Splitting the raw data for vortexR into this package, vortexRdata, keeps 
vortexR's installed package size below the size threshold triggering a NOTE from 
`R CMD check --as-cran`.
