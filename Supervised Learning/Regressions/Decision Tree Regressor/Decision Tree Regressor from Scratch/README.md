# Decision Tree Regressor – From Scratch

## Core Mechanism
A Decision Tree Regressor works by recursively splitting data to minimize variance (MSE).

### Key Steps
1. Try every feature
2. Try every possible threshold
3. Compute weighted MSE after split
4. Choose split with lowest MSE
5. Repeat until max depth reached

### Leaf Node Prediction
Each leaf predicts:
Mean of target values in that node

### Why It Overfits
- Memorizes training data
- Deep trees = low bias, high variance

### Time Complexity
O(n × features × thresholds)

### Why ROC/AUC Is Artificial Here
Regression outputs are converted into binary labels via thresholding purely for visualization.
