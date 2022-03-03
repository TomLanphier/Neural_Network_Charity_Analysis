# Neural Network Charity Analysis
## Overview
The purpose of this project was to create a machine learning program to predict the applicant's success if they were funded by Alphabet soup. A large database of 34,000 organizations that were previously funded was used to train and test this machine learning program.

## Results
### Data Processing
- The target for the model was the "IS_SUCCESSFUL" column.
- The features for the model were the "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION",  "ORGANIZATION", "SPECIAL_CONSIDERATIONS", and "ASK_AMT"
- The "EIN","NAME","USE_CASE","STATUS", and "INCOME_AMT" columns were neither features nor targets and were removed from the database accordingly.

### Compiling, Training, and Evaluating the Model
- Initially, 2 hidden layers were used. The first had 80 neurons, the second had 30. Both used rectified linear unit activation functions and the output layer used a sigmoid activation function.
- No, the best I was able to get was accuracy = 0.7325
- Columns that were initially catagorized as features ("USE_CASE","STATUS", and "INCOME_AMT") were removed, which increased the accuracy of the run. The output activation function was changed to tanh, but this decreased the accuracy, so it was switched back to sigmoid. The number of neurons in the hidden layer was increased and a third hidden layer was added. Also, the redundant column "SPECIAL_CONSIDERATIONS_N" was dropped as it was already represented by "SPECIAL_CONSIDERATIONS_Y".

## Summary
- Removing "USE_CASE","STATUS", and "INCOME_AMT" columns was found to increase the accuracy of the model.
- A limit was reached for the accuracy of the model at 0.7325, further adjustments decreased the accuracy of the model.
- A random forest of decision trees could be used, which may result in better success as this is a classification problem, and decision trees are able to handle them better than the neural network.