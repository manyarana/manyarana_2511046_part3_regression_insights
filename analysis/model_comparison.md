# Model Comparison

## Overview

To understand which factors best explain monthly sales, three regression models were developed and compared. The first two models used a single predictor each (simple linear regression), while the final model combined multiple business variables, including a categorical variable represented using dummy variables.

The purpose of this comparison is to identify which model provides the most reliable explanation of monthly sales and is most useful for supporting business decisions.

---

## Model Comparison Table

| Model       | Dependent Variable | Independent Variable(s)                                                        |        R² | Significant Variables                                                                                          | Business Usefulness                                                                                                                                                 | Limitations                                                                                                                                                                                                           |
| ----------- | ------------------ | ------------------------------------------------------------------------------ | --------: | -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Model 1** | Monthly Sales      | Marketing Spend                                                                | **0.187** | Marketing Spend (p < 0.001)                                                                                    | Shows that higher marketing investment is associated with higher sales, but explains only a small portion of sales variation.                                       | Does not account for customer traffic, inventory, or regional differences.                                                                                                                                            |
| **Model 2** | Monthly Sales      | Footfall                                                                       | **0.718** | Footfall (p < 0.001)                                                                                           | Strong predictor of monthly sales. Customer traffic alone explains a large share of the variation in sales.                                                         | Ignores other operational and regional factors that may influence performance.                                                                                                                                        |
| **Model 3** | Monthly Sales      | Marketing Spend, Footfall, Inventory Availability, Region (East, North, South) | **0.811** | Marketing Spend (p < 0.001), Footfall (p < 0.001), Inventory Availability (p < 0.001), Region_East (p = 0.008) | Best overall model. Combines marketing, customer traffic, inventory management, and regional differences to provide the most accurate explanation of monthly sales. | Regression identifies relationships between variables but cannot prove cause-and-effect. Additional factors such as local competition, pricing strategies, seasonal demand, and economic conditions are not included. |

---

## Comparison of Model Performance

### Model 1 – Marketing Spend

The first model examined the relationship between marketing spend and monthly sales. The results showed a positive and statistically significant relationship, with an R² value of **0.187**. This means marketing spend explains approximately **18.7%** of the variation in monthly sales.

Although marketing investment contributes to sales growth, the relatively low R² indicates that other business factors also play an important role in determining store performance.

---

### Model 2 – Footfall

The second model evaluated the impact of customer footfall on monthly sales. This model performed substantially better, achieving an **R² of 0.718**.

This means customer footfall alone explains nearly **72%** of the variation in monthly sales, making it a much stronger predictor than marketing spend. The results suggest that attracting more customers into stores has a significant positive association with sales performance.

---

### Model 3 – Multiple Regression

The final model combined multiple business variables, including marketing spend, footfall, inventory availability, and regional dummy variables.

This model achieved the highest explanatory power with an **R² of 0.811**, indicating that approximately **81.1%** of the variation in monthly sales is explained by the selected predictors.

The analysis showed that:

* Marketing Spend is positively associated with monthly sales and is statistically significant.
* Footfall is the strongest predictor of monthly sales.
* Higher Inventory Availability is associated with higher sales.
* Stores located in the East region perform significantly differently from the reference region (West), while the North and South regions do not show statistically significant differences after accounting for the other variables.

---

## Significant Variables

The following variables were found to be statistically significant:

* Marketing Spend (p < 0.001)
* Footfall (p < 0.001)
* Inventory Availability (p < 0.001)
* Region_East (p = 0.008)

The following variables were **not** statistically significant:

* Region_North (p = 0.350)
* Region_South (p = 0.557)

These results suggest that the differences between the North and South regions and the reference category (West) are not large enough to be considered statistically meaningful within this model.

---

## Business Usefulness

Among the three models, the multiple regression model provides the strongest support for business decision-making because it considers several operational factors simultaneously rather than evaluating each factor in isolation.

The results suggest that leadership should prioritize initiatives that:

* Increase customer footfall.
* Allocate marketing budgets effectively.
* Maintain high inventory availability to reduce stock-outs.
* Investigate why stores in the East region underperform compared to the West region.

---

## Final Model Selection

The **multiple regression model (Model 3)** was selected as the final model because it provides the highest explanatory power (**R² = 0.811**) while incorporating multiple business drivers.

Unlike the simple regression models, it captures the combined effect of marketing, customer traffic, inventory management, and regional differences, making it the most suitable model for understanding monthly sales performance and supporting business planning.

Although the model performs well, the results should be interpreted as statistical associations rather than proof of causation. Additional business factors not included in the dataset may also influence monthly sales.
