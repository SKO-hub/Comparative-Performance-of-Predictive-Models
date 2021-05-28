# Comparative-Performance-of-Predictive-Models

The notebook contains an implementation of four predictive models; Linear Regression, Ridge regression, Random Forests for regression and Gradient Tree Boosting for regression. The models are implemented individually and their performance is obtained. The models are then implemented in combination with each other (a binary classification followed by a regression).

**IMPLEMENTATION NOTES**

1. The Database used was collected and provided as a csv file. no work has been done within the project to obtain the data from an open data source.
2. Where implementation of techniques was computationally impractical, alternative work was done to complete the predictive models. This is seen in the Random Forests and Gradient Tree models for regression where obtaining the best hyperparameters took significant amounts of time and so implementations without gradient boosting were used.

**PERFORMANCE OF MODELS**
LINEAR REGRESSION VS RIDGE REGRESSION: RIDGE REGRESSION PERFORMED BETTER THAN LINEAR REGRESSION

The ridge regression model provided predictions with a MSE of as low as 278.72 whereas the lowest square error obtained from the linear regression model was 282.05. Ridge regression models gives estimates that minimise the sum of the square error by adding a penalty term. This reduces overfitting which increases it's ability to generalize outside of the original training set. This results in a better performance when the model is presented with unseen test data. In addition, ridge regression tends to perform better with large sets of data

RANDOM FORESTS VS GRADIENT TREE BOOSTING: GRADIENT TREE BOOSTING PERFORMED BETTER THAN RANDOM FORESTS

The Random Forests regression model was able to produce MSE as low as 328.23 whereas with Gradient Tree Boosting the error was as low as 279.477. Gradient Tree Boosting is known to perform better than Random Forest when the parameters have been well tuned. Another explanation is that when dealing with data that contains alot of categorical variables, random forests are biased in favor of the attributes with more level which reduces generalization resulting in less accurate predictions on an unseen test set.

COMBINATION OF MODELS PERFORMED BETTER THAN SINGLE MODELS

In combining two prediction models in various configurations, the MSE was lower than any single model with the highest MSE being 234.61 for a Gradient Tree Boosting and Linear Regression Model and the lowest low being the Random Forest and Ridge Regression Model. One reason for this would be that Gradient Tree Boosting and Random Forests work on the basis of classification. By converting the first half of the prediction into a binary problem, the task was better suited for these models. They had to determine a class rather than an actual value, which they are better suited to do. This resulted in much higher accuracy.

STANDARDIZED VS UNSTANDARDIZED DATA

In the case of this dataset, standardizing the data did not have a great effect on the performance of the the prediction models. The biggest difference in MSE between standardized and unstandardized data was approxiamtely 32.0 in Gradient Boosting and the smallest was 0.07 in Ridge Regression. This may have been because the original datapoints did not have large variances within the different numerical features. The range was between the highest and lowest values in a feature set was negligible and so standardization did not have much of an effect on the overall result
