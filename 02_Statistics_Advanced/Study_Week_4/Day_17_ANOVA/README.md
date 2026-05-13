# 📊 Day 17 — ANOVA (Analysis of Variance)

---

# 🎯 Lesson Objective

Understand how to compare average performance across three or more groups using ANOVA (Analysis of Variance).

---

# 🧠 Core Concepts Covered

| Concept | Purpose |
|---|---|
| ANOVA | Compare averages across multiple groups |
| Group Mean | Average value within each category |
| Between-Group Variance | Difference among group averages |
| Within-Group Variance | Variation inside each group |
| F-statistic | Ratio of between-group variance to within-group variance |
| p-value | Determines statistical significance |
| Null Hypothesis (H₀) | Assumes all group averages are equal |
| Alternative Hypothesis (H₁) | Assumes at least one group differs |

---

# 📊 Dataset Overview

The dataset analyzed employee productivity performance across multiple departments using:
- Productivity Score
- Training Hours
- Monthly Output
- Manager Rating
- Shift Information

Departments included:
- IT
- Finance
- Sales
- Operations
- Support

---

# 📌 Business Question

> Does employee productivity differ significantly across departments?

---

# 📊 Hypotheses

## Null Hypothesis (H₀)

There is no significant difference in average productivity scores across departments.

---

## Alternative Hypothesis (H₁)

At least one department has a significantly different average productivity score.

---

# 🛠 Analysis Performed

A One-Way ANOVA test was performed using:
- Department = grouping variable
- Productivity_Score = numeric comparison variable

The analysis compared average productivity performance across:
- IT
- Finance
- Sales
- Operations
- Support

---

# 📈 ANOVA Results

| Metric | Value |
|---|---:|
| F-statistic | 2.913 |
| p-value | 0.027 |
| F Critical | 2.503 |
| Alpha | 0.05 |

Since:

```text
0.027 < 0.05
```

the null hypothesis was rejected.

---

# 📌 Statistical Decision

Reject the Null Hypothesis (H₀).

---

# 🧠 Business Interpretation

The ANOVA analysis revealed statistically significant productivity differences across departments, suggesting that departmental structure, operational processes, management practices, or training exposure may influence employee performance outcomes.

---

# 📊 Department Productivity Ranking

| Rank | Department | Average Productivity |
|---|---|---:|
| 1 | Operations | 87.15 |
| 2 | IT | 84.75 |
| 3 | Sales | 83.11 |
| 4 | Finance | 77.55 |
| 5 | Support | 76.53 |

---

# 💡 Key Operational Insights

- Operations recorded the highest average productivity score, suggesting strong operational efficiency and workflow consistency.

- IT and Sales also demonstrated relatively strong productivity performance.

- Support recorded the lowest average productivity score, indicating possible operational bottlenecks or workflow inefficiencies.

- Finance demonstrated comparatively lower productivity than Operations, IT, and Sales.

- The statistically significant ANOVA result suggests that department-level factors may meaningfully influence employee productivity outcomes.

- ANOVA successfully identified statistically significant differences across multiple operational groups simultaneously.

---

# ⚠ Important Analytical Limitation

ANOVA confirms that significant differences exist among departments but does not identify the exact department pairs responsible for those differences.

Further post-hoc testing would be required for deeper pairwise comparison analysis.

---

# 🌍 Real-Life Applications

| Industry | ANOVA Application |
|---|---|
| HR Analytics | Compare employee performance across departments |
| Retail | Compare store performance |
| Manufacturing | Compare machine efficiency |
| Marketing | Compare campaign performance across regions |
| Healthcare | Compare treatment effectiveness |
| Finance | Compare investment portfolio performance |

---

# 🧠 Key Learning Outcome

This lesson introduced multi-group statistical comparison using ANOVA and demonstrated how analysts identify meaningful operational differences across business categories using statistical evidence.

---

<footer>

**David Omotoye**  
*Statistics Learning Journey — Day 17*

</footer>
