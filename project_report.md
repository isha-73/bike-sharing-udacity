# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE
Isha Bule

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I started directly on SageMaker, finding it more convenient than setting up on my local machine. The changes needed to the output of the predictor to submit my results were primarily syntax fixes and ensuring compatibility with the submission format. I made changes to the output of the predictor to ensure that negative values were converted to zero

### What was the top ranked model that performed?
The best performing model, based on the fit summary , is the "WeightedEnsemble_L3" model, which achieved a score_val of -53.114142 with a root_mean_squared_error evaluation metric.

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
|initial|600|best_quality|none|1.80472|
|add_features|600|best_quality|regression|0.62593|
|hpo|600|best_quality|tabular autogluon|0.4814|


### Create a line plot showing the top model score for the three (or more) training runs during the project.


![model_train_score.png](/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](/model_test_score.png)

## Summary
In the process of developing a predictive model for bike demand using Amazon SageMaker, the initial approach began with basic model training and syntax adjustments to align the predictor's output with the required submission format. The most effective model identified from the initial models was the "WeightedEnsemble_L3," achieving a root_mean_squared_error of -53.114142. During exploratory data analysis, significant variables such as weather conditions, seasonal changes, and detailed datetime splits (year, month, day, and hour) were found to heavily influence bike demand. Incorporating these features resulted in an impressive 65.92% performance increase, highlighting their predictive importance. Further enhancements through hyperparameter tuning led to an additional improvement, pushing model performance up by 73.25%. If more time were allotted, the focus would shift to even finer hyperparameter adjustments and exploring advanced modeling techniques to potentially elevate performance further. This comprehensive approach underscores the critical interplay between feature engineering and hyperparameter tuning in optimizing predictive models.