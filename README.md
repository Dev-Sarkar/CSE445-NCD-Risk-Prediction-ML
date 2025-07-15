# Predicting NCD Risk Factors in Bangladesh Using Machine Learning

## Overview
This project applies machine learning techniques to predict the risk of major non-communicable diseases (NCDs)—specifically diabetes, hypertension, overweight/obesity, and hyperglycemia. Utilizing the nationally representative Bangladesh WHO STEPS 2018 survey , the pipeline processes complex socio-demographic, behavioral, and clinical data to build highly accurate and interpretable predictive models.


## Methodology & Tech Stack
* **Data Preprocessing:** Handled missing values via median/mode imputation, transformed range-based features, and applied label encoding.
* **Imbalance Handling:** Utilized **SMOTENC** for heavily imbalanced targets (diabetes, hyperglycemia) and class-weight adjustments for moderate imbalances.
* **Modeling Algorithms:** Evaluated Logistic Regression, Random Forest, Support Vector Machines (SVM), XGBoost, LightGBM, CatBoost, and a Stacking Ensemble.
* **Optimization:** Conducted automated hyperparameter tuning using **Optuna** (Tree-structured Parzen Estimator).
* **Evaluation Metrics:** ROC-AUC, PR-AUC, Accuracy, Precision, Recall, and F1-Score.

## Key Results
* **Top Performing Models:** CatBoost and XGBoost achieved the best discriminative performance for diabetes and hypertension. LightGBM and ensemble methods excelled for obesity prediction.
* **Explainable AI (XAI):** Integrated **SHAP** (SHapley Additive Explanations) to solve the "black-box" problem. The global and local SHAP analyses identified age, BMI, blood pressure, physical activity, and dietary habits as the most critical risk factors.