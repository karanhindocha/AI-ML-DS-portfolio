# **🎓 Jamboree Education — Admission Chance Prediction**

## **Linear Regression Case Study**

# **📌 Problem Statement**

Jamboree Education helps students secure admissions to top international universities. They introduced a feature that estimates a student’s probability of admission into Ivy League institutions.

This project analyzes admission factors and builds a predictive model to estimate admission chances from an Indian applicant perspective.

# **🎯 Business Objective**

- Identify the factors influencing graduate admission chances.
- Understand relationships between academic and profile variables.
- Build a model to predict admission probability.
- Enable data-driven student guidance and counseling.

# **📊 Dataset Overview**

**Number of Records: 500 applicants**

**Target Variable: Chance of Admit (0–1 probability)**

## **Features**

- GRE Score (out of 340)
- TOEFL Score (out of 120)
- University Rating (1–5)
- SOP Strength (1–5)
- LOR Strength (1–5)
- CGPA (out of 10)
- Research Experience (0 = No, 1 = Yes)

# **🧹 Data Cleaning & Preparation**

✔ No missing values or duplicates

✔ Column renaming & formatting

✔ Outlier check (minimal impact)

✔ Train-Test split: 80/20

✔ Assumptions tested before modeling

# **📈 Exploratory Data Analysis (EDA)**
## **Key Observations:**

1. Admission chances cluster around 0.7, indicating a strong applicant pool.
2. GRE & TOEFL scores are normally distributed, reflecting competitive applicants.
3. CGPA is concentrated between 8.0–9.0.
4. SOP & LOR ratings are mostly mid-to-high (3–4).
5. Research experience appears frequently among higher admission probabilities.

## **Correlation Insights:**
1. CGPA shows the strongest correlation with admission chance.
2. GRE and TOEFL scores have strong positive relationships.
3. Research experience contributes positively to outcomes.

# **🤖 Model Development**
Model Used: Multiple Linear Regression

## **Why Linear Regression?**
- Target variable is continuous.
- Enables interpretability of feature influence.
- Suitable for understanding admission drivers.

# **Assumptions Checked**

✔ Linearity
✔ Multicollinearity (VIF < 5)
✔ Normality of residuals
✔ Shapiro-Wilk test, Q-Q plot
✔ Goldfeld-Quandt test for heteroskedasticity

# **📊 Model Performance**

**OLS Regression Results:** R²: 0.821 and Adjusted R²: 0.818

**Model Performance Metrics:**
MAE: 0.0425, RMSE: 0.0594, R²: 0.8211, Adjusted R²: 0.8179

**Test Performance:** MAE: 0.0425 and RMSE: 0.0594.

**👉 Model explains ~82% of variance in admission probability.**

**Ridge Regression Validation:** Test R²: 0.8188.

**Ridge Regression Performance:** Train RMSE: 0.0594, R²: 0.8211. Test RMSE: 0.0609, R²: 0.8188

**Lasso Regression Validation:** Test R²: 0.8192.

**Lasso Regression Performance:** Train RMSE: 0.0594, R²: 0.8210. Test RMSE: 0.0608, R²: 0.8192

**👉 Confirms model stability and low overfitting.**

# **🔍 Feature Importance & Interpretation**
## **Statistically Significant Predictors:**

✅ CGPA (strongest impact)
✅ GRE Score
✅ TOEFL Score
✅ LOR Strength
✅ Research Experience

## **Not Statistically Significant Predictors:**

✅ University Rating
✅ SOP Strength

# **💡 Key Insights**

✔ CGPA is the strongest predictor of admission success.

✔ Higher GRE & TOEFL scores significantly improve chances.

✔ Strong Letters of Recommendation positively influence outcomes.

✔ Research experience increases admission probability.

✔ University rating & SOP strength have limited predictive impact when other factors are considered.

# **Significance of Predictor Variables:**
**CGPA** shows the highest positive association with Chance of Admit, suggesting that consistent academic performance is the most critical factor influencing admission decisions.

**GRE Score and TOEFL Score** also exhibit strong positive relationships with the target variable, reinforcing the importance of standardized test performance in evaluating applicants.

**University Rating, SOP, and LOR** demonstrate moderate positive influence, indicating that qualitative assessments and institutional reputation contribute meaningfully, though to a lesser extent than academic scores.

**Research Experience** has a positive but comparatively weaker effect, implying that while research exposure improves admission chances, it acts more as a supporting factor rather than a primary determinant.

# **Actionable Insights & Recommendations:**
**Data Enhancement:** Model performance can be improved by adding contextual variables such as undergraduate institution ranking, field of study, work/internship experience, and research output, which are not captured in the current dataset.

**Real-World Use:** The model is best used as a decision-support tool for preliminary screening and applicant self-assessment, benefiting from the interpretability of linear and regularized regression models.

**Business Value:** A data-driven admission scoring system can reduce manual screening effort, ensure consistent evaluation, and improve candidate prioritization and admission yield.

**Overall Recommendation:** With richer features and periodic retraining, the model can scale into a transparent and reliable analytics tool for supporting graduate admissions decisions.

# **🛠 Tech Stack**

- Python
- Pandas & NumPy
- Matplotlib & Seaborn
- Statsmodels
- Scikit-learn
- Google Colab

# **⚠️ Limitations**

- Dataset represents strong applicants; may not generalize globally.
- Non-academic factors (essays, interviews, extracurriculars) not included.
- Some assumption deviations suggest potential nonlinear relationships.

# **🚀 Future Improvements**

- Try ensemble models (Random Forest, Gradient Boosting).
- Include additional profile attributes.
- Build an interactive admission probability calculator.
- Deploy as a web app.

# **📌 Project Outcome**

**Built a robust predictive model explaining 82% of admission probability variance, enabling data-driven admission guidance.**
