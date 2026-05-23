# 📊 DAY 25 — Moving Averages & Forecasting Intro

## 📌 Project Overview

This project focused on using moving averages to smooth revenue fluctuations and generate simple short-term business forecasts.

The analysis introduced foundational forecasting concepts commonly used in:
- business intelligence,
- financial analytics,
- operational planning,
- and predictive analytics.

---

## 🎯 Objectives

- Analyze weekly revenue trends
- Apply moving averages for smoothing
- Build simple forecasting models
- Evaluate forecast accuracy
- Interpret forecasting volatility
- Visualize trend behavior

---

## 📂 Dataset Features

| Column | Description |
|---|---|
| Week | Weekly observation period |
| Weekly_Revenue | Revenue generated weekly |
| Weekly_Orders | Total weekly orders |
| 3_Week_Moving_Avg | 3-week smoothed revenue |
| 4_Week_Moving_Avg | 4-week smoothed revenue |
| Forecast_Next_Week | Predicted future revenue |
| Actual_vs_Forecast | Forecast error |

---

## 📐 Key Formulas

---

### 📌 3-Week Moving Average

### Formula

```text
3-Week Moving Average = (X₁ + X₂ + X₃) / 3
```

### Excel

```excel
=AVERAGE(B2:B4)
```

---

## 📌 4-Week Moving Average

### Formula

```text
4-Week Moving Average = (X₁ + X₂ + X₃ + X₄) / 4
```

### Excel

```excel
=AVERAGE(B2:B5)
```

---

## 📌 Forecast Formula

### Formula

```text
Forecast(t+1) = Moving Average(t)
```

### Excel

```excel
=D4
```

---

## 📌 Forecast Error Formula

### Formula

```text
Forecast Error = Actual Value − Forecast Value
```

### Excel

```excel
=B5-F5
```

---

## 📊 Visualizations Created

### ✅ Weekly Revenue Trend
- Trendline added
- Growth direction analyzed
- R² interpretation performed

---

### ✅ Revenue vs Moving Average Forecast
- Compared actual revenue against smoothed trend estimates
- Evaluated responsiveness of 3-week vs 4-week averages

---

### ✅ Forecast Error Analysis
- Positive vs negative deviations analyzed
- Forecasting stability evaluated

---

## 📈 Key Findings

- Revenue displayed a strong upward growth trend.
- Moving averages effectively smoothed short-term fluctuations.
- Forecast errors remained moderate for most weeks.
- The forecasting model demonstrated reasonable short-term reliability.
- The 4-week moving average produced smoother trend estimates than the 3-week model.

---

## 📊 Statistical Interpretation

### Trendline Equation

```text
y = 665.07x + 24807
```

Meaning:
- revenue increased by approximately $665 weekly.

---

### R² Value

```text
R² = 0.7985
```
Meaning:
- approximately 79.85% of revenue variation is explained by the overall trend.

---

## 🛠️ Tools Used

- Microsoft Excel
- Line Charts
- Column Charts
- Trendlines
- Moving Average Calculations
- Forecast Error Analysis

---

## 📚 Skills Practiced

- Time Series Analysis
- Forecasting
- Trend Smoothing
- Moving Averages
- Forecast Evaluation
- Data Visualization
- Business Interpretation

---

## ✅ Project Status

✔️ Completed

---

---
📚 Advanced Statistics — Week 5  
📅 Day 25 Completed  
👨🏽‍💻 Built by David Omotoye
