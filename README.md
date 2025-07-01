# 🧠 Task 6 – K-Nearest Neighbors (KNN) Classification

In this task, we applied the **K-Nearest Neighbors (KNN)** algorithm to the **Iris dataset** for multi-class classification.  
We explored different values of K, normalized the features, evaluated the model, and visualized decision boundaries.

---

## 📦 Dataset Used

**Dataset**: [Iris Dataset](https://archive.ics.uci.edu/ml/datasets/iris)  
**Target Variable**: `species` → (setosa, versicolor, virginica)  
**Features**:
- sepal length (cm)
- sepal width (cm)
- petal length (cm)
- petal width (cm)

---

## ✅ Steps Performed

### 🔹 1. Data Preprocessing
- Loaded the dataset from `iris.csv`
- Normalized features using `StandardScaler`
- Split into training and testing sets (70/30)

### 🔹 2. Model Training
- Trained KNN classifier using different K values (K = 1 to 10)
- Chose best `K` based on test accuracy

### 🔹 3. Evaluation
- Accuracy score
- Confusion matrix
- Classification report (precision, recall, f1-score)

### 🔹 4. Visualization
- Accuracy vs. K plot
- Decision boundary plotted using the first two features (2D)

---

## 📊 Results Summary

| K Value | Accuracy |
|---------|----------|
| 3       | 1.00     |
| 5       | 0.97     |
| 7       | 0.97     |

✅ Best accuracy: **100% with K = 3**

---

## 🌈 Visualization Sample

- Accuracy vs K (line plot)
- Decision boundary with two features  
  *(Only works with numeric labels; used `LabelEncoder` for plotting)*

---

## ❓ Interview Q&A

### Q1: What is KNN?
KNN is an **instance-based, non-parametric** algorithm that classifies a sample based on the majority class among its K-nearest neighbors using distance metrics (e.g., Euclidean distance).

### Q2: Why normalize data before KNN?
Because KNN relies on **distance**, and features with larger ranges can dominate. Normalization brings all features to the same scale.

### Q3: How to choose K value?
Try multiple values and evaluate accuracy using **validation data** or **cross-validation**. Use an odd number to avoid ties in binary classification.

### Q4: Time complexity of KNN?
- Training: O(1) – no training
- Prediction: O(n × d), where n = number of samples, d = number of features

### Q5: Pros & Cons of KNN?

| Pros                                | Cons                             |
|-------------------------------------|----------------------------------|
| Simple and intuitive                | Slow for large datasets          |
| No training needed                  | Sensitive to noise/outliers      |
| Works well with small datasets      | Needs good distance metric       |

---

## 📁 Folder Contents

