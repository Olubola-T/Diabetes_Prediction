# Diabetes_Prediction
A classification task for predicting diabetes

INTRODUCTION

The data used in this project is a record for students, including characteristics like age, height, weight, and smoking and diabetes status. The goal of this project was to predict who had diabetes, using the other features.

EXPLORATORY ANALYSIS AND PREPROCESSING

The data was mostly explored by visualization. Missing values were filled, and count plots and barplots were used to visualize the different classes of the categorical variables. New features were also engineered from the original ones to further explore the data. Outliers in some numerical variables were removed. Due to the large variance amongst the features, log normalization was used to transform some variables.

CLASSIFICATION

Four classification models were initially deployed, and hyperparameter tuning was performed for the two with the highest accuracy scores (logistic regression and K nearest neighbours).

RESULTS

While both the logistic regression and K nearest neighbours algorithms had high accuracy scores (> 0.9), they did not perform well with classifying the positive class. The logistic regression model did not classify any instance of the positive class correctly at all. With the negative class to positive class ratio being 9:1, this is not unexpected. Hence, accuracy is not the best metric to use in this case; F1-score is a better option, and it was low. The K nearest neighbours algorithm had better F1-score.

LIMITATIONS

This dataset is unbalanced and the classification algorithms will perform better if there are more positive-class data to train on. I also had difficulty dropping decimal points from some features, including 'Age', 'Heart Rate', and 'Blood Pressure'. I tried converting float to int, using round(), and truncate(), but none of them worked. I hope to be able to figure this out next time.
