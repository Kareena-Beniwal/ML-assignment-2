Decision Tree and Random Forest learn the data perfectly during training and also perform well on new data (test set). 
Random Forest slightly outperforms than the Decision Tree, due to its ensemble approach.
Linear regression predicts the target variable reasonably well, with around 74.85% accuracy on the test set. It's not perfect but explains about 89.38% of the variance in the target variable.

So the classification models are strong at categorizing activities, while the regression model is decent at predicting numerical values but might not be as accurate as the classifiers.

Using linear regression for classification is not justified because it is used for predicting continuous values, not discrete class labels. Linear regression assumes a linear relationship between dependent and independent variables, which may not hold true for classification tasks. Classification requires discrete predictions, which linear regression does not naturally provide. It is better to use algorithms like decision trees or random forest designed specifically for classification.
