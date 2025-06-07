Charity Funding Predictor
Deep Learning Challenge — Module 21
University of California, Irvine – Data Analytics Bootcamp
Author: Jay Boon

Overview
Alphabet Soup, a non-profit organization, is looking to build a predictive model to help decide which applicants are most likely to be successful in receiving funding. The goal is to use machine learning—specifically a neural network—to create a binary classification model based on historical application data.

Data Preparation and Processing
To prepare the dataset for modeling, the following steps were taken:

Removed unnecessary columns:
Dropped EIN and NAME as they do not contribute meaningful predictive value.

Used NAME column for grouping rare entries:
Temporarily reintroduced the NAME column during a second test to help with binning infrequent categories.

Defined the target variable:
The model predicts the column IS_SUCCESSFUL, where:

1 = Applicant was successful

0 = Applicant was not successful

Simplified categorical data:

Used the CLASSIFICATION column for grouping (binning).

Combined rare classifications into a single category labeled "Other".

Converted categorical data to numerical:
Applied one-hot encoding using get_dummies() to prepare text data for modeling.

Split the data:
Divided the dataset into training and testing sets to evaluate performance.

Model Structure, Training, and Evaluation
Model architecture:

Consisted of 3 layers (input, hidden, output)

The number of neurons in the hidden layers was based on the number of input features

Training outcome:

The first model had 477 trainable parameters

Achieved an accuracy of just over 73%

Slightly below the target benchmark of 75%

Optimization Results
Second model improvements:

Included the NAME column for additional binning

Increased complexity: 3,298 trainable parameters

Improved accuracy to over 79%, surpassing the target threshold

Conclusion on architecture:

Deep learning models benefit from multiple layers

These layers help the model learn complex patterns and make better predictions through repeated filtering of input data