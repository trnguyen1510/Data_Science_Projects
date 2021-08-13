# Part A: Linear Regression - Simple version

Regression is an analytical model that can identify the linear relationships (correlation) of variables. 
Simple or Multiple Linear regression can be used as an effective tool in Machine Learning. 
There is an important difference between classification and regression problems. Fundamentally, classification is about predicting a label and regression is about predicting a quantity. 
The Dependent Variable (DV) is typically a continuous variable.

This project consists of two parts:
- Part 1 -   Create a Simple Linear Regression (SLR), a single predictor variable predictive model using birthweight data provided and discuss findings
- Part 2 -   Create a Multiple Linear Regression (MLR), a multiple predictor variable predictive model using birthweight data provided and discuss findings

## Source of dataset

The data Birthweight_reduced.csv will be used for creating and testing the two models i) Simple Linear Regression, ii) Multiple Linear Regression. This (real) dataset contains information on newborn babies and their parents.  It contains all continuous except for one variable “LowBirthWeight” which is categorical. 
Hence this dataset is most useful for correlation and regression.  
The attribute metadata is available in the below table. Birthweight is the dependent variable.

![image](https://user-images.githubusercontent.com/44355005/129426191-38b3e770-8dbd-46e8-8cc5-41b0fdec7c12.png)

## Research questions

1.	Check if baby birthweight is dependent upon mother’s pre-pregnancy weight
2.	Check if the baby length is dependent upon mother's height

### Steps involved:

Step 1: import all our standard libraries. Also include seaborn

	`Import seaborn as sns`
  
1.	Load the CSV file into a dataframe df
2.	Explore the top 5 rows of this dataframe 
3.	How many rows and columns does it have?#
4.	See all the columns this dataset has

Step 2: Using seaborn visualize the pairplots between 'headcirumference', 'length', 'Birthweight', 'mppwt', 'mheight'
Comment of what kind of relationship do we see from the plots?

Step 3: compute the correlations of all these variables. Then show a heatmap of the correlations.

Step 4: We will now develop two SLR Models to answer to the two research questions: 

1.	Research question# 1, configure the attribute “mppwt” as predictor(independent) variable and “Birthweight” outcome (dependent) variable. 
2.	Research question# 2, configure the attribute “mheight” as predictor(independent) variable and “Length” outcome (dependent) variable.

Step 4: We will repeat the following steps to first check relationship between “mppwt” and “Birthweight” and later between “mheight” and “length” of the baby. 

Step 5: Constructing the training and testing sets for the 2 SLR.

1. Put only the “mppwt” data in X

	`X = df['mppwt'].values.reshape(-1, 1)`
  
Make the y matrix for “Birthweight”.

`y = df['Birthweight'].values`

Check to make sure your X and y matrix are good.

2. import necessary libraries for slit test and train sets. Make the testing set 20%.
3. Create and fit your Linear Regression models.
4. Plot the linear regression line on training set and testing set. Use plt.plot function.
5. Print the intercepts and the coefficients.




