🌳 Customer Churn Prediction

A Machine Learning project that predicts whether a customer is likely to leave a bank using a Decision Tree Classifier.

🎯 Objective

Customer churn is a major challenge for businesses. The goal of this project is to identify customers who are likely to leave so that retention strategies can be applied proactively.

🛠️ Tech Stack
Python
Pandas
NumPy
Scikit-Learn
📊 Data Preparation

The following preprocessing steps were performed:

✅ Removed irrelevant identifiers

RowNumber
CustomerId
Surname

✅ Removed potential leakage features

Complain
Satisfaction Score

✅ Checked for

Missing values
Duplicate records

✅ Applied One-Hot Encoding to categorical variables

🤖 Model

Decision Tree Classifier

DecisionTreeClassifier(
    max_depth=6,
    criterion="entropy",
    min_samples_split=50,
    min_samples_leaf=20,
    class_weight={0:1, 1:2.96},
    random_state=42
)


Model tuning focused on reducing overfitting and improving churn detection.

📈 Results
Cross Validation Score
78.93%

Test Accuracy
77.15%

Classification Metrics
Metric	Churn Class (1)Precision	0.46
Recall	0.79
F1 Score	0.58
Confusion Matrix
[[1221 371]
 [  86 322]]


The model prioritizes recall, meaning it successfully identifies most customers who are likely to churn.

💡 Key Takeaways
Built a complete ML pipeline from preprocessing to evaluation.
Learned how to detect and remove data leakage.
Used stratified train-test splitting.
Applied cross-validation.
Worked with imbalanced data using class weights.
Evaluated performance beyond accuracy using Precision, Recall, F1-Score, and ROC-AUC.
🚀 Future Improvements
Random Forest Classifier
XGBoost
Hyperparameter optimization
Feature importance visualization
Interactive dashboard
👨‍💻 Author

Awais Ali

First-Year BS Artificial Intelligence Student

Learning Machine Learning through hands-on projects and real-world datasets.

This style is much closer to what you'd typically see in strong student GitHub repositories: concise, readable, and focused on outcomes rather than explaining every concept.
