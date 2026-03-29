# 📘 MLF UNIT — Data Processing, EDA & Regression (Theory Notes)

---

## 🔹 1. Feature Engineering

Transform raw data into better representations to improve model performance.

---

### 🧩 Missing Value Imputation

**Why Missing Values Occur:**

* Sensor failure
* Data entry errors
* Dropped records

**Methods:**

* **Drop (MCAR):** Remove rows when missing data is minimal
* **Mean:** For normally distributed data
* **Median:** For skewed distributions (robust)
* **Mode:** For categorical data
* **Advanced:** KNN, MICE (for complex missing patterns)

---

### ⚖️ Imbalanced Dataset & SMOTE

* Problem: Model becomes biased toward majority class
* SMOTE: Generates synthetic minority samples using nearest neighbors

---

### 🚨 Outlier Handling

**Detection:**

* IQR:

  ```
  [Q1 − 1.5 × IQR, Q3 + 1.5 × IQR]
  ```
* Z-score:

  ```
  ±3σ
  ```

**Treatment:**

* Remove
* Cap (winsorization)
* Transform (log, sqrt)

---

### 🔢 Data Encoding

* **One-Hot Encoding:** Nominal data
* **Label Encoding:** Suitable for tree-based models
* **Ordinal Encoding:** Preserves order
* **Target Encoding:** Based on target variable

---

## 🔹 2. EDA (Exploratory Data Analysis)

Understand dataset before modeling.

**Types:**

* **Statistical:** Mean, median, standard deviation
* **Visual:** Histogram, boxplot

---

## 🔹 3. Dataset-Specific EDA

### 🍷 Red Wine Dataset

* Target: Quality (3–8)
* Focus:

  * Feature correlation
  * Class imbalance

---

### ✈️ Flight Price Dataset

* Target: Price (continuous)

**Feature Engineering Focus:**

* Duration
* Airline
* Datetime extraction

---

## 🔹 4. ML Workflow

```
Raw Data → EDA → Feature Engineering → Encoding → Train/Test Split → Model
```

📌 EDA drives preprocessing decisions.

---

## 🔹 5. Regression

### 📉 Simple Linear Regression

```
y = mx + b
```

---

### 🎯 Cost Function (MSE)

```
(1/n) Σ(Y_pred − Y_actual)^2
```

---

### 🔄 Gradient Descent

```
m = m − α × gradient
```

* α (learning rate) controls step size

---

### 📊 Multiple Linear Regression

```
Y = b + m1X1 + m2X2 + ...
```

---

### 📏 Evaluation Metrics

* **MAE** → Mean Absolute Error
* **MSE** → Mean Squared Error
* **RMSE** → Root Mean Squared Error

---

### ⚠️ Overfitting vs Underfitting

* **Underfitting:** Model too simple → misses patterns
* **Overfitting:** Model memorizes training data → poor generalization

---

### 🔄 Polynomial Regression

```
Y = b + m1X + m2X^2 + ...
```

⚠️ Higher degree increases overfitting risk

---

## ⚡ Quick Revision

* Feature engineering → improves input quality
* SMOTE → handles class imbalance
* IQR/Z-score → detect outliers
* Encoding → categorical → numeric
* EDA → understand before modeling
* Regression → predict continuous output
* Gradient descent → optimize model
* Overfitting → memorize ❌
* Underfitting → too simple ❌

---
