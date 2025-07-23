#  Credit Risk Modeling - Default Prediction

This project predicts the probability of serious financial distress within 2 years using machine learning techniques. The model helps financial institutions assess credit risk more accurately.

---

##  Project Objective

To build a binary classification model that predicts whether a borrower will default (SeriousDlqin2yrs = 1) based on financial features like debt ratio, income, and credit history.

---

##  Technologies Used

- Python
- CatBoost/XGBoost
- Scikit-learn
- Pandas/Numpy
- SMOTE (Imbalanced Learning)
- Matplotlib/Seaborn
- Jupyter Notebook

---

##  Dataset

Dataset used: **Give Me Some Credit**  
Source: [Kaggle Competition](https://www.kaggle.com/c/GiveMeSomeCredit)

Key Features:
- `DebtRatio`: Total monthly debt payments / monthly income
- `MonthlyIncome`: Borrower's monthly income
- `NumberOfOpenCreditLines`: Open credit lines
- `NumberOfTimes90DaysLate`: Payment delays
- `SeriousDlqin2yrs`: Target variable (1 = default within 2 years)

> ⚠Note: Highly imbalanced dataset (6.68% positive class)

---

##  Model Training

Trained using CatBoost with class imbalance handling:

**Training Configuration:**
- Algorithm: CatBoostClassifier
- Iterations: 2000  
- Learning Rate: 0.01  
- Depth: 8  
- Evaluation Metric: F1-Score  
- Class Handling: Auto Weight Balancing
- SMOTE Oversampling: Applied to minority class

---

##  Performance Metrics

| Metric         | Training | Validation |
|----------------|----------|------------|
| ROC-AUC        | 0.92     | 0.85       |
| F1-Score       | 0.81     | 0.72       |
| Precision      | 0.83     | 0.76       |
| Recall         | 0.79     | 0.68       |

> Threshold optimized at 0.2 for better recall


---
