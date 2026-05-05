# 📈 Day 11 Study Notes — Advanced Correlation Analysis

---

## 🎯 Lesson Objective
Understand how to evaluate relationships between variables using advanced correlation techniques and determine when each method is most appropriate.

---

## 🧠 Core Concepts

### Pearson Product-Moment Correlation
Measures the **strength and direction of a linear relationship** between two continuous variables.

**Use When:**
- Both variables are continuous numeric  
- Relationship is linear  
- No major outliers are present  
- Distribution is reasonably normal/symmetric  

**Best For:**  
Measuring **linear relationships**

**Example:**  
Study Hours vs Exam Score

---

### CORREL()
Excel implementation of **Pearson Product-Moment Correlation**

**Note:**  
Returns the same result as `PEARSON()`

---

### PEARSON()
Alternative Excel implementation of **Pearson Product-Moment Correlation**

```excel
CORREL() = PEARSON()
```

---

### Spearman Rank Correlation
Measures the **strength and direction of a monotonic relationship** between ranked variables.

**Use When:**
- Relationship is monotonic but not linear  
- Data contains outliers  
- Variables are ordinal/ranked  
- A more robust alternative to Pearson is required  

**Best For:**  
Measuring whether variables move consistently in the same general direction regardless of exact linearity

---

### Scatter Plot
Visual diagnostic used to assess:
- Relationship Direction  
- Strength of Association  
- Linearity  
- Outliers / Clustering  

---

## 📊 Key Results from Dataset

| Relationship | Pearson / CORREL | Spearman | Interpretation |
|---|---:|---:|---|
| Study Hours vs Exam Score | 0.90 | 0.913 | Very Strong Positive |
| Attendance % vs Exam Score | 0.11 | 0.045 | Negligible / Very Weak |
| Sleep Hours vs Exam Score | 0.31 | 0.256 | Weak Positive |
| Screen Time vs Exam Score | -0.24 | -0.168 | Weak Negative |
| Practice Test Score vs Exam Score | 0.92 | 0.892 | Very Strong Positive |

---

## 💡 Key Insights

- Practice test score is the strongest predictor of exam performance.
- Study hours also strongly predict exam outcomes.
- Screen time has a weak negative relationship with performance.
- Attendance shows negligible predictive power in this dataset.
- Pearson and Spearman consistency indicates relationships are linear and stable.

---

## 🧭 Correlation Method Selection Framework

### Use Pearson When:
- Variables are continuous  
- Relationship is linear  
- Outliers are minimal  

---

### Use Spearman When:
- Variables are ranked / ordinal  
- Relationship is monotonic but non-linear  
- Outliers may distort Pearson  

---

## 🔍 Interpretation Guide

| Scenario | Meaning |
|---|---|
| Pearson ≈ Spearman | Relationship likely linear and stable |
| Spearman > Pearson | Relationship may be monotonic but non-linear |
| Pearson > Spearman | Relationship may be influenced by outliers |

---

## 📝 Analyst Best Practice

Before running correlation:

1. Review Scatter Plot  
2. Check for Outliers  
3. Confirm Data Type  
4. Assess Relationship Shape  

---

## 🏁 Lesson Conclusion

Pearson Product-Moment Correlation was used to evaluate linear relationships between continuous variables in the dataset.

Spearman Rank Correlation was applied as a robustness check to validate whether those relationships remained consistent after ranking the variables.

The close alignment between Pearson and Spearman coefficients confirms that the observed relationships are statistically stable and structurally reliable.

---

<footer>

**David Omotoye**  
*Statistics Learning Journey — Day 11*

</footer>
