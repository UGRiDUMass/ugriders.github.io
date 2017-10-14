---
layout: post 
title: Data Analysis Steps
---

In this post, we will go over some general tips on how to approach analyzing a new dataset, which we can apply to the [HR Analytics](https://www.kaggle.com/ludobenistant/hr-analytics) dataset hosted on Kaggle.com

## Initial Steps

* Load relevant libraries.
* Set working directory for project.
* Read in all relevant data.
* Rename variables for ease of use (optional).
* Check structure of data and change data types of variables which require it.
* Look for out-of-range observations or values that don't make sense. 
* Hypothesize potential interactions between response variable and explanatory variables, as well as between explanatory variables themselves. 
* Employ feature engineering based on existing features (consider all features, not just "good" ones).

## EDA 

* Plot distribution of response variable (consider transformations like absolute value, log, etc if continuous).
* Plot distribution of missing values; keep only "good" features below a certain threshold i.e. 75% missing.
* Plot correlation of good features with response variable. 
* Plot how response variables changes based on "good" features.
* Consider imputation of missing values based on the median or mode of other observations if there are enough non-missing values.
* Examine outliers. 
* If given time as a variable, plot how the response variable changes over time to determine seasonal vs. general trends. 
* If given locational data, make geographical plots to see how response variable changes by location. 
* Bin data into distinct groups to compare trends at a higher level (i.e. highest, lowest, and 50% around the median based on given metric).
* Use clustering techniques like k-means to look for natural groupings in the data.
* Consider principal component analysis on numeric datasets to reduce down to only most important variables.
* If dataset is not in numeric form, use normalization and hot-encoding for use in algorithms like k-means, KNN, PCA, etc.

## Modeling 

* Linear/logistic regression are good baselines for continuous and binary problems respectively.
  + Major Assumptions of Linear Regression: The relationship between the covariates and response is linear. All covariates have the same variance. The covariates do not interact.
* Consider random forest or KNN for multinomial classification problems.
* Use feature importance in models to inform how you view the data.
* XGBoost/ensemble models for tasks involving lots of data.
