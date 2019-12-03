# Lab11

## Lab Overview
All students attending class will earn participation points for this lab. Students not attending class will need to complete their own lab.

We will revisit the movie earnings dataset using the bootstrap estimator.


```{r}
movies <- read_csv('http://math.montana.edu/ahoegh/teaching/stat446/movies_earnings.csv')
movies <- movies %>% mutate(revenue_millions = revenue/1000000, budget_millions = budget / 1000000)
```

A SRS of 250 movies has been taken for you from the dataset. Using the ratio estimator 

```{r}
movies_sample <- movies %>% sample_n(100)
```


#### 1. (2 points)
Using the standard SRS estimator, compute a point estimate of the mean movie revenue.


#### 2. (2 points)
Using a regression estimator, compute a point estimate of the mean movie earnings. Assume that you know the population mean for the movie budget,

```{r}
xbar_U <- movies %>% summarize(mean(budget_millions)) %>% pull() 
```


#### 3. (3 points)
Now use a bootstrap procedure to estimate the confidence interval for the SRS estimator. Plot the confidence interval along with your point estimate and the true value.



#### 4. (3 points)
Now use a bootstrap procedure to estimate the confidence interval for the regression estimator. Plot the confidence interval along with your point estimate and the true value.


