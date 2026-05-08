# 📘 Day 15 Study Notes — Hypothesis Testing Fundamentals

---

## 🎯 Lesson Objective

Understand how to test business claims using null and alternative hypotheses, evaluate statistical evidence using p-values, and make data-driven business decisions.

---

## 🧠 What This Lesson Is Really About

Businesses constantly make claims such as:

- “The campaign increased sales.”
- “The new strategy improved performance.”
- “The business target was achieved.”

Professional analysts do not automatically accept these claims.

Instead, analysts ask:

> “Does the data provide enough statistical evidence to support this claim?”

This process is called:

## ✅ Hypothesis Testing

---

## 📚 Core Concepts

---

### 1. Null Hypothesis (H₀)

The default assumption.

Usually states:

- No change
- No improvement
- No effect

---

### 📌 For This Dataset

H₀: The campaign did not significantly increase average daily sales.

Meaning:

Avg_Daily_Sales_Before = Avg_Daily_Sales_After

---

### 2. Alternative Hypothesis (H₁)

The claim being tested.

Usually states:

- There IS a change
- There IS improvement
- There IS an effect

---

### 📌 For This Dataset

H₁: The campaign significantly increased average daily sales.

Meaning:

Avg_Daily_Sales_After > Avg_Daily_Sales_Before

---

### 3. Significance Level (α)

The decision threshold.

Most analysts use:

α = 0.05

Meaning:

> Analysts accept only a 5% risk of falsely concluding improvement when none truly exists.

---

### 4. P-Value

The p-value measures:

> How likely the observed result could occur if the null hypothesis were actually true.

---

### 📊 P-Value Interpretation

| P-Value | Interpretation |
|---|---|
| Small p-value | Strong evidence against H₀ |
| Large p-value | Weak evidence against H₀ |

---

### 5. Statistical Decision Rule

| Condition | Decision |
|---|---|
| p-value < 0.05 | Reject H₀ |
| p-value ≥ 0.05 | Fail to Reject H₀ |

---

## ⚠ Important Analyst Understanding

“Fail to reject H₀” does NOT mean the null hypothesis is true.

It means:

> There is insufficient evidence to reject it.

---

## 📊 Dataset Overview

| Variable | Purpose |
|---|---|
| Avg_Daily_Sales_Before | Sales before campaign |
| Avg_Daily_Sales_After | Sales after campaign |
| Campaign_Type | Marketing strategy |
| Sample_Size | Observation strength |
| Target_Sales | Business benchmark |

---

## 🎯 Main Goal of the Analysis

Determine whether marketing campaigns significantly increased average daily sales.

---

## 🛠 Why a Paired t-Test Was Used

The dataset compared:

```text
Avg_Daily_Sales_Before
vs
Avg_Daily_Sales_After
```

for the SAME branches.

Because the same branches were measured twice:

- Before campaign
- After campaign

the observations were dependent/related.

Therefore:

### ✅ Paired t-Test was the correct statistical method.

---

### 📊 Paired t-Test Formula

```text
t = d̄ / (sd / √n)
```

Where:
- d̄ = Mean difference
- sd = Standard deviation of differences
- n = Sample size

---

## 📌 Best Used For

- Before vs after analysis
- Repeated measurements
- Same-group comparisons
- Dependent observations

---

## 📚 Other Common Hypothesis Testing Methods

---

### 1. Independent t-Test

### Purpose
Compare means between TWO independent groups.

---

### 📊 Formula

```text
t = (x̄₁ - x̄₂) / SE
```

---

### ✅ Use When
- Comparing unrelated groups
- Observations are independent

---

### 🌍 Example
Urban vs Rural branch sales.

---

### 2. One-Sample t-Test

### Purpose
Compare a sample mean against a target value.

---

### 📊 Formula

```text
t = (x̄ - μ) / (s / √n)
```

---

### 🌍 Example
Testing whether average sales exceeded target sales.

---

### 3. ANOVA (Analysis of Variance)

### Purpose
Compare means across THREE OR MORE groups.

---

### 📊 Formula Concept

```text
Variance Between Groups / Variance Within Groups
```

---

### 🌍 Example
Compare performance across:
- Email campaigns
- Referral campaigns
- Influencer campaigns
- Discount campaigns

---

### 4. Chi-Square Test

### Purpose
Test relationships between categorical variables.

---

### 📊 Formula

```text
χ² = Σ((Observed - Expected)² / Expected)
```

---

### 🌍 Example
Test whether campaign type affects branch success category.

---

### 5. Z-Test

### Purpose
Test means when:
- Population standard deviation is known
- Sample size is very large

---

### 📊 Formula

```text
Z = (x̄ - μ) / (σ / √n)
```

---

### 📊 Testing Method Selection Guide

| Test Type | Best Used For | Data Type |
|---|---|---|
| One-Sample t-Test | Compare against target | Numeric |
| Independent t-Test | Compare two unrelated groups | Numeric |
| Paired t-Test | Before vs after analysis | Numeric |
| ANOVA | Compare multiple groups | Numeric |
| Chi-Square | Categorical relationships | Categorical |
| Z-Test | Large-sample testing | Numeric |

