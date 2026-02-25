# Cost-Prediction-Using-Multiple-Linear-Regression

Healthcare Expense Analysis with Feature Engineering
📌 Overview
This task analyzes a real-world Medical Cost Personal Dataset to understand the factors that drive healthcare expenses and predict insurance charges using Multiple Linear Regression.
The analysis includes comprehensive preprocessing steps — handling categorical variables, feature scaling, outlier detection, and feature engineering — to build an interpretable regression model that explains how demographic and lifestyle factors influence medical costs.
## Objective
Predict medical insurance charges (Y = Charges) using patient attributes (X variables), including:
* Age
* Sex
* BMI
* Number of children
* Smoking status
* Region
* The project emphasizes data preparation, interpretability, and model evaluation rather than just prediction accuracy.

---
## Dataset
* Medical Cost Personal Dataset (Kaggle)
* The dataset explores relationships between patient characteristics and healthcare expenses.
* Features
* Column	Description
* ID	Unique record identifier
* Patient age
* Gender
* BMI	Body Mass Index
* Children	Number of dependents
* Smoker	Smoking status
* Region	Geographic location
* Charges	Medical expenses (Target Variable)

---
## Methodology
1) Data Preprocessing
* Handling Categorical Variables
* Categorical features were encoded to numeric values:
* Sex
* Smoker
* Region

- Techniques used:
* One-hot encoding or label encoding
* Feature Scaling
* Applied scaling to ensure features were on comparable ranges:
* StandardScaler / MinMaxScaler
* Scaling is particularly important for regression models when variables have different magnitudes.
* Outlier Detection & Removal
* Outliers were identified using methods such as:
* Z-score filtering
* Interquartile Range (IQR)
* Extreme outliers (especially in charges and BMI) were removed to prevent distortion of regression results.

2) Feature Engineering
* Explored relationships between variables to create meaningful features, such as:
* Age × BMI interaction
* Smoking impact on charges
* Family size effects (children)
* Patterns discovered during feature engineering were documented in code comments and analysis notes.

3) Multiple Linear Regression
* Implemented using Scikit-learn:
* Used all available predictors (after preprocessing)
* Trained model to predict medical charges

---
## Model Evaluation
Performance evaluated using:
- R² Score
* Measures how well the model explains variance in charges.
- Mean Squared Error (MSE)
* Measures prediction error magnitude.
* Both metrics were printed and analyzed to assess model quality.

---
## Visualization
* Regression results visualized using Matplotlib:
* Predicted vs actual charges
* Residual analysis
* Feature relationship plots
* Visualization helps interpret how well the model fits real-world data.

---
## Key Insights
* Smoking status is a major driver of healthcare costs
* Age and BMI significantly influence expenses
* Interaction effects between variables improve prediction accuracy
* Proper preprocessing dramatically improves regression performance

---
## Tech Stack
* Python
* Pandas & NumPy — data processing
* Scikit-learn — regression modeling
* Matplotlib — visualization
