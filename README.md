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
In my methodology, I commenced by concatenating the training and testing datasets using the concat method. Subsequently, I initiated the data preprocessing phase by addressing empty or NaN values and replacing them with null values. Following this, I proceeded to isolate the output column from the concatenated data frame. To handle the categorical nature of the 'location' feature, I employed label encoding, thereby converting it into a numerical format.

Once the categorical encoding was completed, I applied standardization techniques to the entire data frame. This involved scaling the features to ensure uniformity and enhance the performance of subsequent machine learning models. The resulting preprocessed data frame serves as a robust foundation for building and training models.


 ### Experiments and results:

In the first approach, the data preprocessing involved concatenating the test and train datasets, followed by encoding and standardizing the combined data. Subsequently, the dataframe was split into training and test sets with 33 percent allocated to the test data. The Linear Regression model produced a Root Mean Square Error (RMSE) of 0.71, and the Lasso model also yielded an RMSE of 0.71.

The second methodology entailed sorting the data chronologically and employing padding. Any rows with null values were removed, and the output column was separated from the dataframe. Subsequently, label encoding was applied to convert the categorical location variable into numerical format, followed by standardization of the dataset. Both Linear Regression and Lasso Regression models were executed, resulting in an identical RMSE of 0.60. However, it was inferred that this method may not be optimal, suggesting the potential existence of more effective approaches.

The third method, AutoML, identified the LGBM Regressor as the most effective model within a time budget of 10 minutes, achieving its respective RMSE scores in 9.6 minutes.

Feature selection was then employed to identify the key contributors to the regressor's output. The analysis revealed that a subset of 3 to 4 features significantly influenced the output, a conclusion supported by a correlation heatmap.

During the prediction phase, the test data was utilized to forecast the upcoming week's death numbers using various regression models. The performance of these models, as measured by their RMSE scores, was carefully evaluated, encompassing Linear Regression, Lasso Regression, and other methodologies.
