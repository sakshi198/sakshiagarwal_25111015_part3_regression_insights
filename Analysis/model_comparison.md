# Task 4: Simple Regression Models

## Model 1: Monthly Sales vs Marketing Spend

### Regression Equation

Monthly Sales = Intercept + (Coefficient × Marketing Spend)
Monthly Sales = 558677.514 + (1.754 x Marketing spend)
---

### Key Metrics

* Dependent Variable: monthly_sales
* Independent Variable: marketing_spend
* R-squared: 0.140
* Coefficient: 1.754
* P-value: 0.000

---

### Business Interpretation

The coefficient shows the expected increase in monthly sales for every one-unit increase in marketing spend.

A positive coefficient suggests that higher marketing investment leads to higher sales.

The p-value helps determine statistical significance. If it is below 0.05, the variable is considered significant.

The R-squared value indicates how much of the variation in sales is explained by marketing spend alone.

---

### Usefulness

Marketing spend appears to be a useful predictor of monthly sales.

## Model 2: Monthly Sales vs Footfall

### Regression Equation

Monthly Sales = 450762.761 + 34.879(Footfall)

---

### Key Metrics

* Dependent Variable: monthly_sales
* Independent Variable: footfall
* R-squared: 0.729
* Coefficient: 34.879
* P-value: 0.000

---

### Business Interpretation

The coefficient shows that for every additional customer visit, monthly sales increase by approximately 34.88 units.

The very low p-value indicates that footfall is highly statistically significant.

The R-squared value of 72.91% shows that footfall alone explains a large proportion of the variation in monthly sales.

---

### Usefulness

Footfall appears to be a strong and useful predictor of monthly sales.


# Task 5: Multiple Regression Model

## Regression Equation

Monthly Sales = 83893.924

* 1.194(Marketing Spend)
* 33.782(Footfall)
* 2991.993(Inventory Availability %)
* 11255.192(Customer Rating)

- 2786.971(Region North)

---

## Variables Used

### Dependent Variable

* monthly_sales

### Independent Variables

Numerical Variables:

* marketing_spend
* footfall
* inventory_availability_pct
* customer_rating

Dummy Variable:

* region_north

Reference Category:

* West

---

## R-squared

R-squared = 0.81

This means the model explains **81% of the variation** in monthly sales.

The model has strong explanatory power.

Adjusted R-squared = 0.80, which confirms that the model remains strong even after adjusting for the number of predictors.

---

## Intercept Interpretation

The intercept is **83893.924**.

This represents the estimated monthly sales when all independent variables are zero.

Its p-value is **0.091**, which means it is not statistically significant.

The intercept mainly acts as a baseline.

---

## Coefficient Interpretation

### Marketing Spend

Coefficient = **1.194**

This means for every 1-unit increase in marketing spend, monthly sales increase by **1.194 units**, holding all other variables constant.

P-value = **0.000**

This variable is highly significant.

Business meaning:
Increasing marketing investment is likely to improve sales.

---

### Footfall

Coefficient = **33.782**

This means for every additional customer visit, monthly sales increase by **33.782 units**.

P-value = **0.000**

This is highly significant.

Business meaning:
Customer traffic is one of the strongest drivers of sales.

---

### Inventory Availability Percentage

Coefficient = **2991.993**

This means that better inventory availability increases monthly sales by **2991.993 units**.

P-value = **0.000**

This variable is highly significant.

Business meaning:
Stores with better stock availability perform better.

---

### Customer Rating

Coefficient = **11255.192**

This means that a 1-unit increase in customer rating increases monthly sales by **11255.192 units**.

P-value = **0.025**

This variable is statistically significant.

Business meaning:
Customer satisfaction has a positive effect on store sales.

---

### Region North (Dummy Variable)

Coefficient = **-2786.971**

This means stores in the North region have lower monthly sales by **2786.971 units** compared to the reference category (West).

P-value = **0.667**

This variable is not statistically significant.

Business meaning:
Regional difference between North and West does not strongly affect sales in this model.

---

## Direction of Relationship

Positive Relationship:

* marketing_spend
* footfall
* inventory_availability_pct
* customer_rating

Negative Relationship:

* region_north

Positive variables increase sales.

Negative variables reduce sales.

---

## Significant Variables

Strong predictors (p < 0.05):

* marketing_spend
* footfall
* inventory_availability_pct
* customer_rating

Weak predictor:

* region_north

---

## Business Recommendation

The regression model suggests that the company should focus on:

* Increasing marketing spend strategically
* Improving customer footfall
* Maintaining high inventory availability
* Improving customer satisfaction

These factors have the strongest impact on monthly sales.

Regional targeting appears less important based on this model.


# Task 6: Model Comparison

## Model 1: Simple Regression (Marketing Spend)

### Variables Used

Dependent Variable:

* monthly_sales

Independent Variable:

* marketing_spend

---

### R-squared

* 0.140

This means the model explains 14% of the variation in monthly sales.

This shows weak explanatory power.

---

### Significant Variables

* marketing_spend

The p-value was below 0.05, which means marketing spend is statistically significant.

---

### Business Usefulness

This model helps understand the effect of marketing investment on monthly sales.

It can support budget planning and marketing strategy decisions.

---

### Limitations

The model only considers one factor and ignores customer traffic, stock availability, and customer satisfaction.

Its explanatory power is relatively low.

---

## Model 2: Simple Regression (Footfall)

### Variables Used

Dependent Variable:

* monthly_sales

Independent Variable:

* footfall

---

### R-squared

* 0.7291

This means the model explains 72.91% of the variation in monthly sales.

This shows strong explanatory power.

---

### Significant Variables

* footfall

The p-value was below 0.05, which means footfall is highly significant.

---

### Business Usefulness

This model helps measure the effect of customer traffic on sales.

It is useful for store traffic planning and operational improvements.

---

### Limitations

The model ignores marketing and inventory-related factors.

It only focuses on customer traffic.

---

## Model 3: Multiple Regression

### Variables Used

Dependent Variable:

* monthly_sales

Independent Variables:

* marketing_spend
* footfall
* inventory_availability_pct
* customer_rating
* region_north

---

### R-squared

* 0.81

This means the model explains 81% of the variation in monthly sales.

This is the strongest model among all three.

---

### Significant Variables

Strong variables:

* marketing_spend
* footfall
* inventory_availability_pct
* customer_rating

Weak variable:

* region_north

The weak variable has a p-value above 0.05.

---

### Business Usefulness

This model gives the most complete understanding of the factors affecting sales.

It supports decision-making for:

* marketing allocation
* inventory planning
* customer experience improvement
* regional strategy

---

### Limitations

The model does not include external factors like seasonality, promotions, and competitor actions.

Some categorical variables may not be strong predictors.

---

## Final Comparison

Among all three models:

* Marketing Spend model has weak explanatory power (R² = 0.140)
* Footfall model performs much better (R² = 0.7291)
* Multiple Regression performs best (R² = 0.81)

The multiple regression model is the most useful for business decision-making because it considers multiple important factors together and explains the highest variation in sales.
