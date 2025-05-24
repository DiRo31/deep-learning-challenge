# deep-learning-challenge
Module 21 Challenge


Hello!

Welcome to the Module 22 Challenge! (It has in fact been that long!)

Details for the assignment can be found here: https://bootcampspot.instructure.com/courses/6909/assignments/92712

Here is the report:



# Overview of the Analysis 
The purpose of this analysis was to create to predict the success of funding applicants for Alphabet Soup using deep learning techniques. This tool helps the organization select the potentially most successful applicants, leading to improving the efficiency of their funding allocation.

## Results

### Data Preprocessing

  What variable(s) are the target(s) for your model?:
      IS_SUCCESSFUL (1 for successful, 0 for unsuccessful)

  What variable(s) are the features for your model?:
      APPLICATION_TYPE
      AFFILIATION
      CLASSIFICATION
      USE_CASE
      ORGANIZATION
      STATUS
      INCOME_AMT
      SPECIAL_CONSIDERATIONS
      ASK_AMT

  What variable(s) should be removed from the input data because they are neither targets nor features?:
      EIN and NAME were removed as they were not relevant for the prediction.

### Compiling, Training, and Evaluating the Model

  How many neurons, layers, and activation functions did you select for your neural network model, and why?:
      Input layer: 43 features (based on the number of parameters in the first dense layer)
      First hidden layer: 80 neurons with ReLU activation
      Second hidden layer: 30 neurons with ReLU activation
      Output layer: 1 neuron with sigmoid activation (binary classification)

  Were you able to achieve the target model performance?:
      The model did not achieve the target performance of 75% accuracy and instead was about 72.57% on the test set.

  What steps did you take in your attempts to increase model performance?:
      Binning of infrequent categories in APPLICATION_TYPE and CLASSIFICATION
      Scaling of numerical features using StandardScaler
      Using two hidden layers with 80 and 30 neurons respectively
      Training for 100 epochs with a batch size of 32 and validation split of 0.1

### Summary

The deep learning model achieved an accuracy of 72.57% in predicting the success of funding applications. This performance is below the 75% target for accuracy, meaning there is opportunity for improvement. Maybe it would be helpful to use a different tool within python for making predictions to see if the predictions would improve. Random Forest Classifier could be better by using decision tress  to make predictions, which might help identify the key factors behind the most successful applications. 
