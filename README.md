# Stroke Prediction Machine Learning Project

## 1. Project Overview

This project aims to develop a machine learning model to **predict the likelihood of a patient experiencing a stroke**. Leveraging demographic and health-related features, the goal is to identify high-risk individuals early to facilitate appropriate preventive measures.

---

## 2. Dataset

The dataset contains patient information, including attributes such as:

* **Demographics:** `gender`, `age`, `ever_married`, `work_type`, `Residence_type`.
* **Health Metrics:** `hypertension`, `heart_disease`, `avg_glucose_level`, `bmi`, and `smoking_status`.
* **Target Variable:** `stroke` (1 if the patient had a stroke, 0 if not).

---

## 3. Methodology

### 3.1. Data Preprocessing

* Missing values in the `bmi` column were imputed using the median.
* The unique identifier (`id`) column was dropped.
* Categorical features were encoded using a combination of Label Encoding and One-Hot Encoding.
* The highly **imbalanced nature** of the dataset was addressed (e.g., using SMOTE or other techniques).

### 3.2. Models Evaluated

The following classification models were evaluated and hyperparameter tuned using cross-validation:

* Logistic Regression
* Random Forest Classifier
* Decision Tree Classifier
* Support Vector Classifier (SVC)
* XGBoost Classifier

### 3.3. Evaluation Metrics

Model performance was assessed using **Accuracy, Precision, Recall, F1-score, and AUC**.

---

## 4. Results and Conclusion

The **Random Forest Classifier** demonstrated the best overall performance, achieving an accuracy of approximately **91.6%** on the test set. This model can be used as a predictive tool to help prioritize individuals at a higher risk of stroke.

---

## 5. Prerequisites

The analysis was performed using Python and common data science libraries. You will need:

* `pandas`
* `matplotlib`
* `seaborn`
* `scikit-learn` (`sklearn`)
* `imblearn` (for handling imbalance)
* `xgboost`
