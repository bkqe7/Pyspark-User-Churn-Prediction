# Pyspark-User-Churn-Prediction

Understanding customer churn is a challenging and common problem for data scientists in any customer-facing business. Sparkify is a digital music service company, similar to Spotify and Pandora. It allows users to stream songs to its service either using free-tier or premium subscription model. Users can upgrade or downgrade the service and cancel the subscription at any time. This project will help Sparkify to predict whether users will cancel the subscriptions using user activity log data. It uses Pyspark SQL and ML packages to manipulate the data and build machine learning models. 

## Installation

The packages used are:

- Pyspark.sql
- Pyspark.ml
- Datetime
- Matplotlib

## Files and how to use

`Sparkify.ipynb` contains four steps of this project.
- Load and Clean user log data into Spark using Spark SQL and Dataframes.
- Exploratory data analysis: perform preliminary analysis to understand the data, define user churn and explore the behavior for users who stayed vs users who churned.
- Feature engineering: extract features from existing data.
- Modeling: select among three classifiers by evaluating accuracy and tuning parameters using Spark ML.

## Liscensing, Authors and Acknowledgements

The dataset is provided by Udacity. The analysis is also poseted on [Medimu](https://medium.com/@jennylvy9/sparkify-customer-churn-prediction-using-pyspark-e3d378fb6eac)
