# Cohort-17-Child-Malnutrition-Analysis
# [cite_start]Predicting Stunting Percentage in Children Under Five Using Maternal Literacy and Prenatal Care Access [cite: 1]

* [cite_start]**SDG Goal:** SDG 2 - Zero Hunger [cite: 2]
* [cite_start]**Cohort Number:** 17 [cite: 3]
* [cite_start]**Submission Date:** 3rd March of 2026 [cite: 4]

## [cite_start]Team Members and Roles [cite: 5]

| USN | Name | Role |
| :--- | :--- | :--- |
| 1GC23CS419 <br> 1GC22CS068 | Tasaduque Ullah <br> Mohammed Umar Maniyar | [cite_start]Data Collection [cite: 6] |
| 1HK22A1062 | Zeba Shine | [cite_start]EDA [cite: 6] |
| 1GC22CS096 | [cite_start]Safdar Iqbal |  [cite: 6] |
| 1ST22CS240 <br> 1EW22IS070 | Vasanth Kumar HR <br> Nakshatra S | [cite_start]ML Engineer [cite: 6] |
| 1ST22CS241 | [cite_start]Vibhashree R |  [cite: 6] |
| 1MV22EC056 | [cite_start]Harshith GK |  [cite: 6] |
| 2AV22CS005 <br> 4AD22EC062 | Amruta Suresh Aralelimath <br> Nayana M B | [cite_start]Evaluation [cite: 6] |
| 1HK22A1063 | [cite_start]Hafeeza Tasneem |  [cite: 6] |
| 1HK22EC051 | Hajira Shahanz A | [cite_start]Documentation [cite: 6] |
| 1DT22IC003 | [cite_start]Akshay S |  [cite: 6] |
| 4VM22IS004 <br> 1RI22CS108 | Benaka M <br> Sridhar Y Gowdar | [cite_start]Git Hub Repo [cite: 6] |

### [cite_start]Cohort Leaders [cite: 8]

| USN | Name | Role |
| :--- | :--- | :--- |
| 1ST22CS240 | Vasanth Kumar HR | [cite_start]President [cite: 7] |
| 2AV22CS005 | Amruta Suresh Aralelimath | [cite_start]Vice President [cite: 7] |
| 4VM22IS004 | Benaka M | [cite_start]Secretary [cite: 7] |
| 1RI22CS108 | Sridhar Y Gowdar | [cite_start]Deputy Secretary [cite: 7] |

---

## [cite_start]ABSTRACT [cite: 9]
[cite_start]This project analyzes the relationship between maternal literacy, prenatal care access, and child stunting prevalence using data sourced from the World Bank's World Development Indicators (WDI) database. [cite: 10] [cite_start]Relevant indicators including stunting prevalence (% of children under five), female literacy rate (%), and prenatal care coverage (%) were extracted and compiled into a structured dataset. [cite: 11] [cite_start]The dataset was cleaned and preprocessed prior to analysis. [cite: 12] [cite_start]Missing categorical values were handled using mode imputation to ensure data completeness. [cite: 12] [cite_start]Exploratory Data Analysis (EDA) was conducted to examine distribution patterns and relationships between variables before proceeding to regression modeling. [cite: 13] [cite_start]The study contributes to understanding how maternal education and healthcare access influence child malnutrition, supporting Sustainable Development Goal 2 (Zero Hunger). [cite: 14]

## [cite_start]1. INTRODUCTION [cite: 15]
[cite_start]Child stunting is an indicator of chronic malnutrition and reflects long-term nutritional deprivation during early childhood. [cite: 16] [cite_start]It significantly affects physical growth, cognitive development, and long-term productivity. [cite: 17] [cite_start]Reducing stunting remains a critical public health objective, especially in developing regions. [cite: 18] [cite_start]Maternal literacy plays a vital role in improving child health outcomes, as educated mothers are more likely to adopt improved nutrition practices, seek healthcare services, and maintain better hygiene standards. [cite: 19] [cite_start]Similarly, access to prenatal care ensures early monitoring of pregnancy, nutritional counseling, and preventive healthcare interventions that directly influence child growth outcomes. [cite: 20] [cite_start]This study applies a data-driven analytical approach to examine the impact of maternal literacy and prenatal care coverage on stunting prevalence. [cite: 21]

