# <ins>Module 20 Report</ins> 

## <ins>Overview of the Analysis</ins>

The purpose of the analysis was to use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.
This model was used to determine which loans were healthy (low-risk) or non-healthy (high-risk) based on the loan status provided by the lending company.
The y variable in this analysis is the "loan status", which shows if a loan is low-risk (0) or at high-risk (1) and the X variable is the loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks and number of total debt. 

The stages of the machine learning process I went through as part of this analysis was as follows:
1. I split the data into training and testing datasets by using train_test_split. 
2. Fitted a logistic regression model by using the training data (X_train and y_train).
3. Saved the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
4. Evaluated the model’s performance by doing the following:
  i) Calculated the accuracy score of the model.  
  ii) Generated a confusion matrix.
  iii) Printed the classification report.


5. Logistic Regression models were created by using the original data set and resampled training data set.  The results were later compared. 

## <ins>Results</ins>

#### <ins>Machine Learning Model 1:</ins>

![Screen Shot 2023-03-24 at 17 58 37](https://user-images.githubusercontent.com/116304118/227604226-1e3a3304-f767-44a3-956a-119881d65ae2.png)

##### Confusion Matrix
![Screen Shot 2023-03-24 at 21 07 56](https://user-images.githubusercontent.com/116304118/227642167-9a5bade4-90df-4325-8df5-ac2df2f1f1e7.png)

##### Classification report
![Screen Shot 2023-03-24 at 17 58 53](https://user-images.githubusercontent.com/116304118/227604253-c4e2b973-5936-4d58-9759-011771f48e83.png)


#### <ins>Machine Learning Model 2:</ins>

![Screen Shot 2023-03-24 at 18 01 48](https://user-images.githubusercontent.com/116304118/227604783-ae3cd9b9-ea84-49b9-85b4-dd2c3e9fc6ad.png)

##### Confusion Matrix
![Screen Shot 2023-03-24 at 21 08 20](https://user-images.githubusercontent.com/116304118/227642211-eb8ecaec-de2d-4ca5-b418-1e9e70d2d409.png)

##### Classification report
![Screen Shot 2023-03-24 at 18 01 55](https://user-images.githubusercontent.com/116304118/227604800-774acc75-9d23-4e59-a641-66ecf94f61b6.png)



## <ins>Summary</ins>
The Logistic Regression model fitted with OverSampled data (model 2) performed a lot better than the model fitted with Imbalanced data due to the data being balanced and generating a higher accuracy score and a higher recall, indicating that the model will make extremely fewer mistakes when classifying non-healthy loans.

The balanced accuracy score is improved using the resampled (oversampling) process from 0.95 to 0.99. It is important to predict the high-risks (1), as lenders do not want to loan out money to those who will struggle to pay it back. In this case I would recommend using model 2. 

