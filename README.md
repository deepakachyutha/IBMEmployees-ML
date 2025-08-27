# IBMEmployees-ML

### Project Overview

This project presents a comprehensive, data-driven approach to predicting employee attrition using the IBM HR Analytics dataset. The objective was to move beyond a simple accuracy score and build an interpretable model that can provide actionable insights for business leaders. By understanding the key drivers of attrition, organizations can proactively address issues, improve retention, and save significant costs associated with talent loss.

This repository details the complete end-to-end machine learning pipeline, from initial data exploration and feature engineering to advanced model interpretation.

### Key Technical Features

1.  **Data Preprocessing & Feature Selection:**
    * Cleaned and preprocessed the dataset by dropping irrelevant columns and performing Label Encoding on all categorical variables to prepare the data for modeling.
    * Utilized **SelectKBest** with an ANOVA F-test to statistically identify the top 10 most influential features, focusing the model on the most impactful data.

2.  **Handling Class Imbalance:**
    * Recognized and addressed the significant class imbalance in the dataset (fewer "Yes" attrition cases) by implementing **SMOTE (Synthetic Minority Over-sampling Technique)** and applying **class weights** during model training. This ensures the model learns to effectively predict the minority class, which is crucial for this problem.

3.  **Model Training & Evaluation:**
    * Trained and evaluated three different classification models: Logistic Regression, Random Forest Classifier, and Support Vector Classifier (SVC).
    * The **Random Forest Classifier** was selected as the final model, achieving an accuracy of **~87%**.
    * Evaluated the model using a **Precision-Recall Curve**, a more robust metric than ROC/AUC for imbalanced datasets.

4.  **Model Interpretability & Explainable AI (XAI):**
    * To ensure the model's predictions were transparent and actionable, two powerful interpretation techniques were used:
        * **SHAP (SHapley Additive exPlanations):** Analyzed SHAP values to understand the impact of each feature on individual predictions, explaining *why* a specific employee was flagged as a flight risk.
        *  **Permutation Importance:** Assessed the global importance of each feature by measuring how model performance changes when a feature is shuffled, providing a clear ranking of attrition drivers.


## Technologies Used

- `Python`
- `Pandas`
- `NumPy`
- `Matplotlib`
- `Seaborn`
- `Scikit-learn`
- `Shap`
- `Imblearn (for SMOTE)`

### Results & Key Findings

The final Random Forest model achieved a strong predictive accuracy and provided clear, actionable insights.

* **Model Performance:**
    * **Accuracy:** The model achieved an accuracy of **~87%** on the test set.
    * **Evaluation:** A Precision-Recall Curve was used to evaluate performance, which is a more robust metric for imbalanced datasets.

* **Key Drivers of Attrition:**
    * The model's feature importance analysis revealed that factors like **OverTime, MonthlyIncome, and TotalWorkingYears** were among the most significant predictors of employee attrition.


---
## Dataset 
IBM HR Analytics Employee Attrition & Performance Dataset
Source: Kaggle
Link: https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset

## Dataset License Notice
The Titanic dataset used in this project is publicly available for educational use and is provided by platforms like Kaggle.

---
*Created by Deepak Battula*