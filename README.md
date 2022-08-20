# Module-19-Neural_Network_Charity_Analysis

## Overview of the Analysis
The purpose of this analysis is to create a binary classifier to determine whether applicants will be successful if funded by Alphabet Soup. The dataset analyzed includes more than 34,000 organizations that have received funding from Alphabet Soup.

## Results
Data Preprocessing
1. What variable(s) are considered the target(s) for your model?
  The variable "is_successful" is considered the target for the model.
2. What variable(s) are considered to be the features for your model?
  The features that were considered was everything else other than "is_successful" and the columns dropped such as "EIN". Those were NAME, APPLICATION, TYPE,    AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT,SPECIAL_CONSIDERATIONS, STATUS, and ASK_AMT
3. What variable(s) are neither targets nor features, and should be removed from the input data?
  "EIN" is an example of neither a target nor feature that should be removed from the input data because the numbers could confuse the computer into thinking its significant.
  
Compiling, Training, and Evaluating the Model
1. How many neurons, layers, and activation functions did you select for your neural network model, and why?
  I increased the hidden layers to 3 from 2, which appeared to increase the accuracy to above 75%. Instead of the first and secon activation function being 'Relu', I changed the second and third function to 'Sigmoid' and the output function was kept as "Sigmoid". The epochs was changed from 30 to 100 to train the data.
2. Were you able to achieve the target model performance?
  Yes, achieved an accuracy score of 77.8%.
  ![Image](https://github.com/cstern28/Module-19-Neural_Network_Charity_Analysis/blob/main/Screenshots/accuracy_scoreV2.png)
3. What steps did you take to try and increase model performance?
  I converted the NAME columns into data points and added a third layer to the model. I also changed the activation function to "Sigmoid" for the 2nd and 3rd layer.
  
## Summary
Overall, an applicant had an 77.8% chance of being successful if:
- The NAME of the applicant appears more than 10 times (this means they have applied more than 10 times).
- The Type of APPLICATION is one of the following: T3, T4, T5, T6, T7, T8, T10, and T19.
- The CLASSIFICATION is on of the following: C1000, C1200, C2100, C2000, and C3000.

I recommend using the Random Forest Model because it is helpful with classification problems and can work with many features.