## [cite_start]2. PROBLEM STATEMENT [cite: 22]
[cite_start]The objective of this project is to predict the stunting percentage in children under five based on maternal literacy and access to prenatal care, while handling missing categorical data using mode imputation. [cite: 23]

## [cite_start]3. SDG IMPACT ANALYSIS [cite: 25]
[cite_start]This project aligns with Sustainable Development Goal 2: Zero Hunger, which aims to end all forms of malnutrition. [cite: 26] [cite_start]Stunting reduction is a measurable indicator of progress toward this goal. [cite: 27] [cite_start]By analyzing the relationship between maternal literacy, prenatal care access, and stunting prevalence, this study provides insights that may support evidence-based public health policies and targeted interventions aimed at reducing malnutrition and improving long-term socio-economic development. [cite: 28]

## [cite_start]4. DATASET DESCRIPTION [cite: 29]

### [cite_start]4.1 Data Source [cite: 30]
[cite_start]The dataset was sourced from the World Bank's World Development Indicators (WDI) database, which provides internationally comparable statistics on development, education, and health indicators. [cite: 31]
* [cite_start]**Source:** https://databank.worldbank.org/source/world-development-indicators [cite: 32, 33]
* [cite_start]The selected indicators include: [cite: 48]
  * [cite_start]Prevalence of stunting, height-for-age (% of children under five) [cite: 49]
  * [cite_start]Female literacy rate (%) [cite: 50]
  * [cite_start]Prenatal care coverage (%) [cite: 51]

### [cite_start]4.2 Raw Dataset (CSV Compilation) [cite: 53]
[cite_start]The extracted indicators were compiled into a structured CSV file for analysis. [cite: 54] [cite_start]This CSV file served as the input dataset for preprocessing and analysis. [cite: 56]

### [cite_start]4.3 Dataset Overview [cite: 57]
[cite_start]The dataset consists of structured observations representing the selected indicators. [cite: 58] [cite_start]The target variable is stunting percentage, which is continuous in nature and suitable for regression analysis. [cite: 59] [cite_start]The independent variables include maternal literacy rate and prenatal care coverage. [cite: 60] [cite_start]The dataset was verified for structure, completeness, and compatibility with statistical modeling. [cite: 88]

## [cite_start]5. DATA PREPROCESSING [cite: 90]

### [cite_start]5.1 Missing Value Analysis [cite: 91]
[cite_start]Missing value analysis was performed to identify incomplete entries in the dataset. [cite: 92] [cite_start]The analysis indicated missing values in the prenatal care variable. [cite: 103]

### [cite_start]5.2 Mode Imputation [cite: 104]
[cite_start]Since the prenatal care variable is categorical in nature, mode imputation was applied. [cite: 105] [cite_start]Mode imputation replaces missing values with the most frequently occurring category in the respective column, preserving distribution characteristics. [cite: 106] [cite_start]After imputation, no missing values remained in the dataset. [cite: 116]

### [cite_start]5.3 Outlier Detection [cite: 117]
[cite_start]Outlier detection was conducted using boxplot visualization to assess the presence of extreme values that could influence regression results. [cite: 118, 119] [cite_start]The visualization indicated no extreme outliers significantly affecting dataset stability. [cite: 129]

### [cite_start]5.4 Encoding and Feature Preparation [cite: 130]
[cite_start]Categorical variables were converted into numerical format using appropriate encoding techniques to ensure compatibility with regression modeling. [cite: 131] [cite_start]The dataset was then structured by separating independent variables (maternal literacy and prenatal care) from the target variable (stunting percentage). [cite: 132]

## [cite_start]6. EXPLORATORY DATA ANALYSIS (EDA) [cite: 133]

### [cite_start]6.1 Distribution of Stunting Percentage [cite: 134]
[cite_start]The distribution analysis indicates variability in stunting prevalence across observations, supporting the need for predictive modeling. [cite: 155]

### [cite_start]6.2 Maternal Literacy vs Stunting [cite: 156]
[cite_start]A negative relationship is observed between maternal literacy and stunting prevalence, suggesting that higher literacy rates correspond to lower stunting percentage. [cite: 171]

### [cite_start]6.3 Prenatal Care vs Stunting [cite: 172]
[cite_start]An inverse relationship is observed between prenatal care coverage and stunting prevalence, indicating that improved access to prenatal care is associated with reduced stunting rates. [cite: 188]

