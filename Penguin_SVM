# 🐧 Penguin Species Classification using SVM
# 📌 Project Overview

This project focuses on classifying penguin species using physical measurements such as bill dimensions, flipper length, body mass, and categorical attributes like island and sex. The goal is to demonstrate a complete machine learning workflow, including EDA, feature preprocessing, model building, evaluation, and interpretation.

The project uses Support Vector Machines (SVM) with different kernels to compare performance and highlight the importance of feature scaling and hyperparameter tuning.

# 🎯 Objectives

- Perform exploratory data analysis (EDA) to understand feature distributions and relationships.

- Handle missing values and preprocess numerical and categorical features.

- Build and compare Linear SVM and RBF SVM classifiers.

- Apply feature scaling and hyperparameter tuning.

- Evaluate models using multiple classification metrics.

# 📊 Dataset

Source: Palmer Penguins dataset

Target Variable: Species (Adelie, Chinstrap, Gentoo)

Features Used: Island, Culmen Length (mm), Culmen Depth (mm), Flipper Length (mm), Body Mass (g), Sex

# 🔍 Exploratory Data Analysis (EDA)
## Key EDA steps included:

- Class distribution of penguin species.

- Distribution of numerical features using histograms and boxplots.

- Comparison of physical characteristics across species.

- Missing value analysis.

- Categorical feature distribution (Island, Sex, Species).

## EDA helped identify:

- Strong separation between species based on flipper length and bill dimensions.

- The importance of scaling numerical features before applying SVM.

# ⚙️ Data Preprocessing

- Dropped rows with missing values.

- Encoded categorical variables (Island, Sex) using one-hot encoding.

- Encoded target variable (Species) using label encoding.

- Applied StandardScaler to numerical features (critical for SVM).

# 🤖 Models Used

Support Vector Machine (Linear Kernel)

Support Vector Machine (RBF Kernel)

Hyperparameter Tuning

Used GridSearchCV for: C (regularization parameter), gamma (for RBF kernel)

5-fold cross-validation

Evaluation based on weighted F1-score

# 📈 Model Evaluation

Models were evaluated using: Accuracy, Precision (weighted), Recall (weighted), F1-score (weighted), ROC-AUC (One-vs-Rest strategy for multiclass)

Both Linear and RBF SVM achieved very high classification performance, demonstrating clear separability between penguin species.

# ✅ Key Findings & Recommendations

- Linear SVM is preferred due to its simplicity and interpretability, despite similar performance to RBF SVM.

- Flipper length and bill measurements are the most influential features for classification.

- Automated species classification can significantly reduce manual effort in ecological research.

- Ensuring high-quality, complete measurements improves model reliability.

- The approach can be scaled to additional species or environmental variables.

# 🛠️ Tech Stack

Python

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn
