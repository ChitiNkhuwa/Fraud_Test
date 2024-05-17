# Fraud_Test

## Objective
Determine the probability of fraud based on features in the dataset.

## Dataset Description
This dataset offers a variety of attributes valuable for comprehensive analysis. It contains 555,719 instances and 22 attributes, a mix of categorical and numerical data types. Importantly, the dataset is complete with no null values. Here's a breakdown of the attributes:
- **Trans_date_trans_time**: Timestamp of the transaction (date and time).
- **Cc_num**: Unique customer identification number.
- **Merchant**: The merchant involved in the transaction.
- **Category**: Transaction type (e.g., personal, childcare).
- **Amt**: Transaction amount.
- **First**: Cardholder's first name.
- **Last**: Cardholder's last name.
- **Gender**: Cardholder's gender.
- **Street**: Cardholder's street address.
- **City**: Cardholder's city of residence.
- **State**: Cardholder's state of residence.
- **Zip**: Cardholder's zip code.
- **Lat**: Latitude of cardholder's location.
- **Long**: Longitude of cardholder's location.
- **City_pop**: Population of the cardholder's city.
- **Job**: Cardholder’s job title.
- **Dob**: Cardholder's date of birth.
- **Trans_num**: Unique transaction identifier.
- **Unix_time**: Transaction timestamp (Unix format).
- **Merch_lat**: Merchant’s location (latitude).
- **Merch_long**: Merchant's location (longitude).
- **Is_fraud**: Fraudulent transaction indicator (1 = fraud, 0 = legitimate). This is the target variable for classification purposes.

## Steps
I created several classification models to see which one would work best on the dataset that I had. I created the models in the following order: Decision tree, Logistic regression, Naïve Bayes, Random Forest, Kernel SVM, Gradient Booster, and XGB Classifier.

## Results
| Model               | Accuracy | CAP Curve (AUC)         |
|---------------------|----------|-------------------------|
| Decision tree       | 0.995    | 0.5340393442622952      |
| Logistic regression | 0.9961   | 0.7136610441767068      |
| Naïve Bayes         | 0.8824   | 0.5824096385542169      |
| Random Forest       | 0.9955   | 0.49975903614457834     |
| Kernel SVM          | 0.996    | 0.7548530120481927      |
| Gradient Booster    | 0.996    | 0.7548530120481927      |
| XGB Classifier      | 0.996    | 0.7548530120481927      |

## Best Model
To avoid the accuracy paradox that may result from relying on an accuracy score from a confusion matrix, I also calculated the AUC. Based on the results, the **XGB Classifier** performed better than the rest. The AUC (Area Under the ROC Curve) score of approximately 0.755 indicates that the XGBoost classifier has improved performance compared to the Gradient Boosting Machine (GBM) classifier. An AUC score of 0.755 indicates the performance of the XGBoost classifier on the test data.

1. **Discriminative Power**: A higher AUC score suggests that the classifier has better discriminative power in distinguishing between the positive and negative classes. In other words, it indicates that the classifier is more capable of assigning higher probabilities to positive instances than negative instances.

2. **Model Performance**: The AUC score provides an overall measure of the model's performance across different classification thresholds. A score of 0.755 indicates that the classifier performs relatively well in terms of correctly ranking the positive and negative instances, compared to random guessing (AUC = 0.5).

Link: https://www.kaggle.com/datasets/kelvinkelue/credit-card-fraud-prediction?resource=download
