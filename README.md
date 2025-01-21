## Credit Card Fraud Detection using Logistic Regression

This project demonstrates how to use a logistic regression model to detect fraudulent transactions in credit card data. The goal is to classify transactions as either legitimate or fraudulent based on several features.

### Project Overview

In this project, we apply machine learning to a credit card dataset to build a model that can distinguish between legitimate and fraudulent transactions. The dataset is unbalanced, with a much larger proportion of legitimate transactions compared to fraudulent ones. We address this issue by sampling a balanced dataset and applying logistic regression for binary classification.

### Steps Involved:

1. **Data Exploration**:
   - The dataset is loaded, and basic exploratory data analysis (EDA) is performed.
   - The presence of missing values is checked, and a summary of the dataset is provided.
   - The distribution of the target variable (`Class`) is analyzed, which indicates the proportion of legitimate (0) vs fraudulent (1) transactions.

2. **Handling Class Imbalance**:
   - The dataset is imbalanced, with a significantly higher number of legitimate transactions than fraudulent ones. To handle this, we take a random sample of legitimate transactions (`legit_sample`) to match the number of fraudulent transactions.
   - The resulting dataset (`new_dataset`) is balanced, with an equal number of legitimate and fraudulent transactions.

3. **Feature Selection**:
   - The target variable (`Class`) is separated from the features. The features (`X`) consist of all columns except for `Class`, and the target (`Y`) is the `Class` column.

4. **Splitting the Data**:
   - The dataset is split into training and testing sets using `train_test_split`, ensuring that the split maintains the balance between the classes through stratification. The training set is used to train the model, and the test set is used to evaluate its performance.

5. **Modeling with Logistic Regression**:
   - A logistic regression model is instantiated and trained using the training data.
   - The model is then used to predict the target variable on both the training and testing data.

6. **Model Evaluation**:
   - The accuracy of the model is evaluated on both the training and test datasets using `accuracy_score`.
   - The performance on the training data gives an indication of how well the model learned, while the performance on the test data shows its ability to generalize to unseen data.

