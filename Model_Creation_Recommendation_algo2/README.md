# Creating a Machine Learning Model
This document outlines the steps for creating a prediction function used for recommendations. The prediction function uses statistical information based on the last 3 weeks of purchases to define the recommendation

## Define the Problem
Before you start building a model, it's important to understand the problem you are trying to solve. This includes identifying the goals of the model, the target audience, and any constraints or limitations that may impact the model's performance.

## Collect the required Data
The next step is to gather the data you will use to train and test your model. You will need to connect to Intempt via APIs to access data, and extract the required collections.

Once you know which collection from Intempt is requred. You will need to save the collections as a list for example: `feature_names = ['churn']` to a pickle file

## Create the prediction function
This function uses the collected data to extract statistics of customer purchases. Based on the results of these logical equations a recommendation is done.

When you are done with the logic of the function save the function as a pickle file

## List all libraries used
The final step would be to provide us with all the libraries that those pkl objects are using and store these into a text file `requirements.txt`

## Conclusion

By following these steps and documenting your work, you can create a machine learning model that is well understood and can be easily reproduced by others. At the end of this process you will end up with the following files:
- feature_names.pkl
- prediction.pkl
- requirements.txt

