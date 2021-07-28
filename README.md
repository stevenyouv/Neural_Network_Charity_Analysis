# Neural_Network_Charity_Analysis

## Analysis Overview

The purpose of this project is to analyze and classify the success of charitable donations by using deep-learning neural networks with the TensorFlow platform in Python.  The following methods were used for the analysis:
- preprocessing the data for the neural network model
- compile, train, and evaluate the model
- optimize the model

## Results

### Data Preprocessing
- The 'EIN' and 'NAME' columns were removed from the input data
- Since the column 'IS_SUCCESSFUL' contains binary data determining whether or not the charity donation was used effectively, the variable is considered the target for our deep learning neural network.
- 'APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT' are all columns that are features for our model.
- Encoding of the categorical variables, splitting into training and testing datasets and standardizations have been applied to the features.

### Compiling, Training, and Evaluating the Model
- This deep-learning neural network model consists of two hidden layers with 80 and 30 neurons.
- The input data has 43 features and 25,724 samples.
- The output layer is made of a unique neuron since it is a vinary classification.
- The 'ReLU' activation function for the was used to speed up the training process for the hidden layers.  As our output is a binary classification, `Sigmoid` is used on the output layer.
- For the compilation, the optimizer is 'adam' and the loss functionis 'binary_crossentropy'.
- The model accurary is under 75% which is not a satisfying performance to help predict the outcome of charitable donations.
- To increase the performance of this model, bucketing was applied to the feature 'ASK_AMT' and the different values were organized by intervals.
- The number of neurons on one of the hidden layers were increased, and a model with three hidden layers was used.
- A different activation function 'tanh' was also used, but none of these steps improved performance

## Summary
The deep learning neural network model was not able to achieve the target of 75% accuracy.
We could use a supervised macine learning model such as the Random Forest Classifier to combine multiple decision trees to generate a classified output and evaluate its performance against our deep learning model.  
