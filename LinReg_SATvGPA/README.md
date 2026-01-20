# Linear Regression: SAT Scores vs GPA

# 📌 Project Overview

This project analyzes the relationship between **SAT scores and college GPA** using **linear regression** across two datasets. The goal is to understand how well standardized test scores and prior academic performance explain college-level academic outcomes.

# 📊 Datasets

### Dataset 1: Multivariate Academic Performance

**Model:**
`fy_gpa = -1.008 + 0.128·sex + 0.016·sat_sum + 0.550·hs_gpa`

**Features:**

* `sex` (encoded categorical variable)
* `sat_sum` (combined SAT score)
* `hs_gpa` (high school GPA)

**Target:**

* `fy_gpa` – First-year college GPA

---

### Dataset 2: Simple Linear Relationship

**Model:**
`GPA = 0.471 + 0.002·SAT`

**Features:**

* `SAT` – Standardized test score

**Target:**

* `GPA` – College GPA

# 🔍 Exploratory Data Analysis (EDA)

* Distribution analysis of SAT scores and GPA
* Scatter plots to visualize linear relationships
* Detection of outliers and range constraints

EDA confirmed a **positive but varying strength relationship** between SAT scores and GPA across datasets.

## Model Interpretation & Insights

### Dataset 1 Insights

* **High School GPA is the strongest predictor** of college GPA.
  A 1-point increase in HS GPA is associated with a **0.55 increase in first-year GPA**, holding other variables constant.

* **SAT score has a positive but smaller effect**.
  A 100-point increase in SAT corresponds to an approximate **0.16 increase in GPA**.

* **Gender shows a measurable difference** in GPA outcomes (based on encoding), suggesting structural or behavioral factors beyond academics.

---

### Dataset 2 Insights

* SAT score alone explains **only a small portion** of GPA variance.
* A 100-point increase in SAT increases GPA by approximately **0.2 points**, indicating limited predictive power when used in isolation.

# ✅ Key Findings & Recommendations

- SAT score alone is not sufficient to accurately predict academic performance.

- College admissions and academic support programs should place greater emphasis on high school GPA rather than SAT scores alone when predicting student success.

- Standardized tests add value but should be treated as supplementary indicators, not primary decision drivers.

- Observed gender differences suggest the need for additional non-academic factors (study habits, course load, support systems) in future models.

- Institutions relying only on standardized test scores may misestimate student potential.

# Limitations

* Linear regression assumes linearity and does not capture non-linear academic patterns.
* Important factors such as study habits, course difficulty, socioeconomic background, and institutional support are not included.

# 🛠️ Tech Stack

Python

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn
