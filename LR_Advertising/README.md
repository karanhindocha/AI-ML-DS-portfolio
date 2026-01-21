# 📊 Advertising Sales Prediction – Linear Regression
# 📌 Project Overview

This project analyzes the relationship between advertising spend across three channels — TV, Radio, and Newspaper — and product sales.
Using simple and multiple linear regression, the goal is to understand which marketing channels drive sales most effectively and how advertising budgets can be optimized using data.

# 🎯 Objective
- Identify the impact of each advertising channel on sales.
- Build predictive models to estimate sales based on ad spend.
- Translate model outputs into actionable business insights.

# 📂 Dataset
TV: TV advertising spend

Radio: Radio advertising spend

Newspaper: Newspaper advertising spend

Target: Sales: Product sales

# 🔍 Exploratory Data Analysis (EDA)

- Distribution analysis of advertising spend across channels.

- Regplot of each feature vs the target variable.

- Scatter plots to visualize relationships between each channel and sales.

- Pairplot and Correlation analysis to assess linear relationships.

## Insights:

- TV advertising shows a strong linear relationship with sales.

- Radio has a moderate positive impact.

- Newspaper shows weak correlation with sales.

# 🧠 Modeling Approach

- Simple Linear Regression: TV vs Sales (Sales = 6.975 + 0.055 * TV), Radio vs Sales (Sales = 12.236 + 0.124 * Radio) and Newspaper vs Sales (Sales = 13.960 + 0.038 * Newspaper).

- Multiple Linear Regression: Combined effect of TV, Radio, and Newspaper on Sales (sales = 4.714 + (0.055 * TV) + (0.101 * Radio) + (0.004 * Newspaper)).

- Visualising training set results, testing set results, plotting residuals and evaluating with coefficient interpretation, residual analysis, R2 Score and RMSE.

- Making predictions on unseen data.

- Feature Selection Experiment: Drop one feature and train the model on the remaining two features: Train the model, coefficient interpretation and evaluating with R2 Score and RMSE:

  1. Drop Newspaper: sales = 4.791 + (0.055 * TV) + (0.103 * Radio)
  2. Drop Radio: sales = 6.048 + (0.055 * TV) + (0.033 * Newspaper)
  3. Drop TV: sales = 12.517 + (0.118 * Radio) + (0.004 * Newspaper)

# 📌 Interpretation

- TV advertising delivers the highest return on investment.

- Radio supports sales growth but is less effective than TV.

- Newspaper advertising provides limited incremental value.

# 💼 Business Insights & Recommendations
1️⃣ Prioritize TV Advertising

TV spend has the strongest influence on sales.
Recommendation: Allocate a larger share of the marketing budget to TV campaigns.

2️⃣ Use Radio as a Supporting Channel

Radio contributes positively but is not the primary driver.
Recommendation: Use Radio advertising alongside TV to reinforce campaigns.

3️⃣ Reevaluate Newspaper Spend

Newspaper advertising shows weak predictive power.
Recommendation: Reduce or strategically reallocate newspaper budgets unless needed for branding.

4️⃣ Optimize Spend, Don’t Maximize It

The model suggests diminishing returns beyond certain spending levels.
Recommendation: Identify optimal spend thresholds rather than increasing budgets indiscriminately.

5️⃣ Use the Model for Forecasting

The regression model can simulate different ad spend scenarios.
Recommendation: Use it as a decision-support tool for marketing planning.

# 🛠️ Tools & Technologies

Python

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn

Statsmodels (OLS)
