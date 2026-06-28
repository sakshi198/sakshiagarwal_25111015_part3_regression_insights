# Task 7: Residual Analysis

## Predicted Sales and Residual Calculation

The final multiple regression model was used to calculate predicted monthly sales.

Regression equation used:

Monthly Sales = 83893.924

* 1.194(Marketing Spend)
* 33.782(Footfall)
* 2991.993(Inventory Availability %)
* 11255.192(Customer Rating)

- 2786.971(Region North)

Residual formula:

Residual = Actual Sales − Predicted Sales

Residuals help identify where the model performs well and where it makes larger errors.

---

## Largest Positive Residuals

These are cases where actual sales were higher than predicted.

This means the model **under-predicted** performance.

| Rank | Residual    |
| ---- | ----------- |
| 1    | 133695.9543 |
| 2    | 122437.6779 |
| 3    | 113900.9183 |
| 4    | 108345.6651 |
| 5    | 103403.1153 |

### Business Meaning

These stores performed much better than expected.

Possible reasons:

* Strong local demand
* Better store management
* Special promotions not captured in the model
* Seasonal effects
* Better customer loyalty

This suggests the model may be missing additional important variables.

---

## Largest Negative Residuals

These are cases where actual sales were lower than predicted.

This means the model **over-predicted** performance.

| Rank | Residual     |
| ---- | ------------ |
| 1    | -112810.1301 |
| 2    | -104355.8170 |
| 3    | -100346.6384 |
| 4    | -94723.7214  |
| 5    | -88210.5869  |

### Business Meaning

These stores performed worse than expected.

Possible reasons:

* Poor execution
* Local competition
* Operational issues
* Low customer satisfaction
* External disruptions

This indicates some stores underperform despite having strong predictor values.

---

## Model Behavior Analysis

The model appears to both under-predict and over-predict in certain cases.

Under-prediction may occur for high-performing stores with factors not included in the model.

Over-prediction may occur for weaker stores facing challenges not captured in the data.

This suggests that while the model explains 81% of the variation in sales, there are still hidden business factors affecting performance.

---

## Business Conclusion

Residual analysis shows that the regression model performs strongly overall but is not perfect.

Leadership should use this model as a decision-support tool, while also considering:

* local market conditions
* store management quality
* promotions
* competition
* seasonality

These factors may improve prediction accuracy in future models.
