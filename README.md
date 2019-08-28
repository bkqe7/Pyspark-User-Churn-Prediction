# Pyspark-User-Churn-Prediction

Understanding customer churn is a challenging and common problem for data scientists in any customer-facing business. Sparkify is a digital music service company, similar to Spotify and Pandora. It allows users to stream songs to its service either using free-tier or premium subscription model. Users can upgrade or downgrade the service and cancel the subscription at any time. This project will help Sparkify to predict whether users will cancel the subscriptions using user activity log data. 

## Problem Statement
This project will use Pyspark SQL and ML packages to manipulate the data and build machine learning models.The problem we want to solve is to predict the churn probability for Sparkify customers. I would select from three supervised learning classifiers, Logistic Regression, Random Forest and Gradient Boosting Tree.The analysis is performed on a small dataset. Then the whole process will be deployed on big a data platform, such as AWS or IBM Watson Studio.

## Installation

The packages used are:

- Pyspark.sql
- Pyspark.ml
- Datetime
- Matplotlib

## Files and how to use

`Sparkify.ipynb` contains the analysis of this project.

## Methodology 

- Load and Clean user log data into Spark using Spark SQL and Dataframes.
- Exploratory data analysis: perform preliminary analysis to understand the data, define user churn and explore the behavior for users who stayed vs users who churned.
- Feature engineering: extract features from existing data.
- Modeling: select among three classifiers by evaluating accuracy and tuning parameters using Spark ML.

## Refinement

To achieve better model outcome, I used 3-fold cross validation and grid search to find the best combination of the hyperparameters for each classifier. I chose F1 score as the evaluation metric. Below are the parameters:

Logistic Regression : regparam (0.1, 0)
Random Forest: numTrees (10,30)
Gradient Boosting Trees: maxDepth (5,8), maxIter(10,20)

## Results

The average F1 scores for the best model of each classifier as below:
Logistic Regression: 0.7526
Random Forest: 0.7669
Gradient Boosting Trees: 0.7962

Gradient Boosting Trees is the winning solution. The parameters for the best model are maxIter=10,maxDepth = 5. The accuracy of model on test set is 0.7447 and F1 score is 0.7260.

## Discussion

The potential improvement for this project:
- Including more features into the model. Other features like the proportion of active time, user activity in last section, location, their machine are all potential variables that we could include into the model.
- Try different classifiers and tune different parameters. Other classifiers are like SVM, Naive Bayes and Neural Network, etc. Other parameters we cound include for Gradient Boosting are minInstancesPerNode, stepSize and etc. 

## Liscensing, Authors and Acknowledgements

The dataset is provided by Udacity. The analysis is also poseted on [Medimu](https://medium.com/@jennylvy9/sparkify-customer-churn-prediction-using-pyspark-e3d378fb6eac)
