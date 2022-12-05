# Neural_Network_Charity_Analysis
## Overview of the analysis: 
The purpose of this analysis was to help the Alphabet Soup foundation decide which applicants to invest in based on their predicted success. 

## Results: 
### Data Preprocessing
- The data was preprocessed into features and target arrays. Features included the following:

  - **APPLICATION_TYPE** — Alphabet Soup application type
  - **AFFILIATION** — Affiliated sector of industry
  - **CLASSIFICATION** — Government organization classification
  - **USE_CASE** — Use case for funding
  - **ORGANIZATION** — Organization type
  - **STATUS** — Active status
  - **INCOME_AMT** — Income classification
  - **SPECIAL_CONSIDERATIONS** — Special consideration for application
  - **ASK_AMT** — Funding amount requested

- The target array was made up of the IS_SUCCESSFUL column:

 - **IS_SUCCESSFUL** — Was the money used effectively

  - Non-features excluded:

**EIN and NAME** — Identification columns

  - Compiling, Training, and Evaluating the Model

For Deliverable 3, I increased the number of nodes and added a third hidden layer. The layers had 120, 80 and 40 respectively. The relu activation function was used on the 3 hidden layers and the sigmoid activation function was used on the output layer due to the output being binary and we are trying to predict the probability of success as the output.

I was not able to achieve the target model performance. The highest accuracy I was able to obtain was 72.5%.

In order to try to increase the model performance, I added a third hidden layer which resulted in a slight increase in the accuracy as shown below: 

![Attempt1_Change](https://user-images.githubusercontent.com/106631875/205740045-5c38104a-2129-4c72-b31d-1aefb2659a9d.png)

![Attempt1_Results](https://user-images.githubusercontent.com/106631875/205740103-84fd46a9-ba72-48d9-b7d1-7a2be7a360ae.png)

I also excluded ORGANIZATION AND SPECIAL_CONSIDERATIONS columns as they seemed non-beneficial as shown below:

![Attempt2_Change](https://user-images.githubusercontent.com/106631875/205740127-0396d2c6-7c86-4117-b8a3-8fda4f027c44.png)

Results of excluding ORGANIZATION AND SPECIAL_CONSIDERATIONS columns: 

![Attempt2_Results](https://user-images.githubusercontent.com/106631875/205740163-cb9447eb-daf7-4483-8fa4-122dd22ad1e4.png)

Finally, I tried using the Random Forest model which resulted in the lowest score achieved by the changes made at 70.5%. 

Below are the changes made to test the Random Forest model on the data:
![Attempt3_Change_1](https://user-images.githubusercontent.com/106631875/205740210-7f66ae99-0371-448f-87c1-eb084faacf9b.png)

![Attempt3_Change_2](https://user-images.githubusercontent.com/106631875/205740221-1f8c651c-c33e-43ba-ab4f-d230d5b4375d.png)

Results of the Random Forest model:
![Attempt3_Results](https://user-images.githubusercontent.com/106631875/205740238-024c65fd-a885-4acb-8c5d-bae617eb48d7.png)

# Summary: 

I used the Sequential and Random Forest models. Their predictive accuracies were both over 70% but neither were able to achieve the desired 75%.

A Gradient Boosting Classifier would be a good next step, it has some similarities to the Random Forest model but builds off the deficiencies of each preceding decision tree created in the model. This should lead to better results. 
