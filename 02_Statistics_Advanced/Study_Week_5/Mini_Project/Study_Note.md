# 📘 Advanced Statistical Analysis — Complete Study Notes

## 📊 Project Overview

This project applied advanced statistical analysis techniques to evaluate operational business performance, customer activity, forecasting behavior, and revenue trends using a 10-year business dataset (2016–2025).

---

## 📌 Statistical Areas Covered

- Descriptive Statistics
- Variability Analysis
- Hypothesis Testing (t-Test)
- ANOVA
- Chi-Square Testing
- Correlation Analysis
- Regression Analysis
- Time Series Analysis
- Moving Averages
- Seasonal Analysis
- Trend Analysis

---

## 📊 DATASET STRUCTURE

### Core Variables

| Variable | Description |
|---|---|
| Employee_ID | Employee identifier |
| Department | Operational department |
| Region | Business location |
| Gender | Employee gender |
| Training_Group | Experimental grouping |
| Month_No | Numeric month identifier |
| Month_Flag | Month abbreviation |
| Year | Operational year |
| Month_Year | Combined month-year field |
| Marketing_Spend | Marketing investment |
| Website_Traffic | Website visitors |
| Sales_Calls | Sales outreach |
| Sales_Revenue | Revenue generated |
| Customer_Orders | Number of customer orders |
| Employee_Satisfaction | Employee rating |
| Attrition | Employee retention status |
| Project_Status | Project completion status |

---

## 📊 NEW COLUMNS CREATED

---

## 📌 Month_Year Column

### Purpose
Convert Month and Year into proper chronological date format for time-series analysis.

---

### Excel Formula

Assuming:
- Year = H2
- Month_No = G2

```excel
=TEXT(DATE(H2,G2,1),"mmm-yyyy")
```

---

## 📌 Quarter Column

### Purpose
Categorize months into quarters for seasonal analysis.

---

### Excel Formula

Assuming:
- Month_Year = J2

```excel
="Q"&ROUNDUP(MONTH(DATEVALUE("1-"&J2))/3,0)
```

---

## 📌 3-Month Moving Average

### Purpose
Smooth short-term revenue fluctuations.

---

### Mathematical Formula

```text
MA₃ = (Xt + Xt-1 + Xt-2) / 3
```
---

## Excel Formula

Assuming:
- Sales_Revenue = N column

First valid formula:

```excel
=AVERAGE(N2:N4)
```

Drag downward.

---

# 📌 4-Month Moving Average

## Purpose
Reveal smoother long-term revenue trend.

---

## Mathematical Formula

```text
MA₄ = (Xt + Xt-1 + Xt-2 + Xt-3) / 4
```
---

## Excel Formula

First valid formula:

```excel
=AVERAGE(N2:N5)
```

Drag downward.

---

# 📌 Revenue Growth Rate

## Purpose
Measure percentage change in revenue over time.

---

## Mathematical Formula

```text
Growth Rate = ((Current - Previous) / Previous) × 100
```

---

## Excel Formula

```excel
=(N3-N2)/N2
```

Format as percentage.

---

# 📌 Growth Performance Flag

## Purpose
Categorize revenue growth behavior.

---

## Excel Formula

```excel
=IF(I2>0.15,"High Growth",
IF(I2>0.05,"Normal Growth",
IF(I2<-0.10,"Severe Decline",
IF(I2<0,"Revenue Decline","Stable"))))
```

---

# 📌 Forecast Error Column

## Purpose
Measure forecasting accuracy.

---

## Mathematical Formula

:contentReference[oaicite:3]{index=3}

---

## Excel Formula

```excel
=Actual_Forecast-Revenue_Forecast
```

Example:

```excel
=N4-O4
```

---

## 📊 DESCRIPTIVE STATISTICS

---

## 📌 Mean

### Formula

```text
Mean = ΣX / n
```

---

### Excel Formula

```excel
=AVERAGE(range)
```

---

# 📌 Median

## Excel Formula

```excel
=MEDIAN(range)
```

---

## 📌 Minimum

### Excel Formula

```excel
=MIN(range)
```

---

## 📌 Maximum

### Excel Formula

```excel
=MAX(range)
```

