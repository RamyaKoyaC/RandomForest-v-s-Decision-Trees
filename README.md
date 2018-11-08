# RandomForest-v-s-Decision-Trees
Implementing the same dataset with random forest and decision tree to see which works best. 

```r
library(rpart)
library(caret)
library(e1071)
```
#### We have now loaded the libraries

```r 
model_dt = train(Class ~ ., data = train_set, method = "rpart")
model_dt_1 = predict(model_dt, data = train_set)
table(model_dt_1, train_set$Class)
mean(model_dt_1 == train_set$Class)
model_dt_test = predict(model_dt, newdata = test_set)
table(model_dt_test, test_set$Class)
mean(model_dt_test == test_set$Class)
```
#### We have implemented a decision tree on test and train sets
