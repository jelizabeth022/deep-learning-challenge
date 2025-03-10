# Deep-Learning-Challenge

# Neural Network Model Performance Report: Alphabet Soup Challenge

# Overview of the Analysis

The purpose of this analysis is to design and evaluate a deep learning model to predict the success of charitable donation campaigns. By leveraging the dataset provided by Alphabet Soup, the goal is to classify whether a donation will be successful (IS_SUCCESSFUL) based on key features of the organization's application and historical data. This model aims to help Alphabet Soup make informed decisions and improve the effectiveness of their fundraising initiatives.

# Results

# Data Preprocessing

1. Target Variable:

 - The target variable is IS_SUCCESSFUL, which indicates whether the donation campaign 
   was successful (1) or not successful (0).

2. Features:

- Key features for the model include:

APPLICATION_TYPE

AFFILIATION

CLASSIFICATION

USE_CASE

ORGANIZATION

STATUS

INCOME_AMT

SPECIAL_CONSIDERATIONS

ASK_AMT

3. Removed Variables:

The EIN and NAME columns were removed because they are unique identifiers and do not contribute to predicting the target variable.

# Compiling, Training, and Evaluating the Model

1. Neurons, Layers, and Activation Functions:

Input Layer:

The model starts with an input layer with a dimension equal to the number of features (preprocessed data with scaling).

Hidden Layers:

The model includes four hidden layers with increasing neurons:

Layer 1: 7 neurons with relu activation.

Layer 2: 14 neurons with relu activation.

Layer 3: 21 neurons with relu activation.

Layer 4: 28 neurons with relu activation (added to improve performance).

Dropout Layers:

Dropout was added after each hidden layer with a rate of 0.2 to prevent overfitting.

Output Layer:

A single neuron with a sigmoid activation function for binary classification.

2. Model Performance:

The target accuracy of 75% was challenging to achieve consistently.

The final model attained an accuracy of approximately 72.23%, indicating strong predictive power but with room for improvement.

3. Steps to Improve Performance:

Added a fourth hidden layer to capture more complex patterns in the data.

Included dropout layers after each hidden layer to reduce overfitting.

Tuned hyperparameters such as the number of epochs and batch size to find the optimal training setup.

Standardized the input data using StandardScaler to normalize features.

# Summary

The deep learning model developed for the Alphabet Soup challenge demonstrates significant predictive potential with an accuracy of approximately 72.23%. While this falls slightly short of the target 75% accuracy, the model effectively identifies patterns in the dataset to classify donation success. Additional strategies to further improve performance include:

Alternative Models:

Implementing a Random Forest or Gradient Boosting model, which may handle feature variability and non-linearity better.

Advanced Techniques:

Utilizing hyperparameter optimization (e.g., GridSearchCV) to fine-tune the model architecture.

Addressing class imbalance through techniques like oversampling or SMOTE (Synthetic Minority Oversampling Technique).

Feature Engineering:

Creating additional features or aggregations that could provide more predictive value.

In conclusion, this deep learning model provides a strong foundation for Alphabet Soup's classification needs, and further optimization or experimentation with alternative models could achieve or exceed the desired accuracy.
