# Deep Learning: Charity Funding Predictor
<img align="center" src="/Images/deep learning.jpg" width="1000" />


## Analysis and Report:

1. **Purpose** 
- Using Machine Learning and Neural Networks to apply target/features to help Alphabet Soup to select applicants with highest chance of success if funded. 

2. **Results**:

  * Data Preprocessing
    * What variable(s) are the target(s) for your model? 
    - IS_SUCCESSFUL is the target, where 1 indicated that the money was used successful and 0 is unsuccessful.
    * What variable(s) are the features for your model? 
    - All columns in data except EIN and NAME
    * What variable(s) should be removed from the input data because they are neither targets nor features? 
    - EIN and NAME were removed.
  
* Compiling, Training, and Evaluating the Model
    * How many neurons, layers, and activation functions did you select for your neural network model, and why?
    - Maximum 80 neurons, 3 layers, and reLU and Sigmoid were used. 
    - reLU (Rectified Linear Unitfunction) was used as a good starting point for modeling positive, nonlinear input data for classification or regression.
    - The sigmoid function values are normalized to a probability between 0 and 1, which is ideal for a binary classification dataset, in this case it's IS_SUCCESSFUL   and not. 
    - 
<img align="center" src="/Images/Compiling_Training_Evaluating Model.png" width="600" />
<img align="center" src="/Images/Compiling_Training_Evaluating Model2.png" width="600" />

    * Were you able to achieve the target model performance?
    - No, as it only result 72% accuracy
    * What steps did you take in your attempts to increase model performance?
    - Dropping more columns, increased the number of application types to include values >150, classification count > 200, change activation hidden layer from ***relu*** to ***tanh***. The accuracy did not reach 75%. Accuracy, in fact, decreased to 63% in optimization file.
 
<img align="center" src="/Images/Optimaztion.png" width="600" />
<img align="center" src="/Images/Optimization2.png" width="600" />
    

3. **Summary**: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
- reLU and Sigmoid yields 72% accuracy, but reLu and Tanh function only yields 63%. 
- Maybe try Random Forest next time, as it if less affected by outliers. Tanh was not a good try because the output of the tanh activation function is Zero centered; hence we can map the output values as strongly negative, neutral, or strongly positive. In this case there is no negative, only 1 and 0. 


## Background

The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

* **EIN** and **NAME**—Identification columns
* **APPLICATION_TYPE**—Alphabet Soup application type
* **AFFILIATION**—Affiliated sector of industry
* **CLASSIFICATION**—Government organization classification
* **USE_CASE**—Use case for funding
* **ORGANIZATION**—Organization type
* **STATUS**—Active status
* **INCOME_AMT**—Income classification
* **SPECIAL_CONSIDERATIONS**—Special consideration for application
* **ASK_AMT**—Funding amount requested
* **IS_SUCCESSFUL**—Was the money used effectively

