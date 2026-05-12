# 📊 Day 16 — T-Tests

---

## 🎯 Lesson Objective

Understand how to perform and interpret:
- One-Sample t-tests
- Paired t-tests
- Independent t-tests

using business datasets and statistical decision-making techniques.

---

# 🧠 Core Concepts Covered

| Concept | Purpose |
|---|---|
| One-Sample t-Test | Compare one sample mean against a business target |
| Paired t-Test | Compare before/after measurements for the same subjects |
| Independent t-Test | Compare differences between two independent groups |
| p-value | Measure statistical evidence against the null hypothesis |
| Null Hypothesis (H₀) | Assumes no significant difference/effect |
| Alternative Hypothesis (H₁) | Assumes significant difference/effect |
| Statistical Significance | Determines whether results are likely due to chance |

---

# 📊 Dataset Overview

The dataset analyzed customer spending behavior before and after campaign exposure across:
- Treatment customers
- Control customers
- Campaign exposure categories
- Customer segments

---

# 🛠 Analyses Performed

## 1️⃣ Paired t-Test

Compared:
- Spend_Before
- Spend_After

### Purpose

Determine whether campaign exposure significantly changed customer spending behavior.

### Result

✅ Spending increased significantly after campaign exposure.

---

## 2️⃣ Independent t-Test

Compared:
- Treatment group spending change
- Control group spending change

### Purpose

Determine whether campaign-exposed customers outperformed non-exposed customers.

### Result

✅ Treatment customers significantly outperformed the Control group.

---

## 3️⃣ One-Sample t-Test

Compared:
- Average Spend_After
- Assumed business target of 200

### Purpose

Determine whether post-campaign spending achieved the expected business target.

### Result

⚠ Average spending remained significantly below the target benchmark.

---

# 📈 Statistical Results Summary

| Test Type | p-value | Decision |
|---|---:|---|
| Paired t-Test | p < 0.001 | Reject H₀ |
| Independent t-Test | p < 0.001 | Reject H₀ |
| One-Sample t-Test | 0.00329 | Reject H₀ |

---

# 🔍 Business Interpretation

The marketing campaign significantly improved customer spending behavior and treatment customers outperformed the control group by a statistically meaningful margin.

However, despite the observed improvement, the average post-campaign spending level still remained below the expected business target benchmark, suggesting that additional optimization may still be required to achieve organizational performance goals.

---

# ⚠ Common Analyst Mistakes

- Using the wrong t-test type
- Ignoring group dependency structure
- Misinterpreting p-values
- Assuming statistical significance means business success
- Comparing independent groups using paired tests
- Forgetting to define hypotheses before analysis

---

# 🌍 Real-Life Applications

| Industry | Application |
|---|---|
| Marketing | Campaign effectiveness testing |
| Retail | Customer spending analysis |
| Healthcare | Treatment effectiveness evaluation |
| Finance | Investment strategy comparison |
| HR Analytics | Employee performance improvement analysis |

---

# 🧠 Key Learning Outcome

This lesson introduced practical statistical testing workflows used by analysts to:
- validate business claims
- measure campaign effectiveness
- compare group performance
- support evidence-based decision-making

---

<footer>

**David Omotoye**  
*Statistics Learning Journey — Day 16*

</footer>
