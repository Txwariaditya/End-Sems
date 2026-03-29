# 📐 UNIT 3 — SIMPLE LINEAR REGRESSION (SLR)

---

## 🔹 1. Introduction to Regression

Regression is a supervised learning technique used to predict **continuous values**.

**Examples:**

* House price prediction
* Temperature forecasting
* Sales prediction

---

## 🔹 2. Simple Linear Regression (SLR)

SLR models the relationship between:

* One independent variable (X)
* One dependent variable (Y)

### 📌 Equation

```
y = mx + b
```

Where:

* m → slope (rate of change)
* b → intercept (value of y when x = 0)

---

## 🔹 3. Intuition

* Data points are scattered on a graph
* We draw a **best-fit straight line**
* Goal: minimize prediction error

---

## 🔹 4. Error Concept

```
Error = Actual - Predicted
```

To avoid cancellation of errors, we square them.

### 📌 Mean Squared Error (MSE)

```
MSE = (1/n) Σ(y_pred - y_actual)^2
```

**Why MSE?**

* Avoids negative cancellation
* Penalizes large errors more

---

## 🔹 5. Objective

Find values of **m and b** such that MSE is minimized.

---

## 🔹 6. Methods to Find Best Fit Line

### ✅ Analytical Method (Closed Form)

```
m = Σ(Xi - X̄)(Yi - Ȳ) / Σ(Xi - X̄)^2
b = Ȳ - mX̄
```

✔ Exact solution
❌ Not scalable for large datasets

---

### ✅ Gradient Descent (Iterative)

Steps:

1. Initialize m, b randomly
2. Compute error
3. Update parameters

```
m = m - α * (∂Cost/∂m)
b = b - α * (∂Cost/∂b)
```

4. Repeat until convergence

---

## 🔹 7. Learning Rate (α)

| Case     | Result             |
| -------- | ------------------ |
| Too High | Overshoots ❌       |
| Too Low  | Slow convergence ❌ |
| Optimal  | Fast convergence ✔ |

---

## 🔹 8. Assumptions of SLR

* Linear relationship between X and Y
* Errors are normally distributed
* Constant variance (homoscedasticity)
* No strong outliers
* Observations are independent

---

## 🔹 9. Evaluation Metrics

| Metric | Formula                      | Meaning                |   |           |
| ------ | ---------------------------- | ---------------------- | - | --------- |
| MAE    | (1/n) Σ                      | y_pred - y_actual      |   | Avg error |
| MSE    | (1/n) Σ(y_pred - y_actual)^2 | Penalizes large errors |   |           |
| RMSE   | √MSE                         | Same unit as output    |   |           |

✔ Lower value = better model

---

## 🔹 10. Overfitting vs Underfitting

| Type         | Meaning              |
| ------------ | -------------------- |
| Underfitting | Model too simple     |
| Overfitting  | Model memorizes data |
| Good Fit     | Generalizes well     |

---

## 🔹 11. Limitations of SLR

* Only works for linear relationships
* Sensitive to outliers
* Cannot capture complex patterns
* Uses only one feature

---

## 🔹 12. Extension → Multiple Linear Regression

```
Y = b + m1X1 + m2X2 + ... + mnXn
```

✔ Uses multiple features

---

## 🔹 13. Real-World Example

**House Price Prediction**

* X → Size of house
* Y → Price

Model learns:

* Larger size → higher price

---

## 🔹 14. Common Mistakes

* Using SLR for nonlinear data
* Ignoring outliers
* Wrong learning rate
* Misinterpreting slope

---

## 🔹 15. Quick Revision

* SLR → one input, one output
* Equation → y = mx + b
* Goal → minimize MSE
* Gradient descent → optimization
* Metrics → MAE, MSE, RMSE
* Limitation → only linear relationships

---
