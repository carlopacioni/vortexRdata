## Test environments
`devtools::check()` and `R CMD check --as-cran` were run on:

* GNU/Linux Ubuntu 16.04.2 LTS, 64 bit, R 3.3.3 (RStudio Desktop)
* GNU/Linux Ubuntu 14.04.5 LTS, 64 bit, R 3.3.2 (RStudio Server)
* MS Windows Server 2008, 64 bit, R "release", "devel", "oldrelease" (winbuilder)
* MS Windows 7 Professional SP1, 64 bit, R v3.3.3 (RStudio Desktop)
* MS Windows 10 Home, 64 bit, R v3.3.2 (RStudio Desktop)

## R CMD check results
In all environments, the results of R CMD check --as-cran were:

0 errors | 0 warnings | 1 note (+1 on winbuilder)

* checking CRAN incoming feasibility ... NOTE
  Maintainer: 'Carlo Pacioni <C.Pacioni@Murdoch.edu.au>'
  New submission
  
    We confirm that this package is a new submission.

* checking package dependencies ... NOTE
  No repository set, so cyclic dependency check skipped
  
    This NOTE only occurred on winbuilder. This package has no dependencies, 
    as it contains only data (.rda and raw text files).
    
    This test passes with OK on GNU/Linux and local Windows test environments.

This package serves as an auxiliary data package for our main package vortexR 
to keep vortexR's installed package size to a minimum.

## Downstream dependencies
We have checked downstream dependencies of vortexR using devtools::revdep_check().
Results: No errors or warnings found.

## License
The maintainer of this package, Carlo Pacioni, is an author on both papers 
which generated the data included here. 
Carlo has the written permission of all of his co-authors to make the data 
included here available in this form (as R package) under the chosen license (GPL-3).
