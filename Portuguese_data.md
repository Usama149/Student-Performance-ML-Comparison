# Student Performance ML Comparison (Portuguese Dataset)

Regression-based machine learning models applied to student performance data using Python.

## Overview

This project compares multiple machine learning regression models on the Student Performance dataset to evaluate how well they predict the final grade (`G3`).

The analysis was carried out in two settings:

1. **With prior grades `G1` and `G2` included**
2. **Without prior grades `G1` and `G2`**

This helps show how much predictive power comes from earlier academic performance.

## Models Tested

* Multiple Linear Regression
* Support Vector Regression (SVR)
* Decision Tree Regression
* Random Forest Regression

## Model Comparison

### With Prior Grades `G1` and `G2`

| Model                      |   R² |
| -------------------------- | ---: |
| Multiple Linear Regression | 0.84 |
| SVR                        | 0.75 |
| Decision Tree              | 0.71 |
| Random Forest              | 0.83 |

### Without Prior Grades `G1` and `G2`

| Model                      |    R² |
| -------------------------- | ----: |
| Multiple Linear Regression |  0.13 |
| SVR                        |  0.21 |
| Decision Tree              | -1.00 |
| Random Forest              |  0.12 |

## Key Notes

* The Portuguese dataset contains more student records than the Math dataset.
* Prior grades `G1` and `G2` are the strongest predictors of final performance.
* Removing `G1` and `G2` caused a major drop in predictive performance across all models.
* Among the reduced models, SVR retained the highest R² score.

## Best and Worst Results

### With Prior Grades `G1` and `G2`

**Best model:** Multiple Linear Regression

* **R²:** 0.84

**Worst model:** Decision Tree

* **R²:** 0.71

### Without Prior Grades `G1` and `G2`

**Best model:** SVR

* **R²:** 0.21

**Worst model:** Decision Tree

* **R²:** -1.00

## Model Comparison With and Without `G1` and `G2`

Add your Portuguese performance comparison plot here.

Example:

```markdown
![Portuguese Model Comparison](figures/performance_comparison_portuguese.png)
```

## Main Findings

* Prior grades `G1` and `G2` play a major role in predicting the final grade `G3`.
* Model performance decreases sharply when `G1` and `G2` are removed.
* This indicates that earlier academic performance carries most of the predictive signal in the dataset.
* The remaining demographic, family, and lifestyle variables have limited standalone predictive power.
* SVR was the most resilient model after removing the strongest predictors, while the Decision Tree was the most unstable.

## Conclusion

This project shows that student final grade prediction in the Portuguese dataset depends heavily on prior grades. While several machine learning models perform well when earlier grades are available, their predictive ability drops strongly without them. This highlights the importance of feature selection and demonstrates how model performance can depend on a small number of highly informative variables.

## Author

**Usama**
