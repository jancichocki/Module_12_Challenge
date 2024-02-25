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

# Answers to Key Questions

## How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels when using the original data?

- The logistic regression model performed exceptionally well in predicting **healthy loans (0)** with almost perfect precision, recall, and F1-score. 
- For **high-risk loans (1)**, the model also demonstrated strong performance, with a **precision of 0.86** and a **recall of 0.91**. 
- This indicates a high ability to correctly identify both healthy and high-risk loans, making it a reliable tool for loan evaluation in its original form.

## How well does the logistic regression model, fit with oversampled data, predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

- When trained with oversampled data, the logistic regression model showed high accuracy in predicting both healthy and high-risk loans.
- Notably, its **recall for high-risk loans was 0.99**, indicating an excellent capability to identify almost all potential defaults. 
- The **precision for high-risk loans was slightly lower at 0.85**, but this is a minor compromise given the importance of correctly identifying as many high-risk loans as possible.

## What are the balanced accuracy scores, precision, and recall scores of both machine learning models?

- For the **original data model**, the balanced accuracy score was **0.9521**. The precision for healthy loans was near perfect, and for high-risk loans, it was **0.86** with a recall of **0.91**.
- For the **resampled data model**, the balanced accuracy score improved to **0.9942**. The precision for high-risk loans was **0.85** with an impressive recall of **0.99**.

## Which model is recommended for use, if any, on the original vs. the resampled data? Or, if neither model is recommended, what is the justification for this reasoning?

- Both models exhibit high performance, but the model trained on oversampled data offers an improved ability to identify high-risk loans without significantly compromising the identification of healthy loans.
- Given the critical importance of minimizing financial risk by accurately identifying potential defaults, the **model trained with oversampled data is recommended**. It balances the need for high recall of high-risk loans with sufficient precision, making it a valuable tool for credit risk management.

