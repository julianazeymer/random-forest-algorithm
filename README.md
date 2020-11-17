
# random-forest-algorithm

> The Random Forest algorithm was chosen in my doctoral thesis to
> predict the dry matter loss of soybeans stored in different conditions
> of temperature, moisture content and time. It is now available to
> anyone who is interested in using it for prediction.

## Code Example

``` r
library("randomForest")
```

``` r
set.seed(1234)
```

``` r
# data frame with simulated values for the variables time, temperature and bs

data <- data.frame(
  time = runif(10, 0, 20),
  temperature = runif(10, 25, 30),
  bs = runif(10, 12, 22)
)
```

``` r
# reading random_forest.rds

random_forest <- readRDS(here::here("random_forest.rds"))
```

``` r
# new predictions

predict(random_forest, newdata = data)
```

    ##            1            2            3            4            5            6 
    ## 0.0073128049 0.0331288628 0.0352716990 0.0330387106 0.0440075828 0.1283100020 
    ##            7            8            9           10 
    ## 0.0009815535 0.0235023441 0.0728076652 0.0251022213
