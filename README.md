# telco-churn-prediction
*Company*: CODTECH IT SOLUTIONS
*Name*: Chetan
*Inern Id*: CT04WM04
*Domain*: Machine Learning
*Duration*: 4 weeks
*Mentor*: Neela Santosh

## Project Overview

This project aims to predict customer churn for a telecommunications company using a Decision Tree classification model. It analyzes customer data to identify key factors driving churn and builds a basic predictive model. This was developed as an introductory machine learning task.

## Dataset

The analysis uses the publicly available **"Telco Customer Churn"** dataset, often found on Kaggle. The dataset includes customer demographic information, account details, subscribed services, and churn status.

## Approach

1.  **Data Loading & Preprocessing:** The dataset was loaded using Pandas. Preprocessing steps included handling missing values (specifically in `TotalCharges`), encoding the binary target variable ('Churn'), and applying One-Hot Encoding to categorical features. The `customerID` was dropped.
2.  **Modeling:** A `DecisionTreeClassifier` from the Scikit-learn library was trained on the preprocessed data.
3.  **Evaluation:** The model's performance was evaluated on a held-out test set using Accuracy, Confusion Matrix, and a Classification Report (Precision, Recall, F1-score).
4.  **Analysis:** Feature importances were extracted from the trained model to identify key drivers of churn. The top levels of the decision tree were also visualized.

## Key Findings

* The model achieved an overall accuracy of approximately **70.5%** on the test data.
* While reasonably good at identifying non-churners, the model struggled to reliably predict customers who *would* churn (Recall for 'Yes' churn class was ~48%).
* The most influential features identified by the model were `MonthlyCharges`, `TotalCharges`, `tenure`, and having `InternetService_Fiber optic`.
* This initial model provides insights but would require further tuning or alternative modeling techniques for more effective churn prediction in a real-world scenario.

## How to Run

1.  Clone or download the repository.
2.  Ensure you have Python installed along with the necessary libraries (see below).
3.  Download the `WA_Fn-UseC_-Telco-Customer-Churn.csv` dataset and place it in the project's root directory, or update the file path in the notebook (`.ipynb` file).
4.  Open and run the Jupyter Notebook (`.ipynb` file)
