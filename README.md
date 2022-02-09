## In this project I will apply regression techniques of supervised learning to predict the medical insurance costs.

### Data Exploration
### Data Preprocessing
### Developing a Benchmark model: Multiple linear regression
1. Training and Testing data set
2. Model building: Multiple linear regression
3. Implementation: Define a Performance Metric
### Machine learning model
The Benchmark model returns $R^2$ value of 72%, so it fit our data test well, but still we can imporve the the performance of by diffirent technique. We will implement the other regression machine learning models discussed in the lectures and try to get a better result compared to our Benchmark model.

Multiple regression algorithms like Linear Regression(Benchmark model), decision trees, random forest, Support Vector Machines, k-nearest neighbors for regression are considered and compared based on the metrics.


As we can see from the result table, Random Forest Regressor (mse: 15,78% and r2_score: 79,7%) has the best performance among these algorithms and this is a significant improvement compared to our benchmark model linear regression ((mse: 17,67% and r2_score: 72.02%). 

A random forest is an ensemble model that consists of many decision trees. Predictions are made by averaging the predictions of each decision tree. Or, to extend the analogy—much like a forest is a collection of trees, the random forest model is also a collection of decision tree models. This makes random forests a strong modeling technique that’s much more powerful than a single decision tree.


In this case, the random forest regression algorithm can be more suitable for  this regression problem than other common and popular algorithms because 

- There are non-linear or complex relationships between features and labels.
- The random forest algorithm is more robust than a single decision tree, as it uses a set of uncorrelated decision trees.
- Random forest is a good choice

### So I choose to use random forest technique for this project and focus on optimizing the random forest model. 
 
 In the case of a random forest, hyperparameters include the number of decision trees in the forest and the number of features considered by each tree when splitting a node. (The parameters of a random forest are the variables and thresholds used to split each node learned during training).
 
 The standard procedure for hyperparameter optimization accounts for overfitting through cross validation.
 
 Look at parameters used by our current forest
 
### The most important settings are 
- the number of trees in the forest (n_estimators) 
- the number of features considered for splitting at each leaf node (max_features)


We will try adjusting the following set of hyperparameters:
- n_estimators = number of trees in the foreset
- max_features = max number of features considered for splitting a node
- max_depth = max number of levels in each decision tree
- min_samples_split = min number of data points placed in a node before the node is split
- min_samples_leaf = min number of data points allowed in a leaf node
- bootstrap = method for sampling data points (with or without replacement)

### Random Search Training
 Use the random grid to search for best hyperparameters. Random search of parameters, using 3 fold cross validation, search across 100 different combinations, and use all available cores
the random grid does help us to search for the better hyperparameters and the result is improved (mse: 13,74% and r2_score: 81,41%) in compare to the result before (mse: 15,78% and r2_score: 79,7%)

### Grid Search with Cross Validation
Random search allowed us to narrow down the range for each hyperparameter. Now that we know where to concentrate our search, we can explicitly specify every combination of settings to try. We do this with GridSearchCV, a method that, instead of sampling randomly from a distribution, evaluates all combinations we define.
Create the parameter grid based on the results of random search.

* The grid search with cross-validation does not significantly improve our result, but there is still a slightly better result in mse.


