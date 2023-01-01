# Creating a Machine Learning Model
This document outlines the steps for creating a prediction function used for recommendations. The prediction function implements LightFM that learns embedding representations of the users and items in such a way that it encodes user preferences over items


## Define the Problem
Before you start building a model, it's important to understand the problem you are trying to solve. This includes identifying the goals of the model, the target audience, and any constraints or limitations that may impact the model's performance.

## Collect the required Data
The next step is to gather the data you will use to train and test your model. You will need to connect to Intempt via APIs to access data, and extract the required collections.

Once you know which collection from Intempt is requred. You will need to save the collections as a list for example: `feature_names = ['customer','transaction','article']` to a pickle file

## Create the user and item embeddings
The user and item embeddings are estimated for every feature, and these features are then added together to be the final representations for users and items. Store this mapping as a pickle file

## Create the Light FM Model
In this notebook, the LightFM model will be using the weighted Approximate-Rank Pairwise (WARP) as the loss.

In general, it maximises the rank of positive examples by repeatedly sampling negative examples until a rank violation has been located. This approach is recommended when only positive interactions are present.

When you are done with the model save the model as pickle file

## Create the prediction function
This function uses the collected data, mappings and LightFM Model to generate recommendations.

When you are done with the logic of the function save the function as a pickle file

## Conclusion

By following these steps and documenting your work, you can create a machine learning model that is well understood and can be easily reproduced by others. At the end of this process you will end up with the following files:
- feature_names.pkl
- light_fm.pkl
- mapping.pkl
- prediction.pkl
- requirements.txt

