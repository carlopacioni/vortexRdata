## Test environments
`devtools::check(check_version = TRUE, force_suggests = TRUE)` and 
`R CMD check --as-cran` were run on:

* GNU/Linux Ubuntu 16.04.2 LTS, 64 bit, R 3.3.3 (RStudio Desktop)
* GNU/Linux Ubuntu 14.04.5 LTS, 64 bit, R 3.3.2 (RStudio Server)
* MS Windows Server 2008, 64 bit, R "release", "devel", "oldrelease" (winbuilder)
* MS Windows 7 Professional SP1, 64 bit, R v3.3.3 (RStudio Desktop)
* MS Windows 10 Home, 64 bit, R v3.3.2 (RStudio Desktop)

## R CMD check results
In all environments, the test results were:

0 errors | 0 warnings | 1 note (+1 on winbuilder "oldrelease")

* NOTE
    ```
    Maintainer: ‘Carlo Pacioni <C.Pacioni@Murdoch.edu.au>’

    New submission

    Possibly mis-spelled words in DESCRIPTION:
    
    Pacioni (12:9)
    
    al (11:17, 12:20)
    
    et (11:14, 12:17)
    
    vortexR (3:35)
    ```
  
    We would like to confirm that this package is a new submission.
    
    We would like to confirm that flagged possible mis-spelling are false positives.

* checking package dependencies ... NOTE
  
    ```No repository set, so cyclic dependency check skipped```
  
    This NOTE only occurred on winbuilder, R version 3.2.5 "oldrelease".

    This NOTE does not appear on local GNU/Linux and local Windows test environments, 
    where we have control over the `.Rprofile`, or on the two other winbuilder
    test environments.
    
    Based on [this answer](https://stat.ethz.ch/pipermail/r-package-devel/2015q3/000293.html)
    by the winbuilder maintainer and [answers](http://stackoverflow.com/q/23164929/2813717) 
    on Stackoverflow we suggest it could be a missing setting 
    `options(repos = c(CRAN="http://cran.r-project.org"))`
    in the `.Rprofile` on that test machine rather than a problem with this package.    
    
## Reviewer notes
The package was submitted as version 1.0.0 to CRAN and was rejected with 
suggestions from one CRAN reviewer. The suggestions were addressed as follows:

* The field `Description` in `DESCRIPTION` now leads with "This package uses..."
  as per the reviewer's suggestions, however this introduces a NOTE (see above).
* The citations now include DOIs in APA style.
* Version bumped to 1.0.1 and resubmitted to CRAN.

A second reviewer requested the following amendments:

* "Please omit the redundant 'The package' and rather start 'Contains ....'.
    We have amended the Description, which also fixed the related NOTE.
* "Please single quote 'vortexR'."
    'vortexR' is now single-quoted in the `DESCRIPTION`'s field `Description`.
* "Please add at least some simple examples."
    All `@usage` examples were converted to `@examples`.
    This will provide working examples of accessing every data object 
    (e.g. `help("pac.clas.lookup")`) and every directory of raw data 
    (e.g. `help("pacioni")`).
    Furthermore, our main package `vortexR` provides advanced examples by 
    parsing raw data provided by `vortexRdata` and analysing the parsed data.

## Downstream dependencies
We have checked downstream dependencies of vortexR using devtools::revdep_check().
Results: No errors or warnings found.

## License
The maintainer of this package, Carlo Pacioni, is an author on both papers 
which generated the data included here. 
Carlo has the written permission of all of his co-authors to make the data 
included here available in this form (as R package) under the chosen license (GPL-3).

## Reason for submission
This package serves as an auxiliary data package for our main package vortexR.
Splitting the raw data for vortexR into this package, vortexRdata, keeps 
vortexR's installed package size below the size threshold triggering a NOTE from 
`R CMD check --as-cran`.

