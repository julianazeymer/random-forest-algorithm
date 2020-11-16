# random-forest-algorithm
 The Random Forest algorithm was chosen in my doctoral thesis to predict the dry matter loss of soybeans stored in different conditions of temperature, moisture content and time. 
 
 
 library("randomForest")

data_test <- data.frame(
  time = c(value_1, ..., value_n), 
  temperature = c(value_1, ..., value_n), 
  bs = c(value_1, ..., value_n)
)

random_forest <- readRds(".../random_forest.rds")

predict(random_forest, newdata = data_test)
