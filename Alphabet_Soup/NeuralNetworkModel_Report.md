# Neural Network Model Report

1. **Overview** of the analysis: Explain the purpose of this analysis.
From the charity information that we have, we want to see if the charity was successful or not

2. **Results:** Using bulleted lists and images to support your answers, address the following questions:
    * Data Preprocessing
        * **What variable(s) are the target(s) for your model?** <br>
         The target variable for our model is the `IS_SUCCESSFUL` column, which represents if the money was used effectively or not.
        * **What variable(s) are the features for your model?** <br>
         For our base model we had 43 features, which are all the given columns except for the `IS_SUCCESSFUL`. However, for the optimization part, we had 19611 features because I kept the `NAME` column.
        * **What variable(s) should be removed from the input data because they are neither targets nor features?** <br> The `EIN` and `NAME` columns.


    * Compiling, Training, and Evaluating the Model
        * **How many neurons, layers, and activation functions did you select for your neural network model, and why?** <br>
         for the base model, I had 43 input features, 2 hidden layers, and 2 different activation functions `relu` and `sigmoid`
        * **Were you able to achieve the target model performance?** No, in the base model, I got an accuracy of 72.7% ![Base Model Accuracy](Results/image.png). However, in my attempts to optimize the model by just keeping the `NAME` column, the accuracy went down to 60%, then it increased by 1% when I added a third hidden layer and adding more neurons to the first and second layers. Finally, in my last attempt trying to optimize the model, the accuracy increased to 74%, that is when I used the same activiation function and reducing the number of epoches from 100 to 50. ![Accuracy Score for optimized model](Results/image-1.png)
        * **What steps did you take in your attempts to increase model performance?** <br>
         In the first attempt, I dropped  fewer columns. (Keeping the `NAME` column from the orignial data). In the second attempt, I added more neurons to a hidden layer (Increasing hidden layer 1 nodes from 80 to 100, increasing hidden layer 2 nodes from 30 to 50), and I added more hidden layers. (Adding a third hidden layer with 25 nodes). In the last attempt, I used different activation functions for the hidden layers.(Change activation function from `relu` to `sigoid` for all hidden layers), and reduced the number of epochs to the training regimen from 100 to 50.


3. **Summary:** Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.


