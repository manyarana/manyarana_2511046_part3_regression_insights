# Residual Analysis

## Purpose

Residual analysis was performed to evaluate how accurately the final multiple regression model predicts monthly sales for each store.

Predicted sales were calculated using the final regression equation, and residuals were computed using the following formula:

**Residual = Actual Monthly Sales − Predicted Monthly Sales**

A positive residual indicates that the actual monthly sales were higher than the predicted value, meaning the model underestimated sales for that store. A negative residual indicates that the predicted sales were higher than the actual sales, meaning the model overestimated sales.

---

## Largest Positive Residuals

The five largest positive residuals identified were:

| Rank |   Residual |
| ---- | ---------: |
| 1    | 123,484.04 |
| 2    | 114,411.59 |
| 3    | 110,722.09 |
| 4    |  98,930.84 |
| 5    |  89,220.26 |

These stores generated significantly higher sales than predicted by the regression model. This suggests that there may be additional factors influencing sales that were not included in the analysis, such as local promotions, seasonal demand, strong store management, customer loyalty, or favourable market conditions.

---

## Largest Negative Residuals

The five largest negative residuals identified were:

| Rank |    Residual |
| ---- | ----------: |
| 1    | -162,814.71 |
| 2    | -141,055.09 |
| 3    | -122,239.03 |
| 4    | -119,045.59 |
| 5    | -111,282.58 |

These stores recorded lower sales than predicted by the model. Possible reasons include temporary operational issues, inventory shortages, lower local demand, increased competition, staffing challenges, or other external factors that were not captured by the available variables.

---

## Model Performance

The final multiple regression model achieved an **R² of 0.811**, meaning it explains approximately **81.1%** of the variation in monthly sales. This indicates that the model has strong predictive performance and captures most of the important business drivers affecting sales.

Although the majority of predictions are reasonably accurate, a small number of stores show relatively large residuals. This suggests that some business factors influencing sales are not included in the current dataset.

---

## Business Interpretation

Overall, the regression model performs well and can be used as a decision-support tool for forecasting monthly sales.

Stores with large positive residuals should be investigated to understand what contributed to their stronger-than-expected performance. Best practices identified from these stores could potentially be applied across other locations.

Similarly, stores with large negative residuals should be reviewed to identify operational issues or local challenges that may have reduced sales.

The residual analysis does not indicate that the model consistently under-predicts or over-predicts store performance. Instead, prediction errors occur in both directions, suggesting that the model is generally balanced while still leaving room for improvement through the inclusion of additional explanatory variables.

---

## Limitations

The regression model explains a large proportion of monthly sales variation, but it does not capture every factor that influences store performance. Variables such as local economic conditions, competitor promotions, weather, store management quality, customer demographics, and seasonal events were not included in the dataset. As a result, regression results should be interpreted as statistical associations that support business decision-making rather than exact predictions.
