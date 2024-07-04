# Student Performance Prediction using Machine Learning

## About the Dataset

### Description
The Student Performance Dataset is designed to examine factors influencing academic student performance. It comprises 10,000 student records, each containing predictors and a performance index.

### Variables
- **Hours Studied:** Total hours spent studying by each student.
- **Previous Scores:** Scores from previous tests.
- **Extracurricular Activities:** Whether the student participates in extracurricular activities (Yes or No).
- **Sleep Hours:** Average hours of sleep per day for each student.
- **Sample Question Papers Practiced:** Number of sample question papers the student has practiced.

### Target Variable
- **Performance Index:** Rounded measure of each student's overall academic performance, ranging from 10 to 100. Higher values indicate better performance.

### Dataset Purpose
The dataset aims to provide insights into how variables such as studying hours, previous scores, extracurricular activities, sleep patterns, and practice with sample question papers relate to student performance. It is a synthetic dataset created for illustrative purposes, offering a platform for researchers and data analysts to explore educational factors and their impacts.

## Objective
The objective of this project is to predict the performance of students based on the extracted features provided in `Student_Performance.csv`.

## Setup

### 1. Installation
Ensure you have the necessary Python libraries installed. You can install them using pip:

```
pip install numpy pandas opendatasets matplotlib seaborn scikit-learn xgboost
```
## Analysis and Modeling

### 1. Data Preprocessing
Checked for null values and transformed categorical data (`Extracurricular Activities`) into numerical format.

### 2. Exploratory Data Analysis (EDA)
Visualized correlations between variables using a heatmap.

### 3. Model Building and Evaluation
- **Linear Regression:** Basic linear regression model.
- **Polynomial Regression:** Captured non-linear relationships using polynomial features.
- **Ridge, Lasso, ElasticNet Regression:** Regularized regression models to handle multicollinearity.
- **Decision Tree and Random Forest:** Tree-based models for capturing complex relationships.
- **Support Vector Regression (SVR):** Non-linear regression model.
- **Gradient Boosting Regression (XGBoost):** Boosting ensemble method for improved accuracy.

### 4. Model Evaluation
Compared models based on R² score and RMSE on the test dataset.
Identified Support Vector Regression (SVR) as the best-performing model.

## Overall Conclusion

 - **SVR Performance:** SVR demonstrates high accuracy with a Test Score R² of **98.59%** and low RMSE of **2.29**. This indicates that SVR fits the data well and generalizes effectively, similar to other linear regression-based models such as Ridge, Lasso, and ElasticNet.

- **Tree-Based Models:** Decision Tree and Random Forest perform well but show slightly lower R² scores and marginally higher RMSE compared to linear models. This could be attributed to their tendency to overfit.

- **Gradient Boosting Regression:** Stands out by achieving comparable performance to linear models, indicating effective ensemble learning and boosting.

## Recommendation

- **For Predictive Tasks:**
  - **Interpretability and Simplicity:** Linear regression-based models (including Ridge, Lasso, ElasticNet, and SVR) are suitable choices due to their high accuracy and ease of interpretation.
  - **Complex Relationships:** If capturing more complex relationships or benefiting from ensemble learning is necessary, Gradient Boosting Regression is recommended for its robust performance.
