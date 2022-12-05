# Neural_Network_Charity_Analysis
# Overview of the analysis: 
The purpose of this analysis was to help the Alphabet Soup foundation decide which applicants to invest in based on their predicted success. 

## Results: 
### Data Preprocessing
- The data was preprocessed into features and target arrays. Features included the following:
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
--CLASSIFICATION—Government organization classification
•	USE_CASE—Use case for funding
•	ORGANIZATION—Organization type
•	STATUS—Active status
•	INCOME_AMT—Income classification
•	SPECIAL_CONSIDERATIONS—Special consideration for application
•	ASK_AMT—Funding amount requested
The target array was made up of the IS_SUCCESSFUL column
•	IS_SUCCESSFUL—Was the money used effectively
Non-features excluded:
•	EIN and NAME—Identification columns

- Compiling, Training, and Evaluating the Model
For Deliverable 3, I increased the number of nodes and added a third hidden layer. The layers had 120, 80 and 40 respectively. The relu activation function was used on the 3 hidden layers and the sigmoid activation function was used on the output layer due to the output being binary and we are trying to predict the probability of success as the output.

I was not able to achieve the target model performance. The highest accuracy I was able to obtain was 72.5%.

In order to try to increase the model performance, I added a third hidden layer which resulted in a slight increase in the accuracy. 

INSERT CHANGE 1 AND RESULTS

I also excluded ORGANIZATION AND SPECIAL_CONSIDERATIONS columns as they seemed non-beneficial. 

INSERT CHANGE 2 AND RESULTS

Finally, I tried using the Random Forest model which resulted in the lowest score achieved by the changes made at 70.5%. 

INSERT CHANGE 3 AND RESULTS

# Summary: 

I used the Sequential and Random Forest models. Their predictive accuracies were both over 70% but neither were able to achieve the desired 75%.

A Gradient Boosting Classifier would be a good next step, it has some similarities to the Random Forest model but builds off the deficiencies of each preceding decision tree created in the model. This should lead to better results. 
