# KNN Regression from Scratch (Google Drive Dataset)

This project implements **KNN Regression from scratch** using an external dataset from Google Drive. All steps are implemented using NumPy without scikit-learn regression models.

## Features

- Load CSV dataset from Google Drive
- Feature scaling using StandardScaler
- KNN regression using **mean of k nearest neighbors**
- Evaluation metrics: MSE, MAE, R2 Score
- Visualization of actual vs predicted values using seaborn

## How It Works

1. Load dataset from Google Drive
2. Separate features and target
3. Split data into training and testing
4. Standardize features
5. Implement KNN regression from scratch
6. Predict on test set
7. Calculate evaluation metrics
8. Visualize results

## Limitations

- Computationally expensive for large datasets
- Poor performance on noisy data
- Sensitive to irrelevant features
- No built-in hyperparameter tuning

## Alternatives

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressors (XGBoost, LightGBM)
