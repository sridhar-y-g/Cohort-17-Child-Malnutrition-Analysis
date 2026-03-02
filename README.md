# Cohort-17-Child-Malnutrition-Analysis
# Predicting Stunting Percentage in Children Under Five Using Maternal Literacy and Prenatal Care Access

* **SDG Goal:** SDG 2 - Zero Hunger
* **Cohort Number:** 17
* **Submission Date:** 3rd March of 2026

## Team Members and Roles

| USN | Name | Role |
| :--- | :--- | :--- |
| 1GC23CS419 <br> 1GC22CS068 | Tasaduque Ullah <br> Mohammed Umar Maniyar | Data Collection |
| 1HK22A1062 | Zeba Shine | EDA |
| 1GC22CS096 | Safdar Iqbal |  |
| 1ST22CS240 <br> 1EW22IS070 | Vasanth Kumar HR <br> Nakshatra S | ML Engineer |
| 1ST22CS241 | Vibhashree R |  |
| 1MV22EC056 | Harshith GK |  |
| 2AV22CS005 <br> 4AD22EC062 | Amruta Suresh Aralelimath <br> Nayana M B | Evaluation |
| 1HK22A1063 | Hafeeza Tasneem |  |
| 1HK22EC051 | Hajira Shahanz A | Documentation |
| 1DT22IC003 | Akshay S |  |
| 4VM22IS004 <br> 1RI22CS108 | Benaka M <br> Sridhar Y Gowdar | Git Hub Repo |

### Cohort Leaders

| USN | Name | Role |
| :--- | :--- | :--- |
| 1ST22CS240 | Vasanth Kumar HR | President |
| 2AV22CS005 | Amruta Suresh Aralelimath | Vice President |
| 4VM22IS004 | Benaka M | Secretary |
| 1RI22CS108 | Sridhar Y Gowdar | Deputy Secretary |

---

## ABSTRACT
This project analyzes the relationship between maternal literacy, prenatal care access, and child stunting prevalence using data sourced from the World Bank's World Development Indicators (WDI) database. Relevant indicators including stunting prevalence (% of children under five), female literacy rate (%), and prenatal care coverage (%) were extracted and compiled into a structured dataset. The dataset was cleaned and preprocessed prior to analysis. Missing categorical values were handled using mode imputation to ensure data completeness. Exploratory Data Analysis (EDA) was conducted to examine distribution patterns and relationships between variables before proceeding to regression modeling. The study contributes to understanding how maternal education and healthcare access influence child malnutrition, supporting Sustainable Development Goal 2 (Zero Hunger).

## 1. INTRODUCTION
Child stunting is an indicator of chronic malnutrition and reflects long-term nutritional deprivation during early childhood. It significantly affects physical growth, cognitive development, and long-term productivity. Reducing stunting remains a critical public health objective, especially in developing regions. Maternal literacy plays a vital role in improving child health outcomes, as educated mothers are more likely to adopt improved nutrition practices, seek healthcare services, and maintain better hygiene standards. Similarly, access to prenatal care ensures early monitoring of pregnancy, nutritional counseling, and preventive healthcare interventions that directly influence child growth outcomes. This study applies a data-driven analytical approach to examine the impact of maternal literacy and prenatal care coverage on stunting prevalence.

## 2. PROBLEM STATEMENT
The objective of this project is to predict the stunting percentage in children under five based on maternal literacy and access to prenatal care, while handling missing categorical data using mode imputation.

## 3. SDG IMPACT ANALYSIS
This project aligns with Sustainable Development Goal 2: Zero Hunger, which aims to end all forms of malnutrition. Stunting reduction is a measurable indicator of progress toward this goal. By analyzing the relationship between maternal literacy, prenatal care access, and stunting prevalence, this study provides insights that may support evidence-based public health policies and targeted interventions aimed at reducing malnutrition and improving long-term socio-economic development.

## 4. DATASET DESCRIPTION

