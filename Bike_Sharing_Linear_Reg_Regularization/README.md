# **🚲 Bike Sharing Demand Prediction**

# **📌 Project Overview**

Bike sharing systems have become an essential part of urban mobility, offering an eco-friendly and convenient transportation alternative. Accurate demand forecasting enables operators to optimize bike availability, improve customer satisfaction, and manage resources efficiently. This project builds a predictive model to estimate hourly bike rental demand using environmental, seasonal, and temporal factors.

# **🎯 Problem Statement**

Given historical bike rental data along with weather and time-related features, predict the number of bikes rented in a given hour.

- Identify the key factors influencing bike rental demand.
- Understand how weather, seasonality, and time impact usage patterns.
- Build a machine learning model to accurately forecast bike demand.
- Provide actionable insights for operational planning and resource optimization.

# **📊 Dataset Description**

The dataset contains day-wise and hourly rental data along with weather and seasonal information.

**count** — Total number of bike rentals (casual + registered) (**Target Variable**)

## **🕒 Date and Time Based Features**

**instant:** record index

**datetime** — date of rental data

**season** — Season of the year (1: Spring, 2: Summer, 3: Fall, 4: Winter)

**month** — Month of the year

**year** — Year

**holiday** — Whether the day is a holiday (0 = No, 1 = Yes)

**weekday** — Day of the week

**workingday** — Whether the day is a working day (0 = No, 1 = Yes)

## **🌦 Weather Features**

**weather** — Weather condition (1: Clear, 2: Mist/Cloudy, 3: Light Rain/Snow, 4: Heavy Rain/Snow)

**temp** — Temperature in Celsius

**atemp** — Feels-like temperature in Celsius

**humidity** — Humdity percentage

**windspeed** — Wind speed

## **👥 User Segmentation**

**casual** — Rentals by casual users

**registered** — Rentals by registered users

# **🛠️ Concepts & Techniques Used**

Exploratory Data Analysis (EDA)

Feature Engineering

Handling categorical & cyclical time features

Outlier & skewness treatment

Regularization

# **Regression Modeling:**

Baseline Linear Regression (OLS)

Regularized Regression (Ridge/Lasso)

# **Model Evaluation Metrics:**

RMSE

MAE

R² Score

# **🔍 Exploratory Data Analysis**
- **High multicollinearity** exists between temp and atemp (corr ≈ 0.99) and between season and month (corr ≈ 0.83), suggesting one from each pair can be dropped in simple models.
- **Strongest predictors of day data** for count are temp/atemp (≈ 0.63), year (≈ 0.57–0.59), and weather-related features (weathersit ≈ -0.3, windspeed ≈ -0.23, humidity weak negative).
- **Strongest predictorsof hour data** for count are registered (≈ 0.97), casual (≈ 0.69), temp/atempyear (≈ 0.4), and hour (≈ 0.39).
- casual (≈ 0.67) and registered (≈ 0.95) show very **high correlation** with count as they are direct components → must be excluded to prevent leakage.
- **Other features** like holiday, weekday, and workingday have mostly weak correlations with the target and other variables, but remain useful in combination with regularization. Demand trends by hour, weekday, and season.

# **🤖 Modeling Approach**

1. Import the required libraries
2. Data cleaning and preprocessing
3. Feature engineering from datetime
4. Load and prepare data
5. Train Validation Test Split
6. Encoding categorical variables
7. Scaling numerical variables
8. Model training and evaluation
9. Model comparison and optimization

**🤖 Model Performance**

# **Day Data:**

<img width="595" height="256" alt="image" src="https://github.com/user-attachments/assets/75026e03-d883-497f-bac8-cd9ac162c62d" />

<img width="392" height="185" alt="image" src="https://github.com/user-attachments/assets/65b25f93-eb10-48f6-850a-98c7be661f72" />

<img width="417" height="168" alt="image" src="https://github.com/user-attachments/assets/42bef958-e01b-44d3-b278-3bd4445d2f7a" />

<img width="439" height="184" alt="image" src="https://github.com/user-attachments/assets/4035275e-5d9e-4b45-a6ef-722f759d58a0" />

<img width="1389" height="1229" alt="image" src="https://github.com/user-attachments/assets/7baaa5d8-21b6-4a5b-8bc5-de3848cde104" />

<img width="329" height="98" alt="image" src="https://github.com/user-attachments/assets/354bf83c-1247-47b5-b163-57847f4d0b7e" />

<img width="476" height="113" alt="image" src="https://github.com/user-attachments/assets/c788fc6f-e43a-4ad5-b65d-9d43f3bee8b1" />

# **Hour Data:**

<img width="562" height="257" alt="image" src="https://github.com/user-attachments/assets/32d549c5-60e4-4a78-a445-9a70ce3a9dee" />

<img width="392" height="181" alt="image" src="https://github.com/user-attachments/assets/66cba617-1d8c-42e3-9c11-9a3062353871" />

<img width="382" height="166" alt="image" src="https://github.com/user-attachments/assets/9f03a09e-a7cd-43f2-85bd-de3017d46402" />

<img width="466" height="184" alt="image" src="https://github.com/user-attachments/assets/f0e18140-62e8-4b4b-9b09-d41058c94431" />

<img width="1389" height="1229" alt="image" src="https://github.com/user-attachments/assets/52b30474-3c5e-40ca-84d9-98ad769341c2" />

<img width="337" height="98" alt="image" src="https://github.com/user-attachments/assets/3caee930-a353-4629-af72-b3cb0b835199" />

<img width="505" height="114" alt="image" src="https://github.com/user-attachments/assets/7c657236-2ebb-4215-b970-f3b9b671907e" />

# **📈 Key Insights**

- Demand peaks during rush hours (commute times).
- Weather conditions significantly affect rentals.
- Temperature positively correlates with demand until extreme heat.
- Working days show commuter-driven usage, while weekends show leisure usage.
- Registered users contribute more to consistent demand.

# **💡 Business Recommendations**

- Ensure bike availability during peak commute hours.
- Increase distribution in business districts on working days.
- Adjust supply during adverse weather conditions.
- Promote leisure usage on weekends and holidays.
- Use predictive demand to optimize fleet distribution.

# **🚀 Future Improvements**

- Incorporate real-time weather forecasts.
- Deploy time-series forecasting models (ARIMA, LSTM).
- Build a demand prediction dashboard.
- Integrate dynamic rebalancing strategies.

# **🧰 Tech Stack**

Python

Pandas & NumPy

Matplotlib & Seaborn

Scikit-learn

Jupyter Notebook
