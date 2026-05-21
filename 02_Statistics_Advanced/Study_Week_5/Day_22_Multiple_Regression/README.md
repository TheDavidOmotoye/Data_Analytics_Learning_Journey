# 📊 DAY 22 — Multiple Regression (Completed Project)

---

## ✅ Project Status

### ✔ Completed

This project successfully applied Multiple Regression Analysis to predict employee Performance Score using multiple explanatory variables.

---

## 🎯 Project Objective

Predict employee performance using:
- Age
- Years_Experience
- Training_Hours
- Monthly_Income

---

## 📂 Dataset Description

| Variable | Description |
|---|---|
| Age | Employee age |
| Years_Experience | Work experience |
| Training_Hours | Training completed |
| Monthly_Income | Employee salary |
| Performance_Score | Employee performance rating |

---

## 🧠 Multiple Regression Concept

Multiple Regression predicts one outcome using several predictors simultaneously.

---

## 📐 Regression Formula

y = a + b₁x₁ + b₂x₂ + b₃x₃ + ... + bₙxₙ

---

## 📈 Final Regression Equation

Performance Score = 74.73 - 0.676(Age) + 1.864(Experience) + 0.570(Training Hours) - 0.0014(Income)

---

## 📊 Regression Results

| Metric | Result |
|---|---|
| Multiple R | 0.8233 |
| R Square | 0.6778 |
| Adjusted R Square | 0.6539 |
| F-statistic | 28.40 |
| Significance F | 1.01E-12 |

---

## 📌 Statistical Interpretation

✅ The regression model is statistically significant.

✅ Approximately 67.8% of performance variation is explained by the predictors.

---

## 📊 Variable Insights

| Variable | Result |
|---|---|
| Years_Experience | Significant positive predictor |
| Training_Hours | Strongest significant predictor |
| Age | Not significant |
| Monthly_Income | Not significant |

---

## 📌 Business Insights

✅ Employee training strongly improves performance.

✅ Experience significantly impacts productivity.

❌ Higher salaries alone do not guarantee stronger performance.

❌ Age is not a reliable predictor of productivity.

---

## 💻 Excel Regression Setup

```text
Data → Data Analysis → Regression
```

---

## 📌 Regression Inputs

| Setting | Value |
|---|---|
| Input Y Range | Performance_Score |
| Input X Range | Numeric predictors |
| Labels | Checked |

---

## 📊 Excel Formulas Used

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

## ⚠ Common Regression Challenges

- Multicollinearity
- Overfitting
- Misinterpreting p-values
- Including text variables improperly

---

## 🏁 Conclusion

This project demonstrated how Multiple Regression helps organizations identify the strongest drivers of employee performance.

The analysis highlighted:
- training effectiveness
- importance of experience
- predictive workforce analytics
- business-focused statistical interpretation

---

<footer>

**David Omotoye**  
*Statistics Learning Journey — Day 22*

</footer>
