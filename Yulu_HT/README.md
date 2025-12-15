## 🚲 Yulu - Hypothesis Testing

## One-line summary:
This project analyzes factors influencing the demand for shared electric bikes in India using exploratory data analysis and hypothesis testing to support data-driven business decisions.

## 🧩 Problem Statement:

Yulu, India’s leading micro-mobility service provider, has recently observed a decline in revenues. To address this, the company wants to understand the key factors affecting the demand for shared electric bikes in the Indian market.

The primary objectives are:
- Identify which variables significantly impact bike demand
- Quantify how well these variables explain variations in rental counts
- The dependent variable is total number of electric bikes rented, and the analysis focuses on understanding its relationship with temporal, seasonal, and weather-related factors.

## 📁 Dataset:
The dataset contains usage data of shared electric bikes across different time periods, weather conditions, and seasons.
Target variable: count (total rental bikes)

- datetime: datetime
- season: season (1: spring, 2: summer, 3: fall, 4: winter)
- holiday: whether day is a holiday or not
- workingday: if day is neither weekend nor holiday is 1, otherwise is 0.
- weather: 1: Clear, Few clouds, partly cloudy, partly cloudy. 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist. 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds. 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
- temp: temperature in Celsius
- atemp: feeling temperature in Celsius
- humidity: humidity
- windspeed: wind speed
- casual: count of casual users
- registered: count of registered users
- count: count of total rental bikes including both casual and registered

## 🛠️ Tools & Technologies Used:
- Programming Language: Python
- Libraries: Pandas, NumPy, Matplotlib, Seaborn, SciPy, Statsmodels
- Visualization: Matplotlib, Seaborn
- Statistical Methods: Shapiro-Wilk Test, Levene's Test, Two-sample t-test, ANOVA, Chi-square test
- Environment: Jupyter Notebook

## 🔍 Approach & Methodology:
The analysis follows a structured statistical workflow:
1. Data loading and initial exploration
2. Dataset structure, data types, and summary statistics
3. Missing value and outlier detection
4. Univariate analysis of continuous and categorical variables
5. Bivariate analysis between demand and key predictors
6. Hypothesis formulation (H₀ and H₁)
7. Assumption checks (normality test, QQ plot, and variance equality)
8. Selection and execution of appropriate statistical tests
9. Interpretation of results using p-value and significance level

## 📈 Key Analysis Performed:
- Dataset shape, structure, and statistical summary
- Univariate analysis using histograms and countplots
- Bivariate analysis between: Working day and rental count, Season and rental count, Weather and rental count
- Outlier and distribution analysis
- Hypothesis testing using Two-sample t-test, One-way ANOVA and Chi-square test of independence

## 🧪 Hypothesis Testing:

Two-sample t-test: To evaluate whether working days affect cycle demand

ANOVA: To check if demand varies across seasons. To check if demand varies across weather conditions

Chi-square test: To assess whether weather is dependent on season.

Each test includes:
- Hypothesis formulation
- Assumption checks
- Test statistic and p-value computation
- Decision and inference

## 💡 Key Insights:
- More bikes were rented during the summer and fall seasons compared to the other seasons.
- More bikes were rented during the holidays.
- From the working day feature, it was observed that whenever there is a holiday or a weekend, more bikes were rented.
- During extreme weather conditions such as heavy rain, thunderstorm, snow or fog, bike rentals dipped.
- When the humidity is less than 20%, the number of bike rentals was extremely low.
- When the temperature is less than 10 degrees, the number of bike rentals decreases and when the windspeed exceeds areound 35, the bike rentals also decreases.

## 📌 Business Recommendations:
- During the summer and fall seasons, the company should have more bikes available since there is more demand compared to other seasons.
- Working days have no effect on bike rentals. However, weather and seasons have an effect on bike rentals. Hence, enhanced rental strategies during adverse weather and seasonal conditions is needed.
- Since season has an effect on bike rentals, the company must cater to the demand during off-season as well as seasonal period.
- Registered users are the top contributors and so the company must continue to sustain the levels throughout the year including maintenance of the bikes and service requests of the users.
