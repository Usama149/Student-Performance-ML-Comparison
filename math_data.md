# Student Performance ML Comparison (Math Dataset)

Regression-based machine learning models applied to student performance data using Python.

## Overview
This project compares multiple machine learning regression models on the Student Performance dataset to evaluate how well they predict the final grade (`G3`).

The analysis was carried out in two settings:
1. **With prior grades `G1` and `G2` included**
2. **Without prior grades `G1` and `G2`**

This helps show how much predictive power comes from earlier academic performance.

## Models Tested
- Multiple Linear Regression
- Support Vector Regression (SVR)
- Decision Tree Regression
- Random Forest Regression

## Model Comparison

### With Prior Grades `G1` and `G2`

| Model | R² | MAE |
|------|------:|------:|
| Multiple Linear Regression | 0.766 | 1.680 |
| SVR | 0.583 | 2.214 |
| Random Forest | 0.843 | 1.255 |
| Decision Tree | 0.785 | 1.270 |

### Without Prior Grades `G1` and `G2`

| Model | R² | MAE |
|------|------:|------:|
| Multiple Linear Regression | 0.191 | 3.690 |
| SVR | 0.034 | 3.904 |
| Random Forest | 0.220 | 3.528 |
| Decision Tree | -0.200 | 4.210 |

## Key Notes
- The `school` column was removed because it had no meaningful impact on the model.
- The strongest predictors were the prior grades `G1` and `G2`.
- Removing `G1` and `G2` caused a clear drop in performance across all models.

## Best and Worst Results

### With Prior Grades `G1` and `G2`
**Best model:** Random Forest  
- **R²:** 0.843  
- **MAE:** 1.255  

**Worst model:** SVR  
- **R²:** 0.583  
- **MAE:** 2.214  

### Without Prior Grades `G1` and `G2`
**Best model:** Random Forest  
- **R²:** 0.220  
- **MAE:** 3.528  

**Worst model:** Decision Tree  
- **R²:** -0.200  
- **MAE:** 4.210  

## Model Comparison With and Without `G1` and `G2`

<img width="989" height="590" alt="Model_Comparison" src="https://github.com/user-attachments/assets/d07763fa-eef2-4efe-be22-1dc3e559d935" />

## Main Findings
- Prior grades `G1` and `G2` play a major role in predicting the final grade `G3`.
- Random Forest achieved the best performance among the tested models.
- Once `G1` and `G2` were removed, model performance dropped substantially.
- This suggests that earlier academic performance is much more informative than the remaining demographic and lifestyle variables.
- Random Forest likely benefited from capturing non-linear patterns and feature interactions better than the other models.4efe-be22-1dc3e559d935" />



### Main Findings
- Prior Grades play a major part in predicting the fina grade G3.
- Random Forest had a decent performance, outperforming other models.
- There were non-linear patterns and feature interactions captured by Random Forest and not by other models.


