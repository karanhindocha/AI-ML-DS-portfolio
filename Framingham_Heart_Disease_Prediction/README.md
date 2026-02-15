# **❤️ Framingham Heart Disease Prediction**
# **📌 Project Overview**

Cardiovascular disease remains one of the leading causes of mortality worldwide. Early identification of individuals at high risk enables preventive care and improved health outcomes. This project uses the Framingham Heart Study dataset to build predictive models that estimate the 10-year risk of coronary heart disease (CHD) using demographic, behavioral, and clinical health indicators. The goal is to develop an interpretable and reliable model while demonstrating rigorous data analysis and preprocessing decisions.

# **🎯 Objectives**
- Perform exploratory data analysis (EDA) to identify key cardiovascular risk patterns.
- Handle missing values using clinically sound strategies.
- Address class imbalance.
- Build and evaluate predictive models.
- Interpret risk factors influencing heart disease.

# **📊 Dataset Description**
**1. Patient Demographics:**

**Male:** Binary (1 = Male; 0 = Female).

**Age:** Continuous; the age of the patient in years.

**Education:** Categorical (1-4); levels typically ranging from some high school to a college degree.

**2. Behavioral Factors:**

**Current Smoker:** Binary (1 = Current smoker; 0 = Non-smoker).

**Cigs Per Day:** Continuous; average number of cigarettes smoked daily.

**3. Medical History:**

**BP Meds:** Binary (1 = On blood pressure medication; 0 = Not).

**Prevalent Stroke:** Binary (1 = Patient previously had a stroke; 0 = No).

**Prevalent Hyp:** Binary (1 = Patient was hypertensive; 0 = No).

**Diabetes:** Binary (1 = Patient has diabetes; 0 = No).

**4. Clinical Measurements:**

**Tot Chol:** Continuous; total cholesterol level in mg/dL.

**Sys BP:** Continuous; systolic blood pressure (top number).

**Dia BP:** Continuous; diastolic blood pressure (bottom number).

**BMI:** Continuous; Body Mass Index ((weight/height)^2).

**Heart Rate:** Continuous; beats per minute.

**Glucose:** Continuous; blood glucose level in mg/dL.

**5. Target Variable:**

**TenYearCHD:** Binary (1 = Developed coronary heart disease within 10 years; 0 = Did not).

# **🔎 Exploratory Data Analysis (EDA)**

EDA was performed to understand feature distributions, relationships, and cardiovascular risk patterns.

## **Key Analyses Performed**
✔ Target class distribution.

✔ Categorical feature distributions & CHD relationships.

✔ Numerical feature distributions & outlier detection.

✔ Pairwise relationships and correlation analysis.

✔ Risk factor comparison against CHD outcome.

## **Additional Risk Insights Explorable Through EDA:**
- CHD risk increases significantly with age.
- Hypertension and elevated systolic BP strongly correlate with CHD.
- Smoking intensity increases cardiovascular risk.
- Diabetes and elevated glucose indicate metabolic risk.
- Higher BMI combined with high BP increases risk.

# **🧹 Data Preprocessing**
## **Missing Value Analysis**
- Imputing the following features to handle the missing values:
1. cigsPerDay, totChol, BMI, heartRate, glucose -> imputed with median
2. BPMeds -> imputed with mode
3. Dropped the education feature since it is redundant

## **Why Median/Mode Imputation?**
- Robust to outliers.
- Clinically interpretable.
- Maintains dataset size and statistical power.

# **⚖️ KNN Imputation Consideration**

- KNN imputation was explored to handle missing values (notably ~9% missing in glucose) because it can leverage similarities between patients and relationships among health indicators. However, it was not included in the final pipeline because:
1. No meaningful performance gain over median/mode imputation in recall or ROC-AUC.
2. Simpler methods improve interpretability, which is important in healthcare risk modeling.
3. Logistic regression performs reliably with robust central-tendency imputations.
4. Reduced complexity improves reproducibility and deployment readiness.

Therefore, median imputation (numerical) and mode imputation (categorical) were retained to balance performance, transparency, and practical usability.

# **⚖️ Class Imbalance Handling**

The dataset contains fewer CHD-positive cases. To address this:
1. Class weighting
2. SMOTE oversampling

were evaluated to improve recall and minority class detection.

# **🤖 Models Implemented**
**Logistic Regression**
- Class-weight balanced model
- SMOTE-enhanced model

