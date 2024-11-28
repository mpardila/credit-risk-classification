## credit-risk-classification

# Overview of the analysis:
The purpose of the analysis is to use a Logistic Regression supervised learning model to classify the credit risk for a lending service company. To do so, the model will use historical data that includes the loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt as the features to analyze the creditworthiness of future borrowers. The target column is "loan status", which has a value of 0 if the loan is healthy and a value of 1 if the loan has a high risk of default.

# Results: 
* Accuracy score: The ratio of correctly predicted observations compared to the total number of observations is 99%, which indicates that the model performs very well across both classes.
* Precision score: The ratio of correctly predicted positive observations of the class to the total predicted positive observations is 100% for healthy loans (there are no false positives), and 87% for high risk of defaulting loans (there are some false positives).
* Recall score: The ratio of correctly predicted positive observations of the class to all actual positive observations is 100% for healthy loans (there are no false negatives), and 95% for high risk of defaulting loans (there are some false negatives).

# Summary: 
The main reason I wouldn't recommend the model is that the data wasn't scaled. We are weighing a debt-to-income ratio (0-1) against the loan size and the borrower's income, which is the thousands or hundreds-thousands scale for the model to predict. On the other hand, the ratio of entries for `0` (healthy loan) and `1` (high-risk loan) is unbalanced as there are 18759 healthy loans versus only 625 high-risk loans. This explains why the precision and recall are so high for healthy loans, and the model has some false positives in the high-risk size and, even more concerning, some false negatives in the same category, meaning not all high-risk loans are identified, which is the model's main purpose.