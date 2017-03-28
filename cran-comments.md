## Test environments
`devtools::check(check_version = TRUE, force_suggests = TRUE)` and 
`R CMD check --as-cran` were run on:

* GNU/Linux Ubuntu 16.04.2 LTS, 64 bit, R 3.3.3 (RStudio Desktop)
* GNU/Linux Ubuntu 14.04.5 LTS, 64 bit, R 3.3.2 (RStudio Server)
* MS Windows Server 2008, 64 bit, R "release", "devel", "oldrelease" (winbuilder)
* MS Windows 7 Professional SP1, 64 bit, R v3.3.3 (RStudio Desktop)
* MS Windows 10 Home, 64 bit, R v3.3.2 (RStudio Desktop)

## R CMD check results
In all environments, the test results were: 0 errors | 0 warnings | 1 note 

* checking CRAN incoming feasibility ... NOTE
    ```
    Maintainer: Carlo Pacioni <C.Pacioni@Murdoch.edu.au>
  
    Days since last update: 3
    ```
    
    We fixed an error in the code docs, so that they now work and are aligned
    with the README. We apologize for the additional submission and do not expect
    to require any more updates to this package.
  
  
Only on winbuilder, R version 3.2.5 "oldrelease":

* checking package dependencies ... NOTE
    ```
    No repository set, so cyclic dependency check skipped
    ```

    This NOTE does not appear on local GNU/Linux and local Windows test environments, 
    where we have control over the `.Rprofile`, or on the two other winbuilder
    test environments.
    
    Based on [this answer](https://stat.ethz.ch/pipermail/r-package-devel/2015q3/000293.html)
    by winbuilder's maintainer and [answers](http://stackoverflow.com/q/23164929/2813717) 
    on Stackoverflow we suggest the NOTE could be due a missing setting 
    `options(repos = c(CRAN="http://cran.r-project.org"))` on winbuilder 
    "oldrelease" rather than a problem with this package.    
    
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
