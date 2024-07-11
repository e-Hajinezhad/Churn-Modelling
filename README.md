# Churn Prediction Modeling

This project aims to predict customer churn using various machine learning classifiers and techniques to handle imbalanced data. The project includes data preparation, exploratory data analysis, data transformation, model training, and evaluation.

## Data Preparation
- **Libraries Used**: 
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `seaborn`
  - `sklearn`
  - `xgboost`
  - `lightgbm`
  - `catboost`
  - `imblearn`
- Loaded the churn dataset.
- Removed unnecessary columns (`RowNumber`, `CustomerId`, and `Surname`).
- Transformed categorical variables (`Geography` and `Gender`) into numerical values.


## Exploratory Data Analysis (EDA)
- The Exploratory Data Analysis (EDA) provides visual insights into various features of the dataset, focusing on differences between customers who have exited (churned) and those who have not. Key features analyzed include:

   - Geography and Gender: Distribution of exited customers by region and gender.
   - Credit Score: Comparison of credit scores between exited and non-exited customers.
   - Number of Products: Distribution of the number of products held by each group.
   - Credit Card Ownership: Analysis of credit card ownership status.
   - Age and Estimated Salary: Age and salary distribution among both groups.
   - Active Membership: Comparison of active membership status.
   - Tenure and Balance: Examination of the tenure and account balance distribution.

These visualizations help identify significant patterns and differences, providing a solid foundation for building predictive models.

## Handling Imbalanced Data
- The dataset showed a significant class imbalance, with class 0 (non-churned customers) being 3.9 times more frequent than class 1 (churned customers).
- In the machine learning models, class weights were first adjusted to handle the imbalance (as the model parameters). Subsequently, one of the following techniques was applied without adjusting class weights.
- Techniques applied to address this imbalance:
  - **SMOTE (Synthetic Minority Over-sampling Technique)**: This method generates synthetic samples for the minority class to balance the class distribution.
  - **Random Over-Sampling**: This technique involves randomly duplicating samples from the minority class to increase its representation in the dataset.
  - **Random Under-Sampling**: This approach involves randomly removing samples from the majority class to balance the class distribution.
- **Isolation Forest**: This method was used to treat class 1 (churned customers) as an outlier, aiming to identify minority class instances by their anomalous behavior in the dataset.

## Modeling
- Classifiers used:
  - `GradientBoostingClassifier`
  - `XGBClassifier`
  - `AdaBoostClassifier`
  - `RandomForestClassifier`
  - `LGBMClassifier`
  - `CatBoostClassifier`
  - `IsolationForest`
  - `SVC` (Support Vector Classifier)

## Model Evaluation
- Models were evaluated using `classification_report` with a focus on:
  - **Recall for Class 1**: Ensuring most churners are identified for retention efforts.
  - **F1-Score for Class 1**: Balancing recall and precision to avoid false positives while identifying churners.

For detailed conclusions and model performance, refer to the [Churn Prediction Report](./Churn_Prediction_Report.md).


## Conclusion
The choice of model and balancing technique should align with business objectives. If identifying most churners is critical, a conservative approach with high recall is preferred. For a more balanced approach, models with higher F1-scores are recommended.

## How to Run
1. Clone the repository.
   ```sh
   git clone https://github.com/e-Hajinezhad/Churn-Modeling.git

 For any questions or feedback, please contact e.hajinezhad@gmail.com