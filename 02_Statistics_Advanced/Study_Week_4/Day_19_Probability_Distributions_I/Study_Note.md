# 📊 Day 19 Study Notes — Probability Distributions I: Normal Distribution & Z-Scores

---

## 🎯 Lesson Objective

Understand how to standardize values and identify unusual observations using normal distributions and z-scores.

---

## 🧠 What Is a Normal Distribution?

A normal distribution is a symmetric bell-shaped distribution where:
- most values cluster around the mean
- fewer values occur at the extremes

It is one of the most important distributions in statistics and analytics.

---

## 📊 Empirical Rule

| Range | Approximate % of Data |
|---|---:|
| Mean ± 1 SD | 68% |
| Mean ± 2 SD | 95% |
| Mean ± 3 SD | 99.7% |

This is called the:
## 68-95-99.7 Rule

---

## 🧠 What Is a Z-Score?

A z-score standardizes a value by measuring how many standard deviations it is away from the mean.

It helps analysts determine:
- whether a value is normal
- whether a value is unusually high
- whether a value is unusually low

---

## 📐 Z-Score Formula

```text
z = (x - μ) / σ
```

Where:
- z = Z-score
- x = Actual value
- μ = Mean
- σ = Standard deviation

---

## 📊 Dataset Variables Used

| Variable | Purpose |
|---|---|
| Final_Score | Main analysis variable |
| Assessment_Score | Supporting metric |
| Interview_Score | Supporting metric |
| Pass_Status | Candidate outcome |

---

## 📊 Statistical Summary

| Metric | Value |
|---|---:|
| Average Final Score | 75.58 |
| Standard Deviation | 8.93 |

---

# 🛠 Excel Procedure

---

## STEP 1 — Calculate Mean

Excel Formula:

```excel
=AVERAGE(Table10[inal_Score])
```

---

## STEP 2 — Calculate Standard Deviation

Excel Formula:

```excel
=STDEV.S(Table10[inal_Score])
```

---

## STEP 3 — Create Z-Score Column

New Column:
### Z-Score

---

## STEP 4 — Compute Z-Scores

Excel Formula:

```excel
=ROUND(([@[Final_Score]]-$A$69)/$A$72,2)
```

---

## STEP 5 — Create Interpretation Column

Excel Formula:

```excel
=IF([@[Z-Score]]>=2,"Exceptional",IF([@[Z-Score]]<=-2,"Very Low",IF(AND([@[Z-Score]]>-2,[@[Z-Score]]<-1),"Below Average",IF(AND([@[Z-Score]]>=-1,[@[Z-Score]]<=1),"Average","Above Average"))))
```

---

## 📊 Interpretation Framework

| Z-score Range | Interpretation |
|---|---|
| ≥ 2 | Exceptional |
| 1 to <2 | Above Average |
| -1 to <1 | Average |
| -2 to <-1 | Below Average |
| ≤ -2 | Very Low |

---

## 📈 Exceptional Applicant Detection

| Applicant | Final Score | Z-score |
|---|---:|---:|
| APP-007 | 98.3 | 2.544 |
| APP-014 | 94.7 | 2.141 |

These applicants performed significantly above average.

---

## 📉 Weak Applicant Detection

| Applicant | Final Score | Z-score |
|---|---:|---:|
| APP-025 | 51.8 | -2.663 |

This applicant performed significantly below average.

---

## 💡 Key Analyst Insights

- Most applicants clustered around the average performance range.
- The distribution appeared relatively balanced and approximately normal.
- Only a few extreme values existed in the dataset.
- Z-score analysis successfully identified exceptional and weak performers.

---

## ⚠ Common Analyst Mistakes

| Mistake | Problem |
|---|---|
| Using raw scores only | Ignores distribution context |
| Ignoring standard deviation | Distorts interpretation |
| Forgetting negative z-scores | Misses weak observations |
| Treating all high scores equally | Z-scores provide relative comparison |
| Ignoring outliers | Extreme values may distort analysis |

---

## 🌍 Real-Life Applications

- Recruitment analytics
- Fraud detection
- Risk analysis
- Quality control
- Student performance evaluation
- Customer behavior analysis

---

## 🔥 Final Lesson Conclusion

Z-score analysis transforms raw observations into standardized comparisons.

This allows analysts to:
- compare observations fairly
- identify unusual values
- detect outliers
- evaluate relative performance professionally

within real-world business datasets.

---

<footer>

**David Omotoye**  
*Statistics Learning Journey — Day 19*

</footer>
