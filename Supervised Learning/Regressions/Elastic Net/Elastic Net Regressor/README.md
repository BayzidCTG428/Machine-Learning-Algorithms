# Elastic Net Regression – Google Colab Implementation

## Overview
This repository contains a complete implementation of **Elastic Net Regression** using Scikit-learn. The workflow includes dataset loading from Google Drive, preprocessing, model training, evaluation, and visualization using Seaborn.

Elastic Net combines **L1 (Lasso)** and **L2 (Ridge)** regularization, making it effective for datasets with multicollinearity and high-dimensional features.

---

## Dataset
- Loaded from Google Drive
- Numerical features supported
- Target variable assumed as the last column

---

## Workflow
1. Mount Google Drive
2. Load dataset using Pandas
3. Split into training and testing sets
4. Standardize features
5. Train Elastic Net Regressor
6. Evaluate using regression metrics
7. Visualize predictions and residuals
8. Demonstrate classification metrics via thresholding

---

## Model Configuration
ElasticNet parameters:
- `alpha = 0.1`
- `l1_ratio = 0.5`
- `random_state = 42`

---

## Regression Metrics
- Mean Squared Error (MSE)
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

---

## Visualizations
- Actual vs Predicted scatter plot
- Residual distribution plot
- Confusion Matrix (threshold-based)
- ROC Curve & AUC

---

## Important Note ⚠️
Elastic Net is a **regression algorithm**.
Confusion Matrix, ROC, and AUC are **classification metrics**.

In this project, regression outputs are converted into binary labels using a threshold **only for educational and visualization purposes**.

---

## Pros
- Handles multicollinearity
- Performs feature selection
- Prevents overfitting
- Stable and interpretable

## Cons
- Requires feature scaling
- Linear assumptions
- Not suitable for non-linear data

---

## Best Use Cases
- High-dimensional datasets
- Correlated features
- Baseline regression models

---

## Future Improvements
- Hyperparameter tuning (GridSearchCV)
- Comparison with Ridge & Lasso
- Polynomial feature expansion