---

## 🛠 Step-by-Step Analytical Workflow

---

### STEP 1 — Calculate Sales Difference

Created:

### Sales_Difference

---

### Excel Formula

```excel
=[@Avg_Daily_Sales_After]-[@Avg_Daily_Sales_Before]
```

---

### Interpretation

| Result | Meaning |
|---|---|
| Positive | Sales increased |
| Negative | Sales decreased |

---

# STEP 2 — Create Difference Indicator

---

# Excel Formula

```excel
=IF([@[Avg_Daily_Sales_After]]>[@[Avg_Daily_Sales_Before]],"+VE","-VE")
```

---

### Purpose

Quickly identify:
- Positive sales movement
- Negative sales movement
- No change

---

### STEP 3 — Calculate Average Sales Metrics

| Metric | Result |
|---|---:|
| Avg Sales Before | 6589.20 |
| Avg Sales After | 7139.51 |
| Avg Sales Change | 550.31 |

---

## Excel Formulas Used

### Before Sales Average

```excel
=AVERAGE(TableName[Avg_Daily_Sales_Before])
```

---

### After Sales Average

```excel
=AVERAGE(TableName[Avg_Daily_Sales_After])
```

---

### Average Sales Difference

```excel
=AVERAGE(TableName[Sales_Difference])
```

---

### STEP 4 — State Hypotheses

---

### Null Hypothesis (H₀)

```text
The campaign did not significantly increase average daily sales.
```

---

### Alternative Hypothesis (H₁)

```text
The campaign significantly increased average daily sales.
```

---

### STEP 5 — Run Paired t-Test

---

### Excel Formula

```excel
=ROUND(T.TEST(Table6[Avg_Daily_Sales_Before],Table6[Avg_Daily_Sales_After],2,1),8)
```

---

### Formula Arguments

| Argument | Meaning |
|---|---|
| Table6[Avg_Daily_Sales_Before] | Before sales |
| Table6[Avg_Daily_Sales_AfterD6:D40 | After sales |
| 2 | Two-tailed test |
| 1 | Paired test |
| ROUND (8) | Round the result to 8 decimal numbers |

---

### 📊 Final Hypothesis Test Result

| Metric | Result |
|---|---:|
| P-Value | 0.0000009 |

---

### 📌 Statistical Decision

Since:

```text
0.0000009 < 0.05
```

### ✅ Reject the Null Hypothesis (H₀)

---

## 🧠 Analyst Interpretation

There is extremely strong statistical evidence that the campaigns significantly increased average daily sales.

The observed sales improvement was unlikely to occur by random chance alone.

---

## 📊 Campaign Type Comparison

| Campaign Type | Avg Before | Avg After | Avg Difference | Interpretation |
|---|---:|---:|---:|---|
| Discount | 7343.00 | 7833.00 | 490.00 | Moderate improvement |
| Email | 6385.00 | 6995.50 | 610.50 | Strong improvement |
| Influencer | 6839.07 | 7448.73 | 609.67 | Strong improvement |
| Referral | 6328.45 | 6759.55 | 431.09 | Weakest improvement |

---

## 🔥 Key Campaign Insights

---

### Email Campaign
Produced one of the strongest sales improvements.

---

### Influencer Campaign
Performed similarly to Email campaigns and strongly improved sales.

---

### Referral Campaign
Produced the weakest average sales increase.

---

### Discount Campaign
Showed moderate improvement, but contained limited observations.


Analysts should avoid overgeneralizing based on insufficient data.

---

## 📌 Biggest Lesson of Day 15

Hypothesis testing helps analysts separate:

| Random Fluctuation | Meaningful Business Change |
|---|---|
| Noise | Statistical Evidence |
| Assumptions | Data-Driven Decisions |

---

## 🌍 Real-Life Applications

---

### Marketing Analytics
Determine whether campaigns truly improve sales.

---

### HR Analytics
Test whether employee training improves performance.

---

### Product Analytics
Evaluate whether redesigns increase conversions.

---

### Healthcare Research
Determine whether treatments improve patient outcomes.

---

### Financial Analytics
Evaluate whether investment strategies significantly improve returns.

---

## 🧠 Analyst Best Practice

Never assume:

```text
"Sales increased, therefore the campaign worked."
```

Instead ask:

```text
"Was the increase statistically significant?"
```

That is professional analytical thinking.

---

## 🏁 Lesson Conclusion

The paired t-test revealed extremely strong statistical evidence that marketing campaigns significantly improved average daily sales.

Among campaign strategies:
- Email and Influencer campaigns produced the strongest average sales increases.
- Referral campaigns generated weaker improvements.
- Discount campaign conclusions require additional data for stronger reliability.

Day 15 introduced statistical decision-making and demonstrated how analysts use hypothesis testing to transform raw business observations into evidence-based strategic recommendations.

---

<footer>

**David Omotoye**  
*Statistics Learning Journey — Day 15*

</footer>
