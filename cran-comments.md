## Test environments
devtools::check() was run on:

* GNU/Linux (kernel 4.4.0-59-generic, arch x86_64, Ubuntu 16.04.2 LTS),
  R version 3.3.3 (RStudio Desktop)
* GNU/Linux (kernel 4.4.0-53-generic, arch x86_64, Ubuntu 14.04.5 LTS),
  R version 3.3.2 (RStudio Server)
* GNU/Linux (kernel 3.13.0-103-generic, arch x86_64, Ubuntu 12.04.5 LTS),
  R version 3.3.2 (TravisCI)
* MS Windows (TODO Carlo: insert windows and R version)

## R CMD check results
In all environments, the results of check() were:

0 errors | 0 warnings | 0 notes

This package serves as an auxiliary data package for our main package vortexR.
Splitting out the data into a separate package helps to keep vortexR's installed 
package size to a minimum, allowing experienced users of vortexR to skip the 
download and installation of vortexRdata.

## Downstream dependencies
We have checked downstream dependencies of vortexR using devtools::revdep_check().
Results: No errors or warnings found.

## License
The maintainer of this package, Carlo Pacioni authored both papers which generated
the data included here. Carlo has the written permission of all of his co-authors 
to make the data included here available in this form (as R package) under the 
chosen license (GPL-3).
