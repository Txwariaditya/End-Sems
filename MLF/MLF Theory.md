# MLF Theory

##  Data Processing and EDA



## 1. Feature Engineering

The process of transforming raw input variables into higher-quality representations to improve model performance.

Missing Value Imputation

Raw datasets frequently contain NaN / null entries due to sensor failures, data entry errors, or dropped records. Strategies:



**Drop**: df.dropna() — valid when missingness is MCAR (Missing Completely At Random) and rows are few

**Mean/Median imputation:** replaces NaN with column statistics — median preferred for skewed distributions

**Mode imputation** used for categorical features

**Advanced:** KNN imputation, MICE (iterative imputer) for MAR (Missing At Random) cases



### Imbalanced Dataset & SMOTE



Class imbalance occurs when target class distribution is skewed (e.g., 95% class 0, 5% class 1). This causes models to be biased toward the majority class, degrading recall on the minority class.



**SMOTE** **(Synthetic Minority Oversampling Technique)**
 generates synthetic feature vectors by interpolating between a minority sample and its k-nearest neighbors in feature space — rather than simply duplicating existing samples (naive oversampling).

**Outlier Handling**
Outliers are data points lying far outside the typical distribution, caused by measurement error or genuine anomalies.

**Detection methods:** IQR method flags values outside [Q1 − 1.5×IQR, Q3 + 1.5×IQR]. Z-score flags values beyond ±3σ. Treatment options: cap/winsorize, transform (log, sqrt), or drop. 



---



## Data Encoding

ML models require numerical input — categorical features must be encoded:

MethodUse CaseNotesOne-Hot Encoding (OHE)Nominal (unordered)Creates binary columns; avoid for high-cardinalityLabel EncodingBinary or tree-based modelsAssigns arbitrary integersOrdinal EncodingOrdered categoriesPreserves rank (Low=1, Med=2, High=3)Target Guided OrdinalSupervised FESorts categories by mean target value



---



## 2. EDA (Exploratory Data Analysis)

Statistical and visual profiling of a dataset prior to modeling to uncover distributions, correlations, and anomalies.



---



## 3. Dataset-specific EDA from your syllabus

Red Wine dataset — target is quality (integer 3–8). EDA focus: correlation of physicochemical features (alcohol, volatile acidity, sulphates) with quality score. Check for class imbalance (very few 3s and 8s).

Flight Price dataset — target is price (continuous). EDA focus: feature engineering on duration, stops, airline (categorical encoding), and departure_time. Key task: handle mixed-type columns and extract datetime features before regression.



---



## 4. ML Workflow context

Preprocessing and EDA sit between raw data collection and model training:

Raw data → EDA → Feature Engineering → Encoding/Scaling → Train/Test Split → Model

Key principle: EDA informs feature engineering decisions — you can't know which encoding or imputation strategy to use without first profiling the data.



## # Simple Linear Regression



## 📐 Regression in Supervised ML

Supervised ML means the model learns from labeled data — you give it inputs and the correct outputs, and it learns the pattern.
Regression is used when the output is a continuous number (e.g., house price, temperature).

---

## 1. Simple Linear Regression

Models the relationship between one input (X) and one output (Y) as a straight line:
Y = mX + b

where m = slope (weight) and b = intercept (bias).

Example: Predicting house price based only on size.

---

## 2. Simple Linear Regression Equations

The best-fit line is found by calculating:
m = Σ(Xi - X̄)(Yi - Ȳ) / Σ(Xi - X̄)²
b = Ȳ - m·X̄

These formulas minimize the error between predicted and actual values.

---

## 3. Cost Function
Measures how wrong your model's predictions are. For regression, the most common is Mean Squared Error (MSE):
Cost = (1/n) Σ(Ypred - Yactual)²

The goal of training is to minimize this cost.

---

## 4. Convergence Algorithms (Gradient Descent)
This is the algorithm used to minimize the cost function iteratively:
Start with random weights
Compute the gradient (slope of cost)
Update weights: m = m - α · (∂Cost/∂m)
Repeat until cost stops decreasing

α (alpha) = learning rate — controls step size. Too high → overshoots. Too low → very slow.

---

## 5. Multiple Linear Regression
Same idea, but with multiple input features (X1, X2, X3...):
Y = b + m1X1 + m2X2 + ... + mnXn
Example: Predicting house price using size, location, AND number of rooms.

---

## 6. Performance Metrics
MetricFormulaMeaningMAE(1/n)Σ|Ypred - Yactual|Average absolute errorMSE(1/n)Σ(Ypred - Yactual)²Penalizes large errors moreRMSE√MSESame unit as output, easier to interpret
Lower values = better model.

---

## 7. Overfitting & Underfitting
Problem Meaning FixUnder fitting Model too simple, misses patternsUse more features / complex modelOverfittingModel memorizes training data, fails on new dataRegularization, more dataGood fitGeneralizes well to unseen data✅ Goal

---

## 8. Polynomial Regression
When the relationship between X and Y is curved, not linear:

Y = b + m1X + m2X² + m3X³ + ...
Example: Predicting growth rate that accelerates over time.

⚠️ Higher degree polynomials can easily overfit.

