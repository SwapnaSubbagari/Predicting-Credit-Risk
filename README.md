# Predicting-Credit-Risk
Purpose
This project was made to build two machine learning models that attempts to predict whether a loan from LendingClub will become high risk or not.

![Scaled](https://user-images.githubusercontent.com/85588653/139784456-cdb35189-a02b-45bf-96e8-fa39e05d2234.PNG)


Background
LendingClub is a peer-to-peer lending services company that allows individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market. LendingClub offers their previous data through an API.

Use this data to create machine learning models to classify the risk level of given loans. Specifically, you will be comparing the Logistic Regression model and Random Forest Classifier.

Instructions
Retrieve the data
In the Generator folder in Resources, there is a GenerateData.ipynb notebook that will download data from LendingClub and output two CSVs:

2019loans.csv
2020Q1loans.csv
Use an entire year's worth of data (2019) to predict the credit risk of loans from the first quarter of the next year (2020).

Note: these two CSVs have been undersampled to give an even number of high risk and low risk loans. In the original dataset, only 2.2% of loans are categorized as high risk. To get a truly accurate model, special techniques need to be used on imbalanced data. Undersampling is one of those techniques. Oversampling and SMOTE (Synthetic Minority Over-sampling Technique) are other techniques that are also used.

Preprocessing: Convert categorical data to numeric
Create a training set from the 2019 loans using pd.get_dummies() to convert the categorical data to numeric columns. Similarly, create a testing set from the 2020 loans, also using pd.get_dummies(). Note! There are categories in the 2019 loans that do not exist in the testing set. If you fit a model to the training set and try to score it on the testing set as is, you will get an error. You need to use code to fill in the missing categories in the testing set.

Consider the models
You will be creating and comparing two models on this data: a logistic regression, and a random forests classifier. Before you create, fit, and score the models, make a prediction as to which model you think will perform better. You do not need to be correct! Write down (in markdown cells in your Jupyter Notebook or in a separate document) your prediction, and provide justification for your educated guess.

Fit a LogisticRegression model and RandomForestClassifier model
Create a LogisticRegression model, fit it to the data, and print the model's score. Do the same for a RandomForestClassifier. You may choose any starting hyperparameters you like.
![Unscaled](https://user-images.githubusercontent.com/85588653/139784623-276383f4-cb43-47a6-927a-6e5ee8579a7f.PNG)

Revisit the Preprocessing: Scale the data
The data going into these models was never scaled, an important step in preprocessing. Use StandardScaler to scale the training and testing sets. Before re-fitting the LogisticRegression and RandomForestClassifier models on the scaled data, make another prediction about how you think scaling will affect the accuracy of the models.
![Scaled](https://user-images.githubusercontent.com/85588653/139784705-291c95d6-e18a-46f8-a4b4-8be99f1430f3.PNG)

