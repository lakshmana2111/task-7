# 💳 Credit Card Fraud Detection Using Random Forest

## 📌 Project Overview

Credit Card Fraud Detection is a Machine Learning project that identifies potentially fraudulent credit card transactions using a **Random Forest Classifier**.

The model analyzes transaction data to classify transactions as genuine or fraudulent. Its performance is evaluated using classification metrics and visualizations to understand how effectively it detects fraudulent transactions.

## 🎯 Objectives

The main objectives of this project are to:

- Analyze credit card transaction data.
- Identify fraudulent and genuine transactions.
- Build and train a Random Forest classification model.
- Evaluate model performance using standard classification metrics.
- Visualize the Confusion Matrix, ROC Curve, and feature importance.
- Analyze detected and missed fraudulent transactions.

## 🛠️ Technologies Used

- **Programming Language:** Python
- **Data Analysis:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Development Environment:** Jupyter Notebook / Google Colab

## 📂 Dataset Information

The project uses a credit card transaction dataset named `creditcard.csv`.

The target column is `Class`, which identifies the type of transaction.

| Class Label | Transaction Type |
|---|---|
| `0` | Genuine Transaction |
| `1` | Fraudulent Transaction |

The dataset contains transaction-related features used to train and evaluate the classification model.

**Note:** The dataset is not included in this repository. Download it separately and update the dataset path in the notebook according to your environment.

## ⚙️ Project Workflow

### 1. Data Loading

Load the credit card transaction dataset using Pandas.

### 2. Data Exploration

Examine the dataset structure, column names, data types, missing values, and distribution of genuine and fraudulent transactions.

### 3. Data Preparation

Separate the input features from the target variable. Prepare the data for model training and evaluation.

### 4. Train-Test Split

Split the dataset into training and testing sets.

- **Training Set:** 80%
- **Testing Set:** 20%
- **Random State:** 42

### 5. Model Training

Train a Random Forest Classifier using 100 decision trees. The model learns patterns in transaction data to distinguish genuine transactions from fraudulent ones.

### 6. Prediction

Use the trained model to predict transaction classes in the test dataset.

### 7. Model Evaluation

Evaluate the model using Precision, Recall, F1-Score, ROC-AUC, the Confusion Matrix, and the Classification Report.

### 8. Fraud Analysis

Analyze the fraudulent transactions in the test dataset to identify:

- Fraudulent transactions correctly detected by the model.
- Fraudulent transactions incorrectly classified as genuine.

### 9. Feature Importance Analysis

Identify and visualize the ten most important features used by the Random Forest model to make predictions.

### 10. Data Visualization

Generate visualizations to understand the model's performance, including:

- Confusion Matrix
- ROC Curve
- Top 10 Feature Importance Chart

## 🤖 Machine Learning Algorithm

### Random Forest Classifier

Random Forest is a supervised Machine Learning algorithm that combines multiple decision trees to make predictions. It can be used for classification tasks involving complex patterns in transaction data.

In this project, the algorithm classifies credit card transactions as genuine or fraudulent.

### Model Configuration

The model uses the following parameters:

| Parameter | Value | Description |
|---|---|---|
| `n_estimators` | `100` | Number of decision trees |
| `class_weight` | `"balanced_subsample"` | Adjusts class weights for individual tree-building samples |
| `random_state` | `42` | Ensures reproducible results |
| `test_size` | `0.2` | Allocates 20% of the data for testing |
| `n_jobs` | `-1` | Uses available CPU cores for parallel processing |

## 📊 Evaluation Metrics

The model's performance is evaluated using the following metrics:

- **Precision:** Measures the proportion of transactions predicted as fraudulent that are actually fraudulent.
- **Recall:** Measures the proportion of actual fraudulent transactions correctly detected by the model.
- **F1-Score:** Represents the harmonic mean of Precision and Recall.
- **ROC-AUC:** Measures how well the model distinguishes between genuine and fraudulent transactions across different classification thresholds.
- **Confusion Matrix:** Displays the number of correct and incorrect predictions for each transaction class.
- **Classification Report:** Summarizes Precision, Recall, F1-Score, and the number of samples for each class.

## 📈 Project Outputs

After executing the notebook, the following outputs are generated:

- Confusion Matrix visualization.
- Classification Report and evaluation metrics.
- Counts of detected and missed fraudulent transactions.
- Top 10 Feature Importance visualization.
- ROC Curve visualization.
- `actual_fraudulent_test_transactions.csv`, containing actual fraudulent transactions from the test dataset.

## 🔮 Future Enhancements

Potential improvements to this project include:

- Comparing Random Forest with other Machine Learning algorithms.
- Performing hyperparameter tuning to improve model performance.
- Applying cross-validation for more reliable evaluation.
- Optimizing the classification threshold to balance fraud detection and false alarms.
- Exploring techniques to handle class imbalance.
- Developing a web application for real-time fraud prediction.

## ⚠️ Limitations

- **Class Imbalance:** Fraudulent transactions are much less common than genuine transactions, which can affect model performance.
- **Evaluation Challenges:** Accuracy alone may not provide a reliable measure of fraud detection effectiveness.
- **Data Dependency:** Model performance depends on dataset quality, feature selection, and model configuration.
- **False Positives:** Some genuine transactions may be incorrectly flagged as fraudulent.
- **False Negatives:** Some fraudulent transactions may go undetected.
- **Deployment Limitations:** This project is intended for educational purposes and requires further validation before being used in a real-world fraud prevention system.

## 🏁 Conclusion

This project demonstrates how Machine Learning can be applied to credit card fraud detection using a Random Forest Classifier. By analyzing transaction data, training a classification model, and evaluating its predictions, the project provides practical experience in detecting potentially fraudulent transactions.

The evaluation metrics and visualizations help assess the model's ability to identify fraudulent activity. Further testing, model optimization, and validation on unseen data are necessary before considering real-world deployment.
