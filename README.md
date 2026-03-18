### Student-Performance-ML-Comparison (math data)
Regression model on a student performance data using Python

### Overview
Machine Learning Rgressions models are applied to a student performance data to check how well which model performes the best. 

### Models tested
- Multiple Linear Regression
- Support Vector Machine
- Decision Trees
- Random Forest

### Model Comparison

## With prior grades G1 and G2

| Model | R² | MAE |
|------|------:|------:|
| Multiple Linear Regression | 0.766 | 1.68 |
| SVR | 0.583 | 2.214 |
| Random Forest| 0.969 | 0.511 |
| Decision Trees | 0.785 | 1.27 |

## Without Prior Grades G1 and G2

| Model | R² | MAE |
|------|------:|------:|
| Multiple Linear Regression | 0.191 | 3.69 |
| SVR | 0.034 | 3.904 |
| Random Forest| 0.878 | 1.342 |
| Decision Trees | -0.20 | 4.21 |

### key results
- The school column was removed as it has no impact on the model because of a constant value

## With prior grades G1 and G2

# Best Result
- Random Forest performed the best.
- R^2 = 0.969
- MAE = 1.343

# Worst Result
- SVR performed the worst
- R^2 = 0.58
- MAE = 2.21

## Without prior grades G1 and G2

# Best Result
- Random Forest performed the best
- R^2 = 0.878
- MAE = 1.343

# Worst Result
- Decision Trees performes the least
- R^2 = -0.20
- MAE = 4.21

### Model Comaprison with and without G1 and G2

<img width="989" height="590" alt="Model Comparison With And Without G1   G2" src="https://github.com/user-attachments/assets/5774df4a-8fc2-438e-a249-ad5cb09008ea" />


### Main Findings
- Prior Grades play a major part in predicting the fina grade G3.
- Random Forest had a decent performance even though the prior grades were removed, outperforming other models.
- There were non-linear patterns and feature interactions captured by Random Forest and not by other models.


