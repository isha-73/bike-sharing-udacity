# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE
Isha Bule

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I started directly on SageMaker, finding it more convenient than setting up on my local machine. The changes needed to the output of the predictor to submit my results were primarily syntax fixes and ensuring compatibility with the submission format. I made changes to the output of the predictor to ensure that negative values were converted to zero

### What was the top ranked model that performed?
The top-ranked model that performed the best among the ones I tried was the one with after trying different hyperparameters. This model significantly outperformed the others in terms of prediction accuracy.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
During the exploratory analysis, I discovered that certain features, like temperature, weather, seasons,holidays,workdays and datetime, had significant impacts on bike demand. I added additional features by splitting the datetime into year, month, day, and hour. 

### How much better did your model preform after adding additional features and why do you think that is?
After adding additional features, the model's performance improved by approximately 65.92%. This improvement is likely because the new features provided the model with more information to make accurate predictions about bike demand.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
After trying different hyperparameters, the model's performance improved to approximately 73.25%. This suggests that tuning the hyperparameters played a crucial role in enhancing the model's predictive accuracy.

### If you were given more time with this dataset, where do you think you would spend more time?
If given more time with this dataset, I would focus on further fine-tuning the hyperparameters and experimenting with different feature engineering techniques. Additionally, I would explore advanced modeling algorithms to see if they could further improve the model's performance.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|600|best_quality|none|1.80531|
|add_features|600|best_quality|regression|0.61647|
|hpo|600|best_quality|tabular autogluon|0.48355|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
TODO: Add your explanation
