# K-Nearest Neighbors (KNN) Classification from Google Drive Dataset

This project demonstrates how to implement **KNN classification** using an **external dataset from Google Drive** in Google Colab. It includes all main evaluation metrics and beautiful visualizations.

## Features

- Load any CSV dataset from Google Drive
- Feature scaling using StandardScaler
- KNN classifier training and prediction
- Evaluation metrics:
  - Accuracy
  - F1 Score
  - Precision
  - Recall
  - Confusion Matrix
  - ROC Curve & AUC (for binary classification)
- Visualizations using seaborn & matplotlib

## How It Works

1. Mount Google Drive to access dataset.
2. Load CSV dataset into a Pandas DataFrame.
3. Separate features (X) and target (y).
4. Split dataset into training and testing sets.
5. Scale features using StandardScaler.
6. Train KNN classifier with Euclidean distance.
7. Make predictions on the test set.
8. Calculate evaluation metrics.
9. Visualize results (confusion matrix, ROC curve).

## Limitations

- **ROC & AUC** are currently implemented for binary classification only.
- Computationally expensive for large datasets (O(n × d) per prediction).
- Sensitive to irrelevant or non-scaled features.
- Sensitive to class imbalance (may need balancing techniques).

## Alternatives

- Logistic Regression
- Support Vector Machine (SVM)
- Random Forest Classifier
- Gradient Boosting (XGBoost, LightGBM)

## Notes

- Ensure the last column in your CSV is the target variable.
- Scaling is mandatory for KNN to work correctly.
- Multi-class ROC curve requires extra implementation if needed.
