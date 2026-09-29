ustomer Churn Prediction using Decision Tree
Overview

This project predicts whether a customer is likely to leave a bank using a Decision Tree Classifier built with Scikit-Learn.

The goal is to identify customers at risk of churn so that businesses can take preventive actions and improve customer retention.

This project was completed as part of my Machine Learning learning journey and focuses on the complete ML workflow, including data preprocessing, feature engineering, model training, evaluation, and hyperparameter tuning.

Dataset

The dataset contains customer information such as:

Credit Score
Geography
Gender
Age
Tenure
Balance
Number of Products
Has Credit Card
Is Active Member
Estimated Salary
Target Variable
Plain Text
Exited
 
0 = Customer Stayed
1 = Customer Churned
Show more lines
Data Preprocessing

The following preprocessing steps were performed:

Removed unnecessary identifier columns:

RowNumber
CustomerId
Surname

Removed potential data leakage features:

Complain
Satisfaction Score

Checked for:

Missing values
Duplicate records

Applied One-Hot Encoding to categorical features using:

Python
pd.get_dummies()
Show more lines
Model

A Decision Tree Classifier was used with the following parameters:

Python
DecisionTreeClassifier(
max_depth=6,
criterion="entropy",
min_samples_split=50,
min_samples_leaf=20,
class_weight={0:1, 1:2.96},
random_state=42
)
Show more lines
Why these settings?

max_depth=6

Reduces overfitting

min_samples_split=50

Prevents unnecessary splits

min_samples_leaf=20

Avoids very small leaf nodes

class_weight

Helps address class imbalance in churn prediction
Model Evaluation
Cross Validation
Plain Text
Cross Validation Accuracy: 78.93%
Show more lines
Test Accuracy
Plain Text
Accuracy: 77.15%
Show more lines
Confusion Matrix
Plain Text
[[1221 371]
[ 86 322]]
Show more lines
Classification Report
Plain Text
Class 0 (Not Churn)
 
Precision: 0.93
Recall: 0.77
F1-Score: 0.84
 
Class 1 (Churn)
 
Precision: 0.46
Recall: 0.79
F1-Score: 0.58
Show more lines
ROC-AUC

ROC-AUC was also used to evaluate the model's ability to distinguish between churned and non-churned customers.

Python
roc_auc_score(y_test, probabilities)
Show more lines
Key Learning Outcomes

Through this project I learned:

Data preprocessing
Feature selection
One-hot encoding
Detecting and removing data leakage
Decision Trees
Hyperparameter tuning
Cross Validation
Confusion Matrix interpretation
Precision, Recall, and F1 Score
Handling imbalanced datasets

One of the most important lessons from this project was learning that very high accuracy can sometimes indicate data leakage rather than a genuinely good model.

Technologies Used
Python
Pandas
NumPy
Scikit-Learn
Future Improvements
Compare results with Random Forest
Compare against Logistic Regression
Perform Grid Search for hyperparameter tuning
Improve churn prediction recall and F1 score
Create visualizations and dashboards
Author

Awais Ali

First-Year BS Artificial Intelligence Student

Learning Machine Learning through hands-on projects and experimentation. 🚀
