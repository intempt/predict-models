# Creating a Machine Learning Model
This document outlines the steps for creating a machine learning model supported by Intempt, as well as the considerations and best practices involved.

## Define the Problem
Before you start building a model, it's important to understand the problem you are trying to solve. This includes identifying the goals of the model, the target audience, and any constraints or limitations that may impact the model's performance.

## Collect the required Data
The next step is to gather the data you will use to train and test your model. You will need to connect to Intempt via APIs to access data, and extract the required collections.

Once you know which collection from Intempt is requred. You will need to save the collections as a list for example: `feature_names = ['churn']` to a pickle file 

## Preprocess the Data
Once you have collected the data, you will need to preprocess it to ensure it is clean and ready for modeling. This may include handling missing values or removing outliers.

The preprocess flow you created will need to turned into a function and save it as a pickle file. This `preprocess_function` will take the collected data from the step above and output a preprocessd dataframe

## Apply Transformations 
Once you have preprocessed the data, it's a good idea to explore and visualize it to get a better understanding of its characteristics and patterns. By doing so you will be able to properly apply transformations like converting non-numeric features into numeric, scaling features, remove skewness or normalize the data.

You will need to define a ColumnTransformer which will be used in a Pipeline to selectively prepare the columns of your dataset. This `model_transform` will also need to be stored as a pickle file 

### Select and Split the Data
After transforming the data, you will need to select a subset of it to use for training and testing. It's generally a good idea to use a portion of the data for training and a separate portion for testing to ensure the model is generalizable.

### Choose a Model and Train It
With the data prepared, you can now select a machine learning model to use and begin training it. There are many different types of models to choose from, including linear regression, decision trees, and neural networks. You will need to select the appropriate model based on the characteristics of your data and the problem you are trying to solve.

## Evaluate the Model
Once the model is trained, you will need to evaluate its performance to determine how well it is solving the problem. This may involve using various metrics, such as accuracy, precision, and recall, to measure the model's performance on the test data.

When you are done with the `model` save the model as pickle file

## List all libraries used
The final step would be to provide us with all the libraries that those pkl objects are using and store these into a text file `requirements.txt`

## Conclusion

By following these steps and documenting your work, you can create a machine learning model that is well understood and can be easily reproduced by others. At the end of this process you will end up with the following files:
- feature_names.pkl
- preprocess_function.pkl
- model_transform.pkl
- model.pkl
- requirements.txt


