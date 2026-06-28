# Model Equations

## Overview

Regression analysis was performed to understand which business factors are most strongly associated with monthly sales across retail stores. Three regression models were developed: two simple linear regression models and one multiple linear regression model.

The simple regression models evaluated the effect of individual variables on monthly sales, while the multiple regression model combined several predictors to provide a more complete explanation of sales performance.

---

# Model 1: Simple Linear Regression (Marketing Spend)

### Regression Equation

**Monthly Sales = 545,400 + (2.372 × Marketing Spend)**

### Equation Interpretation

* **Intercept (545,400):**
  This represents the estimated monthly sales when marketing spend is zero. While a store would not realistically operate with no marketing spend, the intercept provides the starting point for the regression equation.

* **Marketing Spend Coefficient (2.372):**
  For every one-unit increase in marketing spend, monthly sales are expected to increase by approximately **2.37 units**, assuming no other factors change.

### Business Interpretation

The analysis indicates a positive relationship between marketing spend and monthly sales. Increasing marketing investment is associated with higher sales; however, marketing spend alone explains only a portion of the overall variation in store performance. This suggests that marketing is important but should be considered alongside other operational factors.

---

# Model 2: Simple Linear Regression (Footfall)

### Regression Equation

**Monthly Sales = 435,600 + (37.12 × Footfall)**

### Equation Interpretation

* **Intercept (435,600):**
  Represents the estimated monthly sales when customer footfall is zero. Although this scenario is not realistic in practice, the intercept is required to construct the regression equation.

* **Footfall Coefficient (37.12):**
  Every additional customer visiting the store is associated with an increase of approximately **37.12 units** in monthly sales.

### Business Interpretation

Footfall has a much stronger relationship with monthly sales than marketing spend. Stores that attract more customers consistently generate higher sales, making footfall one of the most influential business drivers identified in this analysis.

---

# Model 3: Multiple Linear Regression

### Regression Equation

**Monthly Sales = 149,020.04 + (1.18616 × Marketing Spend) + (33.8665 × Footfall) + (2818.08 × Inventory Availability) − (17,489.89 × Region_East) − (6,944.47 × Region_North) + (4,449.40 × Region_South)**

**Reference Category:** West Region

---

# Explanation of Each Coefficient

## Intercept

**149,020.04**

This represents the estimated monthly sales for a store in the **West region** (the reference category) when all numerical predictor values are zero. Although this situation is not realistic, the intercept serves as the baseline from which the model estimates sales.

---

## Marketing Spend

**Coefficient: 1.18616**

Holding all other variables constant, every additional unit of marketing spend is associated with an increase of approximately **1.19 units** in monthly sales.

This suggests that marketing investment contributes positively to sales growth, although its impact is smaller than customer footfall.

---

## Footfall

**Coefficient: 33.8665**

Holding other variables constant, each additional customer visiting the store is associated with an increase of approximately **33.87 units** in monthly sales.

Among all numerical predictors included in the model, footfall has the strongest positive relationship with monthly sales, highlighting the importance of attracting more customers to stores.

---

## Inventory Availability

**Coefficient: 2818.08**

An increase in inventory availability is associated with higher monthly sales.

Stores with better product availability are less likely to lose sales due to stock shortages, making inventory management an important contributor to overall store performance.

---

# Dummy Variables

Categorical variables cannot be used directly in regression analysis because they contain text values rather than numerical values. To include regional differences in the model, the **Region** variable was converted into dummy variables.

The following dummy variables were created:

* Region_East
* Region_North
* Region_South

The **West** region was intentionally excluded and used as the **reference category**.

---

## Why Was West Used as the Reference Category?

In regression analysis, one category must be omitted to avoid perfect multicollinearity (also known as the *dummy variable trap*).

The omitted category becomes the baseline against which all other categories are compared.

Therefore:

* Region_West = Reference Category
* Region_East = Compared with West
* Region_North = Compared with West
* Region_South = Compared with West

---

## Interpretation of Regional Coefficients

### Region_East

**Coefficient: -17,489.89**

After accounting for marketing spend, footfall, and inventory availability, stores located in the East region are expected to generate approximately **17,490 fewer units** in monthly sales than comparable stores in the West region.

The relationship is statistically significant, suggesting that East region stores perform differently from the reference category.

---

### Region_North

**Coefficient: -6,944.47**

North region stores are estimated to generate slightly lower monthly sales than West region stores.

However, this difference was **not statistically significant**, meaning there is insufficient evidence to conclude that North region stores perform differently from West stores after considering the other variables.

---

### Region_South

**Coefficient: 4,449.40**

South region stores are estimated to generate slightly higher monthly sales than West region stores.

This difference was **not statistically significant**, so it should not be interpreted as a meaningful business difference.

---

# Final Model Selected

The **Multiple Linear Regression Model (Model 3)** was selected as the final model for this analysis.

---

# Reason for Selecting the Final Model

The multiple regression model was selected because it provides the most comprehensive explanation of monthly sales.

Compared with the simple regression models, it considers several important business drivers simultaneously rather than evaluating each factor in isolation.

Key reasons for selecting this model include:

* It achieved the highest explanatory power with an **R² value of 0.811**, meaning it explains approximately **81.1%** of the variation in monthly sales.
* It incorporates multiple operational factors, including marketing spend, customer footfall, inventory availability, and regional differences.
* Marketing spend, footfall, inventory availability, and the East region were all found to be statistically significant predictors.
* The model provides more realistic and useful business insights than the individual simple regression models.

---

# Business Conclusion

The regression analysis suggests that customer footfall is the strongest factor associated with monthly sales, followed by inventory availability and marketing spend.

These findings indicate that leadership should prioritise initiatives that increase customer visits, maintain high inventory availability, and invest marketing budgets effectively.

Although regression analysis identifies important statistical relationships, it does **not** prove that one variable directly causes another. Other business factors such as local competition, pricing strategies, seasonal demand, economic conditions, and management practices may also influence store performance but were not included in the dataset.

Therefore, the regression model should be used as a decision-support tool alongside business knowledge and operational experience rather than as the sole basis for strategic decisions.

