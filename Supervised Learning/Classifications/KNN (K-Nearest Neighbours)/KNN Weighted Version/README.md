# Weighted KNN Classification from Scratch (Google Drive Dataset)

This project implements a **Weighted KNN classifier from scratch** using an external CSV dataset from Google Drive. 

## Features

- Load CSV dataset from Google Drive
- Feature scaling using StandardScaler
- Weighted KNN classification (closer neighbors get higher influence)
- Evaluation metrics: Accuracy, F1 Score, Precision, Recall, Confusion Matrix, ROC & AUC (binary)
- Visualizations using seaborn

## How It Works

1. Load dataset from Google Drive
2. Separate features and target
3. Split into training and testing
4. Standardize features
5. Implement Weighted KNN
6. Predict test samples
7. Calculate evaluation metrics
8. Visualize confusion matrix and ROC (if binary)

## Limitations

- ROC/AUC works only for binary classification
- Slow for large datasets
- Sensitive to irrelevant features
- No hyperparameter tuning

## Alternatives

- Logistic Regression
- Support Vector Machine (SVM)
- Random Forest Classifier
- Gradient Boosting (XGBoost, LightGBM)
