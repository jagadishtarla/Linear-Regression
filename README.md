# Obesity Classification with Logistic Regression

This project analyzes an obesity-related dataset using exploratory data analysis (EDA) and multiple Logistic Regression models. The goal is to understand the relationships between lifestyle factors and obesity levels and to build models that classify individuals as obese vs. non-obese.

## 1. Exploratory Data Analysis (EDA)

- Summarized numeric variables: **Age, Height, Weight, FAF, CH2O, FCVC** using:
  - count, mean, standard deviation, min, 25%, 50%, 75%, max.
- Encoded categorical variables such as:
  - `Gender`, `CALC`, `SMOKE`, `family_history_with_overweight`, `FAVC`.
- Generated summary statistics for these categorical features:
  - count, number of unique values, most frequent value, and its frequency.
- Discussed potentially redundant or less informative features and how removing them would affect the analysis.
- Derived **BMI = Weight / Height²** and examined its correlation with the obesity label (`NObeyesdad`) to see whether BMI is a strong predictor of obesity.

## 2. Logistic Regression with One Variable

- Built a binary label from `NObeyesdad` (obese vs. non-obese).
- Trained a Logistic Regression model using **Weight** as the single predictor.
- Evaluated performance using:
  - Confusion matrix and additional metrics (accuracy, precision, recall, etc.).
- Visualized the decision boundary / probability curve where relevant.

## 3. Logistic Regression with Multiple Variables

- Trained a multi-variable Logistic Regression model using:
  - `Age, Height, Weight, FAF, CALC, SMOKE, family_history_with_overweight, CH2O, FCVC`.
- Implemented **forward feature selection** to automatically choose the most informative subset of features.
- Compared:
  - Full model vs. selected-features model using accuracy and confusion matrix.
- Discussed which features were selected and why they might be important for predicting obesity.

## 4. Regularization and Cost Function Experiments

- Used the best model from Section 3 as a baseline.
- Studied the effect of:
  - **Regularization** (e.g., L2 penalty).
  - **Feature scaling** on model performance.
- Modified the **cost function** as specified in the assignment and compared:
  - Original vs. modified cost in terms of convergence and final performance.
- Evaluated each model using confusion matrices and plots.
