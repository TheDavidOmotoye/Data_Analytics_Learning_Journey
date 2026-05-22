# 📈 DAY 24 — Time Series Basics

## 📌 Objective

Analyze:
- trend,
- seasonality,
- cyclicality,
- and noise

in monthly business performance data using Time Series Analysis.

---

## 📘 What is Time Series Analysis?

Time Series Analysis studies data collected over time to identify:
- growth trends,
- recurring patterns,
- seasonality,
- fluctuations,
- and future forecasting opportunities.

Examples:
- monthly revenue,
- stock prices,
- website traffic,
- sales performance,
- customer orders.

---

## 📊 Core Time Series Components

| Component | Meaning |
|---|---|
| Trend | Long-term upward or downward movement |
| Seasonality | Repeating patterns during periods |
| Cyclicality | Long-term recurring economic/business cycles |
| Noise | Random fluctuations in data |

---

## 📈 Trend Analysis

Trend shows the overall direction of business performance over time.

### Example:
- Increasing revenue over several months
- Declining customer activity
- Stable operational growth

---

## 📘 Moving Average

Moving Average smooths short-term fluctuations to reveal the underlying trend.

---

## 📐 3-Month Moving Average Formula

3-Month Moving Average Formula

```text
Moving Average = (Month1 + Month2 + Month3) / 3
```

---

### 📐 Excel Formula

If Revenue is in Column B:

```excel
=AVERAGE(B2:B4)
```

Drag downward to calculate remaining months.

---

## 📊 Why Moving Average Matters

Moving Average:
- reduces noise,
- smooths fluctuations,
- improves trend visibility,
- helps forecasting.

---

## 📈 Revenue Growth Rate

Measures month-over-month percentage change.

---

### 📐 Growth Rate Formula

Revenue Growth Rate Formula

```text
Growth Rate = ((Current Revenue - Previous Revenue) / Previous Revenue) × 100
```

---

### 📐 Excel Formula

```excel
=(B3-B2)/B2
```

Format as Percentage (%).

---

## 📊 Growth Rate Interpretation

| Result | Meaning |
|---|---|
| Positive | Revenue increased |
| Negative | Revenue declined |
| Large Positive | Strong business expansion |
| Large Negative | Significant decline |

---

## 🚩 Growth Flagging

Growth flagging categorizes business performance.

---

### 📐 Excel Formula

```excel
=IF(I7<-10%,"Severe Decline",IF(I7<0,"Revenue Decline",IF(I7>15%,"High Growth","Normal Growth")))
```

---

## 📊 Flag Categories

| Range | Category |
|---|---|
| > 15% | High Growth |
| 0% to 15% | Normal Growth |
| < 0% | Revenue Decline |
| < -10% | Severe Decline |

---

## 📈 Correlation Analysis

Correlation measures relationship strength between variables.

---

### 📐 Correlation Formula

Correlation Formula

```text
r = Σ[(x - x̄)(y - ȳ)] / √[Σ(x - x̄)² × Σ(y - ȳ)²]
```

Range:
-1 to +1

---

### 📐 Excel Formula

```excel
=CORREL(array1,array2)
```

---

### 📐 Example

Advertising Spend vs Revenue:

```excel
=CORREL(B2:B36,E2:E36)
```

---

## 📊 Correlation Interpretation

| Correlation | Meaning |
|---|---|
| +1 | Perfect Positive |
| +0.7 to +0.99 | Strong Positive |
| +0.4 to +0.69 | Moderate Positive |
| 0 | No Relationship |
| -0.7 to -0.99 | Strong Negative |
| -1 | Perfect Negative |

---

## 📈 Scatter Plot Analysis

Scatter plots visualize relationships between variables.

Examples:
- Revenue vs Advertising Spend
- Website Traffic vs Orders

---

## 📊 Time Series Charts Created

✅ Revenue Trend Chart

✅ Revenue vs 3-Month Moving Average

✅ Seasonal Revenue & Orders Pivot Analysis

✅ Revenue vs Advertising Spend Scatter Plot

✅ Website Traffic vs Orders Scatter Plot

---

## 📈 Trendline Interpretation

Trendline Equation:

```equation
y = 2560.7x + 80348
```


Meaning:
- Revenue increases by approximately $2,561 monthly.

---

## 📊 R² Interpretation

```result
R² = 0.8153
```

Meaning:
- Strong long-term upward trend exists.

---

## 📈 Seasonal Analysis Insight

Q4 generated the strongest average revenue and order volume.

This suggests:
- strong seasonal demand,
- end-of-year business spikes,
- recurring quarterly patterns.

---

## ⚠️ Common Analyst Mistakes

❌ Not sorting dates properly

❌ Using inconsistent date formatting

❌ Ignoring seasonality

❌ Misinterpreting correlation as causation

❌ Using moving averages without enough periods

❌ Ignoring revenue decline periods

❌ Building charts without labels or legends

---

## 📊 Business Applications

Time Series Analysis is used for:

- revenue forecasting,
- sales analysis,
- inventory planning,
- traffic monitoring,
- marketing optimization,
- seasonal demand analysis,
- financial trend tracking.

---

## 📌 Final Lesson Summary

Time Series Analysis helps analysts understand:
- business growth,
- recurring patterns,
- seasonality,
- volatility,
- and long-term operational trends.

This lesson combined:
✅ Moving Average

✅ Revenue Growth Analysis

✅ Trend Analysis

✅ Correlation Analysis

✅ Seasonal Analysis

✅ Business Visualization

---

<footer>

**David Omotoye**  
*Advanced Statistics Learning Journey — Day 24*

</footer>
