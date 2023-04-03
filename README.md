# Deep-Learning-Challenge (Alphabet Soup Charity)

## Background
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

* EIN and NAME—Identification columns
* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special considerations for application
* ASK_AMT—Funding amount requested
* IS_SUCCESSFUL—Was the money used effectively

## Objective

### Purpose:
The purpose of the analysis is to predict whether applicants will be successful if funded by AlphabetSoup using Neural Networks.

### Results:

* Data Preprocessing

    * **What variable(s) are the target(s) for your model?**
       * The target variable is "IS_SUCCESSFUL" which indicates if funding was successful.
    
    * **What variable(s) are the features for your model?**
       * The features of the model include: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
    
    * **What variable(s) should be removed from the input data because they are neither targets nor features?**
       * EIN: Employee Identification Number
       * NAME (it is removed and will be re-added for reoptimization)
    
    
* Compiling, Training, and Evaluating the Model

   * **How many neurons, layers, and activation functions did you select for your neural network model, and why?**
      * Features used: APPLICATION_TYPE, CLASSIFICATION
      * 2 Hidden layers used, first layer have 80 neurons, Second layer have 30 neurons. "ReLu" activation function is used for the input layers and Sigmoid is used for the output layers
      * Trainable Parameters: 5,981
      
      ![image](https://user-images.githubusercontent.com/116117065/229635792-dceb42e6-8146-40e9-81e8-76f59f7c0f57.png)

      
     
   * **Were you able to achieve the target model performance?**
      * The initial accuracy is 73% but after three optimizations the accuracy reached 78% which is above the target model performance.
      
      
      ![image](https://user-images.githubusercontent.com/116117065/229636036-7a95fb14-b331-4493-9eca-92acf519d83d.png)


   
   * **What steps did you take in your attempts to increase model performance?**
      * Dropping fewer columns and binning from APPLICATION to NAME, the target model performance was achieved. I did 3 Optimizations to get to the target since the initial accuracy is only 73% and is below the target of 75%. 
      
      
      **Optimization 1:**
      
      * Features used: NAME, APPLICATION_TYPE, CLASSIFICATION
      * hidden layers: 3 LAYERS (with 20, 26 and 3 neurons)
      * Activation Functions: ReLU (first hidden layer), Sigmoid (second & third hidden layer, outer layer)
      * Trainable Parameters: 6,131
      * Epochs: 100
      * Loss: 0.46
      * Accuracy: 78%
      
        **Target reached:** Yes
        
        
          ![image](https://user-images.githubusercontent.com/116117065/229637355-7dba76f2-8c7d-4ac3-ae9f-5901a933a45d.png)
          
      
      
       **Optimization 2:**
       
       
       * Features used: NAME, APPLICATION_TYPE, CLASSIFICATION
      * hidden layers: 3 LAYERS (with 100, 50 and 20 neurons)
      * Activation Functions: ReLU (first hidden layer and second layer), Sigmoid (third hidden layer and outer layer)
      * Trainable Parameters: 49,891
      * Epochs: 100
      * Loss: 0.46
      * Accuracy: 78%
      
        **Target reached:** Yes
        
       
        ![image](https://user-images.githubusercontent.com/116117065/229637485-be905322-77b5-44ba-bc5d-4c91bd152f51.png)
       
       
        **Optimization 3:**
        
      * Features used: NAME, APPLICATION_TYPE, CLASSIFICATION
      * hidden layers: 3 LAYERS (with 90, 50 and 10 neurons)
      * Activation Functions: ReLU (first hidden layer and second layer), Sigmoid (third hidden layer and outer layer)
      * Trainable Parameters: 44,491
      * Epochs: 100
      * Loss: 0.46
      * Accuracy: 78%
      
        **Target reached:** Yes
          
      ![image](https://user-images.githubusercontent.com/116117065/229637575-2136bd22-d88d-49b4-b9af-c2fb0de39473.png)
      
      
      
## Summary
### Conclusion

To sum up, I obtained a predictive accuracy of 78% in categorizing the success of organizations supported by Alphabet Soup Charity by iterating through three distinct models. My efforts to optimize the models, such as removing columns, grouping categorical variables, incorporating hidden layers and neurons, and experimenting with different activation functions, highlighted the adaptability and sensitivity of deep learning neural networks. However, it took multiple rounds of optimization attempts to attain the 78% target accuracy.

Initially, the features only results in a 73% accuracy, which is below the targeted model performance. However, after trying to change the number neurons and using different features like changing from APPLICATION to NAME for binning brought the accuracy up to 78% and helped me achieve the target. 

Neural networks are flexible and can be used for both regression and classification problems. The deep learning neural networks works fine with this model since we can do different optimization rounds until we reached the target. However, this is not a suitable optimization algorithm when dealing with big data with millions of parameters. This model depends a lot on training data and it is time consuming.

on the other hand, I recommend using the RandomForest Model because it do better with the categorical variables.

     
 
 

      
 
   
   
   
   
   
   
   

