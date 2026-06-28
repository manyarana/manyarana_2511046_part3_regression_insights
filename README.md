# Understanding the Dataset

## Business Problem

The objective of this project is to identify the key factors associated with monthly sales across retail stores. By understanding which variables have the strongest relationship with sales, the leadership team can make better decisions regarding marketing investment, staffing, inventory management, pricing strategies, and store operations.

The analysis uses regression models to measure the relationship between monthly sales and several business variables. The results will help identify which factors are most strongly associated with sales performance while acknowledging that regression measures association rather than proving cause and effect.

---

## Dependent Variable

The dependent variable (target variable) selected for this analysis is:

* **monthly_sales**

This is the outcome that the regression models will attempt to explain and predict.

---

## Potential Independent Variables

The following variables may influence monthly sales and will be considered as predictors in the regression models:

* marketing_spend
* footfall
* avg_discount_pct
* staff_count
* inventory_availability_pct
* competitor_distance_km
* holiday_flag
* customer_rating
* region (using dummy variables)
* store_type (using dummy variables)

---

## Numerical Variables

The numerical variables in the dataset are:

* marketing_spend
* footfall
* avg_discount_pct
* staff_count
* inventory_availability_pct
* competitor_distance_km
* customer_rating
* monthly_sales
* monthly_profit

---

## Categorical Variables

The categorical variables are:

* region
* store_type

These variables cannot be used directly in a regression model and must first be converted into dummy variables.

---

## Variables Requiring Cleaning or Transformation

The following variables require preparation before running regression analysis:

* **month** – stored as a date field and not required as a predictor for this analysis.
* **region** – converted into dummy variables.
* **store_type** – converted into dummy variables.
* **holiday_flag** – verify that values contain only 0 and 1.
* Numerical variables should be checked for missing values and unusual outliers before modelling.

---

## Variables Not Used in the Regression Model

Some variables are not appropriate as independent variables when predicting monthly sales:

* **store_id** – serves only as a unique identifier and has no predictive value.
* **month** – used only for identifying the reporting period and not included in the regression model.
* **monthly_profit** – excluded because it is closely related to monthly sales and could introduce redundancy into the model.

---

## Planned Regression Approach

The analysis will consist of:

1. Data cleaning and preparation.
2. Creation of dummy variables for categorical features.
3. Two simple linear regression models using individual predictors.
4. One multiple linear regression model using several numerical predictors and at least one dummy variable.
5. Comparison of model performance using R² values, p-values, and business interpretation.
6. Residual analysis to evaluate prediction errors and identify stores where the model performs particularly well or poorly.
