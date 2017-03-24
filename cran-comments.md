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

* checking CRAN incoming feasibility ... NOTE
    ```
    Maintainer: 'Carlo Pacioni <C.Pacioni@Murdoch.edu.au>'
    
    New submission
    
    Possibly mis-spelled words in DESCRIPTION:
    
    Pacioni (12:9)
    
    al (11:17, 12:20)
    
    et (11:14, 12:17)
    
    vortexR (3:35, 15:19)
    
    The Description field should not start with the package name,
    'This package' or similar.
    ```
  
    We would like to confirm that this package is a new submission.
    
    We would like to confirm that flagged possible mis-spelling are false positives.
    
    We amended the Description to lead with "This package uses..." as per the CRAN 
    reviewer's suggestion to do so.

* checking package dependencies ... NOTE
  
    ```No repository set, so cyclic dependency check skipped```
  
    This NOTE only occurred on winbuilder, R version 3.2.5 "oldrelease".
    vortexRdata has no dependencies, as it contains no R code besides the data 
    (.rda and raw text files), therefore we see no risk of cyclic dependencies
    limited to R version 3.2.5 but not occurring in all other tested environments.
    
    This does not appear on GNU/Linux and local Windows test environments.
    
## Reviewer notes
The package was submitted as version 1.0.0 to CRAN and was rejected with 
suggestions from one CRAN reviewer. The suggestions were addressed as follows:

* The field `Description` in `DESCRIPTION` now leads with "This package uses..."
  as per the reviewer's suggestions, however this introduces a NOTE (see above).
* The citations now include DOIs in APA style.
* Version bumped to 1.0.1.
* Tests run in GNU/Linux environments, as only metadata in DESCRIPTION has changed
  since version 1.0.0 which was tested in all environments.

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