### 4.1 Data Source
The dataset was sourced from the World Bank's World Development Indicators (WDI) database, which provides internationally comparable statistics on development, education, and health indicators.
* **Source:** https://databank.worldbank.org/source/world-development-indicators
* The selected indicators include:
  * Prevalence of stunting, height-for-age (% of children under five)
  * Female literacy rate (%)
  * Prenatal care coverage (%)

### 4.2 Raw Dataset (CSV Compilation)
The extracted indicators were compiled into a structured CSV file for analysis. This CSV file served as the input dataset for preprocessing and analysis.

### 4.3 Dataset Overview
The dataset consists of structured observations representing the selected indicators. The target variable is stunting percentage, which is continuous in nature and suitable for regression analysis. The independent variables include maternal literacy rate and prenatal care coverage. The dataset was verified for structure, completeness, and compatibility with statistical modeling.

## 5. DATA PREPROCESSING

### 5.1 Missing Value Analysis
Missing value analysis was performed to identify incomplete entries in the dataset. The analysis indicated missing values in the prenatal care variable.

### 5.2 Mode Imputation
Since the prenatal care variable is categorical in nature, mode imputation was applied. Mode imputation replaces missing values with the most frequently occurring category in the respective column, preserving distribution characteristics. After imputation, no missing values remained in the dataset.

### 5.3 Outlier Detection
Outlier detection was conducted using boxplot visualization to assess the presence of extreme values that could influence regression results. The visualization indicated no extreme outliers significantly affecting dataset stability.

### 5.4 Encoding and Feature Preparation
Categorical variables were converted into numerical format using appropriate encoding techniques to ensure compatibility with regression modeling. The dataset was then structured by separating independent variables (maternal literacy and prenatal care) from the target variable (stunting percentage).

## 6. EXPLORATORY DATA ANALYSIS (EDA)

### 6.1 Distribution of Stunting Percentage
The distribution analysis indicates variability in stunting prevalence across observations, supporting the need for predictive modeling.

### 6.2 Maternal Literacy vs Stunting
A negative relationship is observed between maternal literacy and stunting prevalence, suggesting that higher literacy rates correspond to lower stunting percentage.

### 6.3 Prenatal Care vs Stunting
An inverse relationship is observed between prenatal care coverage and stunting prevalence, indicating that improved access to prenatal care is associated with reduced stunting rates.

### 6.4 Correlation Analysis
The correlation matrix confirms meaningful associations between maternal literacy, prenatal care access, and stunting percentage.

## 7. MODEL SELECTION & TECHNICAL STRATEGY
Since the target variable, stunting percentage, is continuous in nature, a regression-based modeling approach was selected. Regression models are appropriate for predicting numerical outcomes and analyzing the relationship between independent variables and a continuous dependent variable. 

To ensure robust evaluation and avoid reliance on a single approach, multiple regression models were implemented and compared. This allows identification of the most suitable model for the dataset. 

The following models were selected:
* **Linear Regression:** Used as a baseline model to evaluate the linear relationship between maternal literacy, prenatal care access, and stunting percentage.
* **Decision Tree Regressor:** Included to capture potential non-linear relationships.
* **Random Forest Regressor:** An ensemble learning method, implemented to improve prediction stability and reduce variance.

## 8. MODEL IMPLEMENTATION
The dataset was divided into training and testing sets using an 80:20 split ratio. The independent variables included maternal literacy rate and prenatal care coverage, while the dependent variable was stunting percentage. Each model was trained using the training dataset and evaluated on the testing dataset. The implementation was carried out using the Scikit-learn library in Python.

For each model, the following steps were performed:
* Model initialization
* Model training using the training dataset
* Prediction on the testing dataset
* Performance evaluation using MAE and $R^{2}$

This ensured consistent comparison across all models.

## 9. MODEL EVALUATION
Model performance was evaluated using the following metrics:
* **Mean Absolute Error (MAE):** Measures the average magnitude of prediction errors.
* **R-squared ($R^{2}$):** Indicates the proportion of variance in the dependent variable explained by the model.

These metrics were calculated using the test dataset to assess predictive performance.

