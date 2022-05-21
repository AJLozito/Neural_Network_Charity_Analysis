# Neural_Network_Charity_Analysis


## Overview of the Analysis

     The purpose of this project was to create a binary classifier to determine the viability of a company funding a charity by accessing its past investments.


## Results

o	Data Preprocessing
        The target variable considered for the model was “IS_SUCCESSFUL” because it indicates the success of a project

        The variables considered to be featured for the model included:
          -	EIN
          -	NAME
          -	APPLICATION_TYPE
          -	AFFILIATION
          -	CLASSIFICATION
          -	USE_CASE
          -	ORGANIZATION
          -	STATUS
          -	INCOME_AMT
          -	SPECIAL_CONSIDERATIONS
          -	ASK_AMT

         EIN and NAME were removed because these variables were neither targets nor features

o	Compiling, Training, and Evaluating the Model
         I started with 2 hidden node layers:
          -	First = 80 neurons
          -	Second = 30 neurons
          -	These count figures were general benchmarks that were reevaluated later in this analysis
          -	Each node layer included a relu activation function
               •	This function was chosen over others because it overcomes mathematical obstacles to solve problems

         The target model performance level of 75% accuracy was not achieved
     ![image](https://user-images.githubusercontent.com/96176817/169627270-9507771a-74e5-4b29-a4ef-266155dc42e7.png)

         The steps below describe my attempts at improving the model’s performance:

               Attempt 1: 
               -	The Status and Special Considerations variables were removed

               -	The number of neurons was changed in each layer:
                    o	1 = 200
                    o	2 = 100
                    o	3 = 50

               -	The output layer was changed to tanh
               ![image](https://user-images.githubusercontent.com/96176817/169627288-80085ce5-026d-46eb-86eb-356915a7f610.png)

               Attempt 2:
               -	The Status and Special Considerations variables were removed

               -	The number of neurons was changed in each layer:
                    o	1 = 200
                    o	2 = 100
                    o	3 = 50

               -	All 3 hidden layers were changed to tanh

               -	The output layer was changed to tanh
               ![image](https://user-images.githubusercontent.com/96176817/169627300-f93be936-76ee-4f4e-bbed-ca37f2958da4.png)

               Attempt 3:
               -	The Status and Special Considerations variables were removed

               -	Two extra hidden node layers were added

               -	The number of neurons was changed in each layer:
                    o	1 = 400
                    o	2 = 200
                    o	3 = 100
                    o	4 = 50
                    o	5 = 25

               -	All 5 hidden node layers were changed to relu

               -	The output layer was changed to relu

               -	The number of training epochs was changed to 60

               -	The number of callback training epochs was changed to 200
               ![image](https://user-images.githubusercontent.com/96176817/169627321-ff95c527-df25-4704-826d-4362f404d468.png)


## Summary:
     The base accuracy and loss rates of .7251 and .5559 were not significantly increased through this project. A random forest could be used to develop decision trees and generate a more accurate model.
