# Evaluation_Metrics_Handling_Imbalanced_Data

This project explores the use of machine learning models to assist in **breast cancer diagnosis**. The goal is to classify tumors as **malignant** (cancerous) or **benign** (non-cancerous) using clinical measurement data. Multiple models were evaluated to determine which approach provides the most reliable predictions for medical decision making.

## Dataset

- **Dataset:** Breast Cancer Wisconsin (Diagnostic)
- **Samples:** 569
- **Features:** 30 numerical features including radius, texture, perimeter, area, smoothness, etc.
- **Target:** Diagnosis (`M` = malignant, `B` = benign)

## Key Metrics

- **True Positive (TP):** Correctly predicted cancer cases  
- **False Positive (FP):** Predicted cancer but actually benign  
- **False Negative (FN):** Predicted benign but actually cancer  

> **Recall** is critical in medical diagnosis to minimize missed cancer cases.  
> **F1-score** is preferred for imbalanced datasets as it balances precision and recall.

## Model Comparison

| Model                     | Accuracy | Macro Precision | Macro Recall | Macro F1-score |
|----------------------------|----------|----------------|--------------|----------------|
| Logistic Regression        | 0.98     | 0.98           | 0.98         | 0.98           |
| Balanced Logistic Regression | 0.96     | 0.95           | 0.96         | 0.95           |
| Decision Tree              | 0.91     | 0.90           | 0.92         | 0.91           |

### Confusion Matrices

- **Logistic Regression:**
- [[41 1]
[ 1 71]]


- **Balanced Logistic Regression:**
- [[41 1]
[ 4 68]]


## Observations

- **Logistic Regression**: High stability and predictive performance; less prone to overfitting.  
- **Balanced Logistic Regression**: Slightly lower performance because the dataset is already balanced.  
- **Decision Tree**: More interpretable but prone to overfitting due to complex rules.  

**Conclusion:** Logistic Regression is the preferred model for this dataset due to its stability and high recall, which is crucial in medical diagnosis.
