# **📈 AdEase Time Series Forecasting**
Forecasting Wikipedia Page Views using ARIMA, SARIMAX & Prophet.

# **📌 Problem Statement**

AdEase is a digital advertising platform that helps businesses maximize clicks while minimizing advertising costs. To improve ad placement and campaign effectiveness, AdEase needs accurate forecasts of Wikipedia page traffic across different languages and regions.

The objective of this project is to analyze daily page view data for over 145,000 Wikipedia pages spanning 550 days and forecast future traffic patterns using time series modeling techniques. These forecasts can help optimize ad inventory allocation, campaign planning, and audience targeting across multiple geographies.

# **🎯 Business Objective**
- Forecast future Wikipedia page traffic to optimize advertising decisions.
- Identify traffic patterns across languages and regions.
- Compare multiple forecasting techniques and select the most accurate model.
- Improve ad placement strategies through demand forecasting.
- Understand the impact of external campaign events on page traffic.

# **📊 Dataset Overview**
Primary Dataset: train_1.csv

145,063 Wikipedia pages

550 daily observations per page

Time period: 1 July 2015 – 31 December 2016

Multi-language traffic covering English, Chinese, Japanese, German, French, Russian, Spanish, Wikimedia Commons, and MediaWiki

Exogenous Dataset: Exog_Campaign_eng

Campaign indicator for English pages

Binary variable: 1 → Campaign/Event Day and 0 → Regular Day

Used as an exogenous feature in SARIMAX forecasting.

# **🧹 Data Cleaning & Feature Engineering**
**Preprocessing Steps**

- Converted 550 date columns into proper datetime format.
- Analyzed missing data patterns.
- Forward-filled missing values and handled page creation gaps.
- Parsed page metadata into: Title, Language, Access Type, and Access Origin.
- Extracted language identifiers for region-wise analysis.
- Created stratified language samples for scalable modeling.
- Converted data into time-series compatible structures for forecasting models.

# **📈 Exploratory Data Analysis (EDA)**
**Dataset Characteristics:**
- Dataset contains 145k+ pages and 550 days of observations.
- Overall sparsity was 7.75%.
- Missing values were concentrated in early dates due to pages being created after the observation period began.
- Traffic distributions showed heavy positive skew driven by a small number of highly popular pages.

# **Key Visual Insights**
- Strong weekly seasonality observed across page traffic.
- English pages generated the highest total page views.
- Traffic volumes differed significantly across language groups.
- Page-view distribution is highly right-skewed.
- Sudden spikes suggested the impact of external events and trending topics.

# **📊 Stationarity Analysis**

Before forecasting, stationarity was evaluated using:

Techniques Applied

Augmented Dickey-Fuller (ADF) Test

Time Series Decomposition

Differencing

Log Transformation

ACF Analysis

PACF Analysis

# **Findings**
- Raw high-traffic series was stationary.
- Log-transformed series became stationary after first-order differencing (d = 1).
- Weekly seasonality was identified as a significant pattern.

# **🤖 Models Implemented**
## **1️⃣ ARIMA**

### **Approach:**
Log Transformation

First-Order Differencing

ACF/PACF-Based Parameter Selection

Hyperparameter Tuning using AIC

### **Models Evaluated:**

ARIMA(1,1,1)

ARIMA(2,1,1)

ARIMA(1,1,2)

### **Best Model:** ARIMA(2,1,1)

### **Performance:** MAPE	1.23%

ARIMA delivered the best forecasting accuracy after variance stabilization through log transformation.

## **2️⃣ SARIMAX**
### **Approach:**
Weekly seasonality modeling

Campaign event data used as exogenous variable

Hyperparameter tuning using AIC

### **Best Model:** SARIMAX(1,1,2) × (1,1,1,7)

### **Performance:** MAPE	11.72%

While SARIMAX captured trend and seasonality successfully, the sparse campaign signal limited predictive improvement.

## **3️⃣ Prophet**
### **Approach:**

Weekly seasonality modeling

Changepoint sensitivity tuning

Multiplicative seasonality experiments

### **Best Configuration**

Weekly Seasonality

Changepoint Prior Scale = 0.5

### **Performance:** MAPE	13.46%

Prophet captured overall trends but underperformed relative to ARIMA due to the relatively stable nature of the time series.

# **🏆 Model Comparison:**

ARIMA	1.23%

SARIMAX	11.72%

Prophet	13.46%

# **Best Performing Model:** ARIMA (2,1,1)

The combination of log transformation, differencing, and parameter tuning resulted in significantly superior forecasting accuracy.

# **🔍 Key Insights**
## **Traffic Insights**
- Strong weekly seasonality exists across Wikipedia traffic.
- English-language pages generated the highest traffic volumes.
- Page view distribution is highly concentrated among a small subset of pages.
- Traffic spikes are influenced by external events and trending topics.

## **Modeling Insights**
- Data preprocessing had the greatest impact on forecasting performance.
- Log transformation reduced MAPE from approximately 16.5% to 1.23%.
- ARIMA outperformed more sophisticated models when data was well-structured.
- Exogenous campaign data added limited value due to sparse event occurrences.

# **💡 Business Recommendations**
- Use ARIMA as the primary forecasting framework for page-view prediction.
- Prioritize ad spend and inventory allocation toward high-traffic language segments.
- Incorporate richer event and holiday data to improve SARIMAX performance.
- Monitor traffic spikes to identify emerging trends and advertising opportunities.
- Use Prophet for future use cases involving non-linear trends and structural changes.

# **🛠 Tech Stack**

Python

Pandas

NumPy

Matplotlib

Seaborn

Statsmodels

Facebook Prophet

Scikit-learn

Jupyter Notebook

# **🚀 Future Improvements**
- Auto-ARIMA for automated parameter optimization.
- Bayesian Optimization for scalable model tuning.
- Multi-series forecasting pipelines.
- Holiday and event-based forecasting features.
- Deep Learning models (LSTM, TFT, N-BEATS).
- Hierarchical forecasting across languages and regions.

# **📌 Project Outcome**

Built an end-to-end multilingual traffic forecasting solution for Wikipedia pages using ARIMA, SARIMAX, and Prophet, achieving 1.23% MAPE with a tuned ARIMA model and demonstrating how accurate traffic forecasting can optimize ad placement and digital marketing decisions across global audiences.
