# 📘 DAY 22: Multiple Regression — Study Note

---

## 🎯 Lesson Objective

Use Multiple Regression to predict employee Performance Score using multiple explanatory variables.

---

## 🧠 What is Multiple Regression?

Multiple Regression predicts one outcome variable using several predictor variables simultaneously.

---

## 📐 Multiple Regression Formula

Actual Formula:

y = a + b₁x₁ + b₂x₂ + b₃x₃ + ... + bₙxₙ

Where:

| Symbol | Meaning |
|---|---|
| y | Predicted outcome |
| a | Intercept |
| b | Coefficients |
| x | Predictor variables |

---

## 📊 Variables Used

| Variable | Role |
|---|---|
| Performance_Score | Dependent Variable |
| Age | Predictor |
| Years_Experience | Predictor |
| Training_Hours | Predictor |
| Monthly_Income | Predictor |

---

## 📈 Final Regression Equation

Performance Score = 74.73 - 0.676(Age) + 1.864(Experience) + 0.570(Training Hours) - 0.0014(Income)

---

## 📊 Regression Statistics

| Metric | Result |
|---|---|
| Multiple R | 0.8233 |
| R Square | 0.6778 |
| Adjusted R Square | 0.6539 |
| F-statistic | 28.40 |
| Significance F | 1.01E-12 |

---

## 📌 R² Formula

R² = SSR / SST

---

## 📌 F-Statistic Formula

F = MS Regression / MS Residual

---

## 📊 Variable Interpretation

---

### 🔵 Age

Coefficient = -0.676

p-value = 0.160

❌ Not statistically significant.

---

### 🔵 Years_Experience

Coefficient = 1.864

p-value = 0.00034

✅ Significant positive predictor.

---

### 🔵 Training_Hours

Coefficient = 0.570

p-value = 4.21E-09

✅ Strongest significant predictor.

---

### 🔵 Monthly_Income

Coefficient = -0.0014

p-value = 0.223

❌ Not statistically significant.

---

## 💻 Excel Regression Setup

Go to:

```text
Data → Data Analysis → Regression
```

---

## 📌 Input Settings

| Setting | Range |
|---|---|
| Input Y Range | Performance_Score |
| Input X Range | Numeric predictor variables |
| Labels | Checked |
| Output Range | Empty cells |

---

## 📊 Excel Functions Used

### Correlation

```excel
=CORREL(B5:B64,G5:G64)
```

---

### Predicted Performance

```excel
=74.73-(0.676*B5)+(1.864*C5)+(0.570*E5)-(0.0014*F5)
```

---

### Residual Formula

```excel
=Actual_Performance-Predicted_Performance
```

---

## 📊 Interpretation Rules

| Metric | Meaning |
|---|---|
| p-value < 0.05 | Significant |
| p-value > 0.05 | Not significant |
| Higher R² | Stronger model |

---

## ⚠ Common Analyst Mistakes

❌ Including categorical variables incorrectly

❌ Ignoring Adjusted R²

❌ Misinterpreting p-values

❌ Overfitting models

❌ Ignoring multicollinearity

---

## 💡 Key Findings

✅ Experience significantly improves performance.

✅ Training hours strongly improve productivity.

❌ Income alone does not predict performance.

❌ Age is not a reliable performance predictor.

---

## 🏁 Lesson Conclusion

Multiple Regression improves predictive analytics by combining several explanatory variables into one statistical model.

This lesson demonstrated how analysts evaluate:
- variable importance
- business drivers
- predictive power
- workforce performance factors

---

<footer>

**David Omotoye**  
*Statistics Learning Journey — Day 22*

</footer>
