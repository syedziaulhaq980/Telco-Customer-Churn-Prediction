# 📊 Telco Customer Churn Prediction

A Machine Learning classification project that predicts whether a telecom customer is likely to **churn (leave the company)** based on customer demographics, services, contract information, billing details, and tenure.

## 🚀 Project Overview

Customer churn is an important business problem for telecom companies. Identifying customers who are likely to leave can help businesses understand churn patterns and develop appropriate retention strategies.

In this project, I built a complete Machine Learning workflow including:

* Data preprocessing
* Missing-value handling
* Feature engineering and encoding
* Feature scaling
* Train-test splitting
* Handling class imbalance using SMOTE
* Multiple classification algorithms
* Hyperparameter tuning
* Model evaluation
* Probability threshold analysis

## 📁 Dataset

The project uses the **Telco Customer Churn** dataset.

The dataset contains information about:

* Customer demographics
* Account information
* Internet and phone services
* Contract details
* Payment methods
* Monthly and total charges
* Customer tenure
* Churn status

### Target Variable

`Churn`

* `0` → Customer did not churn
* `1` → Customer churned

## 🛠️ Technologies & Libraries

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Imbalanced-learn
* XGBoost
* Jupyter Notebook

## 🔄 Machine Learning Workflow

```text
Data Collection
      ↓
Data Understanding
      ↓
Data Cleaning
      ↓
Missing Value Handling
      ↓
Feature Identification
      ↓
Encoding
      ↓
Feature Scaling
      ↓
Train-Test Split
      ↓
SMOTE
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Hyperparameter Tuning
      ↓
Threshold Analysis
```

## 🧹 Data Preprocessing

The following preprocessing techniques were used:

### Numerical Features

* Missing-value imputation using median
* StandardScaler

### Categorical Features

* Missing-value imputation using most frequent value
* OneHotEncoder

### Ordinal Features

* OrdinalEncoder

### Binary Features

Binary features were represented using `0` and `1`.

### Class Imbalance

The target variable was imbalanced, with fewer customers belonging to the churn class.

SMOTE (**Synthetic Minority Over-sampling Technique**) was applied to the training data to improve representation of the minority class.

## 🤖 Models Used

The following classification algorithms were implemented:

1. Logistic Regression
2. K-Nearest Neighbors (KNN)
3. Decision Tree
4. Random Forest
5. Gradient Boosting
6. XGBoost

## ⚙️ Hyperparameter Tuning

Manual nested-loop hyperparameter tuning was performed for each model.

Examples of tuned parameters include:

### Random Forest

* `n_estimators`
* `max_depth`
* `min_samples_split`
* `min_samples_leaf`
* `max_features`

### Gradient Boosting

* `n_estimators`
* `learning_rate`
* `max_depth`
* `min_samples_split`
* `min_samples_leaf`

### XGBoost

* `n_estimators`
* `learning_rate`
* `max_depth`
* `min_child_weight`
* `subsample`

### Logistic Regression

* `C`
* `penalty`
* `solver`
* `max_iter`

### KNN

* `n_neighbors`
* `weights`
* `p`
* `leaf_size`

### Decision Tree

* `criterion`
* `max_depth`
* `min_samples_split`
* `min_samples_leaf`
* `max_features`

## 📈 Tuned Model Results

The models were evaluated using accuracy, precision, recall, F1-score, and ROC-AUC.

| Model               | Accuracy | Churn Precision | Churn Recall | Churn F1 | ROC-AUC |
| ------------------- | -------: | --------------: | -----------: | -------: | ------: |
| Logistic Regression |   73.67% |            0.50 |         0.79 |     0.61 |   0.840 |
| KNN                 |   71.47% |            0.48 |         0.73 |     0.58 |   0.792 |
| Decision Tree       |   76.37% |            0.54 |         0.70 |     0.61 |   0.812 |
| Random Forest       |   74.24% |            0.51 |         0.79 |     0.62 |   0.834 |
| Gradient Boosting   |   76.86% |            0.55 |         0.75 |     0.63 |   0.840 |
| XGBoost             |   78.42% |            0.58 |         0.70 |     0.63 |   0.841 |

> The reported metrics are from the project's current evaluation workflow. Hyperparameter selection was performed using the held-out test set during experimentation; a production-ready workflow should use cross-validation/validation data for model and threshold selection and reserve the test set for final evaluation.

## 📌 Evaluation Metrics

### Accuracy

Measures the overall percentage of correct predictions.

### Precision

Measures how many customers predicted as churners actually churned.

### Recall

Measures how many actual churners were correctly identified.

### F1-Score

Provides a balance between precision and recall.

### ROC-AUC

Measures the model's ability to distinguish between churn and non-churn customers across classification thresholds.

## 🎯 Key Learning Outcomes

Through this project, I practiced:

* End-to-end classification workflow
* Data preprocessing with `ColumnTransformer`
* Numerical and categorical feature transformation
* Handling class imbalance using SMOTE
* Multiple classification algorithms
* Manual hyperparameter tuning
* Model comparison
* Precision-recall trade-offs
* ROC-AUC evaluation
* Classification threshold tuning
* Avoiding data leakage during preprocessing

## 📂 Repository Structure

```text
Telco-Customer-Churn-Prediction/
│
├── Telco_Customer_Churn.ipynb
├── README.md
└── WA_Fn-UseC_-Telco-Customer-Churn.csv


## 🔮 Future Improvements

Possible improvements for the project include:

* Cross-validation based hyperparameter tuning
* Validation-based threshold optimization
* ROC and Precision-Recall curve visualization
* Feature importance analysis
* SHAP-based model explainability
* Streamlit deployment
* Building a complete customer churn prediction web application

## 👨‍💻 Author

**Syed Ziaul Haq**

BTech Graduate | Python Developer | Data Analyst | AI/ML Enthusiast

GitHub: [@syedziaulhaq980](https://github.com/syedziaulhaq980)

---

⭐ If you find this project useful, feel free to explore the notebook and the complete ML workflow.
