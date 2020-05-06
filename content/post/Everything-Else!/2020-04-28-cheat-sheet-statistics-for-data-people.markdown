---
title: 'Stats Cheat Sheet: Summary Functions'
author: Amy Linehan
date: '2020-05-05'
slug: cheat-sheet-statistics-for-data-people
categories:
  - Other
tags:
  - Other
  - Statistics
subtitle: ''
summary: 'Tips, Tricks and Reminders for those of us who struggle to remember what our professors/Google taught us: Functions to summarise your data'
authors: ["alinehan"]
lastmod: '2020-04-28T09:37:48-07:00'
featured: no
image:
  caption: ''
  focal_point: ''
  preview_only: no
projects: []
---

Ok let's get honest... I somehow made it through AP courses in high school and four years of math and economics courses at UCLA without really understanding statistics. Yes yes yes I memorized the formulas and learned how to use my calculator enough to survive any and all stats requirements during college but it never really stuck. A few months ago, I realized my coworkers just assumed I was a stats major because I used R and "liked math". So I've decided to make a little cheat sheet/ basic stats review for all of you out there who, like me, occassionally need to pretend they know stats. 

The first part of this guide is focusing on the basic functions that I rely on a lot to get a grasp of my data when I first get it. For instance, I want to see the smallest and largest values in a set of numbers and look for any outliers that may skew my analysis.


Overall, R is used a lot for statistical analyses and I'm probably in the minority as a programmer who uses R primarily for non-stats reasons. R has all of your basic stats functions that you remember from school: min, max, mean, median and range. Here are some simple examples of how those functions work: 






```r
min(c(34,2,45,99))
```

```
## [1] 2
```

```r
max(c(34,2,45,99))
```

```
## [1] 99
```

```r
median(c(34,2,45,99))
```

```
## [1] 39.5
```

```r
range(c(34,2,45,99))
```

```
## [1]  2 99
```


The min, max, and range functions are all part of the base R package while median is part of the stats package. To see a full list of all the functions in this package, run the following code in your console: library(help="stats"). There are a lot and many of them are more complex than simple statistical calculations require so I won't be going into detail on them here. 

Another useful function in the stats package is quantile(). This function returns sample quantiles for the inputted values. The function defaults to outputting quartile results (0%, 25%, 50%, 75% and 100%)  where 0% is the minimum value of the set, 50% is the median, and 100% is the maximum value. You can also set what percentile value you want outputted within the function:


```r
# default
quantile(x <- c(10,25,2,21,16,13,9,3,10001))
```

```
##    0%   25%   50%   75%  100% 
##     2     9    13    21 10001
```


```r
# only return 80%, 95% and 99% percentiles
quantile(x, c(.8,.90,.99))
```

```
##     80%     90%     99% 
##   22.60 2020.20 9202.92
```

This is a really useful function to use when you're reviewing new data to summarise the data and get an idea with what's going on.
In the example set above, using the maximum or range functions along to summarize the data would not indicate the occurance of an outliar as clearly as looking at the quantile function. 


Next up in my attempt to remember statistics: normal distributions! 




