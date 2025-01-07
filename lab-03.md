Lab 03 - Nobel laureates
================
Insert your name here
Insert date here

### Load packages and data

``` r
library(tidyverse) 
```

``` r
nobel <- read_csv("data/nobel.csv")
```

## Exercises

### Exercise 1

``` r
dim(nobel)
```

    ## [1] 935  26

### Exercise 2

``` r
nobel_living <- filter(nobel, 
                       !is.na(country),
                       gender != "org",
                       is.na(died_date))
```

### Exercise 3

Remove this text, and add your answer for Exercise 1 here. Add code
chunks as needed. Don’t forget to label your code chunk. Do not use
spaces in code chunk labels.

### Exercise 4

…

### Exercise 5

…

### Exercise 6

…
