Sepsis Survival Classification Naives Bayes
================
Rex Manglicmot
2022-12-18

-   <a href="#status-continuing-working-docuemtn"
    id="toc-status-continuing-working-docuemtn">Status: Continuing Working
    Docuemtn</a>
-   <a href="#introduction" id="toc-introduction">Introduction</a>
-   <a href="#loading-the-libraries" id="toc-loading-the-libraries">Loading
    the Libraries</a>
-   <a href="#loading-the-data" id="toc-loading-the-data">Loading the
    Data</a>
-   <a href="#cleaning-the-data" id="toc-cleaning-the-data">Cleaning the
    Data</a>
-   <a href="#exploratory-data-analysis"
    id="toc-exploratory-data-analysis">Exploratory Data Analysis</a>
-   <a href="#naives-bayes" id="toc-naives-bayes">Naives Bayes</a>
-   <a href="#limitations" id="toc-limitations">Limitations</a>
-   <a href="#conclusion" id="toc-conclusion">Conclusion</a>
-   <a href="#inspiration-for-this-project"
    id="toc-inspiration-for-this-project">Inspiration for this project</a>

## Status: Continuing Working Docuemtn

## Introduction

## Loading the Libraries

``` r
library(tidyverse)
```

## Loading the Data

``` r
#load the data
data_orig <- read.csv('Sepsis Survival.csv')

#view first 7 rows
head(data_orig, 7)
```

    ##   age_years sex_0male_1female episode_number hospital_outcome_1alive_0dead
    ## 1        21                 1              1                             1
    ## 2        20                 1              1                             1
    ## 3        21                 1              1                             1
    ## 4        77                 0              1                             1
    ## 5        72                 0              1                             1
    ## 6        83                 0              1                             1
    ## 7        74                 0              1                             1

## Cleaning the Data

**Bust out the Clorox, cuz we got some cleaning to do!**

Make a copy change column names call unique to see values

``` r
#make a copy of the original dataset
data <- data_orig

#change colnames
colnames(data) <- c('age', 'sex', 'epi', 'result')

#check for all values
uni <- lapply(data, unique)
uni
```

    ## $age
    ##   [1]  21  20  77  72  83  74  69  53  82  75  45  56  46  48  40  39  70  47
    ##  [19]  27  11  91   7  79  84  16  73  17  18  63  88  89  76  41  66  80  62
    ##  [37]  59  55  68  33  71   8  58  78  51  43  44  60  86  61  67  57  81  49
    ##  [55]  64  25  65  42  36  38  85  24  19  37  35   6  50  87  54  29  12  10
    ##  [73]  23  52   9  15  31  92  28  30  13  94  90  26  32  95   5  93  34  96
    ##  [91]  22  97  98 100  14   4  99   3   2   1   0
    ## 
    ## $sex
    ## [1] 1 0
    ## 
    ## $epi
    ## [1] 1 2 3 4 5
    ## 
    ## $result
    ## [1] 1 0

``` r
class(data)
```

    ## [1] "data.frame"

## Exploratory Data Analysis

## Naives Bayes

## Limitations

## Conclusion

## Inspiration for this project
