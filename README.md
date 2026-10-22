# Customer Churn Prediction

## Overview
This project explores customer churn in a telecommunications dataset and builds machine learning models to predict whether a customer is likely to leave the service.

The notebook covers exploratory data analysis, preprocessing, model training, and evaluation using Logistic Regression and Random Forest.

## Objectives
- Explore customer churn patterns in the dataset.
- Inspect missing values, duplicate records, and feature types.
- Visualize churn distribution and relationships between selected features.
- Prepare numerical and categorical features for machine learning.
- Train and compare classification models.
- Evaluate results using accuracy, precision, recall, F1-score, and confusion matrices.

## Dataset
The notebook uses the **Telco Customer Churn** dataset, commonly distributed as `WA_Fn-UseC_-Telco-Customer-Churn.csv`.

The original notebook loads the CSV from Google Drive. To run it elsewhere:
1. Obtain the dataset from its original source.
2. Upload it to your Google Drive or update the notebook's CSV path.
3. Do not upload the dataset to this repository unless its license and sharing terms permit redistribution.

## Models
- Logistic Regression
- Random Forest Classifier (`n_estimators=200`, `class_weight='balanced'`)

## Results
On the saved 20% test split, the notebook reports:

| Model | Accuracy | Precision (Churn = Yes) | Recall (Churn = Yes) | F1-score (Churn = Yes) |
|---|---:|---:|---:|---:|
| Logistic Regression | 0.807 | 0.660 | 0.561 | 0.607 |
| Random Forest | 0.788 | 0.625 | 0.500 | 0.556 |

The dataset is imbalanced, so accuracy alone is not sufficient. Recall and F1-score for the churn class are important when assessing how many customers who actually churn are identified. Based on the current notebook results, Logistic Regression performs better than Random Forest on these reported metrics.

These results reflect the notebook's current workflow and are not a guarantee of performance on future customers.

## Tools and Libraries
- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## How to Run
1. Download or clone this repository.
2. Open `customerChurn.ipynb` in [Google Colab](https://colab.research.google.com/) or Jupyter Notebook.
3. Obtain the dataset and make it accessible to the notebook.
4. Update the CSV file path in the data-loading cell if needed.
5. Run the notebook cells in order.

## Repository Contents
- `customerChurn.ipynb` — exploratory data analysis, preprocessing, model training, and evaluation.
- `README.md` — project documentation.

## Future Improvements
- Use a Scikit-learn pipeline so preprocessing is fitted only on training data and data leakage is avoided.
- Tune hyperparameters using cross-validation.
- Compare additional models and thresholds.
- Investigate ways to improve recall for the churn class.
- Add a simple interface for making predictions, if useful.

## Disclaimer
This is an educational machine learning project. It should not be used as the sole basis for real business decisions without further validation.
