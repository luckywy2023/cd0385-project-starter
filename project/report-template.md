# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
Kaggle doesn't allow negative values. Hence I need to transform the negative values into 0 before submitting the results. Among all the predicitions I did including initial training, training after EDA and hyper parameter tuning, only the result of hyper parameter tuning contains negative values and needs me to do the transformation.

### What was the top ranked model that performed?
WeightedEnsemble_L3. It is a weighted ensemble that aggregates the predictions of many other models. Because a single model may not make the perfect prediction for a given data set. With combining multiple models, we have the chance to boost the overral accuracy.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
- From EDA, I was able to find the distribution of the features and the rough distribution of the target (count) and how it is related with the features.
- I use the pandas.to_datetime() method and datetime.dt.year method to create additional features.

### How much better did your model preform after adding additional features and why do you think that is?
The score is improved from 1.80242 to 0.54447 after adding additional features. IMO, the month, day, hour are 3 features which have impact on the bike sharing demand. The added additional features are able to give these information and be trained and involved in the new model which gives us a better prediction on the test data. 

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
TODO: Add your explanation

### If you were given more time with this dataset, where do you think you would spend more time?
TODO: Add your explanation

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|?|?|?|?|
|add_features|?|?|?|?|
|hpo|?|?|?|?|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
TODO: Add your explanation