### 9.1 Linear Regression Results
The Linear Regression model shows a scattered distribution of predicted values compared to actual values. Predictions appear concentrated within a limited range and tend to underpredict higher stunting percentages. The visual pattern indicates that the model struggles to accurately capture variability in higher stunting values, suggesting limited ability to model complex relationships between maternal literacy, prenatal care, and stunting percentage.

### 9.2 Decision Tree Regressor Results
The Decision Tree Regressor demonstrates an improved upward trend compared to Linear Regression. Predicted values increase as actual values increase, indicating the model captures non-linear relationships. However, noticeable dispersion and some extreme predictions are observed, suggesting moderate instability and possible overfitting tendencies.

### 9.3 Random Forest Regressor Results
The Random Forest model exhibits a clearer and more consistent upward trend between actual and predicted values. The points are more closely aligned along the expected direction, indicating stronger predictive performance. Compared to the other models, Random Forest demonstrates better generalization and reduced variance, making it more reliable for predicting stunting percentage.

## 10. MODEL COMPARISON
The performance of all three regression models was compared using Mean Absolute Error (MAE) and R-squared ($R^{2}$) values obtained from the test dataset.

| Model | MAE | $R^{2}$ |
| :--- | :--- | :--- |
| Linear Regression | 10.994 | 0.233 |
| Decision Tree | 7.072 | 0.474 |
| Random Forest | 6.776 | 0.629 |

The results indicate that Random Forest Regressor achieved the lowest MAE and highest $R^{2}$ score among the three models.

## 11. BEST MODEL JUSTIFICATION
Based on the evaluation results, the Random Forest Regressor demonstrated superior predictive performance compared to Linear Regression and Decision Tree models. With an $R^{2}$ score of approximately 0.63, it explains about 63% of the variance in stunting percentage. Additionally, it achieved the lowest MAE (6.78), indicating more accurate predictions. Therefore, Random Forest Regressor is selected as the final model for predicting stunting percentage.

## 12. OVERFITTING ANALYSIS
To assess model stability, training and testing performance were compared. Random Forest demonstrated improved performance on the test dataset compared to the baseline models. The difference between training and testing accuracy was not excessively large, indicating that the model does not exhibit severe overfitting. This suggests that the Random Forest model generalizes reasonably well to unseen data.

## 13. RESULTS & KEY INSIGHTS
The modeling results indicate that maternal literacy and prenatal care access significantly influence stunting prevalence. Linear Regression showed limited performance, suggesting that the relationship between predictors and stunting is not purely linear. Decision Tree improved performance by capturing non-linear patterns, while Random Forest provided the most accurate and stable predictions. The findings suggest that improvements in maternal education and healthcare access are associated with reduced stunting percentages. This highlights the importance of educational and healthcare interventions in addressing child malnutrition.

## 14. CONCLUSION
This study successfully developed and evaluated regression models to predict stunting percentage based on maternal literacy and prenatal care access. Among the models tested, Random Forest Regressor achieved the best performance with the lowest MAE and highest $R^{2}$ score. The results indicate that ensemble learning methods provide better predictive capability for this dataset. The findings support Sustainable Development Goal 2 (Zero Hunger) by demonstrating how maternal education and healthcare access contribute to reducing child malnutrition.

## 15. FUTURE SCOPE
Future work may include:
* Include additional socio-economic variables
* Expand dataset to more regions and years
* Apply advanced ensemble or boosting models
* Develop an interactive prediction interface

## 16. TEAM COLLABORATION & MEETING LOGS
Regular group meetings were conducted to ensure systematic progress and collaborative decision-making throughout the project. During these meetings, the team discussed dataset selection, preprocessing strategies, exploratory data analysis, model implementation, evaluation metrics, and report structuring.

* **26th February 2026:** Finalizing dataset selection, reviewing variables, and planning preprocessing steps.
* **27th February 2026:** Handling missing values using mode imputation, reviewing EDA outputs, and correlation analysis interpretation.
* **28th February 2026:** Training regression models, comparing Linear Regression, Decision Tree, and Random Forest, and reviewing evaluation metrics (MAE and $R^{2}$).
* **1st March 2026:** Model comparison, selecting best-performing model, and finalizing documentation structure.
