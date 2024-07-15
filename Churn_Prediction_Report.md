## Analysis of Classification Reports

### Summary
This analysis compares the performance of several classifiers on an imbalanced dataset, employing various techniques to address class imbalance. These techniques include adjusting class weights as model parameters and using methods such as computing sample weights, SMOTE, over-sampling, and under-sampling. The models evaluated include Gradient Boosting, XGBoost, RandomForest, LGBM, CatBoost, AdaBoost, Isolation Forest, and SVM. Below is a summary of their performance, focusing on precision, recall, and F1-score for the minority class (class 1, churned customers).

### Key Metrics
- **Precision**: Measures the proportion of true positive predictions among all positive predictions (true positives + false positives).
- **Recall (Sensitivity)**: Measures the proportion of true positive predictions among all actual positive instances (true positives + false negatives).
- **F1-score**: Harmonic mean of precision and recall, providing a balance between the two.

## Model Performance Summary

### Gradient Boosting
| Metric            | Original |+ argument to handle imbalance | + Sample-Weight |  + SMOTE    | + Over-Sampling | + Under-Sampling |
|-------------------|----------|-------------------------------|-----------------|-------------|-----------------|------------------|
| Class 1 Precision |  0.77    |           --                  |       0.72      |    0.60     |      0.51       |       0.50       |
| Class 1 Recall    |  0.47    |           --                  |       0.53      |    0.63     |      0.74       |       0.76       |
| Class 1 F1-Score  |  0.59    |           --                  |       0.59      |    0.61     |      0.61       |       0.60       |


### XGBoost
| Metric            | Original |+ argument to handle imbalance | + Sample-Weight |  + SMOTE    | + Over-Sampling | + Under-Sampling |
|-------------------|----------|-------------------------------|-----------------|-------------|-----------------|------------------|
| Class 1 Precision |  0.71    |           0.56                |       0.67      |    0.61     |      0.57       |      0.46        |
| Class 1 Recall    |  0.50    |           0.64                |       0.52      |    0.59     |      0.62       |      0.75        |
| Class 1 F1-Score  |  0.58    |           0.60                |       0.58      |    0.60     |      0.59       |      0.57        |


### RandomForest
| Metric            | Original |+ argument to handle imbalance | + Sample-Weight |  + SMOTE    | + Over-Sampling | + Under-Sampling |
|-------------------|----------|-------------------------------|-----------------|-------------|-----------------|------------------|
| Class 1 Precision |  0.77    |           0.79                |      0.78       |    0.62     |      0.68       |      0.48        |
| Class 1 Recall    |  0.47    |           0.45                |      0.45       |    0.59     |      0.54       |      0.74        |
| Class 1 F1-Score  |  0.58    |           0.57                |      0.57       |    0.60     |      0.60       |      0.58        |


### LGBM
| Metric            | Original |+ argument to handle imbalance | + Sample-Weight |  + SMOTE    | + Over-Sampling | + Under-Sampling |
|-------------------|----------|-------------------------------|-----------------|-------------|-----------------|------------------|
| Class 1 Precision |  0.74    |           0.54                |      0.70       |    0.62     |      0.55       |      0.48        |
| Class 1 Recall    |  0.49    |           0.70                |      0.53       |    0.61     |      0.70       |      0.76        |
| Class 1 F1-Score  |  0.59    |           0.61                |      0.59       |    0.62     |      0.62       |      0.58        |


### CatBoost
| Metric            | Original |+ argument to handle imbalance | + Sample-Weight |  + SMOTE    | + Over-Sampling | + Under-Sampling |
|-------------------|----------|-------------------------------|-----------------|-------------|-----------------|------------------|
| Class 1 Precision |  0.76    |           0.54                |      0.71       |    0.62     |       0.56      |      0.49        |
| Class 1 Recall    |  0.50    |           0.71                |      0.53       |    0.61     |       0.68      |      0.76        |
| Class 1 F1-Score  |  0.60    |           0.62                |      0.60       |    0.62     |       0.61      |      0.60        |


### AdaBoost
| Metric            | Original |+ argument to handle imbalance | + Sample-Weight |  + SMOTE    | + Over-Sampling | + Under-Sampling |
|-------------------|----------|-------------------------------|-----------------|-------------|-----------------|------------------|
| Class 1 Precision |  0.72    |            --                 |       0.69      |    0.52     |       0.47      |      0.47        |
| Class 1 Recall    |  0.45    |            --                 |       0.48      |    0.65     |       0.74      |      0.75        |
| Class 1 F1-Score  |  0.55    |            --                 |       0.54      |    0.58     |       0.57      |      0.58        |


### Isolation Forest
| Metric            | Original |+ argument to handle imbalance | + Sample-Weight |  + SMOTE    | + Over-Sampling | + Under-Sampling |
|-------------------|----------|-------------------------------|-----------------|-------------|-----------------|------------------|
| Class 1 Precision |  0.23    |            --                 |     --          |     --      |       --        |        --        |
| Class 1 Recall    |  0.86    |            --                 |     --          |     --      |       --        |        --        |
| Class 1 F1-Score  |  0.36    |            --                 |     --          |     --      |       --        |        --        |

### SVM
| Metric            | Original |+ argument to handle imbalance | + Sample-Weight |  + SMOTE    | + Over-Sampling | + Under-Sampling |
|-------------------|----------|-------------------------------|-----------------|-------------|-----------------|------------------|
| Class 1 Precision |  0.80    |            0.50               |       0.73      |    0.61     |       0.50      |       0.48       |
| Class 1 Recall    |  0.38    |            0.74               |       0.47      |    0.58     |       0.73      |       0.74       |
| Class 1 F1-Score  |  0.52    |            0.59               |       0.54      |    0.60     |       0.59      |       0.58       |


