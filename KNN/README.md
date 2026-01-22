# Machine-Learning-Algorithms
**Machine Learning Algorithms** is a practical repository featuring from-scratch and library-based implementations of core ML algorithms. It focuses on mathematical intuition, clean code, and proper evaluation to help learners truly understand how models work in real-world scenarios.

# K-Nearest Neighbors (KNN) – Theory and Practical Implementation

This repository contains **theoretical explanations and practical implementations** of KNN algorithms:
1. KNN Classification using scikit-learn
2. KNN Classification from scratch
3. KNN Regression from scratch
4. Weighted KNN Classification from scratch

The goal is to **teach someone KNN from the ground up**, including **mathematical examples**, intuition, limitations, and alternatives.

---

## 1️⃣ What is KNN?

**K-Nearest Neighbors (KNN)** is a **non-parametric, lazy learning algorithm** used for **classification** and **regression**.

- **Non-parametric**: No assumptions about the underlying data distribution.
- **Lazy learning**: No explicit training phase; computation happens at prediction.
- **Instance-based**: Stores all training data and compares new inputs to them.

### Basic Idea (Classification)
1. Choose a positive integer **K**.
2. Compute distance from new point to **all training points**.
3. Select **K closest neighbors**.
4. Use **majority vote** to predict the class.

Mathematically:

For a new input \(x\):

\[
y = \text{mode} \{ y_i \,|\, x_i \in N_K(x) \}
\]

Where:
- \(N_K(x)\) = set of K nearest neighbors of \(x\)
- \(y_i\) = label of neighbor \(i\)

---

### Distance Metric (Euclidean Example)

\[
d(x, x_i) = \sqrt{\sum_{j=1}^{n} (x_j - x_{ij})^2}
\]

Where:
- \(n\) = number of features
- \(x_j\) = feature of new sample
- \(x_{ij}\) = feature of training sample \(i\)

---

### Example:

| Feature 1 | Feature 2 | Class |
|-----------|-----------|-------|
| 2         | 3         | A     |
| 3         | 4         | A     |
| 5         | 6         | B     |
| 6         | 5         | B     |

**New point**: (4,5)  
Compute distances:

- To (2,3): \(\sqrt{(4-2)^2 + (5-3)^2} = \sqrt{4+4} = 2.83\)
- To (3,4): \(\sqrt{(4-3)^2 + (5-4)^2} = \sqrt{1+1} = 1.41\)
- To (5,6): \(\sqrt{(4-5)^2 + (5-6)^2} = \sqrt{1+1} = 1.41\)
- To (6,5): \(\sqrt{(4-6)^2 + (5-5)^2} = \sqrt{4+0} = 2.0\)

If K=3, neighbors = [(3,4), A], [(5,6), B], [(6,5), B] → Majority class = **B**

---

## 2️⃣ KNN Regression

For **regression**, instead of majority vote, we take **mean** (or weighted mean) of neighbors:

\[
\hat{y} = \frac{1}{K} \sum_{i \in N_K(x)} y_i
\]

**Example:**

| Feature | Target |
|---------|--------|
| 1       | 100    |
| 2       | 150    |
| 3       | 200    |
| 4       | 250    |

New point \(x=2.5\), K=2 → Neighbors: 2 → 150, 3 → 200

\[
\hat{y} = \frac{150 + 200}{2} = 175
\]

---

## 3️⃣ Weighted KNN

Weighted KNN assigns **higher influence to closer neighbors**:

\[
\hat{y} = \frac{\sum_{i \in N_K(x)} w_i y_i}{\sum_{i \in N_K(x)} w_i}
\]

Where weight \(w_i = \frac{1}{d(x, x_i) + \epsilon}\)

**Example:**

Distances: 1.41 (A), 1.41 (B), 2.0 (B)  
Weights: 1/1.41 = 0.71, 1/1.41 = 0.71, 1/2 = 0.5  
Votes: A → 0.71, B → 0.71 + 0.5 = 1.21 → Predicted = **B**

---

## 4️⃣ Feature Scaling

KNN is **distance-based**, so scaling features is crucial.

- StandardScaler: \( z = \frac{x - \mu}{\sigma} \)
- Ensures all features contribute equally

---

## 5️⃣ Advantages

- Simple and intuitive
- Works for classification & regression
- Non-parametric → flexible

---

## 6️⃣ Disadvantages / Limitations

- Slow for large datasets → O(n × d) per prediction
- Sensitive to irrelevant features
- Curse of dimensionality (high-d features reduce effectiveness)
- Sensitive to imbalanced data

---

## 7️⃣ Evaluation Metrics

**Classification:**
- Accuracy
- F1 score
- Precision & Recall
- Confusion Matrix
- ROC & AUC (binary)

**Regression:**
- Mean Squared Error (MSE)
- Mean Absolute Error (MAE)
- R² Score

---

## 8️⃣ Practical Notes

- Always scale features
- Choose K via cross-validation
- Consider Weighted KNN for better accuracy
- Binary vs multi-class affects ROC/AUC calculation

---

## 9️⃣ Alternatives to KNN

- **Classification:** Logistic Regression, SVM, Random Forest, Gradient Boosting  
- **Regression:** Linear Regression, Decision Trees, Random Forest Regressor, Gradient Boosting

---

## 10️⃣ References / Learning Resources

- Pattern Recognition and Machine Learning – Christopher Bishop  
- Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow – Aurélien Géron  
- scikit-learn documentation: [https://scikit-learn.org/stable/modules/neighbors.html](https://scikit-learn.org/stable/modules/neighbors.html)

---

This theoretical README **teaches KNN from scratch**, explains **classification, regression, and weighted variations**, provides **math formulas**, and shows **step-by-step examples**.

