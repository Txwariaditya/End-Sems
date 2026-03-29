# 📐 UNIT 3 — SIMPLE LINEAR REGRESSION (SLR)

---

## 🔹 1. What is Regression?

Regression is a supervised learning technique used to predict **continuous values**.

**Examples:**

* House price prediction
* Temperature forecasting
* Sales prediction

---

## 🔹 2. Simple Linear Regression (SLR)

SLR models the relationship between **one independent variable (X)** and **one dependent variable (Y)**.

### 📌 Equation:

```math
Y = mX + b
```

Where:

* **m** → slope (weight)
* **b** → intercept (bias)

---

## 🔹 3. Intuition

* We try to fit a **best straight line** through data points
* This line minimizes prediction error

📌 Goal: Find optimal **m and b**

---

## 🔹 4. Best Fit Line (Mathematical Formulas)

```math
m = Σ(Xi - X̄)(Yi - Ȳ) / Σ(Xi - X̄)^2
```

```math
b = Ȳ - mX̄
```

✔ These formulas minimize total error

---

## 🔹 5. Cost Function (Error Measurement)

### Mean Squared Error (MSE)

```math
Cost = (1/n) Σ(Y_pred - Y_actual)^2
```

📌 Purpose:

* Measures how wrong predictions are
* Higher error → worse model

---

## 🔹 6. Gradient Descent (Optimization)

Used to minimize cost function.

### 🔁 Steps:

1. Initialize m, b randomly
2. Calculate error
3. Update parameters:

```math
m = m - α * ∂Cost/∂m
```

```math
b = b - α * ∂Cost/∂b
```

4. Repeat until convergence

---

### 📌 Learning Rate (α)

* Too high → overshooting ❌
* Too low → slow convergence ❌
* Optimal → fast & stable ✔

---

## 🔹 7. Assumptions of SLR

* Linear relationship between X and Y
* No/low multicollinearity
* Homoscedasticity (constant variance)
* No significant outliers
* Errors are normally distributed

---

## 🔹 8. Evaluation Metrics

| Metric | Formula                      | Meaning                |   |                    |
| ------ | ---------------------------- | ---------------------- | - | ------------------ |
| MAE    | (1/n) Σ                      | Y_pred - Y_actual      |   | Avg absolute error |
| MSE    | (1/n) Σ(Y_pred - Y_actual)^2 | Penalizes large errors |   |                    |
| RMSE   | √MSE                         | Same unit as output    |   |                    |

✔ Lower values = better model

---

## 🔹 9. Overfitting vs Underfitting

| Type         | Meaning                 | Problem             |
| ------------ | ----------------------- | ------------------- |
| Underfitting | Model too simple        | Misses patterns     |
| Overfitting  | Memorizes training data | Poor generalization |
| Good Fit     | Balanced                | Ideal               |

---

## 🔹 10. Limitations of SLR

* Works only for **linear relationships**
* Sensitive to **outliers**
* Cannot capture complex patterns

---

## 🔹 11. Real-World Example

**House Price Prediction**

* X → Size (sq ft)
* Y → Price

Model learns:

* Bigger size → higher price

---

## 🔹 12. Quick Revision

* SLR → one input, one output
* Equation → Y = mX + b
* Goal → minimize error (MSE)
* Gradient descent → optimization
* Metrics → MAE, MSE, RMSE
* Limitation → only linear relationships

---
