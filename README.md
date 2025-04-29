# Linear Regression Project

This project analyzes house sales data from Boston, specifically South End street, covering houses sold between July 2012 and July 2013. The analysis includes data wrangling, exploratory data analysis (EDA), and multiple linear regression techniques to predict house prices.

## Table of Contents

1. [Project Description](#project-description)
2. [Dataset Overview](#dataset-overview)
3. [Features](#features)
4. [Analysis Steps](#analysis-steps)
5. [Results](#results)


---

## Project Description

This project aims to predict house prices using features such as square footage, number of bedrooms, bathrooms, and location. The dataset provides insights into the Boston housing market and helps demonstrate the use of machine learning techniques such as linear and ridge regression.

---

## Dataset Overview

The dataset contains house sales data for South End street, Boston, USA. It includes:
- Houses sold between July 2012 and July 2013.
- Features such as house size, number of floors, waterfront view, and more.

---

## Features

Here are the key features in the dataset:
- **price**: Sale price of the house (target variable).
- **bedrooms**: Number of bedrooms.
- **bathrooms**: Number of bathrooms.
- **sqft_living**: Square footage of living space.
- **sqft_lot**: Square footage of the lot.
- **floors**: Number of floors in the house.
- **waterfront**: Whether the house has a waterfront view (1 = Yes, 0 = No).
- **view**: Quality of the house's view.
- **condition**: Condition of the house (e.g., good, fair).
- **grade**: Grade of the house's construction and design.
- **lat** and **long**: Latitude and longitude of the house location.

---

## Analysis Steps

### 1. Data Wrangling
- Dropped irrelevant columns such as `id` and `Unnamed: 0`.
- Replaced missing values (`NaN`) with the mean of their respective columns.

### 2. Exploratory Data Analysis
- Counted unique floor values using `value_counts()`.
- Plotted boxplots to analyze price outliers for houses with and without waterfront views.
- Analyzed the correlation between house prices and square footage above ground using regression plots.

### 3. Model Development
- **Linear Regression**:
  - Fitted a model using features such as `sqft_living` and others.
  - Calculated R² values to evaluate model accuracy.
- **Ridge Regression**:
  - Applied Ridge regularization with polynomial feature transformations to improve performance.

### 4. Model Evaluation
- Compared R² values from different models and feature combinations.
- Automated preprocessing and modeling using pipelines.

---

## Results

### Key Findings:
1. **Simple Linear Regression**:
   - Feature: `sqft_living`
   - R² Value: ~0.494

2. **Linear Regression with Multiple Features**:
   - Features: `floors`, `waterfront`, `lat`, `bedrooms`, `sqft_basement`, `view`, `bathrooms`, `sqft_living15`, `sqft_above`, `grade`, `sqft_living`
   - R² Value: ~0.661

3. **Ridge Regression**:
   - Regularization Parameter: 0.1
   - R² Value: ~0.661

4. **Ridge Regression with Polynomial Features**:
   - Degree: 2
   - Regularization Parameter: 0.1
   - R² Value: ~0.700

---




