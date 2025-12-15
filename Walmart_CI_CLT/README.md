## 🛒 Walmart - Confidence Interval and Central Limit Theorem:

## One-line summary:
This project analyzes Black Friday purchase behavior at Walmart to understand how customer spending varies across gender, marital status, and age groups using descriptive statistics and confidence intervals.

## 🧩 Problem Statement:

Walmart Inc. wants to analyze customer purchase behavior, specifically purchase amount, to understand whether spending habits differ across customer demographics.

The primary business question is: Do female customers spend more than male customers during Black Friday sales?

Assuming an equal population of 50 million male and 50 million female customers, the analysis aims to use sampling, confidence intervals, and the Central Limit Theorem (CLT) to generalize insights to the population level.

## 📁 Dataset:
The dataset contains transactional data from Walmart customers who made purchases during Black Friday.
Target variable: Purchase Amount

- User_ID:	User ID (Unique customer identifier)
- Product_ID:	Product ID (Unique product identifier)
- Gender:	Sex of the user
- Age:	Age in bins
- Occupation:	Occupation(Masked)
- City_Category:	Category of the city (A,B,C)
- StayInCurrentCityYears:	Number of years stay in current city
- Marital_Status:	Marital Status
- ProductCategory:	Product Category (Masked)
- Purchase:	Purchase Amount

## 🛠️ Tools & Technologies:
- Programming Language: Python
- Libraries: Pandas, NumPy, Matplotlib, Seaborn, SciPy
- Visualization: Matplotlib, Seaborn
- Statistics Concepts: Central Limit Theorem, Confidence Interval
- Environment: Jupyter Notebook

## 🔍 Approach & Methodology:
The analysis follows a structured statistical and exploratory approach:
1. Importing and understanding the dataset
2. Data type inspection and statistical summary
3. Missing value and outlier detection
4. Non-graphical analysis using value counts
5. Univariate analysis of continuous and categorical variables
6. Bivariate analysis across demographic segments
7. Sampling and computation of confidence intervals
8. Application of the Central Limit Theorem
9. Comparison of spending patterns across demographic groups (Married vs Unmarried and Age across bins 0-17, 18-25, 26-35, 36-50, 51+ years).

## 📈 Key Analysis Performed:
- Dataset shape, structure, and summary statistics
- Missing value detection using isnull()
- Outlier detection using boxplots and descriptive statistics
- Univariate analysis using histograms, countplots, and distplots
- Bivariate analysis using boxplots and grouped comparisons
- Correlation analysis using heatmaps and pairplots
- Sampling-based analysis of purchase amounts
- Confidence interval estimation at different confidence levels (90%, 95%, 99%)
- CLT-based distribution analysis of sample means

## 🧮 Statistical Analysis:
- Comparison of average spending between male and female customers
- Confidence interval estimation for population mean spending
- Overlap analysis of confidence intervals
- Spending behavior comparison for: Married vs Unmarried customers, Age groups based on life stages 0-17, 18-25, 26-35, 36-50, 51+ years

## 💡 Key Insights:


## 📌 Business Recommendations:

## 💡 Key Insights on Genderwise Spending:
- 28% customers are Female and 72% customers are Male.
- Male customers typically spend more on average than female customers. The confidence interval for male purchases shows a greater upper bound and a broader range than the confidence interval for female purchases, with male consumers initiating 75.3% of transactions and female customers 24.7%.

## 📌 Business Recommendations on Genderwise Spending:
- Wide selection of products from clothing and beauty products to household essentials that align with the preferences and requirements of female customers.
- Active feedback from customers to understand their preferences, concerns, and suggestions to make improvements that cater to their needs.
- Loyalty programs, exclusive perks like discounts, early access to sales, and unique rewards can enhance engagement and attract customers.

## 💡 Key Insights on Marital Status wise Spending:
- The overlapping confidence intervals of average spending for married and unmarried customers indicate that both male and female customers spend a similar amount per transaction and a resemblance in spending behavior between the two.

## 📌 Business Recommendations on Marital Status wise Spending:
- Enhance the shopping experience for both married and unmarried customers Unified category evn by treating both categories as unified for more effective results.

## 💡 Key Insights on Age Group wise Spending:
- Spending by Age_group 0-17 is low compared to other age groups. Customers in Age_group 51-55 spend the most.

## 📌 Business Recommendations on Age Group wise Spending:
- Toys, clothing, electronics, books, school supplies, and other items that appeal to children and teenagers should be available in a variety of products that are both entertaining and suitable for their age.
- Entertaining and safe play spaces where kids may do developmental activities through learning resources, craft kits, and educational toys.
- Make Walmart the preferred shopping destination for kids and parents by introducing specific deals and discounts for the 0–17 age range.

## 🔥 Optional Enhancements:
- Hypothesis testing for mean comparison
- Bootstrapping-based confidence intervals
- Interactive dashboard for executive reporting
