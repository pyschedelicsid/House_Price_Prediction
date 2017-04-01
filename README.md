# House_Price_Prediction

Estimating Housing Prices using supervised machine learning algorithm.

You want to sell your house at the best market price possible. In order to get the best possible deal, you decide to use machine learning. You are going to use various statistical analysis tools to build the best model to predict the value of a given house. Your task is to find the best price your client can sell their house at. The best guess from a model is one that best generalizes the data.

## Choosing the Model

We will use a Decision Tree Regressor with Adaboost to solve this problem. A decision tree is a tree where each node makes a simple decision that contributes to the final output, the leaf node represents the output values and the branches represents the intermediate decisions that were made based on input features.

## Adaboost - Adaptive Boosting

This is a technique that is used to boost the accuracy of the results from another system. This combines the output from different versions of the algorithms called weak learners, using a weighted summation to get the final output. The information that is collected at each stage of the adaboost algorithm is fed back into the system so that the learners at the later stage focus on training examples that are difficult to classify, this increases the accuracy of the sytem. Using Adaboost we fit a regressor on the dataset, we compete the error and fit the regressor on the same dataset again based on error estimate. Think of it as a fine tuning of the regressor until we get the desired accuracy.

## Getting the Dataset

This dataset was taken from the StatLib library which is maintained at Carnegie Mellon University. You can download it from https://archive.ics.uci.edu/ml/datasets/Housing. This contains dataset conatins various paramters that affect the price of the house, our goal is to estimate the relationship between parameter and house prices so that we can use it to estimate the price given unknown parameters. Scikit-learn provides a function to directly load the dataset- "from sklearn import datasets". Each data point has 13 parameters that affect the price of the house, you can access the input data using housing_data.data and corresponding price using housing_data.target.
