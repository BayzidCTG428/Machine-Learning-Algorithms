# Elastic Net Regression – From Scratch

## Core Idea
Elastic Net combines:
- L1 Regularization (Lasso) → sparsity
- L2 Regularization (Ridge) → stability

### Cost Function
MSE + α [ l1_ratio·|w| + (1−l1_ratio)·w² ]

### Optimization
- Gradient Descent
- Manual weight updates
- Regularization applied directly in gradient

### Why Scaling Is Mandatory
Regularization penalizes weight magnitude.
Unscaled features distort penalties.

### Strengths
- Handles multicollinearity
- Feature selection + stability
- Better than Lasso/Ridge alone

### Weaknesses
- Linear only
- Needs tuning
- Slower convergence

### ROC/AUC Note
Regression outputs are thresholded only for visualization.
Elastic Net is NOT a classifier.
