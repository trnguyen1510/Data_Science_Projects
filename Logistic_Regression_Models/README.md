# Logistic Regression Models using Advertising Dataset

In this project we will be working with an advertising data set (“advertising.csv”), indicating whether or not a particular internet user clicked on an Advertisement. 
We will try to create a model that will predict whether or not they will click on an ad based off the features of that user.

 This dataset contains the following features: 
 

- 'Daily Time Spent on Site': consumer time on site in minutes
- 'Age': customer age in years
- 'Area Income': Avg. Income of geographical area of consumer
- 'Daily Internet Usage': Avg. minutes a day consumer is on the internet
- 'Ad Topic Line': Headline of the advertisement
- 'City': City of consumer
- 'Male': Whether or not consumer was male
- 'Country': Country of consumer
- 'Timestamp': Time at which consumer clicked on Ad or closed window
- 'Clicked on Ad': 0 or 1 indicated clicking on Ad

## Steps involved: 

Step 1: Import all the necessary libraries

Step 2: Get the data and load it into a data frame called ad_data

Step 3: Write code to check basic information about the data including number of rows, columns and get a statistical summary of the features.

Step 4: We will conduct some visual exploratory data analysis using seaborn.

- Set the style to ‘whitegrid’
- Create a histogram of the ‘Age’
- Create a jointplot showing the kde distributions of ‘Daily Time Spent on Site’ vs ‘Age’.
- Create a pairplot with the hue defined by the ‘Clicked on Ad’ column feature

Step 5: Create test, train and split data sets. Make sure that the target predictive feature is ‘Clicked on Ad’. For test size choose 0.33 this time.

Step 6: Import the necessary logistic regression libraries from sklearn. Build the logistic model. 

Step 7: Make the predictions using your model on the X_test data set.

Step 8: How good is the classification? Perhaps we can show accuracy of our model, print the confusion matrix and also the classification report.

## Result Interpretation
