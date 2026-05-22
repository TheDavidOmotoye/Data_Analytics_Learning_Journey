# 📘 DAY 23: Regression Diagnostics — Study Note

---

## 🎯 Lesson Objective

Evaluate regression model quality using:
- residual analysis
- error diagnostics
- RMSE
- outlier detection
- residual plots

---

## 🧠 What are Regression Diagnostics?

Regression Diagnostics are techniques used to evaluate whether a regression model is:
- reliable
- stable
- accurate
- statistically appropriate

Diagnostics help analysts validate prediction quality.

---

## 📌 Core Concepts

| Concept | Meaning |
|---|---|
| Residual | Prediction error |
| Absolute Residual | Magnitude of prediction error |
| Squared Residual | Residual squared for RMSE calculations |
| RMSE | Average prediction error size |
| Outlier | Observation with unusually large error |
| Residual Plot | Visualization of prediction errors |

---

## 📐 Residual Formula

Formula:

Residual = Actual Sales - Predicted Sales

---

## 📐 Absolute Residual Formula

Absolute Residual = |Residual|

Excel Formula:

```excel
=ABS(D2)
```

---

## 📐 Squared Residual Formula

Squared Residual = Residual²

Excel Formula:

```excel
=D2^2
```

---

## 📐 Mean Residual Formula

Mean Residual = Average of all residuals

Excel Formula:

```excel
=AVERAGE(D2:D51)
```

---

## 📐 MSE Formula

MSE = Σ(Residual²) / n

Excel Formula:

```excel
=AVERAGE(F2:F51)
```

---

## 📐 RMSE Formula

RMSE = √MSE

Formula:

RMSE = √(ΣResidual² / n)

Excel Formula:

```excel
=SQRT(F55)
```

---

## 📊 Interpretation Rules

| Metric | Interpretation |
|---|---|
| Mean Residual ≈ 0 | Balanced model |
| Small RMSE | Better prediction accuracy |
| Large Residuals | Possible outliers |
| Random residual scatter | Good model fit |
| Curved residual pattern | Poor linearity |

---

## 📊 Dataset Variables

| Variable | Description |
|---|---|
| Actual_Sales | Real observed sales |
| Predicted_Sales | Forecasted sales |
| Residual | Prediction error |
| Advertising_Spend | Marketing spend |
| Price | Product price |
| Competitor_Price | Competitor pricing |

---

## 💻 Excel Workflow

---

### 🔵 Step 1 — Calculate Residuals

```excel
=Actual_Sales-Predicted_Sales
```

---

### 🔵 Step 2 — Calculate Absolute Residuals

```excel
=ABS(Residual)
```

---

### 🔵 Step 3 — Calculate Squared Residuals

```excel
=Residual^2
```

---

### 🔵 Step 4 — Calculate Mean Residual

```excel
=AVERAGE(Residual_Range)
```

---

### 🔵 Step 5 — Calculate RMSE

1. Average Squared Residuals
2. Apply square root

```excel
=SQRT(AVERAGE(Squared_Residual_Range))
```

---

### 🔵 Step 6 — Create Residual Scatter Plot

X-Axis:
- Predicted_Sales

Y-Axis:
- Residual

Go to:

```text
Insert → Scatter Plot
```

---

### 🔵 Step 7 — Detect Outliers

Rule used:

Potential Outlier if:

Absolute Residual > 2 × Average Error

Excel Formula:

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

## 📌 Interpretation of Results

✅ Model demonstrated acceptable predictive accuracy.

✅ Residuals were relatively balanced around zero.

✅ RMSE indicated moderate forecasting error relative to total sales scale.

⚠ Several observations showed unusually large residuals and were flagged as outliers.

---

## ⚠ Common Analyst Mistakes

❌ Ignoring residual analysis

❌ Assuming high R² guarantees good predictions

❌ Ignoring outliers

❌ Failing to validate prediction stability

❌ Not examining residual plots

---

## 💡 Business Insights

✅ Regression diagnostics improve forecasting reliability.

✅ Outlier detection helps identify unstable predictions.

✅ RMSE provides realistic understanding of forecast accuracy.

✅ Residual analysis validates whether predictive models can support business decisions.

---

## 🏁 Lesson Conclusion

Regression Diagnostics evaluates the reliability and stability of predictive models.

This lesson demonstrated:
- residual analysis
- RMSE evaluation
- outlier detection
- residual plotting
- model validation

These are critical skills for professional predictive analytics and forecasting evaluation.

---

<footer>

**David Omotoye**  
*Advanced Statistics Learning Journey — Day 23*

</footer>
