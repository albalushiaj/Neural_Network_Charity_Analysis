# Neural_Network_Charity_Analysis
## Overview of the analysis: 
  - The purpose of this project is to create a a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup Company.
  -  After processing the data, a Neural Network Model is compiled, trained and evaluated. Lastly, an attempted is made to increase the optimized model to 75% or higher.
## Results: 
### Data Preprocessing

- What variable(s) are considered the target(s) for your model? 
  - The variable considered the target for this model is "IS_SUCCESSFUL"
- What variable(s) are considered to be the features for your model?
  - All other variables in the dataframe are considered features (excluding IS_SUCCESSFUL). 
  - The numerical variables are standardized using Scikit-Learn’s StandardScaler module.
- What variable(s) are neither targets nor features, and should be removed from the input data?
  - The "EIN" and "NAME" columns were dropped from the dataset. These identification columns did not contain any valuable information that would help with the analysis.

- Columns that had more than 10 unique values (Example: "CLASSIFICATION" and "APPLICATION_TYPE") possessed their rare categorical variables which were binned into a new "other" column. A list of categorical variables is created and is then encoded through using  OneHotEncoder. These encoded variable names are added to a new dataframe. After merging the one-hot encoded features, the originals are dropped. 

### Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
Were you able to achieve the target model performance?
What steps did you take to try and increase model performance?

## Summary:

Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
