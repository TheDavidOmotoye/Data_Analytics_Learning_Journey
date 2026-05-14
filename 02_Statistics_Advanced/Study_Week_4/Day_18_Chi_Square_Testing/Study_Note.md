# 📊 Day 18 Study Notes — Chi-Square Testing

---

## 🎯 Lesson Objective

Understand how to test relationships between categorical variables using Chi-Square testing.

---

## 🧠 What Is Chi-Square Testing?

Chi-Square Testing is a statistical method used to determine whether two categorical variables are statistically related.

It compares:
- observed category counts
vs
- expected category counts

to determine whether observed differences are meaningful or caused by random variation.

---

## 📌 Core Concepts

| Concept | Meaning |
|---|---|
| Observed Frequency | Actual category counts from dataset |
| Expected Frequency | Counts expected if no relationship exists |
| Contingency Table | Cross-tabulated count table |
| Chi-Square Statistic | Measures deviation between observed and expected counts |
| p-value | Statistical significance indicator |

---

## 📊 Dataset Variables Used

| Variable | Type |
|---|---|
| Overtime | Categorical |
| Attrition | Categorical |

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

## 🛠 Excel Procedure

---

### STEP 1 — Create Pivot Table

Go to:

```text
Insert → PivotTable
```

---

### STEP 2 — Build Contingency Table

| Area | Field |
|---|---|
| Rows | Overtime |
| Columns | Attrition |
| Values | Count of Employee_ID |

---

### 📊 Observed Frequency Table

| Overtime | Attrition No | Attrition Yes |
|---|---:|---:|
| No | 40 | 11 |
| Yes | 17 | 12 |

---

### STEP 3 — Compute Expected Frequencies

Formula:

```text
(Row Total × Column Total) ÷ Grand Total
```

---

### 📊 Expected Frequency Table

| Overtime | Attrition No | Attrition Yes |
|---|---:|---:|
| No | 36.3375 | 14.6625 |
| Yes | 20.6625 | 8.3375 |

---

### Chi-Square Formula

χ² = Σ ((O - E)² / E)

Where:

- χ² = Chi-Square statistic
- Σ = Sum of all calculations
- O = Observed Frequency
- E = Expected Frequency

---

### Expected Frequency Formula

Expected Frequency = (Row Total × Column Total) / Grand Total

---

### Excel Formula

=CHISQ.TEST(observed_range, expected_range)

Example:

=CHISQ.TEST(B91:C92,B98:C99)

---

### STEP 4 — Run Chi-Square Test

Excel Formula:

```excel
=CHISQ.TEST(B91:C92,B98:C99)
```

---

## 📊 Statistical Output

| Metric | Value |
|---|---:|
| p-value | 0.0598 |
| Alpha | 0.05 |

---

## 📌 Statistical Decision

Since:

```text
0.0598 > 0.05
```

Fail to Reject the Null Hypothesis (H₀).

---

## 🧠 Interpretation

The analysis did not find statistically significant evidence that overtime and attrition were related within this dataset.

---

## 💡 Analyst Insights

- Employees working overtime appeared to show somewhat higher attrition frequency.
- However, the observed difference was not statistically strong enough to confirm a reliable relationship.
- Overtime alone may not fully explain employee resignation behavior.
- Other HR factors may influence attrition more strongly.

---

## ⚠ Common Analyst Mistakes

| Mistake | Problem |
|---|---|
| Using percentages instead of counts | Chi-Square requires frequencies |
| Using averages | Chi-Square tests categories |
| Ignoring expected frequencies | Can invalidate results |
| Assuming significance means causation | Relationship ≠ causation |
| Misreading contingency tables | Produces incorrect expected values |

---

## 🌍 Real-Life Applications

- Employee attrition analysis
- Promotion fairness analysis
- Customer segmentation studies
- Campaign effectiveness analysis
- Healthcare treatment comparison

---

## 🔥 Final Lesson Conclusion

Chi-Square testing allows analysts to determine whether categorical business variables are statistically related.

This lesson demonstrated how analysts move beyond visible patterns and use statistical evidence to validate operational relationships within business datasets.

---

<footer>

**David Omotoye**  
*Statistics Learning Journey — Day 18*

</footer>
