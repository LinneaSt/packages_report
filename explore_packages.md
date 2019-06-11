explore\_packages.R
================
linnea.stenbeck
2019-06-11

``` r
library(tidyverse)
```

    ## Registered S3 methods overwritten by 'ggplot2':
    ##   method         from 
    ##   [.quosures     rlang
    ##   c.quosures     rlang
    ##   print.quosures rlang

    ## -- Attaching packages --------------------------------------------------------- tidyverse 1.2.1 --

    ## v ggplot2 3.1.1     v purrr   0.3.2
    ## v tibble  2.1.3     v dplyr   0.8.1
    ## v tidyr   0.8.3     v stringr 1.4.0
    ## v readr   1.3.1     v forcats 0.4.0

    ## -- Conflicts ------------------------------------------------------------ tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
.libPaths()
```

    ## [1] "/Library/Frameworks/R.framework/Versions/3.6/Resources/library"

``` r
ipt <- installed.packages() %>%
  as_tibble() %>%
  select(Package, LibPath, Version, Priority, Built)
ipt
```

    ## # A tibble: 115 x 5
    ##    Package    LibPath                               Version Priority  Built
    ##    <chr>      <chr>                                 <chr>   <chr>     <chr>
    ##  1 BH         /Library/Frameworks/R.framework/Vers~ 1.69.0~ <NA>      3.6.0
    ##  2 DBI        /Library/Frameworks/R.framework/Vers~ 1.0.0   <NA>      3.6.0
    ##  3 KernSmooth /Library/Frameworks/R.framework/Vers~ 2.23-15 recommen~ 3.6.0
    ##  4 MASS       /Library/Frameworks/R.framework/Vers~ 7.3-51~ recommen~ 3.6.0
    ##  5 Matrix     /Library/Frameworks/R.framework/Vers~ 1.2-17  recommen~ 3.6.0
    ##  6 R6         /Library/Frameworks/R.framework/Vers~ 2.4.0   <NA>      3.6.0
    ##  7 RColorBre~ /Library/Frameworks/R.framework/Vers~ 1.1-2   <NA>      3.6.0
    ##  8 Rcpp       /Library/Frameworks/R.framework/Vers~ 1.0.1   <NA>      3.6.0
    ##  9 askpass    /Library/Frameworks/R.framework/Vers~ 1.1     <NA>      3.6.0
    ## 10 assertthat /Library/Frameworks/R.framework/Vers~ 0.2.1   <NA>      3.6.0
    ## # ... with 105 more rows
