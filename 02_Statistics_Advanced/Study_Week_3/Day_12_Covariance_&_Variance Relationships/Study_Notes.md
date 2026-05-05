# 📘 Day 12 Study Notes — Variance, Standard Deviation & Covariance Analysis

---

## 🎯 Lesson Objective
Understand variance, standard deviation, and covariance relationships across multiple variables to evaluate how business metrics vary individually and move together.

---

## 🧠 Core Concepts

### Variance
Measures how spread out a variable’s values are around its mean.

**Formula:**

Var(X) = Σ(x - x̄)² / (n - 1)

**Interpretation:**
- High Variance → Greater volatility / spread  
- Low Variance → More consistency / clustering  

---

### Standard Deviation
Square root of variance; expresses spread in original units.

**Formula:**

SD = √Variance

**Interpretation:**
- Easier to interpret than variance because units remain unchanged  

---

### Covariance
Measures how two variables move together.

**Formula:**

Cov(X,Y) = Σ[(x - x̄)(y - ȳ)] / (n - 1)

**Interpretation:**
- Positive → Variables move together  
- Negative → Variables move oppositely  
- Near Zero → Little directional relationship  

---

### Correlation vs Covariance
Covariance shows **direction** of movement, but correlation standardizes the relationship to show **strength**.

---

## 📊 Covariance vs Correlation Comparison

Covariance analysis revealed the **direction** in which business metrics move together, while correlation provided a **standardized measure of relationship strength**.

---

### Why Compare Covariance and Correlation?

Because each metric answers a different question:

| Metric | What It Tells You |
|---|---|
| **Covariance** | Whether variables move together or oppositely |
| **Correlation** | How strong that relationship is on a standardized scale (-1 to +1) |

---

### Correlation Pairs Evaluated

| Relationship | Purpose |
|---|---|
| Marketing Spend vs Sales Revenue | Standardize revenue driver relationship |
| Website Traffic vs Sales Revenue | Compare traffic impact vs marketing impact |
| Units Sold vs Sales Revenue | Measure sales-volume dependence |
| Units Sold vs Customer Complaints | Test operational strain |
| Website Traffic vs Customer Complaints | Test traffic/service relationship |
| Discount Rate vs Units Sold | Quantify discount effectiveness |
| Discount Rate vs Sales Revenue | Quantify revenue effect of discounts |

---

### Expected Analytical Outcome

You’ll likely find:

- Some **large covariances become only moderate correlations**
- Some **smaller covariances may reveal stronger standardized relationships**

---

### Core Statistical Insight

> Raw covariance magnitude can mislead without standardization.

Because covariance is influenced by variable scale, large covariance values do **not necessarily indicate stronger relationships**.

Correlation resolves this limitation by standardizing the relationship.

---

### Practical Analyst Takeaway

> Use **Covariance** to assess movement direction.  
> Use **Correlation** to assess relationship strength.

---

## 📈 Key Analytical Interpretation

| Analytical Area | Key Finding | Meaning |
|---|---|---|
| **Strongest Revenue Driver** | Units Sold vs Sales Revenue (**r = 0.975**) | Revenue is most directly influenced by sales volume. |
| **Strongest Marketing Lever** | Marketing Spend vs Sales Revenue (**r = 0.966**) | Marketing investment strongly aligns with revenue growth. |
| **Discount Effectiveness** | Moderate Positive Correlation | Discounts moderately improve both volume and revenue. |
| **Operational Efficiency Signal** | Moderate Negative Complaint Relationships | Complaints decline as sales/traffic rise, suggesting scalable operations. |

---

## 📊 Key Dataset Insights

### Revenue Drivers
- Marketing Spend and Sales Revenue move positively together.
- Website Traffic and Sales Revenue also move positively.
- Units Sold positively aligns with Sales Revenue.

---

### Operational Impact
- Increased Units Sold did not correspond with more customer complaints.
- Website Traffic also showed no positive complaint relationship.

---

### Discount Effects
- Discounts appear to increase Units Sold.
- Discounts may contribute positively to overall Sales Revenue.

---

## 📌 Why Variance and Standard Deviation Were Included

Variance and standard deviation were computed before covariance analysis because covariance measures **joint variability**, which depends on each variable’s individual spread.

Understanding standalone dispersion helps contextualize covariance values and prevents misinterpretation.

---

## 🧩 Integrated Statistical Interpretation

Variance and standard deviation established the volatility profile of each business metric, covariance identified directional movement between variables, and correlation standardized those relationships to reveal their true strength.

Together, these measures provided a layered understanding of both standalone metric behavior and multivariable business interactions.

---

## 🔍 Analyst Best Practice

Before interpreting covariance:

1. Review Variance / Standard Deviation  
2. Understand Variable Scale Differences  
3. Use Correlation for Standardized Strength Comparison  

---

## 🏁 Lesson Conclusion

Variance and standard deviation establish the standalone volatility of each business metric, while covariance reveals how those metrics move together.

Together, these measures provide foundational insight into both individual metric stability and multivariable business relationships.

---

<footer>

**David Omotoye**  
*Statistics Learning Journey — Day 12*

</footer>
