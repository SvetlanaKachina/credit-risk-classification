# Credit Risk Classification #
## Split the Data into Training and Testing Sets ##
Opened the starter code notebook and used it to complete the following steps:
1.	Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
2.	Created the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
3.	Split the data into training and testing datasets by using train_test_split.
## Created a Logistic Regression Model with the Original Data ##
Using knowledge of logistic regression when completing the following steps:
1.	Fitted a logistic regression model by using the training data (X_train and y_train).
2.	Saved the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
3.	Evaluated the model’s performance by doing the following:
+ Generated a confusion matrix.
+ Printed the classification report.
4.	Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels? 
## Wrote a Credit Risk Analysis Report ##
Wrote a brief report that includes a summary and analysis of the performance of the machine learning models that was used in this homework. Wrote this report as the README.md file included in your GitHub repository.
Structured report by using the report template that Starter_Code.zip includes, ensuring that it contains the following:
1.	An overview of the analysis: Explained the purpose of this analysis.
2.	The results: Using a bulleted list, described the accuracy score, the precision score, and recall score of the machine learning model.
3.	A summary: Summarized the results from the machine learning model. Included justification for recommending the model for use by the company. 

## Credit Risk Analysis Report ##
### Overview of the Analysis ###
The purpose of this analysis was to apply a machine learning model to financial lending data to assess credit risk. Specifically, the objective was to predict whether a loan is healthy (low risk) or high-risk (likely to default), enabling lenders to make data-driven decisions.
The dataset contained financial information about loans, including features such as borrower's income, debt-to-income ratio, and other key financial metrics. The target variable was loan_status, where:
+ 0 indicates a healthy loan (low risk),
+ 1 indicates a high-risk loan (likely to default).
We reviewed the distribution of the target variable, where the majority of loans were labeled as healthy loans (0), and a smaller proportion were labeled as high-risk loans (1), indicating some class imbalance.
### Stages of the Machine Learning Process: ###
1.	Data Preprocessing: The dataset was loaded, and the target (y) and features (X) were separated.
2.	Train-Test Split: The data was split into training and testing datasets using train_test_split with a random_state of 1 to ensure reproducibility.
3.	Modeling: A Logistic Regression model was instantiated and trained on the training dataset.
4.	Evaluation: The model was evaluated using a confusion matrix and a classification report to review precision, recall, f1-score, and accuracy.


The Results
Results
Machine Learning Model 1:
Logistic Regression Model
+ Accuracy: 99%
+ Precision:
+ Class 0 (healthy loan): 1.00
+ Class 1 (high-risk loan): 0.85
+ Recall:
+ Class 0 (healthy loan): 0.99
+ Class 1 (high-risk loan): 0.91
+ F1-Score:
+ Class 0: 1.00
+ Class 1: 0.88
### Summary ###
The logistic regression model performs very well overall, especially in identifying healthy loans with near-perfect precision and recall. The model also performs strongly in predicting high-risk loans, achieving a precision of 85% and a recall of 91%, which is commendable given the likely imbalance in the dataset.

### Recommendation: ###
I recommend using this logistic regression model, particularly because it maintains high recall for identifying high-risk loans (1). In financial contexts, recall for high-risk loans can be crucial, as failing to identify a risky loan could have costly implications. However, the model also maintains excellent performance for healthy loans, making it well-rounded.

While no model is perfect, this logistic regression provides a strong baseline for credit risk assessment. Future work could explore balancing the dataset or testing other models (e.g., decision trees or ensemble methods) to further improve performance for high-risk loans.
