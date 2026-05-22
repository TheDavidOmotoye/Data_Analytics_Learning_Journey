# 📈 DAY 24 — Time Series Basics

## 📌 Project Overview

This project focused on analyzing monthly business performance using Time Series Analysis techniques.

The analysis explored:
- trend,
- seasonality,
- moving averages,
- growth rates,
- correlation analysis,
- and business forecasting foundations.

---

## 📊 Dataset Features

| Column | Description |
|---|---|
| Month | Monthly observation period |
| Revenue | Monthly business revenue |
| Orders | Total customer orders |
| Average_Order_Value | Average order value |
| Ad_Spend | Advertising expenditure |
| Website_Traffic | Website visitor count |
| Season | Quarterly seasonal category |

---

## 📘 Concepts Covered

✅ Time Series Fundamentals

✅ Trend Analysis

✅ Seasonality Analysis

✅ Moving Averages

✅ Revenue Growth Rate

✅ Growth Performance Flagging

✅ Correlation Analysis

✅ Scatter Plot Visualization

✅ Trendline Analysis

✅ Seasonal Pivot Analysis

---

## 📐 Key Formulas Used

---

## 📈 3-Month Moving Average

3-Month Moving Average Formula

```text
Moving Average = (Month1 + Month2 + Month3) / 3
```

### Excel Formula

```excel
=AVERAGE(B2:B4)
```

---

### 📈 Revenue Growth Rate

Revenue Growth Rate Formula

```text
Growth Rate = ((Current Revenue - Previous Revenue) / Previous Revenue) × 100
```

### Excel Formula

```excel
=(B3-B2)/B2
```

---

### 📈 Correlation Formula

Correlation Formula

```text
r = Σ[(x - x̄)(y - ȳ)] / √[Σ(x - x̄)² × Σ(y - ȳ)²]
```

### Excel Formula

```excel
=CORREL(array1,array2)
```

---

## 📊 Growth Performance Flag Formula

```excel
=IF(I7<-10%,"Severe Decline",IF(I7<0,"Revenue Decline",IF(I7>15%,"High Growth","Normal Growth")))
```

---

## 📊 Analysis Performed

### ✅ Revenue Trend Analysis

- Created Revenue Trend chart
- Added Trendline
- Interpreted R² value

---

### ✅ Moving Average Analysis

- Calculated 3-Month Moving Average
- Smoothed short-term fluctuations
- Identified long-term growth direction

---

### ✅ Revenue Growth Analysis

- Computed monthly growth rates
- Flagged business performance periods

---

### ✅ Seasonal Analysis

Created Pivot Table to evaluate:
- Average Revenue by Quarter
- Average Orders by Quarter

---

### ✅ Correlation Analysis

Measured relationships between:
- Advertising Spend vs Revenue
- Website Traffic vs Orders

---

## 📈 Key Findings

| Analysis | Insight |
|---|---|
| Revenue Trend | Strong long-term growth observed |
| Q4 Performance | Highest average revenue recorded |
| Ad Spend vs Revenue | Strong positive correlation (0.886) |
| Website Traffic vs Orders | Strong positive correlation (0.779) |
| Moving Average | Confirmed stable business expansion |
| Growth Analysis | Revealed both strong growth and decline periods |

---

## 📊 Visualizations Created

✅ Revenue Trend Line Chart

✅ Revenue vs Moving Average Chart

✅ Seasonal Revenue Pivot Table

✅ Revenue vs Advertising Spend Scatter Plot

✅ Website Traffic vs Orders Scatter Plot

---

## 📌 Business Insights

- Business performance improved consistently over time.
- Seasonal demand strongly influenced revenue patterns.
- Advertising investment significantly impacted revenue generation.
- Website traffic contributed positively to order growth.
- Revenue fluctuations highlighted periods of operational volatility.

---

## 🧠 Skills Practiced

- Time Series Analysis
- Trend Identification
- Seasonal Analysis
- Moving Average Computation
- Growth Rate Analysis
- Correlation Analysis
- Business Visualization
- Excel Analytical Techniques

---

## ✅ Project Status

✔ Completed Successfully

This project demonstrates beginner-to-intermediate proficiency in:
- Time Series Analysis,
- Business Trend Analysis,
- and Revenue Performance Evaluation using Microsoft Excel.

---

<footer>

**David Omotoye**  
*Advanced Statistics Learning Journey — Day 24*

</footer>
