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

``` r
nobel_living <- nobel_living %>%
  mutate(
    country_us = if_else(country == "USA", "USA", "Other")
  )
nobel_living_science <- nobel_living %>%
  filter(category %in% c("Physics", "Medicine", "Chemistry", "Economics"))
```

### Exercise 3

``` r
ggplot(nobel_living_science, aes(y = country_us)) +
  geom_bar() +
  facet_grid(~ category) +
  labs(title = "Are they USA-based?", x = "Country", y = "Counts") +
  theme_minimal()
```

![](lab-03_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

### Exercise 4

…

### Exercise 5

…

### Exercise 6

…
