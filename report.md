# Report: Predict Bike Sharing Demand with AutoGluon Solution
Jyothiraditya Mugireddy

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
When I submitted the dataset's predictions, I saw that there are some negative values for the RMSE score. And because the negative values must be adjusted to zero, we set them to zero. In addition, we must change the data type of datetime from object to datetime.

### What was the top ranked model that performed?
The final model i.e K-nearest neighbour bag L1, that I trained by adjusting hyperparameters is the one that produced a better rmse score.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
Obtaining information about the data and its data type, converting the data type of the columns based on the requirements and understanding, and deleting the factors that did not affect the prediction of the output all contributed to improve the model's performance.

Upon Exploratory Data Analysis, I inferred the following:

The features: Season and Weather are categorical.
The features: holiday and working day are binary values.
Datetime is a datetime object, and it is transformed to 3 different features - day, month, year, hour, weekday.

### How much better did your model preform after adding additional features and why do you think that is?
The model performed substantially better when the additional characteristics were added. The RMSE score fell from 1.7945 to 1.33318.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
Model performed slightly better after hyper parameter tuning. RMSE score reduced from 1.33318 to 1.30572.

### If you were given more time with this dataset, where do you think you would spend more time?
I could spend some time more on EDA and see if I could derive new features to improve the model's prediction.
I would also explore on different feature engineering techniques such as feature scaling,normalization and removing outliers.
Perform hyperparameter tuning on best chosen model.


### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.

|model|names|time|presets|score|
|--|--|--|--|--|
|initial|first_model|400|best_quality|1.79450|
|add_features|second_model|600s|best_quality|1.33318|
|hpo|third_model|500s|best_quality|1.30572|

### Create a line plot showing the top model score for the three (or more) training runs during the project.


![model_train_score.png](https://github.com/AdityaMugireddy/Predict-Bike-Sharing-Demand-with-AutoGluon/blob/main/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

![model_test_score.png](https://github.com/AdityaMugireddy/Predict-Bike-Sharing-Demand-with-AutoGluon/blob/main/model_train_score.png)

## Summary
This project required me to solve a regression problem in order to forecast bike sharing demand based on previous data. AutoGluon was utilised as the framework. The original model was generated with the default predictor, and it performs poorly. Exploratory Data Analysis was used to assign the correct data types to the features, and feature engineering was used to construct new features based on the date and time. The model's performance has significantly improved as a result of the added features. Hyper parameter tuning is also used to boost performance, but it has yet to produce superior results. The final submission was made to Kaggle, where it received a kaggle score of 1.30572. The model with new characteristics outperforms the previous model.
