# BigMart-Sales-Prediction

## Introduction
The data scientists at BigMart have collected 2013 sales data for 1559 products across 10 stores in different cities. Also, certain attributes of each product and store have been defined. 
The objective is to build a predictive model and find out the sales of each product at a particular store. 
By the help of this model, BigMart will try to understand the features of products and stores which have a significant impact in increasing the sales. 

Please note that the data may have missing values as some stores might not report all the data due to technical glitches. Hence, it will be required to treat them accordingly.

## Problem Statement
Predict the sales of each products at a particular store using product's and store's features.

## Data
The data has 8253 records and 12 featues. 6 product's feature and 5 store's feature and 1 target feature(Item sales)
The test data contain 5681 records.

## IDE used
Jupyter Notebook

## Approach
Train data was loaded in a dataframe and after exploring the data it was found that 2 features have missing values.
- Item_Weight
- Outlet_Size

After filling out the missing values and cleaning some irregularities, the Exploratory Data Analysis (EDA) was done.
In EDA the relationship between target and rest of the features was checked and basic questions answered.
E.g. 
- Which Outlet has the highest sales
- How many different Product are there, and which Product type has the highest count
- Is there any relationship(strong, weak) between the continuous variable

Then after the EDA, Feature Encoding comes into picture. As Machine Learning algorithm only with continuous variable so we have to convert the discrete variables into continuous variable.
One-Hot encoding did the job of converting the variable type. After One-Hot encoding there were quite a few new variables created.

Now comes the part of splitting the data in training and test using the train_test_split function of sklearn.
- Train data 80%
- Test data  20%

I consider three ML model to ran on the dataset
- Linear Regression
- Random Forest
- Gradient Boosting

Evaluation metrics used
- Root Mean Square Error (RMSE)
- R-squared

so all three model was ran on the dataset and results recorded.

Next the hyperparameter tuning was performed using
- GridSearch CV
- Randomized Search
on Random Forest as it generated good RMSE and R-squared.

Finally the results from the GridSearch was better so it was selected as the final trained model and same model is tested on the unseen/actual test dataset.
