---
title: "excercise1"
output:
  pdf_document: default
  word_document: default
  html_document:
    df_print: paged
date: "2024-01-15"
---



## Import data:


```r
df = read.csv('C:/Users/tsong/Downloads/performance_data (1).csv')

head(df,20)
```

## Including Plots

You can also embed plots, for example:


```r
df = read.csv('C:/Users/tsong/Downloads/performance_data (1).csv')
plot(df[,c("worker1","worker2","worker3")])
```

![](Excercise1_files/figure-latex/unnamed-chunk-28-1.pdf)<!-- --> 

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.



```r
df = read.csv('C:/Users/tsong/Downloads/performance_data (1).csv')
plot(x=df[,c("worker1")], type = 'l')
```

![](Excercise1_files/figure-latex/unnamed-chunk-29-1.pdf)<!-- --> 

```r
plot(x=df[,c("worker2")], type = 'l')
```

![](Excercise1_files/figure-latex/unnamed-chunk-29-2.pdf)<!-- --> 

```r
plot(x=df[,c("worker3")], type = 'l')
```

![](Excercise1_files/figure-latex/unnamed-chunk-29-3.pdf)<!-- --> 




Create two columns to denote interventions on w2 and w3 numerically


```r
df = read.csv('C:/Users/tsong/Downloads/performance_data (1).csv')
df['A'] = ifelse(df["w2_intervention"]=='A',1,0)
df['B'] = ifelse(df["w3_intervention"]=='B',1,0)
```





By plotting the following three variables on scatter plots, we can see that intervention A did have an positive effect on performance as 0 and 1 have different distributions for worker 2

```r
df = read.csv('C:/Users/tsong/Downloads/performance_data (1).csv')
df['A'] = ifelse(df["w2_intervention"]=='A',1,0)
df['B'] = ifelse(df["w3_intervention"]=='B',1,0)
plot(df[,c('A','worker1','worker2')])
```

![](Excercise1_files/figure-latex/unnamed-chunk-31-1.pdf)<!-- --> 

```r
df = read.csv('C:/Users/tsong/Downloads/performance_data (1).csv')
df['A'] = ifelse(df["w2_intervention"]=='A',1,0)
df['B'] = ifelse(df["w3_intervention"]=='B',1,0)
plot(df[,c('B','worker1','worker3')])
```

![](Excercise1_files/figure-latex/unnamed-chunk-32-1.pdf)<!-- --> 

The intervention on worker has negative effect as the the scatter plot shows the distribution moves downwards 
