## Project Overview
This project aims to predict medical insurance costs using regression techniques from supervised learning. All code and explanations are provided in the `medical-insurance-cost-predict.ipynb` notebook.

## Methodology
After thorough data exploration and preprocessing, various regression algorithms were tested and compared, including:
- **Linear Regression** (Benchmark Model)
- **Decision Trees**
- **Random Forest**
- **Support Vector Machines**
- **K-Nearest Neighbors**

Each model was evaluated based on key metrics like mean squared error (MSE) and R² score.

## Results and Model Selection
Among the algorithms, the **Random Forest Regressor** achieved the best performance, with the following metrics:
- **MSE:** 15.78%
- **R² Score:** 79.7%

This was a significant improvement over the benchmark model, Linear Regression, which had:
- **MSE:** 17.67%
- **R² Score:** 72.02%

Based on these results, the Random Forest model was selected, and further efforts were focused on optimizing this model.

## Model Optimization
1. **Randomized Search:** A random search was conducted to identify better hyperparameters, improving the model performance to:
   - **MSE:** 13.74%
   - **R² Score:** 81.41%

2. **Grid Search with Cross-Validation:** Further tuning with grid search provided a slight improvement in MSE but no significant changes overall.

## Final Model Performance
The final optimized Random Forest model achieved:
- **Mean Squared Error:** 0.1373
- **R² Score:** 0.8142

This result demonstrates the effectiveness of the Random Forest approach for predicting medical insurance costs.
