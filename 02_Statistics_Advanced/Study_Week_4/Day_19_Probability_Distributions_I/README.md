# 📊 Day 19 — Probability Distributions I: Normal Distribution & Z-Scores

---

## 🎯 Lesson Objective

Understand how to standardize values and identify unusual observations using normal distributions and z-scores.

---

## 🧠 Core Concepts Covered

| Concept | Purpose |
|---|---|
| Normal Distribution | Understand data spread and central tendency |
| Z-score | Standardize observations |
| Mean | Average value |
| Standard Deviation | Measure of variability |
| Outlier Detection | Identify unusual observations |
| Standardization | Compare values fairly |

---

## 📊 Dataset Overview

The dataset analyzed applicant recruitment performance using:
- Assessment Score
- Experience Years
- Interview Score
- Final Score
- Role Applied
- Pass Status

---

## 📌 Business Question

> Which applicants performed unusually high or low relative to the overall applicant population?

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

## 📊 Statistical Results

| Metric | Value |
|---|---:|
| Average Final Score | 75.58 |
| Standard Deviation | 8.93 |

---

## 🛠 Analysis Performed

The analysis involved:
- calculating average final score
- calculating standard deviation
- standardizing final scores using z-scores
- classifying applicants based on score distribution

---

## 📘 Excel Z-Score Formula

```excel
=ROUND(([@[Final_Score]]-$A$69)/$A$72,2)
```

---

## 📊 Z-Score Interpretation Framework

| Z-score Range | Interpretation |
|---|---|
| ≥ 2 | Exceptional |
| 1 to <2 | Above Average |
| -1 to <1 | Average |
| -2 to <-1 | Below Average |
| ≤ -2 | Very Low |

---

## 📈 Exceptional Applicants

| Applicant | Final Score | Z-score |
|---|---:|---:|
| APP-007 | 98.3 | 2.544 |
| APP-014 | 94.7 | 2.141 |

These applicants demonstrated exceptionally strong performance relative to the overall candidate population.

---

## 📉 Weak Applicant Detection

| Applicant | Final Score | Z-score |
|---|---:|---:|
| APP-025 | 51.8 | -2.663 |

This applicant performed significantly below the average applicant distribution.

---

## 💡 Key Analytical Insights

- Most applicants clustered near the average performance range.
- The applicant distribution appeared relatively balanced and approximately normal.
- Z-score analysis successfully identified exceptional and weak performers.
- Standardization improved fairness and consistency in candidate comparison.

---

## ⚠ Important Analytical Principle

Raw scores alone do not fully explain performance quality.

Z-scores provide:
- distribution context
- relative comparison
- outlier detection
- standardized evaluation

---

## 🌍 Real-Life Applications

| Industry | Application |
|---|---|
| HR Analytics | Candidate performance evaluation |
| Finance | Fraud detection |
| Retail | Unusual sales detection |
| Healthcare | Abnormal patient result detection |
| Manufacturing | Quality control monitoring |

---

## 🧠 Key Learning Outcome

This lesson introduced statistical standardization and demonstrated how analysts use z-scores to evaluate relative performance and identify unusual observations within business datasets.

---

<footer>

**David Omotoye**  
*Statistics Learning Journey — Day 19*

</footer>
