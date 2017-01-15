Tidy Style Guide
================
Yeedle
January 15, 2017

general script structure
========================

library declarations should always come at the top of a script.

`magrittr` Pipes
================

Avoid the assignment operator `%<>%` whenever possible (which is to say, always).[1] Instead, use explicit assignment.

``` diff
+mtcars <- mtcars %>% 
+  transform(cyl = cyl * 2)
```

``` diff
-mtcars 
```

<style>
div.blue pre { background-color:lightgreen; }
div.blue pre.r { background-color:red; }
</style>
``` r
summary(cars)
```

    ##      speed           dist       
    ##  Min.   : 4.0   Min.   :  2.00  
    ##  1st Qu.:12.0   1st Qu.: 26.00  
    ##  Median :15.0   Median : 36.00  
    ##  Mean   :15.4   Mean   : 42.98  
    ##  3rd Qu.:19.0   3rd Qu.: 56.00  
    ##  Max.   :25.0   Max.   :120.00

``` r
summary(cars)
```

    ##      speed           dist       
    ##  Min.   : 4.0   Min.   :  2.00  
    ##  1st Qu.:12.0   1st Qu.: 26.00  
    ##  Median :15.0   Median : 36.00  
    ##  Mean   :15.4   Mean   : 42.98  
    ##  3rd Qu.:19.0   3rd Qu.: 56.00  
    ##  Max.   :25.0   Max.   :120.00

[1] [R for Data Science](http://r4ds.had.co.nz/pipes.html#other-tools-from-magrittr)
