# 📘 Day 14 Study Notes — Confidence Intervals

---

## 🎯 Lesson Objective

Estimate realistic population ranges using sample data and evaluate the reliability and precision of sample estimates.

---

## 🧠 Core Concept Overview

In real-world analytics, analysts rarely have access to entire populations. Instead, they rely on samples to estimate population values.

Because sample values naturally vary, analysts use confidence intervals to estimate a realistic range within which the true population value is likely to fall.

Rather than saying:

> “The average employee salary is ₦5,900.”

Analysts say:

> “We are 95% confident the true average salary lies between ₦5,500 and ₦6,300.”

This provides a more realistic and statistically reliable interpretation.

---

## 📚 Core Definitions

---

### Population Parameter
The true value for an entire population.

Example:
- True company average salary
- True workforce performance level

Usually unknown.

---

### Sample Statistic
A value calculated from sample data.

Examples:
- Sample mean
- Sample standard deviation

Used to estimate population parameters.

---

### Confidence Interval (CI)
A range likely to contain the true population value.

---

### Margin of Error (MOE)
The amount added to and subtracted from the sample mean.

---

### Standard Error (SE)
Measures how much the sample mean is expected to vary across repeated sampling.

Smaller SE:
- More precision
- Lower uncertainty

Larger SE:
- Less precision
- Higher uncertainty

---

## 📊 Core Statistical Formulas

---

### 📊 Confidence Interval Formula

CI = x̄ ± ME

Where:
- x̄ = Sample Mean
- ME = Margin of Error

---

### 📊 Standard Error Formula

SE = s / √n

Where:
- s = Standard Deviation
- n = Sample Size

---

### 📊 Margin of Error Formula

ME = Z × SE

For this lesson:
- 95% Confidence Level → Z = 1.96
---

## 📚 Confidence Level Reference

| Confidence Level | Z-Score |
|---|---|
| 90% | 1.645 |
| 95% | 1.96 |
| 99% | 2.576 |

---

## 🛠 Dataset Variables

| Variable | Purpose |
|---|---|
| Monthly_Income | Salary estimation |
| Years_Experience | Workforce experience analysis |
| Performance_Rating | Employee performance evaluation |
| Sample_Group | Sample segmentation |

---

## 📊 Step-by-Step Analytical Workflow

---

### STEP 1 — Separate Sample Groups

The dataset already contained:
- Sample A
- Sample B

These represented two separate employee samples.

---

### STEP 2 — Calculate Descriptive Statistics

For each variable and sample group, calculate:

- Mean
- Standard Deviation
- Sample Size (n)

---

### Excel Formulas Used

### Mean

=AVERAGEIFS(Table5[Monthly_Income],Table5[Sample_Group],"Sample A")

---

### Standard Deviation

=ROUND(STDEV.S(FILTER(Table5[Monthly_Income],Table5[Sample_Group]="Sample A")),2)

---

### Sample Size

=COUNTIFS(Table5[Sample_Group],"Sample A")

---

### STEP 3 — Calculate Standard Error

### Formula

SE = s / √n

---

### Excel Formula

=Standard_Deviation/SQRT(Sample_Size)

Example:

=G2/SQRT(H2)

---

### STEP 4 — Calculate Margin of Error

### Formula

ME = Z × SE

---

### Excel Formula

=1.96*SE

---

### STEP 5 — Calculate Confidence Intervals

---

### Lower Confidence Interval

=Mean-MOE

---

### Upper Confidence Interval

=Mean+MOE

---

## 📊 Final Confidence Interval Results

| Metric | Sample | Mean | Std Dev | n | SE | MOE | Lower CI | Upper CI |
|---|---|---:|---:|---:|---:|---:|---:|---:|
| Monthly Income | A | 5949.84 | 929.77 | 25 | 185.95 | 364.47 | 5585.37 | 6314.31 |
| Monthly Income | B | 5881.32 | 850.57 | 25 | 170.11 | 333.42 | 5547.90 | 6214.74 |
| Years Experience | A | 7.96 | 4.37 | 25 | 0.874 | 1.71 | 6.25 | 9.67 |
| Years Experience | B | 8.36 | 3.88 | 25 | 0.776 | 1.52 | 6.84 | 9.88 |
| Performance Rating | A | 3.64 | 1.11 | 25 | 0.222 | 0.44 | 3.20 | 4.08 |
| Performance Rating | B | 3.48 | 1.12 | 25 | 0.224 | 0.44 | 3.04 | 3.92 |

---

## 🧠 Interpretation Summary

---

### Monthly Income
- Sample A and Sample B produced very similar income estimates.
- The confidence intervals overlapped heavily, suggesting no major income difference between the two groups.
- Monthly income showed wider confidence intervals because salaries naturally vary more between employees.

---

### Years_Experience
- Workforce experience levels appeared similar across both samples.
- Confidence intervals strongly overlapped, indicating comparable experience distributions.

---

### Performance Rating
- Performance ratings remained relatively stable across both samples.
- Narrow confidence intervals suggested more reliable and precise estimates.

---

## 📊 Interval Width Comparison

| Variable | Interval Width | Interpretation |
|---|---|---|
| Monthly Income | Wide | Higher variability |
| Years Experience | Moderate | Moderate variability |
| Performance Rating | Narrow | More stable metric |

---

## 🔥 Key Analytical Insight

Confidence intervals help analysts measure uncertainty and estimate realistic population ranges using sample data.

Wider intervals indicate:
- Greater variability
- Higher uncertainty

Narrower intervals indicate:
- More stability
- Higher estimate precision

---

## 🌍 Real-Life Applications

---

### Salary Benchmarking
Organizations estimate realistic salary ranges rather than relying on a single average figure.

---

### Employee Evaluation
Businesses estimate expected workforce performance with measurable reliability.

---

### Customer Satisfaction Research
Analysts estimate realistic satisfaction ranges across customer populations.

---

### Election Polling
Pollsters estimate likely voter support ranges instead of exact percentages.

---

### Healthcare Research
Researchers estimate treatment effectiveness ranges using patient samples.

---

## 📌 Analyst Best Practice

Never assume:

"The sample average is the exact population value."

Instead think:

"The true population value is likely somewhere within this confidence interval."

That is the mindset of a professional analyst.

---

## 🏁 Lesson Conclusion

The analysis showed that both samples produced relatively similar estimates across income, experience, and performance metrics.

Monthly income exhibited the highest variability, while performance ratings remained more stable and precise.

Confidence intervals provided a more reliable understanding of realistic population ranges beyond simple sample averages.

---

<footer>

**David Omotoye**  
*Statistics Learning Journey — Day 14*

</footer>
