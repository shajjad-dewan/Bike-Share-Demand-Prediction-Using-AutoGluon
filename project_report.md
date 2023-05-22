# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### SHAJJAD DEWAN

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
TODO: The predicted value contains some negative values. As the value will not be 0 so kaggle rejected the submission. Thus I have found out how many prediction values were less than 0. Then those values were set to 0.

### What was the top ranked model that performed?
TODO: WeightedEnsemble_L3

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
TODO: It found that some of the features were initially categorical which where converted to int. So again converted them back to category so that autogluon can know this is a categorical feature.

### How much better did your model preform after adding additional features and why do you think that is?
TODO: The model performed dramatically well by reducing the score almost 0.68 when features were added. Because more feature can train the data more well and accurately.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
TODO: The hyperparameter helped the model to give even more good result by reducing the score 0.10.

### If you were given more time with this dataset, where do you think you would spend more time?
TODO: If more time were given I would analyse the dataset further and try to extract some other better features. Also as some of the features are categorical I would spend some time to train those feature separately using the categorical hyperparameter tuning of Autogluon.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|'time_limit=600, presets=best_quality, eval_metric=root_mean_squared_error'|No Extra Features Added|No Model Tuned|2.37331|
|add_features|'time_limit=600, presets=best_quality, eval_metric=root_mean_squared_error'|3 Features (hour,month,year) added|No Model Tuned|1.69983|
|hpo|time_limit=600, presets=best_quality, eval_metric=root_mean_squared_error|3 Features (hour,month,year) added|NN,RF,GBM,CAT models are tuned|1.59261|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](nd009t-c1-intro-to-ml-project-starter/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](nd009t-c1-intro-to-ml-project-starter/model_test_score.png)

## Summary
TODO: This project is done to predict bike sharing demand using AutoGluon. The data is extracted from Kaggle. The overal project is evaluated by submitting the prediction in kaggle competition regarding this dataset for three times. The first time by training the data as it is, the second time by creating some new features and changing some datatypes, the third time by tuning some hyperparameters of the model along with the previous change. Result shows that the last submission has performed better than other previous submission. This indicates that spending time on EDA and hyperparameter tuning gives more good result.
