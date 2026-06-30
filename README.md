# Regression-Based Business Insights & Model Interpretation

## Business Problem Summary

This project analyzes the factors that influence monthly sales across stores for a retail chain. The leadership team wants to understand which business variables have the strongest association with sales so they can make informed decisions regarding marketing investment, inventory management, staffing, and regional business strategy.

Regression analysis was used to identify important sales drivers and evaluate how well different models explain variations in monthly sales. The objective was not only to build predictive models but also to translate the statistical results into practical business recommendations.

---

# Dataset Description

The dataset contains monthly operational and sales information for retail stores.

It includes variables related to marketing activities, customer traffic, store operations, regional information, and financial performance.

The dataset contains information such as:

* Store ID
* Month
* Region
* Store Type
* Marketing Spend
* Footfall
* Average Discount Percentage
* Staff Count
* Inventory Availability Percentage
* Competitor Distance
* Holiday Flag
* Customer Rating
* Monthly Sales
* Monthly Profit

Before analysis, the dataset was reviewed to ensure it was suitable for regression modelling.

---

# Dependent and Independent Variables

### Dependent Variable

The dependent variable selected for all regression models was:

* **Monthly Sales**

This is the business outcome that leadership wants to understand and improve.

---

### Independent Variables

Several business variables were considered as potential predictors, including:

* Marketing Spend
* Footfall
* Inventory Availability Percentage
* Average Discount Percentage
* Staff Count
* Customer Rating
* Region
* Store Type

The final regression model included:

* Marketing Spend
* Footfall
* Inventory Availability Percentage
* Region (using dummy variables)

---

# Data Preparation and Cleaning

Before building the regression models, the dataset was reviewed for potential data quality issues.

The following checks were performed:

* Verified missing values.
* Checked for duplicate Store IDs.
* Reviewed numerical variables for obvious errors.
* Examined categorical variables for consistency.
* Confirmed that Monthly Sales was suitable as the dependent variable.
* Created dummy variables for the selected categorical variable.

The original dataset was preserved, and all transformations were completed on separate worksheet(s) within the regression workbook.

---

# Dummy Variable Approach

Since regression analysis requires numerical inputs, the categorical **Region** variable was converted into dummy variables.

The following dummy variables were created:

* Region_East
* Region_North
* Region_South

The **West** region was intentionally excluded and used as the **reference category**.

Using a reference category avoids the dummy variable trap and allows the regression model to compare every other region against West.

---

# Regression Approach

Three regression models were developed during the analysis.

### Model 1 – Simple Linear Regression

Dependent Variable:

* Monthly Sales

Independent Variable:

* Marketing Spend

This model evaluated whether marketing investment alone explains changes in monthly sales.

---

### Model 2 – Simple Linear Regression

Dependent Variable:

* Monthly Sales

Independent Variable:

* Footfall

This model measured the relationship between customer traffic and monthly sales.

---

### Model 3 – Multiple Linear Regression

Dependent Variable:

* Monthly Sales

Independent Variables:

* Marketing Spend
* Footfall
* Inventory Availability Percentage
* Region (Dummy Variables)

This model combined multiple business variables to provide a more complete explanation of store sales performance.

---

# Model Comparison Summary

Three regression models were compared based on explanatory power and business usefulness.

| Model   | Variables Used                                            |    R² | Summary                                                                                                                |
| ------- | --------------------------------------------------------- | ----: | ---------------------------------------------------------------------------------------------------------------------- |
| Model 1 | Marketing Spend                                           | 0.187 | Marketing spend has a positive relationship with monthly sales but explains only a small portion of sales variation.   |
| Model 2 | Footfall                                                  | 0.718 | Footfall is a strong predictor of monthly sales and explains a large proportion of sales variation.                    |
| Model 3 | Marketing Spend, Footfall, Inventory Availability, Region | 0.811 | Best-performing model that combines multiple business drivers and explains over 81% of the variation in monthly sales. |

The multiple regression model achieved the highest explanatory power and was selected as the final model.

---

# Final Model Selected

The **Multiple Linear Regression Model** was selected because it provides the most comprehensive explanation of monthly sales.

Key findings include:

* **R² = 0.811**, meaning the model explains approximately **81.1%** of the variation in monthly sales.
* Marketing Spend is positively associated with sales.
* Footfall is the strongest predictor of monthly sales.
* Inventory Availability has a significant positive relationship with sales.
* The East region performs significantly differently from the West region after accounting for other business factors.

Compared with the simple regression models, the multiple regression model provides more meaningful business insights because it considers several variables simultaneously.

---

# Business Recommendation

Based on the regression analysis, the following recommendations are made:

* Focus on increasing customer footfall, as it has the strongest association with monthly sales.
* Maintain high inventory availability to minimise stock-outs and improve customer satisfaction.
* Continue investing in marketing activities while regularly evaluating their effectiveness.
* Investigate the reasons behind lower performance in the East region and identify opportunities for improvement.
* Use regression analysis as a decision-support tool alongside business expertise when planning future strategies.

---

# Assumptions and Limitations

Although the regression model explains a large proportion of the variation in monthly sales, several limitations should be considered.

* Regression analysis identifies statistical relationships but does not prove causation.
* The model assumes linear relationships between the selected variables and monthly sales.
* Factors such as pricing strategy, economic conditions, weather, competitor promotions, and local customer preferences were not included in the dataset.
* Results should therefore be interpreted alongside business knowledge rather than being used as the sole basis for decision-making.

---

# Repository Structure

```text
part3_regression_insights/
├── data/
│   └── business_regression_data.xlsx
├── analysis/
│   ├── regression_workbook.xlsx
│   ├── model_comparison.md
│   └── residual_analysis.md
├── outputs/
│   ├── regression_summary.xlsx
│   ├── final_recommendation.md
│   └── model_equations.md
├── screenshots/
│   ├── simple_regression_output.png
│   ├── multiple_regression_output.png
│   ├── residuals_preview.png
│   └── model_comparison_preview.png
└── README.md
```

---

# Screenshots Included

The repository includes the following screenshots as evidence of the analysis:

* **simple_regression_output.png** – Output of the simple linear regression model.(https://github.com/manyarana/manyarana_2511046_part3_regression_insights/blob/main/screenshots/simple_regression_output.png)
* **multiple_regression_output.png** – Output of the final multiple regression model.(https://github.com/manyarana/manyarana_2511046_part3_regression_insights/blob/main/screenshots/multiple_regression_output.png)
* **residuals_preview.png** – Predicted monthly sales and residual calculations.(https://github.com/manyarana/manyarana_2511046_part3_regression_insights/blob/main/screenshots/residuals_preview.png)
* **model_comparison_preview.png** – Comparison table summarising all regression models.(https://github.com/manyarana/manyarana_2511046_part3_regression_insights/blob/main/screenshots/model_comparison_preview.png)

These screenshots provide supporting evidence for the statistical analysis and conclusions presented in this project.

---

# Conclusion

This project demonstrates how regression analysis can be used to support business decision-making by identifying the factors most strongly associated with monthly sales. The analysis shows that customer footfall, inventory availability, and marketing spend are important business drivers, with customer footfall having the strongest relationship with sales performance.

The multiple regression model was selected as the final analytical model because it provides the highest explanatory power while incorporating several operational and regional factors. Although regression cannot establish cause-and-effect relationships, it offers valuable insights that can help leadership make more informed strategic decisions and prioritise business improvements.


