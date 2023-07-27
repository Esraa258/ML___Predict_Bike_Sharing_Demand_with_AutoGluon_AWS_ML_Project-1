# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I need to fix some syntax errors and I have some problems starting the project on my local environment so I choose to do everything in sagemaker studio. 
### What was the top ranked model that performed?
The top ranked model was acheived by completing the second run, the top ranked score is 0.68686
## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
the datetime need to be split into year, month, day, and hour, and for the season I assume that I see the 4 seasons in the distribution and the weather is the same, has 3 categories of input, holidays and workdays are binary fields, and humidity and windspeed are left and right skewed.
### How much better did your model preform after adding additional features and why do you think that is?
the model performed better than the initial one due to splitting the datetime into year, month, day, hour.
## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
the model performed better than the initial one but worse than the improvement with the features.
### If you were given more time with this dataset, where do you think you would spend more time?
some one-hot encoding
### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|score|"initial"|1.78873
"add_features"|0.68686"hpo"|0.68978

pd.DataFrame({
"model": [initial, add_features, hpo (top-hpo-model: hpo2)],
"hpo1": [prescribed_values, prescribed_values, Tree-Based Models: (GBM, XT, XGB & RF)],
"hpo2": [prescribed_values, prescribed_values, KNN],
"hpo3": ["presets:'high quality'(auto_stack=True)", "presets:'high quality'(auto_stack=True)", "presets:'optimize_for_deployment"],
"score": [1.78873, 0.68686, 0.68978]
})

### Create a line plot showing the top model score for the three (or more) training runs during the project.
img/model_train_score.png

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.
img/model_test_score.png

![model_test_score.png](img/model_test_score.png)

## Summary
it so important to work with features to gain great insights from the exporatory data analysis.
