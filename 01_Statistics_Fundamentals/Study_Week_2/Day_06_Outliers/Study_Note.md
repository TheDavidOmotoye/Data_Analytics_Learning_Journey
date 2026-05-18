# 📘 Day 6 Study Note — Outliers

## 🎯 Objective
Detect unusually high or low values using the IQR method.

---

## 🧠 Key Concepts

## What Are Outliers?
Outliers are values significantly different from the rest of the dataset.

They may indicate:
- Data entry errors
- Fraudulent activity
- Rare events
- Exceptional cases

---

## 📌 IQR Method for Detecting Outliers

### Step 1: Calculate IQR

Formula:
IQR = Q3 − Q1

---

### Step 2: Calculate Lower & Upper Bounds

Lower Bound:
Q1 − 1.5(IQR)

Upper Bound:
Q3 + 1.5(IQR)

---

### Step 3: Identify Outliers

Any value:
- Below the lower bound
- Above the upper bound

is considered an outlier.

---

## 📊 Results

| Metric | Value |
|---|---|
| Q1 | 53.75 |
| Q3 | 77.5 |
| IQR | 23.75 |
| Lower Bound | 18.125 |
| Upper Bound | 113.125 |

---

## 🚨 Outliers Identified

| Transaction | Amount |
|---|---|
| T037 | 150 |
| T038 | 165 |
| T039 | 12 |
| T040 | 9 |

---

## 💻 Excel Functions

=QUARTILE.INC(range,1)
=QUARTILE.INC(range,3)

---

## 🔍 Key Insight

Outlier detection is important in:
- Fraud detection
- Risk analysis
- Quality control
- Financial analysis

---

## 📝 Reflection

Outliers can distort analysis and influence statistical results. Analysts must investigate them carefully before making decisions.
