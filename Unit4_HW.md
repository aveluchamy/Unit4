# Unit 4 Homework
Aravind Veluchamy  
June 3, 2016  
# Bootstrap demo using random sample generated using rnorm function
##1st example

```r
#First random distribution with sample size 50 (mean 22 nd SD 3)
 x1 <-rnorm(50,22,3)
xbar1 <- mean(x1)
xbar1
```

```
## [1] 22.64208
```

```r
nsims1 <- 1000
bootnorm1 <- numeric(nsims1)
for(i in 1:nsims1){
temp1 <- sample (x1,50,replace=TRUE)
bootnorm1[i] <- mean(temp1) 
}
mean(bootnorm1)
```

```
## [1] 22.64109
```

```r
summary(bootnorm1)
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##   21.34   22.32   22.66   22.64   22.96   24.04
```

```r
#to demonstrate central limit theorem with the histogram plot
hist(bootnorm1)
```

![](Unit4_HW_files/figure-html/unnamed-chunk-1-1.png)<!-- -->
##2nd example

```r
#Second random distribution with sample size 100  (mean 22 and SD 3)
 x2 <-rnorm(100,22,3)
xbar2 <- mean(x2)
xbar2
```

```
## [1] 21.74359
```

```r
nsims2 <- 1000
bootnorm2 <- numeric(nsims2)
for (i in 1:nsims2){
temp2 <- sample (x2,100,replace=TRUE)
bootnorm2[i] <- mean(temp2) 
}
mean(bootnorm2)
```

```
## [1] 21.73011
```

```r
summary(bootnorm2)
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##   20.70   21.50   21.73   21.73   21.93   22.75
```

```r
#to demonstrate central limit theorem with the histogram plot
hist(bootnorm2)
```

![](Unit4_HW_files/figure-html/unnamed-chunk-2-1.png)<!-- -->
# Bootstrap demo using random sample generated using rexp function
##1st Example

```r
#Second random distribution with  sample size 50  
 x3 <-rexp(50)
xbar3 <- mean(x3)
xbar3
```

```
## [1] 0.9121398
```

```r
nsims3 <- 1000
bootnorm3 <- numeric(nsims3)
for (i in 1:nsims3){
temp3 <- sample (x3,50,replace=TRUE)
bootnorm3[i] <- mean(temp3) 
}
mean(bootnorm3)
```

```
## [1] 0.9109803
```

```r
summary(bootnorm3)
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##  0.5300  0.8242  0.9029  0.9110  0.9923  1.4070
```

```r
#to demonstrate central limit theorem with the histogram plot
hist(bootnorm3)
```

![](Unit4_HW_files/figure-html/unnamed-chunk-3-1.png)<!-- -->
##2nd Example

```r
#Second random distribution with  sample size 100  
 x4 <-rexp(100)
xbar4 <- mean(x4)
xbar4
```

```
## [1] 0.7860885
```

```r
nsims4 <- 1000
bootnorm4 <- numeric(nsims4)
for (i in 1:nsims4){
temp4 <- sample (x4,100,replace=TRUE)
bootnorm4[i] <- mean(temp4) 
}
mean(bootnorm4)
```

```
## [1] 0.7860468
```

```r
summary(bootnorm4)
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##  0.5561  0.7337  0.7844  0.7860  0.8339  1.0150
```

```r
#to demonstrate central limit theorem with the histogram plot
hist(bootnorm4)
```

![](Unit4_HW_files/figure-html/unnamed-chunk-4-1.png)<!-- -->
