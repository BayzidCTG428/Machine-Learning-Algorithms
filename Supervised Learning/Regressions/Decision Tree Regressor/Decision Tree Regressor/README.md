# Decision Tree Regressor – Google Colab Implementation

## Overview
This repository demonstrates a complete implementation of a **Decision Tree Regressor** using Python and Scikit-learn. The project includes external dataset loading from Google Drive, detailed evaluation metrics, and graphical analysis using Seaborn.

---

## Dataset
- Loaded directly from **Google Drive**
- Supports any number of numerical features
- Target variable assumed to be the **last column**

---

## Workflow
1. Mount Google Drive
2. Load dataset using Pandas
3. Split data into training and testing sets
4. Train a Decision Tree Regressor
5. Evaluate using regression metrics
6. Visualize predictions and residuals
7. (Optional) Demonstrate classification metrics using thresholding

---

## Model Used
**DecisionTreeRegressor**
- `max_depth = 5`
- `random_state = 42`

---

## Regression Evaluation Metrics
- Mean Squared Error (MSE)
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

---

## Visualizations
- Actual vs Predicted scatter plot
- Residual distribution plot
- Confusion Matrix (after binarization)
- ROC Curve & AUC (educational purpose only)

---

## Important Note ⚠️
Confusion Matrix, ROC, and AUC are **classification metrics**.
They are **not natively applicable** to regression models.

In this project, regression outputs are **artificially converted into binary classes** using a threshold **only for educational demonstration**.

---

## Pros
- Interpretable model
- Handles non-linear relationships
- No feature scaling required

## Cons
- Highly prone to overfitting
- Poor generalization
- Not suitable for extrapolation

---

## Best Use Case
- Baseline regression
- Small to medium datasets
- Teaching and learning purposes

---

## Future Improvements
- Random Forest Regressor
- Gradient Boosting
- Hyperparameter tuning with GridSearchCV
