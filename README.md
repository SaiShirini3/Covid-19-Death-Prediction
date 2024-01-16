# Covid-19-Death-Prediction
-------------------------------------------------------
### Objective
The objective of this project is to predict the next week Death’s due to Covid using the previous data upto till date. This is a regression problem and we are about to do regression models to look into and compare which model is giving better result.

### About Dataset
•	Training Dataset – 129156 rows data is used for training the model
•	Test Dataset - 43505 rows data are used to test the model
•	Train.csv - Contains the details week wise from onset of Covid Jan 2020 to June 2022 
•	Test.csv - Contains the details week wise from onset of Covid Jan 2020 to June 2022

### Methodology
Here I joined train data and test data by concat method and started data preprocessing by replacing the empty or NaN with null values and then separating the output column from the concated data frame and then we used label encoder to convert the location (categorical feature) into numerical feature and then we applied standardization methods to the data frame to get our preprocessed dataframe on which we can make models.


 ### Experiments and results:

The performance of the three methods and in first method we concated the both test and train data and then encoded and then standardized the data. Then Split the dataframe into Train and test with 33 percent as test data and then during Linear regression model we get Rmse (Root Mean Square Error) as 0.71. During Lasso model we get Rmse (Root Mean Square Error) as 0.71.

In second method, during preprocessing of data, we sorted it year wise and then used padding but we had few null values we dropped those rows then separating the output column form the data frame and then we used label encoder to convert the location (categorical) in to numerical and then applied standardization to the data set. During Linear Regression and Lasso Regression we got 0.60 as Rmse in both models. So we can conclude this might not be the best method, there can be more better methods.

In AutoMl method, LGBM Regressor is found to be best method during time budget of 10 minutes. It took 9.6 mins to find out these with each of it’s respective Rmse scores.  

Then we used Feature selection Method to find which feature is contributing more towards the output of regressor. We find here that there are 3,4 features which are contributing more as compared to others. Using correlation heatmap below also we can confirm those.

During the prediction phase, given test data is used to predict the Next Week’s Death Numbers   by using Different Regression Models and the performance of those models with rmse scores is found out, be it for Linear or Lasso or other methods.
