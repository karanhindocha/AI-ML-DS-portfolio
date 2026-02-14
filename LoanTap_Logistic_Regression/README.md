# **💳 LoanTap Credit Risk Assessment**

## **Loan Approval Prediction using Logistic Regression**

# **📌 Problem Statement**

LoanTap is an online platform committed to delivering customized loan products to millennials. They innovate in an otherwise dull loan segment, to deliver instant, flexible loans on consumer friendly terms to salaried professionals and businessmen.

The data science team at LoanTap is building an underwriting layer to determine the creditworthiness of MSMEs as well as individuals. LoanTap deploys formal credit to salaried individuals and businesses 4 main financial instruments:

- Personal Loan
- EMI Free Loan
- Personal Overdraft
- Advance Salary Loan

This case study will focus on the underwriting process behind Personal Loan only.

# **🎯 Business Objective**
- Predict loan approval / default risk.
- Identify key factors influencing borrower creditworthiness.
- Optimize underwriting decisions.
- Reduce financial risk while maintaining approval rates.

# **📊 Dataset Overview**

**Target Variable: loan_status (Binary classification: Fully Paid vs Charged Off)**

##  **Dataset Data dictionary:**

- **loan_amnt:** The listed amount of the loan applied for by the borrower. If at some point in time, the credit department reduces the loan amount, then it will be reflected in this value.

- **term:** The number of payments on the loan. Values are in months and can be either 36 or 60.

- **int_rate:** Interest Rate on the loan.

- **installment:** The monthly payment owed by the borrower if the loan originates.

- **grade:** LoanTap assigned loan grade.

- **sub_grade:** LoanTap assigned loan subgrade.

- **emp_title:** The job title supplied by the Borrower when applying for the loan.

- **emp_length:** Employment length in years. Possible values are between 0 and 10 where 0 means less than one year and 10 means ten or more years.

- **home_ownership:** The home ownership status provided by the borrower during registration or obtained from the credit report.

- **annual_inc:** The self-reported annual income provided by the borrower during registration.

- **verification_status:** Indicates if income was verified by LoanTap, not verified, or if the income source was verified.

- **issue_d:** The month which the loan was funded.

- **loan_status:** Current status of the loan - Target Variable.

- **purpose:** A category provided by the borrower for the loan request.

- **title:** The loan title provided by the borrower.

- **dti:** A ratio calculated using the borrower’s total monthly debt payments on the total debt obligations, excluding mortgage and the requested LoanTap loan, divided by the borrower’s self-reported monthly income.

- **earliest_cr_line:** The month the borrower's earliest reported credit line was opened.

- **open_acc:** The number of open credit lines in the borrower's credit file.

- **pub_rec:** Number of derogatory public records.

- **revol_bal:** Total credit revolving balance.

- **revol_util:** Revolving line utilization rate, or the amount of credit the borrower is using relative to all available revolving credit.

- **total_acc:** The total number of credit lines currently in the borrower's credit file.

- **initial_list_status:** The initial listing status of the loan. Possible values are – W, F.

- **application_type:** Indicates whether the loan is an individual application or a joint application with two co-borrowers.

- **mort_acc:** Number of mortgage accounts.

- **pub_rec_bankruptcies:** Number of public record bankruptcies.

- **Address:** Address of the individual.

# **🧹 Data Cleaning & Feature Engineering**
## **Preprocessing Steps**

✔ Removed irrelevant & high-cardinality text fields

✔ Feature Engineering

✔ Converting the categorical features into the category type

✔ Ensure numeric columns are actually numeric

✔ Handled missing values (notably mort_acc, emp_length)

✔ Converted categorical variables via encoding

✔ Extracted time-based features from credit history

✔ Scalled numerical features

✔ Addressed class imbalance using class weights

# **📈 Exploratory Data Analysis (EDA)**
## **Risk Pattern Insights**
- Higher interest rates strongly correlate with defaults.
- Borrowers with high DTI ratios show increased default risk.
- Lower loan grades exhibit significantly higher charge-offs.
- High revolving utilization indicates financial stress.
- Longer employment history correlates with repayment reliability.

# **🤖 Logistic Regression Models**
**Model A - Basic Model**

**Model B - with class_weight = 'balanced'**

**Model C - with SMOTE using Pipeline**

# **🤖 Model Development**
- Encode target: Convert loan_status into binary 0/1
- Import the required libraries
- Train Test Split
- Missing Values Treatment
- Outlier Treatment
- Simple Feature Engineering steps (Creation of Flags)
- Encoding Categorical Features
- Scaling Numerical Features
- Logistic Regression Models
- Model Evaluation

## **Why Logistic Regression?**
- Interpretable risk probabilities.
- Suitable for binary classification.
- Enables precision–recall tradeoff tuning.
- Aligns with financial risk modeling standards.

# **⚖ Precision–Recall Tradeoff**

Since lending risk has asymmetric costs:
- False Positive (Approve risky borrower) → Financial loss.
- False Negative (Reject good borrower) → Lost business.
- Threshold tuning was performed to balance risk and approval volume.

# **📊 Model Performance**

<img width="594" height="220" alt="image" src="https://github.com/user-attachments/assets/b43994dd-c020-43c4-a462-240fad15d141" />

