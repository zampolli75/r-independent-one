01\_write-installed-packages.R
================
joaquinrodriguez
Mon Jan 28 18:52:38 2019

``` r
## deja vu from earlier!

## create a data frame of your installed packages
## hint: installed.packages() is the function you need
library(tidyverse)
```

    ## ── Attaching packages ──────────────────────────────────────────────────────────────────────────────────────────── tidyverse 1.2.1 ──

    ## ✔ ggplot2 3.0.0     ✔ purrr   0.2.5
    ## ✔ tibble  1.4.2     ✔ dplyr   0.7.6
    ## ✔ tidyr   0.8.1     ✔ stringr 1.3.1
    ## ✔ readr   1.1.1     ✔ forcats 0.3.0

    ## ── Conflicts ─────────────────────────────────────────────────────────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

``` r
df <- installed.packages() %>% as.tibble()

head(df)
```

    ## # A tibble: 6 x 16
    ##   Package LibPath Version Priority Depends Imports LinkingTo Suggests
    ##   <chr>   <chr>   <chr>   <chr>    <chr>   <chr>   <chr>     <chr>   
    ## 1 abind   /Libra… 1.4-5   <NA>     R (>= … method… <NA>      <NA>    
    ## 2 assert… /Libra… 0.2.0   <NA>     <NA>    tools   <NA>      testthat
    ## 3 backpo… /Libra… 1.1.2   <NA>     R (>= … utils   <NA>      <NA>    
    ## 4 base    /Libra… 3.5.1   base     <NA>    <NA>    <NA>      methods 
    ## 5 base64… /Libra… 0.1-3   <NA>     R (>= … <NA>    <NA>      <NA>    
    ## 6 base64… /Libra… 1.4     <NA>     <NA>    backpo… <NA>      "base64…
    ## # ... with 8 more variables: Enhances <chr>, License <chr>,
    ## #   License_is_FOSS <chr>, License_restricts_use <chr>, OS_type <chr>,
    ## #   MD5sum <chr>, NeedsCompilation <chr>, Built <chr>

``` r
## optional: select just some of the variables, such as
##   * Package
##   * LibPath
##   * Version
##   * Priority
##   * Built

## write this data frame to data/installed-packages.csv
## hint: readr::write_csv() or write.table()
## idea: try using here::here() to create the file path

## YES overwrite the file that is there now (or delete it first)
## that's a old result from me (Jenny)
## it an example of what yours should look like and where it should go
```
