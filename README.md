# deep_learning_challenge

Data Analytics Bootcamp - University of California, Irvine – 
Module 21 
Topic: Neural Networks and Machine Learning
Title: Alphabet Soup Investors Analysis (ML)
By:Jay Boon


Project Objective
This project focuses on helping the non-profit foundation Alphabet Soup predict the likelihood of funding success for applicants. A deep learning model was developed to analyze applicant data and produce a binary outcome—indicating whether funding is likely to be awarded.

The target variable in the dataset is IS_SUCCESSFUL, where 1 represents a successful funding outcome and 0 represents an unsuccessful one.

Data Preparation & Preprocessing
Data preparation and preprocessing were critical to ensuring the model could learn meaningful patterns. Below are the key steps, in proper order:

Standardized Feature Scaling
All numeric input values were standardized to ensure consistent scaling across features, enabling the model to interpret them equally during training.

Removed Non-Contributory Columns
Irrelevant columns such as EIN and NAME were dropped. In a later variation, NAME was temporarily retained to aid in category binning.

Identified High-Cardinality Features
Columns with excessive unique values were analyzed. Rare entries were grouped into a generic "Other" category to minimize noise.

Encoded Categorical Variables
One-hot encoding was applied to transform text-based categories into numerical format suitable for neural network input.

Split Data for Training and Evaluation
The cleaned dataset was divided into training and test sets to assess model performance on unseen data.

Model Development
A deep neural network was implemented using TensorFlow and Keras, structured as follows:

An input layer matching the number of processed features

Two hidden layers using ReLU activation

A final output layer with sigmoid activation to enable binary classification

The model used binary cross-entropy as its loss function and tracked accuracy during training.

Results: Baseline Model
The baseline model consisted of three total layers and 477 trainable parameters. Upon evaluation, the model achieved an accuracy of approximately 73%, which was slightly below the target threshold of 75%.

Optimization and Improvement
Several changes were applied to improve performance:

Temporarily reintroducing the NAME column for refined binning

Increasing the number of neurons in the hidden layers

Adjusting the network architecture, resulting in 3,298 trainable parameters

After these optimizations, the improved model reached an accuracy of over 79%, successfully surpassing the project benchmark.

Key Takeaways
Standardizing and encoding data correctly has a major impact on model performance

Binning rare categories improves generalization and reduces noise

Increasing model complexity (with more nodes and layers) can lead to significantly better results when properly managed

Tools Used
Python

Pandas

TensorFlow / Keras

Scikit-learn

For additional questions or professional inquiries, connect via LinkedIn.