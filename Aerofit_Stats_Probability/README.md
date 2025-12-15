## AeroFit - Statistics and Probability

## 🏃‍♂️ One-line summary:
This project performs descriptive analytics on AeroFit treadmill purchase data to understand customer characteristics and purchasing behavior across different treadmill models.

## 🧩 Problem Statement:
AeroFit is a leading fitness equipment brand offering multiple treadmill models targeting different customer segments.
The market research team wants to identify the characteristics of the target audience for each treadmill product in order to:
1. Improve product recommendations for new customers
2. Understand how customer demographics and fitness behavior differ across products
3. The objective is to analyze whether customer characteristics vary by treadmill type and build customer profiles for each product.

## 📁 Dataset:
The company collected the data on individuals who purchased a treadmill from the AeroFit stores during the prior three months. The dataset has the following features:
- Product Purchased:	KP281, KP481, or KP781
- Age:	In years
- Gender:	Male/Female
- Education:	In years
- MaritalStatus:	Single or partnered
- Usage:	The average number of times the customer plans to use the treadmill each week.
- Income:	Annual income (in $)
- Fitness:	Self-rated fitness on a 1-to-5 scale, where 1 is the poor shape and 5 is the excellent shape.
- Miles:	The average number of miles the customer expects to walk/run each week

## 🛠️ Tools & Technologies Used:
- Programming Language: Python
- Libraries: Pandas, NumPy, Matplotlib, Seaborn
- Visualization: Matplotlib, Seaborn
- Environment: Jupyter Notebook

## 🔍 Approach & Methodology:
The analysis follows a structured descriptive analytics approach:
1. Importing and understanding the dataset
2. Checking structure, data types, and statistical summary
3. Detecting missing values and outliers
4. Univariate analysis (categorical & continuous variables)
5. Bivariate analysis to study relationships with product purchased
6. Probability analysis (marginal & conditional probabilities)
7. Customer profiling based on observed patterns

## 📈 Key Analysis Performed:
- Dataset shape, data types, and statistical summaries
- Value counts and unique attribute analysis
- Outlier detection using boxplots and summary statistics
- Univariate analysis using histograms, countplots, and distplots
- Bivariate analysis using boxplots and countplots
- Correlation analysis using heatmaps and pairplots
- Two-way contingency tables using pandas.crosstab
- Marginal and conditional probability calculations

## 💡 Key Insights:
- Product KP281 brings in the highest revenue followed by KP481 and KP781.
- Majority of the customers are in the age group of 22-33 years with a 60-40 distribution of the male and female customers.
- Majority of the customers spend 14, 16, 18 years on their education.
- Most of the customers use the treadmill 3-4 times a week with a fitness level of 3-4. Majority of the customers earn between 30k and 70k.
- Majority of the customers set a target of 50-135 miles.
- The product KP781 is prefered by high-income earning individuals, their fitness levels are generally on high scale, the number of target miles they set are also higher.

## 📌 Business Recommendations:
- A premium product for highly-educated, high income and active customers to increase the revenue.
- Marketing to promote more products for females.
- Since KP281 and KP481 also brings in significant revenue and is prefered by young & learnings individuals, added features and specialized discounts could help boost sales.
