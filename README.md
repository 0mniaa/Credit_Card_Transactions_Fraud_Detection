# Credit Card Transactions Fraud Detection

## Overview
This project aims to detect fraudulent transactions from a dataset of credit card transactions. The dataset contains various attributes, such as transaction amount, location details, and timestamps, used to classify transactions as fraudulent or non-fraudulent.

## Dataset
The dataset is loaded from CSV files and contains the following key features:
- **amt**: Transaction amount
- **zip**: Zip code of the transaction location
- **city_pop**: Population of the city where the transaction occurred
- **cc_num**: Credit card number (encoded)
- **fraud**: The target variable indicating whether the transaction is fraudulent.

## Steps Involved

### 1. Data Preprocessing
- **Balancing the Dataset**: The dataset is imbalanced, with far more non-fraudulent transactions. To address this, undersampling of non-fraudulent transactions is applied.

### 2. Feature Engineering
- Removal of unnecessary columns, such as transaction identifiers and location metadata, to focus on relevant features.

### 3. Feature Scaling
- Numeric features like `amt`, `zip`, and `city_pop` are standardized using `StandardScaler`.
- Categorical features like `cc_num` are encoded for model compatibility.

### 4. Model Training
- A `RandomForestClassifier` is used to train the model.

### 5. Model Evaluation
- Model performance is evaluated using accuracy, precision, recall, and F1-score metrics.

## Dependencies
- Python 3.x
- Libraries: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`