**K-Nearest Neighbors (KNN)**
- Evaluated with multiple k values.

**XGBoost Classifier:**
- Captures nonlinear relationships.
- Evaluated for performance comparison.

# **📈 Model Evaluation Metrics**
- Models were evaluated using Accuracy, Recall (critical for disease detection), Precision, F1-score, ROC-AUC, Confusion Matrix.
- Recall was prioritized to minimize missed high-risk patients.

## **🔬 Key Findings**
### Risk Factors Associated with CHD:**

✔ Age is the strongest predictor.

✔ Hypertension significantly increases risk.

✔ Elevated systolic BP correlates strongly with CHD.

✔ Smoking and cigarette consumption increase risk.

✔ Diabetes and glucose levels indicate metabolic risk.

✔ Higher BMI contributes to cardiovascular strain.

# **🧠 Most Influential Risk Factors (Ranked)**
🔴 Strong Predictors

✔ Age
✔ Systolic BP
✔ Hypertension

🟠 Moderate Predictors

✔ Glucose / Diabetes
✔ Smoking intensity
✔ Cholesterol

🟡 Supporting Predictors

✔ BMI
✔ Heart rate

# **📊 Model Performance**
## **Building models after dropping missing values in the dataset:**

<img width="615" height="619" alt="image" src="https://github.com/user-attachments/assets/3052d799-5c05-4c37-be9d-e729ee96b039" />

<img width="589" height="621" alt="image" src="https://github.com/user-attachments/assets/133187ec-27d5-450a-a8a8-af4215280128" />

<img width="537" height="603" alt="image" src="https://github.com/user-attachments/assets/1889985e-166f-4ff5-ad68-7d46648e2f85" />

<img width="572" height="366" alt="image" src="https://github.com/user-attachments/assets/dd569936-2da6-4d3a-ae54-669b8459c79c" />

<img width="502" height="598" alt="image" src="https://github.com/user-attachments/assets/dd5e3e28-f518-4670-a40e-8b489ce0a5f1" />

<img width="566" height="619" alt="image" src="https://github.com/user-attachments/assets/aede9861-09f2-4d15-9570-36572fe117ba" />

<img width="523" height="616" alt="image" src="https://github.com/user-attachments/assets/cbb7a72d-99d1-445e-bbfc-e86a131bc447" />

## **Building models after missing values imputation in the dataset:**

<img width="539" height="618" alt="image" src="https://github.com/user-attachments/assets/df040610-f1e2-449c-bc1e-9c4c99b0c659" />

<img width="532" height="616" alt="image" src="https://github.com/user-attachments/assets/a319034d-8e6d-4216-8c9f-619588a13a37" />

<img width="526" height="601" alt="image" src="https://github.com/user-attachments/assets/7af1ea04-db14-4364-ac2a-9d85104e9341" />

<img width="530" height="366" alt="image" src="https://github.com/user-attachments/assets/8381eceb-302c-4c1c-ba20-cc3413051784" />

<img width="494" height="600" alt="image" src="https://github.com/user-attachments/assets/08178575-e02f-4f7a-8d29-496a9b5387d1" />

<img width="545" height="613" alt="image" src="https://github.com/user-attachments/assets/a0453952-3851-40b8-86c5-ac977c24a51d" />

<img width="562" height="617" alt="image" src="https://github.com/user-attachments/assets/a7e4d775-60dc-41b7-9f9e-9bf9a0e9ba7f" />

# **🏆 Final Insights**

- Cardiovascular risk is driven by age, blood pressure, metabolic health, and smoking behavior.
- Preventive screening should prioritize individuals with hypertension, diabetes, and elevated systolic BP.
- Lifestyle interventions targeting smoking cessation and weight management can reduce long-term CHD risk.

# **🧠 Skills Demonstrated**

- Exploratory Data Analysis & risk interpretation.
- Missing data strategy & clinical reasoning.
- Class imbalance handling.
- Predictive modeling & evaluation.
- Healthcare-focused model interpretability.

# **🚀 Future Improvements**

- Feature engineering for risk scoring. 
- Calibration of predicted probabilities.
- Model explainability using SHAP.
- Deployment as a risk assessment tool.

# **🛠️ Tech Stack**

- Python
- Pandas & NumPy
- Matplotlib & Seaborn
- Scikit-learn
- XGBoost
