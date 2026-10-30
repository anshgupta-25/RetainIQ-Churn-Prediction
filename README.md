# RetainIQ: Customer Churn Early-Warning Engine

CSE305 Machine Learning Fundamentals – Mini Project 2 (CA3), Option 2.

Logistic Regression model that predicts whether a telecom customer is likely to churn, using the
[Telco Customer Churn dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn).

## Files
| File | Description |
|---|---|
| `RetainIQ_Churn_Prediction.ipynb` | Fully executed notebook (Tasks 1–9) |
| `RetainIQ_Report.docx` | Project report |
| `WA_Fn-UseC_-Telco-Customer-Churn.csv` | Dataset (loaded with a relative path) |
| `figures/` | Plots saved by the notebook and used in the report |

## Key results (test set, 1,409 customers)
| Threshold | Accuracy | Precision | Recall | F1 |
|---|---|---|---|---|
| 0.50 (default) | 0.806 | 0.659 | 0.559 | 0.605 |
| **0.30 (chosen)** | 0.750 | 0.520 | **0.757** | **0.617** |

Lowering the threshold to 0.30 catches 74 more churners (283 vs 209) at the cost of 153 extra false alarms.

## Run
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook RetainIQ_Churn_Prediction.ipynb
```
