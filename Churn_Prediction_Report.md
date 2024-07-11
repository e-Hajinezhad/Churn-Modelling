## Analysis of Classification Reports

### Summary
This analysis compares the performance of several classifiers on an imbalanced dataset, employing various techniques to address class imbalance. These techniques include adjusting class weights as model parameters and using methods such as SMOTE, over-sampling, and under-sampling. The models evaluated include Gradient Boosting, XGBoost, AdaBoost, RandomForest, LGBM, CatBoost, Isolation Forest, and SVM. Below is a summary of their performance, focusing on recall, and F1-score for the minority class (class 1, churned customers).

### Key Metrics

- **Recall**: Measures the ability to identify all actual positives.
- **F1-score**: Harmonic mean of precision and recall, providing a balance between the two.

## Model Performance Summary

### Gradient Boosting
| Metric            | Original | + SMOTE | + Over-Sampling | + Under-Sampling |
|-------------------|----------|---------|-----------------|------------------|
| Class 1 Recall    | 0.78     | 0.71    | 0.78            | 0.62             |
| Class 1 F1-Score  | 0.60     | 0.60    | 0.61            | 0.63             |

### XGBoost
| Metric            | Original | + SMOTE | + Over-Sampling | + Under-Sampling |
|-------------------|----------|---------|-----------------|------------------|
| Class 1 Recall    | 0.65     | 0.65    | 0.63            | 0.64             |
| Class 1 F1-Score  | 0.60     | 0.58    | 0.59            | 0.60             |

### AdaBoost
| Metric            | Original | + SMOTE | + Over-Sampling | + Under-Sampling |
|-------------------|----------|---------|-----------------|------------------|
| Class 1 Recall    | 0.79     | 0.71    | 0.76            | 0.62             |
| Class 1 F1-Score  | 0.60     | 0.58    | 0.57            | 0.60             |

### RandomForest
| Metric            | Original | + SMOTE | + Over-Sampling | + Under-Sampling |
|-------------------|----------|---------|-----------------|------------------|
| Class 1 Recall    | 0.45     | 0.66    | 0.53            | 0.61             |
| Class 1 F1-Score  | 0.57     | 0.59    | 0.60            | 0.61             |

### LGBM
| Metric            | Original | + SMOTE | + Over-Sampling | + Under-Sampling |
|-------------------|----------|---------|-----------------|------------------|
| Class 1 Recall    | 0.75     | 0.69    | 0.70            | 0.64             |
| Class 1 F1-Score  | 0.62     | 0.60    | 0.60            | 0.62             |

### CatBoost
| Metric            | Original | + SMOTE | + Over-Sampling | + Under-Sampling |
|-------------------|----------|---------|-----------------|------------------|
| Class 1 Recall    | 0.73     | 0.67    | 0.70            | 0.62             |
| Class 1 F1-Score  | 0.62     | 0.59    | 0.62            | 0.62             |

### Isolation Forest
| Metric            | Original | + SMOTE | + Over-Sampling | + Under-Sampling |
|-------------------|----------|---------|-----------------|------------------|
| Class 1 Recall    | 0.79     |         |                 |                  |
| Class 1 F1-Score  | 0.34     |         |                 |                  |

### SVM
| Metric            | Original | + SMOTE | + Over-Sampling | + Under-Sampling |
|-------------------|----------|---------|-----------------|------------------|
| Class 1 Recall    | 0.77     | 0.66    | 0.77            | 0.56             |
| Class 1 F1-Score  | 0.57     | 0.57    | 0.58            | 0.61             |