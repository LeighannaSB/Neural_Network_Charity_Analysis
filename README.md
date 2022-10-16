# Charity Analysis Using Neural Networks
![image](https://user-images.githubusercontent.com/107161421/196058697-8c2e789a-a241-4789-af51-d2b837b8e1a0.png)


## Overview of the analysis

The purpose of this analysis was to assist a company with deciding which organizations to donate money to by creating a neural network to help determine whether applicants will be successful if given funding. A CSV containing details of over 34,000 organizations including data such as their application type, if they were successful in the past, and other categories was used for this analysis.

## Results: Using bulleted lists and images to support your answers, address the following questions.

- ** Data Preprocessing **
  - The target variable for the model is whether the organization was successfully funded
  - The feature variable for the model is the "IS_SUCCESSFUL" column
  - The "EIN" and "NAME" columns were immediately removed from the dataset as they provide no data that will help         increase the accuracy of the model

- ** Compiling, Training, and Evaluating the Model **
    - When attempting to optimize the the model four hidden layers were added with varying  amounts of neurons per          layer. Each layer used either relu or sigmoid activation after some trial and error, tanh was tested but yielded        lower accuracy overall. 
        - Hidden layer 1: 90 neurons (relu activation)
        - Hidden layer 2: 70 neurons (relu activation)
        - Hidden layer 3: 50 neurons (relu activation)
        - Hidden layer 4: 30 neurons (sigmoid activation)
        
     ![image](https://user-images.githubusercontent.com/107161421/196060059-6e203b5b-922a-4e80-91c4-5c099d7eed36.png)

    - Although the accuracy goal was 75%, after multiple adjustments the best accuracy the model was able to attain was     72.6%
    
    - While attempting to improve the accuracy of the model several changes were made:
        - The "Special Considerations" and "Ask Amount" columns were also removed from the data frame
        - The hidden layer count was changed from two to four
        - The neuron count in the hidden layers was also adjusted from (80, 30) to (90, 70, 50, 30)
        - Other activation functions were tested but relu and sigmoid provided the best accuracy
        - The number of epochs in the training regimen were upped from 100 to 150
        
        ![image](https://user-images.githubusercontent.com/107161421/196060367-ecc07a01-ec4e-4c50-86e8-fdd7f10b0339.png)

## Summary

Relu and Sigmoid activations yielded the highest accuracy at 72.6%. It may be beneficial to continue adding hidden layers to attempt to improve the accuracy. Increasing the epochs from 100 to 150 did not make any significant difference in the accuracy of the model but lowering the epochs below 100 may provide a more significant change in the model.  
