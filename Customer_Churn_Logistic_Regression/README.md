# **📉 Telco Customer Churn Prediction Logistic Regression**

# **📌 Problem Statement**

Customer churn is a major challenge in the telecom industry. Losing existing customers increases acquisition costs and reduces profitability. This project builds a predictive model to identify customers likely to churn and uncovers the factors driving attrition, enabling proactive retention strategies.

# **🎯 Business Objective**
- Predict customers at risk of churn.
- Identify key churn drivers.
- Enable proactive retention interventions.
- Improve customer lifetime value (CLTV).
- Reduce revenue loss

# **📊 Dataset Overview**

Dataset: Telco Customer Churn

Records: ~7,000 customers

Target Variable: Churn (Yes = customer left, No = retained)

## **📘 Column Description**
### **👤 Customer Demographics**
**gender** — Male / Female

**SeniorCitizen** — 0 = No, 1 = Yes

**Partner** — Has a partner

**Dependents** — Has dependents

### **📁 Account Information**

**tenure** — Number of months with the company

**Contract** — Month-to-month, One year, Two year

**PaperlessBilling** — Yes / No

**PaymentMethod** — Mode of payment

### **📡 Services Subscribed**

**PhoneService**

**MultipleLines**

**InternetService**

**OnlineSecurity**

**OnlineBackup**

**DeviceProtection**

**TechSupport**

**StreamingTV**

**StreamingMovies**

### **💰 Billing Information**

**MonthlyCharges** — Monthly bill amount

**TotalCharges** — Total amount billed

Services that each customer has signed up for – phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies.

Customer account information – how long they’ve been a customer, contract, payment method, paperless billing, monthly charges, and total charges Demographic info about customers – gender, age range, and if they have partners and dependents.

### **🎯 Target Variable**

**Churn** — Whether the customer discontinued service

# **🧹 Data Cleaning & Preparation**

✔ Converted TotalCharges to numeric.

✔ Dropped irrelevant fields.

✔ Handled missing values & inconsistencies.

✔ Encoded categorical variables.

✔ Feature scaling applied.

✔ Train-test split (80:20).

✔ Addressed class imbalance.

✔ Evaluated using precision–recall tradeoff.

# **📈 Exploratory Data Analysis (EDA)**
## **Key Observations**
- Customers with month-to-month contracts churn significantly more.
- Short tenure customers are at highest risk.
- Higher monthly charges correlate with churn.
- Customers lacking tech support & security services churn more.
- Electronic check payments show elevated churn rates.

# **🤖 Model Development**
Model Used: Logistic Regression

Models Built: Baseline Logistic Regression and Balance-Weighted Logistic Regression.

## **Approach:**

1. Define X and y
2. Train Test Split
3. Scaling
4. model.fit()
5. Predictions
6. Confusion Matrix, Classification Report
7. Making predictions on unseen data

## **Why Logistic Regression?**
- Suitable for binary classification.
- Produces interpretable churn probabilities.
- Enables precision–recall optimization.
- Widely used in customer retention analytics

# **⚖ Precision–Recall Tradeoff**

Churn prediction requires balancing business costs:

False Negative → Lose a customer

False Positive → Retentive offer cost

The model prioritizes improved recall to identify at-risk customers early.

# **📊 Model Performance**
**Evaluation Metrics:** Accuracy, Precision, Recall, F1 Score, ROC-AUC.

The balanced logistic regression model improved detection of churners while maintaining reasonable precision.

👉 Enables targeted retention without excessive incentive costs.

## **Baseline Logistic Regression Performance:**

<img width="534" height="618" alt="image" src="https://github.com/user-attachments/assets/73c61380-a8c0-4aff-a20d-ac1a5fc5cb8b" />

## **Balance-Weighted Logistic Regression:**

<img width="560" height="617" alt="image" src="https://github.com/user-attachments/assets/585c4f22-30d8-4d44-997f-f05a8862f3ff" />

# **Model Performance Summary:**
**Baseline Logistic Regression**

Accuracy: ~81%

Churn Recall: ~56%

Precision: ~66%

ROC-AUC: ~0.84

**Balanced Logistic Regression**

Accuracy: ~74%

Churn Recall: ~78%

Precision: ~50%

ROC-AUC: ~0.84

Both models achieve similar ROC-AUC scores, indicating comparable ranking ability, but they differ significantly in how they trade off precision and recall.

# **🔍 Key Churn Drivers**
**Strong Indicators of Churn Risk**

⚠ Month-to-month contracts
⚠ High monthly charges
⚠ Short tenure
⚠ Electronic check payment method

## **Indicators of Customer Retention**

✅ Long-term contracts

✅ Longer tenure

✅ Tech support & online security services

✅ Lower monthly charges

# **💡 Business Insights**

✔ The first 6–12 months are critical for retention.

✔ Contract type is one of the strongest predictors of churn.

✔ Value-added services increase customer stickiness.

✔ Pricing perception influences churn decisions.

# **🧠 Strategic Recommendations**
## **🎯 Immediate Retention Actions**

✅ Target new customers with onboarding engagement programs

✅ Offer incentives to convert month-to-month users into annual plans

✅ Provide retention offers for high-bill customers

## **📊 Service Strategy**
- Bundle tech support & security add-ons.
- Provide loyalty rewards for long-tenure customers.

## **📈 Long-Term Strategy**
- Deploy churn risk scoring dashboard.
- Implement automated retention triggers.
- Personalize offers based on churn probability.

# **Insights and Recommendations:**

- Customers on month-to-month contracts exhibit the highest churn rates.

- Electronic check users churn more compared to customers using automatic payment methods.

- Short-tenure customers and those with higher monthly charges are more likely to churn.

- Balanced Logistic Regression significantly improves churn detection at the cost of more false positives.

- Use the Balanced Logistic Regression model for churn prevention campaigns where missing a churner is costly.

- Target high-risk segments such as month-to-month customers and electronic check users with retention offers.

- Encourage long-term contracts and automatic payment methods through incentives.

- Focus proactive retention efforts on early-tenure customers with high monthly charges.

# **🛠 Tech Stack**

- Python
- Pandas & NumPy
- Matplotlib & Seaborn
- Scikit-learn
- Jupyter Notebook

# **⚠️ Limitations**
- No behavioral usage metrics included.
- Competitor pricing not considered.
- Static dataset (no time-based churn prediction).

# **🚀 Future Improvements**

- Apply ensemble models (Random Forest, XGBoost).
- Implement SHAP for explainability.
- Deploy real-time churn prediction API.
- Perform survival analysis for churn timing.

# **📌 Project Outcome**

Developed a churn prediction model that enables proactive retention strategies, helping telecom providers reduce customer attrition and improve long-term revenue.
