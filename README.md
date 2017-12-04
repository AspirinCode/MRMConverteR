# MRMConverteR

[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](http://www.repostatus.org/badges/latest/active.svg)](http://www.repostatus.org/#active)
 [![Build Status](https://travis-ci.org/wilsontom/MRMConverteR.svg?branch=master)](https://travis-ci.org/wilsontom/MRMConverteR) [![Build status](https://ci.appveyor.com/api/projects/status/s79ced2qebvqv4bn/branch/master?svg=true)](https://ci.appveyor.com/project/wilsontom/mrmconverter/branch/master) [![codecov](https://codecov.io/gh/wilsontom/MRMConverteR/branch/master/graph/badge.svg)](https://codecov.io/gh/wilsontom/MRMConverteR)
![License](https://img.shields.io/badge/license-GNU%20GPL%20v3.0-blue.svg "GNU GPL v3.0")

>__convert MRM-MS (.mzML) files to LC-MS style .mzML__


```R
devtools::install_github('wilsontom/MRMConverteR')
```

#### Usage

MRM-MS `.mzML` files should have been created using the ProteoWizard `msconvert` tool.

> __NOTE__ this package has only been tested with MRM-MS data acquired on a TSQ Vantage (ThermoScientific) which were then converted to `.mzML` using ProteoWizard 3.0.10246 64-bit.

There is only one function exported from `MRMConverteR`; __`convert`__

The function input is __(1)__ the `.mzML` to convert and __(2)__ the destination path for the converted file. Filenames of converted files are the same as the input; with `convert-` prepended.


````R
library(MRMConverteR)

convert('inst/extdata/example_qqq.mzML', 'inst/extdata')

list.files('inst/extdata')
[1] "convert-example_qqq.mzML" "example_qqq.mzML"  

```
