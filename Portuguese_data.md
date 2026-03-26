# Student Performance Prediction using Regression and Tree-Based Models

## Project Overview

This project explores how well different machine learning models can predict student final exam performance using the **Student Performance Dataset**. The analysis compares model performance on student-related features such as study time, absences, family background, and social factors, with special attention to the role of prior grades **G1** and **G2**.

The main goal was to understand both:

* how accurately different models can predict the final grade **G3**, and
* which features carry the most predictive power.

## Dataset

The project uses the **Student Performance Dataset**, which contains student demographic, social, school, and academic information.

Target variable:

* **G3** — final grade

Important predictor variables:

* **G1** — first period grade
* **G2** — second period grade
* Study time
* Absences
* Failures
* Family and social background variables

Two versions of the dataset were explored:

* **Mathematics dataset**
* **Portuguese dataset**

## Models Used

The following regression models were applied:

* Multiple Linear Regression
* Support Vector Regression (SVR)
* Decision Tree Regression
* Random Forest Regression

## Main Findings

### 1. Prior grades dominate prediction

The strongest result from the analysis is that **G1 and G2 are the most important predictors of G3**.

When G1 and G2 were included, all models performed well.
When G1 and G2 were removed, model performance dropped sharply.

### 2. Performance with and without G1 and G2

For the Portuguese dataset, the comparison showed:

* **Multiple Linear Regression**: strong performance with G1/G2, weak performance without them
* **SVR**: retained the best performance after removing G1/G2, but still dropped substantially
* **Decision Tree**: became unstable and performed very poorly without G1/G2
* **Random Forest**: performed strongly with G1/G2, but dropped significantly without them

### 3. Interpretation

This suggests that **earlier academic performance is far more useful for predicting final grade than demographic or lifestyle variables alone**.

In other words, once prior grades are removed, the remaining features provide only limited predictive signal.

## Results Summary

### Portuguese dataset

Approximate R² results:

| Model                      | With G1 and G2 | Without G1 and G2 |
| -------------------------- | -------------: | ----------------: |
| Multiple Linear Regression |           0.84 |              0.13 |
| SVR                        |           0.75 |              0.21 |
| Decision Tree              |           0.71 |             -1.00 |
| Random Forest              |           0.83 |              0.12 |

## Key Conclusion

The analysis shows that:

* **G1 and G2 are essential predictive features**
* Removing them causes a major decline in model quality
* The dataset contains limited standalone predictive power outside prior academic achievement
* SVR was the most resilient model after removing the dominant predictors
* Decision Trees were the most sensitive to feature removal

## Project Structure

```bash
.
├── data/
│   ├── student-mat.csv
│   └── student-por.csv
├── notebooks/
│   ├── Performance Comparison (Portuguese).ipynb
│   └── other_model_experiments.ipynb
├── figures/
│   └── performance_comparison.png
└── README.md
```

## Skills Demonstrated

* Data preprocessing
* Feature analysis
* Regression modeling
* Model comparison
* Performance evaluation using R²
* Interpretation of feature importance
* Communicating findings through visualizations and documentation

## Future Improvements

Possible next steps for this project:

* Perform cross-validation for more robust evaluation
* Tune hyperparameters for SVR, Decision Tree, and Random Forest
* Compare feature importance across both datasets
* Evaluate MAE and RMSE in addition to R²
* Explore model explainability using SHAP or permutation importance

## Why this project matters

This project demonstrates an important data science lesson:

> A model may appear highly accurate, but much of that accuracy can come from a small number of highly informative features.

By removing G1 and G2, this project shows how strongly the prediction task depends on prior student grades and helps reveal the true predictive value of the remaining variables.

## Author

**Usama**

Master’s student exploring machine learning, data science, and applied predictive modeling.
