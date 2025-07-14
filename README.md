
# Telco Churn Prediction

A logistic regression pipeline for predicting customer churn in a telecommunications company. This project demonstrates data loading, preprocessing, feature selection, model training, and evaluation using Python and scikit-learn.

---


##  Project Overview

Customer acquisition is more expensive than retention. In this notebook-based project we:

1. **Load** the IBM Telco Churn dataset from S3  
2. **Select** a subset of key features (`tenure`, `age`, `address`, `income`, `ed`, `employ`, `equip`)  
3. **Normalize** and **split** data into train/test sets  
4. **Train** a logistic regression model  
5. **Evaluate** performance using log-loss and interpret model coefficients

---

##  Dataset

The raw data is hosted in an Amazon S3 bucket used by the IBM Data Science Professional Certificate:  
`https://s3.amazonaws.com/ibm-datascience-course/ChurnData.csv`  

Each row represents a customer record with demographic, account, and service usage fields, plus a binary `churn` flag (1 = left, 0 = stayed).

---

##  Features

| Name     | Description                                 |
|----------|---------------------------------------------|
| tenure   | Months as customer                          |
| age      | Customer age (years)                        |
| address  | Years at current address                    |
| income   | Annual income (USD)                         |
| ed       | Education level (numeric code)              |
| employ   | Years with current employer                 |
| equip    | Number of equipment services subscribed     |
| churn    | Target variable: 1 = churn, 0 = no churn    |

---

##  Usage

1. **Download** the dataset (the notebook includes code to fetch the CSV from S3).  
2. **Run cells sequentially** to reproduce data cleaning, normalization, model training, and evaluation.  
3. **Inspect coefficients** and **compute log-loss** on the held-out test set.

---

##  Modeling & Evaluation

* **Train/Test Split**: 80% train / 20% test (`random_state=4`)  
* **Model**: `LogisticRegression()` from scikit-learn  
* **Metric**: Log Loss (binary cross-entropy)

---

##  Results

* **Log Loss:** 0.6258  
* **Interpretation:**  
  * Positive coefficients ↗ increase churn probability  
  * Negative coefficients ↘ decrease churn probability

---

##  Next Steps

1. **Additional Metrics**: accuracy, precision, recall, ROC-AUC  
2. **Hyperparameter Tuning**: regularization (L1/L2), cross-validation, grid/random search  
3. **Feature Engineering**: interaction terms, tenure buckets, categorical encodings  
4. **Alternate Models**: decision trees, random forests, gradient boosting


---

## 📄 License

This project is released under the MIT License. See [LICENSE](LICENSE) for details.
