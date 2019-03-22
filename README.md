
# Project 2 - Ames Housing Data

*Author: Grace Campbell*

## Problem Statement

I have been given data from the Ames Housing Dataset, which according to the data description "...contains information from the Ames Assessor’s Office used in computing assessed values for individual residential properties sold in Ames, IA from 2006 to 2010." I want to know which features of a property have the greatest effect on the price of the property at sale, and then be able to predict the price of a house based on those features.


For the entire data description, click here: http://bit.ly/2FcUzsc

#### Note:
This project is part of a competition on Kaggle. This data has two parts: a training set, on which I will be performing explanatory analysis and fitting my model, and a final hold-out test set. I only have access to the explanatory variable data for the test set; I do not know the values for the target variable. I will find out the final performance of my model on the test set when I submit its predictions to Kaggle.


## Modeling Steps
1. Perform a log transformation on `y` because its distribution is positively skewed
2. One-hot encode the categorical variables in the dataset so they can be included in the model
3. Transform all explanatory variables with `PolynomialFeatures` to better capture the the explanatory variables' relationships with the target and with each other
4. Scale the variables with `StandardScaler` 
5. Fit the data to a `Lasso` regularization

## Final Model Performance
My final model has an  $R^2$  score of 0.839, which means about ~84% of the variance in the data can be explained by my model compared to the null model.

![image.png](attachment:image.png)
