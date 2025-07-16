# IBMEmployees-ML

## IBMEmployeesModel

This project uses machine learning to analyze IBM HR employee data and predict employee attrition. The objective is to help businesses understand why employees leave and take preemptive actions.


### Tasks Performed

1. Data Preprocessing
- Cleaning Data by dropping irrelevant columns like: `EmployeeCount`, `Over18`, `StandardHours`
- Label encoded all categorical variables
- Exported the cleaned dataset for further use

2. Feature Selection
- Used SelectKBest with ANOVA F-test to select the Top 10 Features influencing attrition

3. Model Training & Evaluation
- Trained and evaluated 3 classification models: `Logistic Regression`, `Random Forest Classifier` and `Support Vector Classifier (SVC)`
- For each model, we calculated: `Accuracy`, `Classification Report` and `Confusion Matrix`

4. Feature Importance
- Extracted feature importance using `RandomForestClassifier`
- Visualized the Top 15 most influential features on attrition using `RandomForestClassifier` from `sklearn`

### Results

- Top 15 Features by SelectKBest: MonthlyIncome, Overtime, Age, Dailyrate, TotalWorkingYears, MonthlyRate, HourlyRate, etc.
- Random Forest Accuracy: ~87.0748% 
- Logistic Regrssion Accuracy: ~87.0748%
- SVC Accuracy: ~86.7346%

Feature Importance Plot: A horizontal bar chart showing most critical factors for attrition.


### Things I Learnt

- Data preprocessing & encoding techniques
- Feature selection using statistical tests
- Comparison of machine learning models
- Interpretability using feature importance
- Evaluation using precision, recall, F1-score

### Future Upgrades
- I want to learn and use SHAP/LIME for deeper explaination
- Handle class imbalance using SMOTE or class_weight

## IMBEmployeeVisu (Data Visualisation)

### Tasks Performed

1. Data Visualisation
- Plotted a Barh Graph comparing Attrition Rate by Department

## Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Dataset 
IBM HR Analytics Employee Attrition & Performance Dataset
Source: Kaggle



## Dataset License Notice
The Titanic dataset used in this project is publicly available for educational use and is provided by platforms like Kaggle.

*Created by Deepak Battula*