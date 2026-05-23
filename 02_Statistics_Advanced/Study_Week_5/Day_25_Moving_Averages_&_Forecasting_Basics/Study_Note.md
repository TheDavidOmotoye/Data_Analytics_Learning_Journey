# 📘 DAY 25 — Moving Averages & Forecasting Intro

## 📌 Objective
Use rolling averages to smooth trends and make simple forecasts.

---

## 📖 What is a Moving Average?

A Moving Average smooths short-term fluctuations in data to help analysts identify the true trend over time.

It reduces noise and improves forecasting interpretation.

---

## 📖 What is Forecasting?

Forecasting is the process of predicting future values using historical data.

Businesses use forecasting to estimate:
- future revenue,
- customer demand,
- inventory needs,
- staffing,
- and operational planning.

---

## 📊 Core Concepts

| Concept | Meaning |
|---|---|
| Moving Average | Average of recent observations |
| Forecast | Predicted future value |
| Trend | Long-term direction of data |
| Volatility | Degree of fluctuation |
| Forecast Error | Difference between actual and forecast |
| Smoothing | Reduction of short-term noise |

---

## 📐 Formula Breakdown

---

## 📌 3-Week Moving Average Formula

### Mathematical Formula

```text
3-Week Moving Average = (X₁ + X₂ + X₃) / 3
```

### Excel Formula

```excel
=AVERAGE(B2:B4)
```

---

## 📌 4-Week Moving Average Formula

### Mathematical Formula

```text
4-Week Moving Average = (X₁ + X₂ + X₃ + X₄) / 4
```

### Excel Formula

```excel
=AVERAGE(B2:B5)
```

---

## 📌 Forecast Formula

### Mathematical Formula

```text
Forecast(t+1) = Moving Average(t)
```

### Excel Formula

```excel
=D4
```

---

## 📌 Forecast Error Formula

### Mathematical Formula

```text
Forecast Error = Actual Value − Forecast Value
```

### Excel Formula

```excel
=B5-F5
```

---

## 📊 Interpretation Guide

| Result | Meaning |
|---|---|
| Positive Error | Actual > Forecast |
| Negative Error | Forecast > Actual |
| Small Error | Accurate Forecast |
| Large Error | Forecasting Weakness |

---

## 📈 Chart Analysis

### 1️⃣ Weekly Revenue Trend
Shows overall business growth direction.

---

### 2️⃣ Revenue vs Moving Average Forecast
Compares actual revenue against smoothed trends.

---

### 3️⃣ Forecast Error Analysis
Visualizes:
- overforecasting,
- underforecasting,
- volatility,
- and forecast accuracy.

---

## 📊 Forecasting Insights

### ✅ 3-Week Moving Average
- reacts faster,
- more sensitive to short-term changes.

---

## ✅ 4-Week Moving Average
- smoother,
- less volatile,
- better for long-term trend observation.

---

## 📌 Business Applications

Moving averages are used for:
- sales forecasting,
- inventory planning,
- staffing estimation,
- financial forecasting,
- operational planning,
- demand prediction,
- traffic forecasting.

---

## ⚠️ Common Analyst Mistakes

❌ Using unsorted time periods

❌ Ignoring seasonality

❌ Misinterpreting short-term spikes

❌ Forecasting with missing data

❌ Using moving averages without error analysis

❌ Confusing smoothing with prediction accuracy

---

## 📌 Final Lesson Summary

This lesson introduced:
- forecasting foundations,
- moving average smoothing,
- trend analysis,
- forecasting evaluation,
- and predictive analytics basics.

The project demonstrated how analysts use historical business performance to estimate future operational outcomes.

---

---
📚 Advanced Statistics — Week 5  
📅 Day 25 Completed  
👨🏽‍💻 Built by David Omotoye
