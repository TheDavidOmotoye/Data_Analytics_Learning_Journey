## Key Insights

- Practice test performance emerged as the strongest predictor of final exam score, showing a very strong positive correlation (r = 0.92).
- Study hours also demonstrated a substantial positive relationship with exam outcomes (r = 0.90), reinforcing the importance of preparation effort.
- Screen time showed a weak negative correlation with exam performance, suggesting excessive device usage may modestly hinder academic outcomes.
- Attendance percentage exhibited negligible correlation with exam performance, indicating physical presence alone did not strongly predict results in this sample.
- Pearson and Spearman results were highly consistent, validating that the observed relationships are both linear and rank-stable.

Advanced correlation analysis showed that preparation-related metrics (study hours and practice test scores) are the most influential drivers of academic performance, while passive factors such as attendance and sleep exhibited weaker relationships. The consistency between Pearson and Spearman coefficients confirms the reliability and stability of these findings.

## Notes
### When Each Correlation Method Is Appropriate
1. Pearson Product-Moment Correlation
Use When:
- Both variables are continuous numeric
- Relationship is linear
- Data has no major outliers
- Distribution is reasonably normal/symmetric (ideal but not always required)

Best For:

- Measuring linear relationships

Example:

Study Hours vs Exam Score (score rises proportionally as study increases)

2. CORREL()
What It Is:

Excel implementation of Pearson Correlation (Same situations as Pearson).

Why It Exists:

Simply an Excel function shortcut.

3. PEARSON()
What It Is:

Another Excel implementation of Pearson Correlation.

Use When:

Same as CORREL()

Important Note:

In Excel:

CORREL() = PEARSON()

They return identical results.

4. Spearman Rank Correlation
Use When:
Relationship is monotonic but not linear
Data contains outliers
Variables are ordinal/ranked
You want a robust alternative to Pearson

Best For:

Measuring whether variables move in the same general direction, regardless of exact linearity

Example:

Customer Satisfaction Rank vs Service Quality Rank

## How They Compare

| Method   | Measures               | Data Type            | Assumes Linearity? | Sensitive to Outliers? | Uses Raw Values or Ranks? |
| -------- | ---------------------- | -------------------- | ------------------ | ---------------------- | ------------------------- |
| Pearson  | Linear relationship    | Continuous           | Yes                | Yes                    | Raw Values                |
| CORREL   | Linear relationship    | Continuous           | Yes                | Yes                    | Raw Values                |
| PEARSON  | Linear relationship    | Continuous           | Yes                | Yes                    | Raw Values                |
| Spearman | Monotonic relationship | Ordinal / Continuous | No                 | Less Sensitive         | Ranks                     |

## Correlation Method Selection Framework

### Step 1 — Are Both Variables Numeric?

- **No** → Correlation not appropriate  
- **Yes** → Proceed  

---

## Step 2 — Is the Relationship Roughly Linear?  
(Check Scatter Plot)

- **Yes** → Pearson Product-Moment Correlation  
- **No / Unsure** → Consider Spearman Rank Correlation  

---

## Step 3 — Are There Significant Outliers?

- **Yes** → Spearman Preferred  
- **No** → Pearson Appropriate  

---

## Step 4 — Are Variables Ranked / Ordinal Instead of Continuous?

- **Yes** → Spearman Rank Correlation  
- **No** → Pearson Appropriate  

---

# Method Comparison Table

| Method | Best Used When | Avoid When |
|---|---|---|
| Pearson Product-Moment Correlation | Variables are continuous, relationship is linear, no major outliers | Data is ranked, non-linear, or heavily skewed with outliers |
| Spearman Rank Correlation | Relationship is monotonic, ranked, non-linear, or contains outliers | Need strict linear relationship measurement |

---

# Interpretation Guide

| Scenario | What It Suggests |
|---|---|
| Pearson ≈ Spearman | Relationship is likely linear and stable |
| Spearman > Pearson | Relationship may be monotonic but non-linear |
| Pearson > Spearman | Relationship may be influenced by outliers |

---

# Analyst Best Practice

> Never calculate correlation before first reviewing:
> 1. Scatter Plot  
> 2. Outliers  
> 3. Data Type  
> 4. Relationship Shape

## Conclusion
Pearson Product-Moment Correlation was used to evaluate linear relationships between continuous variables where data quality and distribution assumptions were acceptable. Spearman Rank Correlation was additionally applied as a robustness check to assess whether relationships remained consistent when variables were converted to ranked values, thereby reducing sensitivity to outliers and non-linearity.
