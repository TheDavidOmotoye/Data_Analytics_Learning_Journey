# 📊 DAY 23 — Regression Diagnostics (Completed Project)

---

## ✅ Project Status

## ✔ Completed

This project evaluated regression model quality using residual diagnostics, RMSE analysis, and outlier detection techniques.

---

## 🎯 Project Objective

Assess regression model reliability using:
- residual analysis
- error diagnostics
- residual plots
- RMSE evaluation
- outlier identification

---

## 📂 Dataset Overview

| Variable | Description |
|---|---|
| Actual_Sales | Real observed sales |
| Predicted_Sales | Model forecast |
| Residual | Prediction error |
| Advertising_Spend | Marketing investment |
| Price | Product price |
| Competitor_Price | Competitor pricing |

---

## 🧠 Regression Diagnostics Concept

Regression Diagnostics evaluates:
- prediction quality
- model stability
- forecasting reliability
- residual behavior

---

## 📐 Core Diagnostic Formulas

### Residual Formula

Residual = Actual Sales - Predicted Sales

---

### RMSE Formula

RMSE = √(ΣResidual² / n)

---

### MSE Formula

MSE = Σ(Residual²) / n

---

## 💻 Excel Formulas Used

### Residual Formula

```excel
=Actual_Sales-Predicted_Sales
```

---

### Absolute Residual Formula

```excel
=ABS(D2)
```

---

### Squared Residual Formula

```excel
=D2^2
```

---

### RMSE Formula

```excel
=SQRT(AVERAGE(Squared_Residual_Range))
```

---

### Outlier Detection Formula

```excel
=IF([@[Absolute_Residual]]<=$B$65,"Normal","Outlier")
```

---

## 📊 Final Diagnostic Results

| Metric | Result |
|---|---|
| Mean Residual | 925.32 |
| Max Residual | 11133 |
| Average Error | 3743.8 |
| MSE | 21,403,029.32 |
| RMSE | 4626.341 |

---

## 📊 Residual Plot Findings

✅ Residuals showed relatively random scatter around zero.

✅ No major curvature pattern was observed.

✅ Model assumptions appeared reasonably satisfied.

⚠ Several outlier observations were detected.

---

## 📌 Outlier Observations

| Observation | Residual |
|---|---|
| DIA-037 | -7914 |
| DIA-040 | 11133 |
| DIA-046 | -8388 |
| DIA-049 | 10899 |

---

## 📌 Business Insights

✅ Model demonstrated acceptable predictive accuracy.

✅ RMSE indicated moderate forecasting error relative to sales scale.

✅ Residual diagnostics identified several difficult-to-predict observations.

✅ Additional explanatory variables may further improve forecast reliability.

---

## ⚠ Diagnostic Challenges

- Outlier presence
- Forecast instability
- Missing explanatory variables
- Moderate prediction error

---

## 🏁 Conclusion

This project demonstrated how regression diagnostics helps analysts validate forecasting reliability using:
- residual analysis
- RMSE evaluation
- outlier detection
- residual plots

The analysis strengthened predictive analytics understanding beyond basic regression modeling.

---

<footer>

**David Omotoye**  
*Advanced Statistics Learning Journey — Day 23*

</footer>
