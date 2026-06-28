# Task 3: Dummy Variable Creation

## Purpose

Regression models cannot directly use categorical text variables. Therefore, categorical variables were converted into dummy variables.

## Categorical Variables Selected

The following categorical variables were converted:

* region
* store_type

---

## Dummy Variable Creation for Region

The original `region` variable had three categories:

* North
* South
* West

To avoid redundancy, only two dummy variables were created:

* `region_North`
* `region_South`

Reference category:

* **West**

Encoding:

* If region = North → region_North = 1, else 0
* If region = South → region_South = 1, else 0
* If both are 0 → West (reference)

This avoids the dummy variable trap.

---

## Dummy Variable Creation for Store Type

The original `store_type` variable had three categories:

* Mall
* Standalone
* Franchise

Two dummy variables were created:

* `store_Mall`
* `store_Standalone`

Reference category:

* **Franchise**

Encoding:

* If store_type = Mall → store_Mall = 1, else 0
* If store_type = Standalone → store_Standalone = 1, else 0
* If both are 0 → Franchise (reference)

This avoids redundancy.

---

## Final Approach

The dummy variables were created in the `Dummy_Variables` worksheet of the regression workbook.

To avoid multicollinearity and improve model stability, the final regression model used only the numerical predictors while keeping dummy variables documented for categorical transformation.


# Task 8: Model Equations

## Simple Regression Equations

### Model 1: Marketing Spend

Monthly Sales = Intercept + (Coefficient × Marketing Spend)

Monthly Sales = 558677.514 + 1.754 × (marketing_spend)

### Business Meaning

This model estimates how monthly sales change based only on marketing spend.

The coefficient shows how much additional sales are expected for every extra unit spent on marketing.

This helps the business evaluate whether increasing marketing budgets may improve sales.

---

### Model 2: Footfall

Monthly Sales = 450762.761 + 34.878(Footfall)

### Business Meaning

This model estimates how monthly sales change based on customer visits.

The coefficient shows that every additional customer visit increases monthly sales by approximately 34.878 units.

This highlights the importance of store traffic in improving revenue.

---

## Multiple Regression Equation

Monthly Sales = 83893.924

* 1.194(Marketing Spend)
* 33.782(Footfall)
* 2991.993(Inventory Availability %)
* 11255.192(Customer Rating)

- 2786.971(Region North)

---

## Explanation of Each Coefficient

### Marketing Spend (1.194)

For every additional 1-unit increase in marketing spend, monthly sales increase by 1.194 units.

Business meaning:
Investing more in marketing has a positive impact on sales growth.

---

### Footfall (33.782)

For every additional customer visit, monthly sales increase by 33.782 units.

Business meaning:
Stores with higher customer traffic generate stronger sales.

This is one of the strongest sales drivers.

---

### Inventory Availability Percentage (2991.993)

Higher inventory availability increases monthly sales by 2991.993 units.

Business meaning:
Stores that maintain better stock levels can meet customer demand more effectively.

This improves revenue performance.

---

### Customer Rating (11255.192)

A 1-point increase in customer rating increases monthly sales by 11255.192 units.

Business meaning:
Customer satisfaction strongly influences store sales.

Better customer experiences lead to better business performance.

---

### Region North (-2786.971)

Stores in the North region have lower sales by 2786.971 units compared to the reference category.

Business meaning:
Regional location may slightly affect performance, but in this model the effect was weak.

---

## Dummy Variable Explanation

Dummy variables are used to convert categorical variables into numerical form for regression analysis.

For this model:

Region was converted into:

* region_north
* region_south

Each dummy variable takes:

* 1 = if the store belongs to that category
* 0 = otherwise

This allows the model to compare performance across regions.

---

## Reference Category Used

Reference category for region:

* West

This means:

If both region_north and region_south are 0, the store belongs to West.

All regional comparisons are made against West.

---

## Final Model Selected

Final selected model:

* Multiple Regression Model

---

## Reason for Selecting Final Model

The multiple regression model was selected because it had the highest explanatory power.

Model comparison:

* Marketing Spend model → R² = 0.140
* Footfall model → R² = 0.7291
* Multiple Regression model → R² = 0.81

This means the final model explains the highest percentage of sales variation.

From a business perspective, it provides a more complete understanding of the factors affecting sales and supports stronger decision-making in:

* marketing investment
* inventory planning
* customer satisfaction
* store operations
