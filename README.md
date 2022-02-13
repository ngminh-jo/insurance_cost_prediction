## In this project I will apply regression techniques of supervised learning to predict the medical insurance costs.
all the work is clearly explained and interpreted  in medical-insurance-cost-predict.ipynb.

After the data exploration and data preprocessing, multiple regression algorithms like Linear Regression(Benchmark model), decision trees, random forest, Support Vector Machines, k-nearest neighbors for regression are considered and compared based on the metrics.
Random Forest Regressor (mse: 15,78% and r2_score: 79,7%) has the best performance among these algorithms and this is a significant improvement compared to our benchmark model linear regression ((mse: 17,67% and r2_score: 72.02%).
So I choose to use random forest technique for this project and focus on optimizing the random forest model.
* The random grid does help us to search for the better hyperparameters and the result is improved (mse: 13,74% and r2_score: 81,41%) in compare to the result before (mse: 15,78% and r2_score: 79,7%)
* After that the grid search with cross-validation does not significantly improve our result, but there is still a slightly better result in mse.
Final result has 
* mean_squared_error : 0.137330
* r2_score : 0.814193
