# 📊 Day 18 — Chi-Square Testing

---

## 🎯 Lesson Objective

Understand how to test relationships between categorical variables using Chi-Square testing.

---

## 🧠 Core Concepts Covered

| Concept | Purpose |
|---|---|
| Chi-Square Test | Tests relationship between categorical variables |
| Observed Frequency | Actual category counts |
| Expected Frequency | Theoretical counts if no relationship exists |
| Contingency Table | Cross-tabulated frequency table |
| p-value | Determines statistical significance |
| Null Hypothesis (H₀) | Assumes variables are independent |
| Alternative Hypothesis (H₁) | Assumes variables are related |

---

## 📊 Dataset Overview

The dataset analyzed employee-related categorical variables including:
- Gender
- Department
- Attrition
- Promotion Status
- Overtime
- Job Satisfaction

---

## 📌 Business Question

> Does overtime significantly relate to employee attrition?

---

## 📊 Hypotheses

### Null Hypothesis (H₀)

Overtime and Attrition are independent.

---

### Alternative Hypothesis (H₁)

Overtime and Attrition are significantly related.

---

#  # 🛠 Analysis Performed

A Chi-Square Test of Independence was performed using:
- Overtime
- Attrition

A contingency table was created using Pivot Tables to compare observed employee counts across categories.

---

## 📐 Chi-Square Formula

χ² = Σ ((O - E)² / E)

Where:

- χ² = Chi-Square statistic
- Σ = Sum of all calculations
- O = Observed Frequency
- E = Expected Frequency

---

## Expected Frequency Formula

Expected Frequency = (Row Total × Column Total) / Grand Total

---

## Excel Formula

=CHISQ.TEST(observed_range, expected_range)

Example:

=CHISQ.TEST(B91:C92,B98:C99)

---

# 📊 Statistical Results

| Metric | Value |
|---|---:|
| p-value | 0.0598 |
| Alpha | 0.05 |

Since:

```text
0.0598 > 0.05
```

the null hypothesis was not rejected.

---

# 📌 Statistical Decision

Fail to Reject the Null Hypothesis (H₀).

---

# 🧠 Business Interpretation

The analysis did not find statistically significant evidence that overtime and attrition were related within this dataset.

Although overtime employees appeared to show relatively higher attrition counts, the observed difference was not statistically strong enough to confirm a reliable relationship at the 5% significance level.

---

# 💡 Key Analytical Insights

- Visible patterns alone are insufficient for analytical conclusions.
- Statistical testing is necessary to validate observed relationships.
- Overtime alone may not fully explain employee attrition.
- Additional factors such as promotion opportunities, job satisfaction, and management quality may influence employee retention.

---

# ⚠ Important Analytical Limitation

Chi-Square testing determines whether a relationship exists between categorical variables but does not:
- measure relationship strength
- determine causation
- identify operational drivers directly

---

# 🌍 Real-Life Applications

| Industry | Chi-Square Application |
|---|---|
| HR Analytics | Attrition vs Overtime |
| Marketing | Campaign Type vs Conversion |
| Retail | Customer Type vs Purchase Behavior |
| Healthcare | Treatment Type vs Recovery |
| Finance | Risk Category vs Default Status |

---

# 🧠 Key Learning Outcome

This lesson introduced categorical relationship testing and demonstrated how analysts use Chi-Square testing to validate whether observed operational patterns are statistically meaningful.

---

<footer>

**David Omotoye**  
*Statistics Learning Journey — Day 18*

</footer>