### [cite_start]6.4 Correlation Analysis [cite: 189]
[cite_start]The correlation matrix confirms meaningful associations between maternal literacy, prenatal care access, and stunting percentage. [cite: 227]

## [cite_start]7. MODEL SELECTION & TECHNICAL STRATEGY [cite: 232]
[cite_start]Since the target variable, stunting percentage, is continuous in nature, a regression-based modeling approach was selected. [cite: 233] [cite_start]Regression models are appropriate for predicting numerical outcomes and analyzing the relationship between independent variables and a continuous dependent variable. [cite: 234] 

[cite_start]To ensure robust evaluation and avoid reliance on a single approach, multiple regression models were implemented and compared. [cite: 235] [cite_start]This allows identification of the most suitable model for the dataset. [cite: 236] 

[cite_start]The following models were selected: [cite: 237]
* [cite_start]**Linear Regression:** Used as a baseline model to evaluate the linear relationship between maternal literacy, prenatal care access, and stunting percentage. [cite: 238, 241, 242]
* [cite_start]**Decision Tree Regressor:** Included to capture potential non-linear relationships. [cite: 239, 243]
* [cite_start]**Random Forest Regressor:** An ensemble learning method, implemented to improve prediction stability and reduce variance. [cite: 240, 244]

## [cite_start]8. MODEL IMPLEMENTATION [cite: 245]
[cite_start]The dataset was divided into training and testing sets using an 80:20 split ratio. [cite: 246] [cite_start]The independent variables included maternal literacy rate and prenatal care coverage, while the dependent variable was stunting percentage. [cite: 247] [cite_start]Each model was trained using the training dataset and evaluated on the testing dataset. [cite: 248] [cite_start]The implementation was carried out using the Scikit-learn library in Python. [cite: 249]

[cite_start]For each model, the following steps were performed: [cite: 250]
* [cite_start]Model initialization [cite: 251]
* [cite_start]Model training using the training dataset [cite: 252]
* [cite_start]Prediction on the testing dataset [cite: 254]
* [cite_start]Performance evaluation using MAE and $R^{2}$ [cite: 255]
[cite_start]This ensured consistent comparison across all models. [cite: 256]

## [cite_start]9. MODEL EVALUATION [cite: 257]
[cite_start]Model performance was evaluated using the following metrics: [cite: 258]
* [cite_start]**Mean Absolute Error (MAE):** Measures the average magnitude of prediction errors. [cite: 259]
* [cite_start]**R-squared ($R^{2}$):** Indicates the proportion of variance in the dependent variable explained by the model. [cite: 260]

[cite_start]These metrics were calculated using the test dataset to assess predictive performance. [cite: 261]

### [cite_start]9.1 Linear Regression Results [cite: 262]
[cite_start]The Linear Regression model shows a scattered distribution of predicted values compared to actual values. [cite: 280] [cite_start]Predictions appear concentrated within a limited range and tend to underpredict higher stunting percentages. [cite: 281] [cite_start]The visual pattern indicates that the model struggles to accurately capture variability in higher stunting values, suggesting limited ability to model complex relationships between maternal literacy, prenatal care, and stunting percentage. [cite: 282]

### [cite_start]9.2 Decision Tree Regressor Results [cite: 284]
[cite_start]The Decision Tree Regressor demonstrates an improved upward trend compared to Linear Regression. [cite: 301] [cite_start]Predicted values increase as actual values increase, indicating the model captures non-linear relationships. [cite: 302] [cite_start]However, noticeable dispersion and some extreme predictions are observed, suggesting moderate instability and possible overfitting tendencies. [cite: 303]

### [cite_start]9.3 Random Forest Regressor Results [cite: 304]
[cite_start]The Random Forest model exhibits a clearer and more consistent upward trend between actual and predicted values. [cite: 321] [cite_start]The points are more closely aligned along the expected direction, indicating stronger predictive performance. [cite: 322] [cite_start]Compared to the other models, Random Forest demonstrates better generalization and reduced variance, making it more reliable for predicting stunting percentage. [cite: 323]

## [cite_start]10. MODEL COMPARISON [cite: 324]
[cite_start]The performance of all three regression models was compared using Mean Absolute Error (MAE) and R-squared ($R^{2}$) values obtained from the test dataset. [cite: 325]

