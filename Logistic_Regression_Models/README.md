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

### Dataset Exploration

Based on our observation,  there is no missing values occurred in this dataset. 

![image](https://user-images.githubusercontent.com/44355005/134078391-3b3d5590-e21a-4eb6-a11c-c0b3d7311004.png)

The dataset contains object data-type features such as 'Country','Timestamp','Ad Topic Line'. We will drop these features since they are not valuable information for this analysis.  

The distribution of customers' age (in year) range from 20 - 60 years old. Based on the histogram demonstrate the distribution of customers' age below, we can see that the histogram slightly skewed right and the majority customers are around 30 - 35 years old. 

![image](https://user-images.githubusercontent.com/44355005/134078448-ec3ce49d-db82-4b70-bffd-a1c223bfb931.png)

The highest Daily time spent of site is averagely 70-80 minutes per day as seen in the jointplot showing below (KDE distributions of 'Daily Time Spent on Site' vs. 'Age' ).  

![image](https://user-images.githubusercontent.com/44355005/134078476-f7da5fe2-5cab-4b31-8837-dce001114158.png)

We will take a closer look into the 'Clicked on Ad' feature. Result as the following:

![image](https://user-images.githubusercontent.com/44355005/134078495-dc4dbda1-e9f4-4db6-8750-be56a50862de.png)

Customers with the age above 30 years old have tendency of clicking on ads more than younger demographic customers. 

Customers who spent less than average of 200 minutes a day on the internet, they have tendency of clicking on these ads. 

Customers who area income less than $50K. have tendency of clicking on ads. 

And there is no significant different between genders (male and female) for clicking on the ads. 

### Logistic Regression Model
As mentioned in the introduction, we will split the dataset into train set and test set with test size of 0.33 and random state is 1. Target predictive feature is 'Clicked on Ad' and we will use sklearn library to build Logistic Regression model. 

#### Model result interpretation

We plot the confusion matrix and classification report for easier interpretation. 

![image](https://user-images.githubusercontent.com/44355005/134078669-1dea0b04-025c-46a5-9940-3e639a95d338.png)

![image](https://user-images.githubusercontent.com/44355005/134078700-817fedf9-e970-4037-9f21-17f1b52fcba0.png)

The Accuracy of the classifier is 88%. This result shows the accuracy of model performance is pretty good.


Precision is the ability of a classifier not to label an instance postive that is actually negative. Other word, this rate show how often is the precidiction is correct. In this case, we have precision of 83% for not clicked on the ad and 93% for clicked on ad. Both of the precision rates for 0 and 1 have pretty high rate in prediction correctness.


Recall is the ability of a classifier to find all positive instances. For each class it is defined as the ratio of true positives to the sum of true positives and false negatives. In this case the Recall rate for 0 is 94% and 1 is 82%. Both of them were selected with high rate of relevant items to be evaluate.


Precision and Recall rates from both of the 0 and 1 are reverse when we compare both of the metrics altogether (One has better recall and the other one has better precision). However the differences between results aren't much different from each other +/- 10%.


We can take a look on f1 score. F1 score can be interpreted as a weighted average of the precision and recall, where an F1 score reaches its best value at 1 and worst score at 0. The relative contribution of precision and recall to the F1 score are equal. 0 has f1 score of 0.88 and 1 has f1 score as 0.87. The values of f1 score in this case somewhat similar to each other and close to 1.


Overall, Precision and Recall results are close to the accuracy score, and all of the scores are pretty high (but not overfitting), therefore, this model performance is pretty good.


#### How to improve the model

To me the model's performance is good enough, however, if it wasn't, there are couple ways to improve the model. The easiest method is to increase the data size

To boost the recall is to increase the number of samples that you define as predicted positive by lowering the threshold for predicted positive. But this may also increase the number of false positives.