<img width="351" height="235" alt="image" src="https://github.com/user-attachments/assets/2ee478c7-2c12-47d1-8031-5ebba06e289c" />

<img width="583" height="234" alt="image" src="https://github.com/user-attachments/assets/6489b78c-62c4-42df-96f7-6eed8dd4120e" />

<img width="433" height="234" alt="image" src="https://github.com/user-attachments/assets/4e2e02c9-3d51-45e1-9bbc-5d94ec1ca2f6" />

<img width="590" height="233" alt="image" src="https://github.com/user-attachments/assets/2e45408b-df5e-487a-a379-dba540397c45" />

<img width="497" height="241" alt="image" src="https://github.com/user-attachments/assets/ecd59ac6-aafe-42a6-8497-874761f3de3c" />

## **Classification Metrics**
- Recall improved for detecting defaults.
- Balanced F1-score achieved.
- ROC-AUC indicates strong separability.

👉 Model effectively identifies high-risk borrowers while maintaining approval efficiency.

# **🔍 Key Risk Drivers**
## **Strong Default Predictors**

✅ High Interest Rate
✅ High Debt-to-Income Ratio
✅ Lower Loan Grade
✅ High Revolving Utilization
✅ Recent credit history & delinquencies

## **Indicators of Creditworthiness**

✅ Higher income levels
✅ Longer employment tenure
✅ Lower credit utilization
✅ Verified income sources

# **💡 Business Insights**

✔ Borrowers with high Dti & utilization show significant default risk.
✔ Loan grades effectively reflect borrower risk tiers.
✔ Verified income and employment stability improve repayment likelihood.
✔ Credit history depth strongly influences creditworthiness.

# **Key Insights:**

**1. Class Imbalance Dominates Baseline Performance**
- The Basic (Naive) model achieves high overall accuracy (80.6%) but extremely poor recall on Charged Off (0.99 → 0.63 in Balanced, 0.93 in SMOTE) — it heavily favors the majority class (Fully Paid).

**2. Imbalance Handling Significantly Improves Defaulter Detection**
- SMOTE gives the highest recall on Charged Off (92.78%) — catches most real defaulters.
- Balanced model offers the best precision-recall trade-off for Charged Off (precision 88.82%, recall 63.20%).
- Both outperform the naive model in F1-score for the minority class (0.87–0.74 vs 0.89 in naive, but naive precision is inflated by imbalance).

**3. ROC AUC is Stable, but PR AUC Shows True Value**
- ROC AUC remains similar (~0.66–0.71) across models — less sensitive to imbalance.
- PR AUC varies more (0.29–0.37) — SMOTE has lower PR AUC due to aggressive oversampling → highlights the precision cost

**4. Strong Multicollinearity in Features**
- loan_amnt and installment (~0.95) — high multicollinearity → drop one (installment recommended).
- open_acc and total_acc (~0.68) — related credit history features → consider keeping or creating ratio.
- pub_rec and pub_rec_bankruptcies (~0.70) — overlapping risk signals → keep pub_rec_bankruptcies (more specific).


# **Recommendations:**

1. **Primary Model Choice** → SMOTE for maximum defaulter detection (recall 92.78%) or Balanced for better overall trade-off (highest F1 for Charged Off at 0.7385)

2. **Threshold Tuning** → Use PR curve to lower threshold (0.35–0.45) on SMOTE/Balanced → push recall > 90% while keeping precision > 30–40%

3. **Feature Engineering** → Drop installment due to multicollinearity; consider open_acc/total_acc ratio; keep flags (mort_acc_flag, pub_rec_bankruptcies_flag) — they add value in SMOTE model

4. **Business Strategy**
Growth mode: SMOTE + threshold ~0.40 → high recall, more approvals, controlled NPAs. **Safety mode:** Balanced + threshold ~0.80 → very low NPA, fewer approvals but safer lending

5. **Final Choice** → Balanced model + adjustable threshold → best balance between catching defaulters and maintaining lending volume.

> **Customized Loan Products:** To improve product-market fit, create customized loan products for the most prevalent borrower classes.

> **Loan Term Structuring:** To reduce risk, give higher-grade loans more flexible terms while taking into account harsher conditions for lower-grade and longer-term loans.

> **Additional statistical analysis:** To make sure that lending strategies are data-driven, do further statistical tests to confirm the relevance of the connections and insights found.

> **Model Monitoring and Adjustment:** Keep an eye on credit scoring models and make necessary adjustments in response to shifts in borrower behavior and the state of the economy.

# **🛠 Tech Stack**
- Python
- Pandas & NumPy
- Seaborn & Matplotlib
- Scikit-learn
- Jupyter Notebook

# **⚠️ Limitations**
- Behavioral and transaction-level data not included.
- External credit bureau scores not available.
- Economic conditions and macro factors not considered.

# **🚀 Future Improvements**
- Try ensemble models (XGBoost, Random Forest)
- Implement probability-based risk scoring
- Deploy automated underwriting decision engine
- Build real-time risk dashboards

# **📌 Project Outcome**

**Developed an interpretable credit risk model enabling data-driven underwriting decisions, improving default detection and portfolio risk control.**
