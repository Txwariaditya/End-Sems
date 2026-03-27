# MLF UNIT – Data Processing, EDA & Regression (Clean Notes)

## 1. FEATURE ENGINEERING
Transform raw data → better representation → improve model performance

### Missing Value Imputation
**Why Missing Values Occur**
- Sensor failure  
- Data entry errors  
- Dropped records  

**Methods**
- Drop (MCAR)
- Mean (normal distribution)
- Median (skewed, robust)
- Mode (categorical)
- KNN / MICE (advanced)

---

### Imbalanced Dataset & SMOTE
- Problem: biased model due to skewed classes  
- SMOTE: creates synthetic samples using nearest neighbors  

---

### Outlier Handling
**Detection**
- IQR: [Q1 − 1.5×IQR, Q3 + 1.5×IQR]
- Z-score: ±3σ  

**Treatment**
- Remove
- Cap
- Transform  

---

### Data Encoding
- One-Hot (nominal)
- Label Encoding (tree models)
- Ordinal Encoding (ordered)
- Target Encoding (supervised)

---

## 2. EDA
Understand dataset before modeling

- Statistical: mean, median, std  
- Visual: histogram, boxplot  

---

## 3. DATASET-SPECIFIC EDA

### Red Wine Dataset
- Target: Quality (3–8)
- Focus: correlation, imbalance  

### Flight Price Dataset
- Target: Price  
- Feature engineering: duration, airline, datetime  

---

## 4. ML WORKFLOW
Raw → EDA → Feature Engineering → Encoding → Split → Model

---

## 5. REGRESSION

### Simple Linear Regression
y = mx + b  

### Cost Function (MSE)
(1/n) Σ(Ypred - Yactual)^2  

### Gradient Descent
m = m - α * gradient  

### Multiple Regression
Y = b + m1X1 + m2X2 + ...  

---

### Metrics
- MAE
- MSE
- RMSE  

---

### Overfitting vs Underfitting
- Underfitting: too simple  
- Overfitting: memorization  

---

### Polynomial Regression
Y = b + m1X + m2X^2 + ...  
