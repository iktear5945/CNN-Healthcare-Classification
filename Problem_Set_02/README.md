# Problem Set 02 - Bank Marketing Prediction

## Problem Statement

A banking institution wants to predict whether a customer will subscribe to a term deposit based on their demographic information and banking behaviour. Logistic Regression is used to solve this binary classification problem.

## Dataset

The Bank Marketing dataset contains information about customers, including demographic details, account information, contact information, and previous marketing campaign results.

The target variable is `y`.

- `yes` = Customer subscribed to a term deposit
- `no` = Customer did not subscribe to a term deposit

## Methodology

The following steps were performed:

1. Loaded the Bank Marketing dataset.
2. Examined the dataset structure and statistical information.
3. Checked missing values and duplicate records.
4. Performed basic exploratory data analysis.
5. Separated input features and the target variable.
6. Converted the target variable from `yes/no` to `1/0`.
7. Divided the dataset into 80% training data and 20% testing data.
8. Applied StandardScaler to numerical features.
9. Applied One-Hot Encoding to categorical features.
10. Built a Logistic Regression model.
11. Trained the model using the training dataset.
12. Predicted customer subscription on the test dataset.
13. Evaluated the model using Accuracy, Precision, Recall, F1-score, and Confusion Matrix.
14. Analyzed Logistic Regression coefficients to identify influential features.

## Model

Logistic Regression was selected because the target variable is binary.

- `0` = No subscription
- `1` = Subscription

## Results

| Metric | Score |
|---|---:|
| Accuracy | 90.12% |
| Precision | 64.45% |
| Recall | 34.78% |
| F1 Score | 45.18% |

## Findings

The Logistic Regression model achieved an accuracy of 90.12% on the test dataset.

The precision was 64.45%, meaning that when the model predicted that a customer would subscribe, about 64% of those predictions were correct.

The recall was 34.78%, which indicates that the model identified approximately 35% of the customers who actually subscribed to the term deposit.

The F1-score was 45.18%, showing that there is room for improvement in balancing precision and recall.

Although the accuracy was relatively high, the lower recall indicates that the model missed a considerable number of customers who actually subscribed. This is important because identifying potential subscribers is a major goal of the banking institution.

Overall, Logistic Regression provides a useful baseline model for this binary classification problem.

## Feature Analysis

The Logistic Regression coefficients showed that some features had stronger influence on the prediction than others.

Among the features with larger absolute coefficients were:

- `poutcome_success`
- `month_mar`
- `month_jan`
- `contact_unknown`
- `duration`

Positive coefficients indicate an increased tendency toward the subscription class, while negative coefficients indicate the opposite direction.

## Example Prediction

For one sample customer, the model produced:

- Probability of No subscription: 99.26%
- Probability of Yes subscription: 0.74%

Therefore, the model predicted that this customer would not subscribe to the term deposit.

## Conclusion

The project demonstrates how Logistic Regression can be applied to predict term deposit subscription using customer banking data.

The model achieved 90.12% accuracy, but its relatively low recall shows that further improvements may be required to identify more potential subscribers. Techniques such as class balancing, hyperparameter tuning, or other machine learning algorithms could be explored in future work.
