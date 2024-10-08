# dso-r: R companion package for [dso](https://github.com/Boehringer-Ingelheim/dso)

The purpose of this package is to provide access to files and configuration organized in a dso project. 
It provides two main functions: 
  * `read_params(stage_path)` loads the configuration for the specified stage into an R object. The stage name must 
    be relative to the project root. This function works independent of the current working directory, as long as
    you are in any subdirectory of the project. 
  * `stage_here(rel_path)` is inspired by [here()](https://here.r-lib.org/). While `here()` resolves paths that
    are relative to the project root `stage_here()` resolves paths that are relative to the stage specified in `read_params`. 

Additionally, `dso-r` provides an R interface to some of the most important CLI commands of `dso`. 

## Installation

For now, it is just possible to install the development version from GitHub:

```r
remotes::install_github("Boehringer-Ingelheim/dso-r")
```