# Credit Risk Classification Project

## Overview
This project tackles the challenge of credit risk classification, a fundamental issue in the finance industry. Credit risk poses a classification problem that's inherently imbalanced, as healthy loans significantly outnumber risky ones. Utilizing a dataset of historical lending activity from a peer-to-peer lending services company, this project aims to build a model that can accurately identify the creditworthiness of borrowers.

## Objectives
- To split the dataset into training and testing sets.
- To create and evaluate a logistic regression model with the original dataset.
- To enhance model performance by employing a logistic regression model with resampled training data.

## Technologies Used
- Python
- Pandas for data manipulation.
- Scikit-learn for model building, training, and evaluation.
- Imbalanced-learn for dealing with imbalanced data.

## Dataset
The dataset used in this project includes historical lending data from a peer-to-peer lending services company. It contains several features related to loan applications, such as loan size, interest rate, borrower income, and more.

## Steps Followed
1. **Data Preprocessing**: The data was read into a Pandas DataFrame, followed by splitting into labels (y) and features (X).
2. **Model Training and Evaluation**:
   - A logistic regression model was trained using the original data.
   - The model's performance was evaluated using accuracy score, confusion matrix, and classification report.
3. **Handling Imbalanced Data**:
   - The training data was resampled using `RandomOverSampler` to balance the distribution of labels.
   - A logistic regression model was then trained on the resampled data and evaluated.

## Results
- The logistic regression model trained on the original dataset showed high accuracy in predicting both healthy and high-risk loans.
- After resampling the data, the logistic regression model's ability to identify high-risk loans improved, demonstrating the importance of dealing with imbalanced datasets in credit risk classification.

## Conclusion
The project underscores the significance of using logistic regression for credit risk classification and highlights the effectiveness of resampling techniques in enhancing model performance on imbalanced datasets. The models developed can serve as a valuable tool for assessing loan applications and managing credit risk more efficiently.
