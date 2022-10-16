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
- After preparing the data, a deep learning model is created to create a binary classification model that can predict if an Alpabet Soup funded organization will be successful depending on the features in the charity database. 
- ReLU (Rectified Linear Unit) is used as the activation function for the first and second layer.
- For the output layers, a sigmoid activation function is used.
- For training the model, a callback saves the model's weights every 5 epochs. 
- After training, the model's Loss and Accuracy values are evaluated. Below is the output of the model.

![image](https://user-images.githubusercontent.com/106709942/196049285-4f0be8e5-79fc-4a5c-afeb-fef499c60533.png)


  - The accuracy of 72.6% is somewhat high.
 
 _*Optimization Attempt 1*_
 
- The number of neurons in the hidden layers were increased. This had a negligible effect on the model's accuracy.

 _*Optimization Attempt 2*_
 
 - A third hidden layer was added to the model with 4 neurons. This slightly reduced the model's accuracy, and the number of epochs were also reduced to 40 (From 50 epochs to 40) 

 _*Optimization Attempt 3*_
 
 - The activation function in the second hidden layer is changed to a tanh function. 
 - This reduced the models accuracy.
 - Thus, it can be determined that the activation function that best suits this model is ReLu.


## Summary:
- None of the optimization attempts were successful to produce a model with a predictive accuracy level of 75% or higher. The following methods were attempted:
    - Adding an additional hidden layer.
    - Adding more neurons to a hidden layer.
    - Using different activation functions.
    - Decreasing the number of epochs in the training.
- There could be a number of reasons as to why this analysis was not successful such as the number of neurons in the hidden layers may need to be adjusted or the number of epochs during trainiing may need to be increased or there may be outliers in the data which are disrupting the model.  
- Possibly conducting a Random forest classifier may be better in this binary classification project due to the reason that Deep Learning models are complex to setup and time consuming to train whilst Random Forest Classifiers are much simpler to setup and can be trained quicker. In addition, the predictive accuracy of these two methods would be close in number whilse Random Forest Classifier has an upper hand with it's ease of implementation, and how applicable it is in this analysis. I would recommend using Random Forest Classifier for future analysis of this project. 
