# 📊 Day 16 Study Notes — T-Tests

---

# 🎯 Lesson Objective

Understand how to perform and interpret:
- One-Sample t-tests
- Paired t-tests
- Independent t-tests

using statistical evidence and business decision-making principles.

---

# 🧠 Core Concepts

## What Is a t-Test?

A t-test is a statistical method used to determine whether differences between averages are statistically significant or likely caused by random variation.

---

# 📚 Types of t-Tests

| Test Type | Purpose |
|---|---|
| One-Sample t-Test | Compare one sample mean against a target value |
| Paired t-Test | Compare before/after results for the same subjects |
| Independent t-Test | Compare averages across two separate groups |

---

# 📌 Key Statistical Components

| Component | Meaning |
|---|---|
| H₀ | Null Hypothesis |
| H₁ | Alternative Hypothesis |
| p-value | Probability result occurred by chance |
| α = 0.05 | Common significance threshold |
| Reject H₀ | Evidence supports significant difference |
| Fail to Reject H₀ | Insufficient evidence of difference |

---

# 🧪 1️⃣ Paired t-Test

## Purpose

Determine whether customer spending significantly changed after campaign exposure.

---

# 📌 Why Paired t-Test Was Used

Because:
- same customers
- measured twice
- before vs after comparison

---

# 📊 Hypotheses

## Null Hypothesis (H₀)

There is no significant difference between Spend_Before and Spend_After.

## Alternative Hypothesis (H₁)

There is a significant difference between Spend_Before and Spend_After.

---

# 📌 Excel Formula

```excel
=T.TEST(C6:C65,D6:D65,2,1)
```

---

# 📊 Result

```text
p < 0.001
```

---

# 🧠 Interpretation

Customer spending increased significantly after campaign exposure.

---

# 🧪 2️⃣ Independent t-Test

## Purpose

Determine whether Treatment customers outperformed Control customers.

---

# 📌 Why Independent t-Test Was Used

Because:
- Treatment and Control groups are unrelated
- groups are independent
- spending differences were compared between groups

---

# 📊 Hypotheses

## Null Hypothesis (H₀)

Treatment and Control groups have no significant difference in spending change.

## Alternative Hypothesis (H₁)

Treatment and Control groups have a significant difference in spending change.

---

# 📌 Step-by-Step Procedure

## Step 1 — Create Spend Difference

```excel
=[@Spend_After]-[@Spend_Before]
```

---

## Step 2 — Separate Groups

Create mini tables:
- Treatment_Diff
- Control_Diff

by filtering and copying spending differences.

---

## Step 3 — Run Independent t-Test

```excel
=T.TEST(Treatment_Range,Control_Range,2,3)
```

---

# 📌 Why Type 3 Was Used

Type 3 performs:
- unequal variance independent t-test
- Welch’s t-test

This is preferred for real-world business data.

---

# 📊 Result

```text
p < 0.001
```

---

# 🧠 Interpretation

Treatment customers significantly outperformed Control customers in spending improvement.

---

# 🧪 3️⃣ One-Sample t-Test

## Purpose

Determine whether average post-campaign spending achieved the expected business target.

---

# 📌 Benchmark Used

Since no business target existed in the dataset, a benchmark target of:

```text
200
```

was manually assumed.

---

# 📊 Hypotheses

## Null Hypothesis (H₀)

Average Spend_After = 200

## Alternative Hypothesis (H₁)

Average Spend_After ≠ 200

---

# 📌 Formula Breakdown

## Mean

```excel
=AVERAGE(D6:D65)
```

---

## Standard Deviation

```excel
=STDEV.S(D6:D65)
```

---

## Standard Error Formula

SE = s / √n

Where:

- s = Sample Standard Deviation
- n = Sample Size

---

## t-statistic Formula

t = (x̄ - μ) / (s / √n)

Where:

- x̄ = Sample Mean
- μ = Hypothesized / Target Mean
- s = Sample Standard Deviation
- n = Sample Size

---

## p-value

```excel
=T.DIST.2T(ABS(t_statistic),df)
```

---

# 📊 Result

| Metric | Value |
|---|---:|
| Sample Mean | 172 |
| Target | 200 |
| t-statistic | -3.064 |
| p-value | 0.00329 |

---

# 🧠 Interpretation

Average post-campaign customer spending remained significantly below the business target benchmark of 200.

---

# ⚠ Common Analyst Mistakes

- Using the wrong t-test type
- Comparing unrelated groups with paired tests
- Ignoring variance assumptions
- Misinterpreting p-values
- Assuming significance equals business success

---

# 🌍 Real-Life Applications

| Industry | Application |
|---|---|
| Marketing | Campaign effectiveness testing |
| Healthcare | Treatment effectiveness |
| Retail | Customer spending analysis |
| Finance | Portfolio comparison |
| HR Analytics | Performance intervention analysis |

---

# 🔥 Final Lesson Conclusion

This lesson introduced practical hypothesis testing workflows used by analysts to validate business claims using statistical evidence.

The dataset demonstrated that:
- customer spending increased significantly after campaign exposure
- campaign-exposed customers significantly outperformed control customers
- despite improvement, average spending still remained below the expected business benchmark

Together, these findings illustrate how statistical testing supports evidence-based business decision-making.

---

<footer>

**David Omotoye**  
*Statistics Learning Journey — Day 16*

</footer>
