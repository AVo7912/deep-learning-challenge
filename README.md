# Deep Learning Challenge
## Overview

For this project, a deep learning model is used to develop a binary classifier that can predict the likelihood of applicants achieving success if they receive funding from Alphabet Soup. The project will utilize the features present in the given dataset and employ diverse machine learning methods to train and assess the model's performance. The objective is to optimize the model in order to attain an accuracy score surpassing 75%.

## Results
### Data Preprocessing

•	What variable(s) are the target(s) for your model?

  o	The target for each model was the IS_SUCCESSFUL column. The model aims to predict the success of applicants if they receive funding

•	What variable(s) are the features for your model?

  o	The feature variables are every column other than the target variable and the non-relevant variables. The following columns were considered as features for the model:
  
    APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE,	ORGANIZATION,	STATUS,	INCOME_AMT,	SPECIAL_CONSIDERATIONS,	ASK_AMT
    
•	What variable(s) should be removed from the input data because they are neither targets nor features?

  o	The EIN column and the NAME columns.
  
### Compiling, Training, and Evaluating the Model

•	How many neurons, layers, and activation functions did you select for your neural network model, and why?

  o	Initial Model: I included 3 layers, an input layer of 120 neurons, a second layer of 40 neurons, and an output layer of 1 neuron. I chose the numbers to ensure that the total number of neurons in the model was at least 3 times the number of input features. ReLu activation function was applied for the first and second layers, and the sigmoid activation function for the output layer since the goal was binary classification.

•	Were you able to achieve the target model performance?
  
  o	In my initial model, I was not able to achieve the target model performance. The accuracy score was 72.68%

•	What steps did you take in your attempts to increase model performance?
  
  o	Optimization 1: the model was changed by adding 2 dropout layers with a rate of 0.5 to enhance generalization and changed the activation function to tanh in the input and hidden layer. The units were also increased in each layer. With that I got an accuracy score of 73.01%
 
  o	Optimization 2: the model was changed by removing the dropout layers, adding a third hidden layer, and making the number of units the same among the three layers. With that I got an accuracy score of 72.76%
  
  o	Optimization 3: the model was changed by using ReLu and only used 2 hidden layers. The units were kept at 100. With that I got an accuracy score of 72.89%

### Summary

I wouldn't suggest any of the models above. I would explore alternative approaches like incorporating the Random Forest Classifier and experimenting with different preprocessing modifications. I believe that making changes to the dropout layers, trying out various activation functions, and adjusting the number of layers and neurons could also contribute to optimizing the model.