---

## 📌 Range

### Formula

```text
Range = Maximum - Minimum
```

---

### Excel Formula

```excel
=MAX(range)-MIN(range)
```

---

## 📌 Standard Deviation

### Formula

```text
σ = √[Σ(x-μ)² / n]
```

---

## Excel Formula

```excel
=STDEV.S(range)
```

---

# 📌 Variance

## Formula

```text
Variance = σ²
```

---

## Excel Formula

```excel
=VAR.S(range)
```

---

## 📊 HYPOTHESIS TESTING (t-Test)

### Purpose
Determine whether significant differences exist between two groups.

---

## 📌 Hypotheses

### Null Hypothesis (H₀)

```text
There is no significant difference between the two groups.
```

---

### Alternative Hypothesis (H₁)

```text
There is a significant difference between the two groups.
```

---

## 📌 Decision Rule

| Condition | Decision |
|---|---|
| p-value < 0.05 | Reject H₀ |
| p-value > 0.05 | Fail to Reject H₀ |

---

## 📊 ANOVA

### Purpose
Compare means across multiple groups.

---

## 📌 Hypotheses

### Null Hypothesis (H₀)

```text
All group means are equal.
```

---

### Alternative Hypothesis (H₁)

```text
At least one group mean differs.
```

---

## 📌 Decision Rule

| Condition | Decision |
|---|---|
| p-value < 0.05 | Reject H₀ |
| p-value > 0.05 | Fail to Reject H₀ |

---

## 📊 CHI-SQUARE TEST

### Purpose
Determine whether categorical variables are independent.

---

### 📌 Expected Frequency Formula

```text
Expected Frequency = (Row Total × Column Total) ÷ Grand Total
```

---

### 📌 Chi-Square Component Formula

```text
Chi-Square Component = ((Observed - Expected)²) ÷ Expected
```

---

## 📊 CORRELATION ANALYSIS

### Purpose
Measure relationship strength between variables.

---

### 📌 Correlation Formula

```text
r = Σ[(X - X̄)(Y - Ȳ)] ÷ √[Σ(X - X̄)² . Σ(Y - Ȳ)²]
```

OR

```text
r = Cov(X,Y) ÷ (σx × σy)
```

---

### Excel Formula

```excel
=CORREL(array1,array2)
```

---

## 📊 REGRESSION ANALYSIS

### Purpose
Predict dependent variable using independent variables.

---

## 📌 Regression Equation

```text
Y = a + b₁X₁ + b₂X₂ + b₃X₃
```

---

## 📌 Interpretation

| Metric | Meaning |
|---|---|
| R² | Model explanatory power |
| p-value | Variable significance |
| Coefficient | Variable impact size |

---

## 📊 TIME SERIES ANALYSIS

### Purpose
Analyze business behavior across time.

---

### 📌 Time-Series Components

| Component | Meaning |
|---|---|
| Trend | Long-term movement |
| Seasonality | Recurring patterns |
| Cyclical Movement | Long business cycles |
| Noise | Random fluctuations |

---

## 📊 SEASONAL ANALYSIS

### Purpose
Identify quarterly operational behavior.

---

### 📌 Pivot Structure

| Section | Variable |
|---|---|
| Rows | Quarter |
| Values | Average Revenue |

---

## 📊 YEAR-OVER-YEAR TREND ANALYSIS

### Purpose
Evaluate long-term operational growth.

---

### 📌 Pivot Structure

| Section | Variable |
|---|---|
| Rows | Year |
| Values | Average Revenue |

---

## 📊 KEY LEARNING OUTCOMES

- Statistical interpretation
- Forecasting analysis
- Time-series structuring
- Business intelligence reporting
- Regression interpretation
- Correlation analysis
- Pivot table analysis
- Analytical storytelling
- Trend analysis
- Seasonal decomposition

---

## 📌 FINAL REFLECTION

This mini project transformed theoretical statistical concepts into practical analytical experience using real-world business analysis workflows within Excel.

The project significantly improved:
- business interpretation ability,
- forecasting logic,
- Excel troubleshooting skills,
- and confidence in analytical storytelling.

---
Generated as part of Advanced Statistical Analysis Mini Project