| Model | MAE | $R^{2}$ |
| :--- | :--- | :--- |
| Linear Regression | 10.994333081810574 | [cite_start]0.2338700101475073 | [cite: 326]
| Decision Tree | 7.0727810650887575 | [cite_start]0.47462017637887555 | [cite: 326]
| Random Forest | 6.776491124260356 | [cite_start]0.6298109799307027 | [cite: 326]

[cite_start]The results indicate that Random Forest Regressor achieved the lowest MAE and highest $R^{2}$ score among the three models. [cite: 327]

## [cite_start]11. BEST MODEL JUSTIFICATION [cite: 328]
[cite_start]Based on the evaluation results, the Random Forest Regressor demonstrated superior predictive performance compared to Linear Regression and Decision Tree models. [cite: 329] [cite_start]With an $R^{2}$ score of approximately 0.63, it explains about 63% of the variance in stunting percentage. [cite: 330] [cite_start]Additionally, it achieved the lowest MAE (6.78), indicating more accurate predictions. [cite: 331] [cite_start]Therefore, Random Forest Regressor is selected as the final model for predicting stunting percentage. [cite: 332]

## [cite_start]12. OVERFITTING ANALYSIS [cite: 333]
[cite_start]To assess model stability, training and testing performance were compared. [cite: 334] [cite_start]Random Forest demonstrated improved performance on the test dataset compared to the baseline models. [cite: 335] [cite_start]The difference between training and testing accuracy was not excessively large, indicating that the model does not exhibit severe overfitting. [cite: 336, 337] [cite_start]This suggests that the Random Forest model generalizes reasonably well to unseen data. [cite: 338]

## [cite_start]13. RESULTS & KEY INSIGHTS [cite: 339]
[cite_start]The modeling results indicate that maternal literacy and prenatal care access significantly influence stunting prevalence. [cite: 340] [cite_start]Linear Regression showed limited performance, suggesting that the relationship between predictors and stunting is not purely linear. [cite: 341] [cite_start]Decision Tree improved performance by capturing non-linear patterns, while Random Forest provided the most accurate and stable predictions. [cite: 342] [cite_start]The findings suggest that improvements in maternal education and healthcare access are associated with reduced stunting percentages. [cite: 343] [cite_start]This highlights the importance of educational and healthcare interventions in addressing child malnutrition. [cite: 344]

## [cite_start]14. CONCLUSION [cite: 345]
[cite_start]This study successfully developed and evaluated regression models to predict stunting percentage based on maternal literacy and prenatal care access. [cite: 346] [cite_start]Among the models tested, Random Forest Regressor achieved the best performance with the lowest MAE and highest $R^{2}$ score. [cite: 347] [cite_start]The results indicate that ensemble learning methods provide better predictive capability for this dataset. [cite: 348] [cite_start]The findings support Sustainable Development Goal 2 (Zero Hunger) by demonstrating how maternal education and healthcare access contribute to reducing child malnutrition. [cite: 349]

## [cite_start]15. FUTURE SCOPE [cite: 350]
[cite_start]Future work may include: [cite: 351]
* [cite_start]Include additional socio-economic variables [cite: 352]
* [cite_start]Expand dataset to more regions and years [cite: 353]
* [cite_start]Apply advanced ensemble or boosting models [cite: 354]
* [cite_start]Develop an interactive prediction interface [cite: 354]

## [cite_start]16. TEAM COLLABORATION & MEETING LOGS [cite: 356]
[cite_start]Regular group meetings were conducted to ensure systematic progress and collaborative decision-making throughout the project. [cite: 357] [cite_start]During these meetings, the team discussed dataset selection, preprocessing strategies, exploratory data analysis, model implementation, evaluation metrics, and report structuring. [cite: 363]

* [cite_start]**$26^{th}$ February 2026:** Finalizing dataset selection, reviewing variables, and planning preprocessing steps. [cite: 358, 359, 364, 365, 366, 367, 368]
* [cite_start]**$27^{th}$ February 2026:** Handling missing values using mode imputation, reviewing EDA outputs, and correlation analysis interpretation. [cite: 358, 360, 385, 386, 387, 388, 389]
* [cite_start]**$28^{th}$ February 2026:** Training regression models, comparing Linear Regression, Decision Tree, and Random Forest, and reviewing evaluation metrics (MAE and $R^{2}$). [cite: 358, 361, 396, 397, 398, 399]
* [cite_start]**$1^{st}$ March 2026:** Model comparison, selecting best-performing model, and finalizing documentation structure. [cite: 358, 362, 416, 417, 418, 419, 420]
