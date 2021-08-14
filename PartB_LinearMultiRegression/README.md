# Linear Multiple Regression

Continue from the previous project with Brithweight_reduced.csv dataset

See part A for dataset description and previous findings using Simple Regression

Link to Part A Simple Regression : [Part A](https://github.com/trnguyen1510/Data_Science_Projects/tree/master/PartA_Linear_regression_Simple)

Research question: 

In this part, we like to investigate which other variables are significant in predicting the birthweight? Also, check how close your prediction is to actual values?

Step 1: Some data cleanup may be necessary. Let us go ahead and drop the features “id”, “LowBirthWeight”, and “lowbwt”.

Verify that these columns are now gone. 

Step 2: Setup X matrix with all the independent variables left and target of prediction is “Birthweight” which goes to y matrix.

Step 3: Split data set into training and testing with a split ratio of 75:25. 

Step 4: After importing the necessary Linear Regression libraries, create and fit model. 

Step 5: Print intercept value.

Step 6: Print all coefficients.

Step 7: Make predictions. Remember provide X_test data now. 

Step 8: Check prediction value with actual real values. 

Do a scatter plot to see how they align. 

Step 9: from sklearn import metrics

Show the values MAE, MSE, RMSE. 

### Result Interpretation

- The intercept has a negative value -12.34. The expected values on Birthweight is -12.339 if all of the independent variables are 0.

- In the coefficient result, the most stand out value is -0.803 from Mother over 35 variable. This indicates that if Mother over 35 there will be a negative impact or decrease in Weight of baby.

- Based on the result of prediction with actual real values above, we can see the prediction and the actual values not too much different from each other.

- Mean absolute error (MAE) value is 0.85 implies that, on average, the predicting distance from the true value is 0.85, this value is closer to 0 meaning the model is a good predictor of the outputs.

- Root Mean Square Error (RMSE) is measure of how spread out the residuals are, which the result is 1.075

- The mean squared error ( MSE) shows how close a regression line is to set of points. It does this by taking the distances from the points to the regression line and squaring them. MSE has the value of 1.156

- The MAE, RMSE, and MSE results indicate that the model above is a moderate prediction model.
