# Predicting House Prices Using Machine Learning

## A Comparative Analysis of Algorithms and Features

This repository explores the prediction of house prices using various machine learning algorithms. The dataset includes house features from Bengaluru, and we perform extensive data cleaning, exploratory data analysis (EDA), model training, and evaluation.

### Table of Contents
- [Project Overview](#project-overview)
- [Data Dictionary](#data-dictionary)
- [Data Cleaning](#data-cleaning)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Feature Engineering](#feature-engineering)
- [Model Training & Evaluation](#model-training--evaluation)
- [Model Tuning](#model-tuning)
- [Results](#results)
- [Saving the Model](#saving-the-model)

---

## Project Overview

This project performs a comparative analysis of different machine learning algorithms to predict house prices in Bengaluru. Models such as Linear Regression, Ridge, Lasso, Decision Tree, Random Forest, and Gradient Boosting are trained and evaluated.

## Data Dictionary

| Column Name  | Description |
|--------------|-------------|
| `Area_Type`  | Type of the property area |
| `Availability` | Availability for possession |
| `Location`   | Location of the property |
| `Size`       | Number of rooms (BHK) |
| `Society`    | Whether the property is in a society |
| `Total_Sqft` | Area of the property |
| `Bathroom Nos`| Number of bathrooms |
| `Balcony`    | Number of balconies |
| `Price`      | Price of the property (Target Variable) |

---


## Data Cleaning

Steps involved in cleaning the dataset:

1. **Removing Duplicates**: Duplicate rows are dropped.
2. **Handling Missing Values**: We drop columns and rows with excessive missing values.
3. **Unit Conversion**: Various area units are converted to `sqft`.
4. **Outlier Removal**: Outliers based on price per sqft are removed.
5. **Feature Engineering**: Columns such as `price_per_sqft` are added for better analysis.
---

## Exploratory Data Analysis (EDA)

Key insights from the dataset:
- Majority of properties have 2 or 3 BHKs.
- Some locations exhibit significant variations in price per sqft.
- Positive correlation between total area and price.

Visualization samples:
- Pie chart of area type distribution.
- Box plots showing price distribution by `size` and `area_type`.

---

## Feature Engineering

We performed the following:
1. **Dimensionality Reduction**: Grouped rare `location` values under "other locations".
2. **Encoding**: Converted categorical variables such as `area_type` and `location` into numerical forms.
3. **KNN Imputation**: Filled missing balcony values using KNN Imputer.

---

## Model Training & Evaluation

We trained multiple models to predict house prices, including:
- **Linear Regression**
- **Ridge Regression**
- **Lasso Regression**
- **Decision Tree**
- **Random Forest**
- **Gradient Boosting**

## Model Tuning

We fine-tuned the best-performing models:
1. **Random Forest Regressor**: Tuned using `GridSearchCV`.
2. **Gradient Boosting Regressor**: Tuned using `RandomizedSearchCV`.

---

## Results

- **Random Forest Regressor** performed best with an R² score of **0.87** on the training set and **0.65** on the test set. Overfitting was managed through hyperparameter tuning.

---

## Saving the Model

The final Random Forest model is saved as a `.joblib` file.
