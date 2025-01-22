# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Catriona Murphy

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
Needed to change all negative values to zero. The template guided me to do this

### What was the top ranked model that performed?
WeightedEnsemble_L3 was top ranked from the initial run with no features added or tuning of hyperparameters

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
I added additional features by parsing the hour data from the datetime data. The exploratory analysis found that 

### How much better did your model preform after adding additional features and why do you think that is?
After adding the additional hour features the model performed much better. I think it's because the hour of day has more of an influence on whether bikes will be available, and so to have this as a stand alone extra feature enabled the models to perform better.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
It didn't make much of a difference - the new features were definitely more impactful

### If you were given more time with this dataset, where do you think you would spend more time?
I would definitely read up more on all the different hyperparameters available for all of the different models.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
model	hpo1	score
0	initial	default	1.80043
1	add_features	default	0.61219
2	hpo	auto_stack = 'True', cat_hps = {'iterations' : 100, 'depth' : 10}	0.58484


### Create a line plot showing the top model score for the three (or more) training runs during the project.

https://jnp4vhnpfldlgib.studio.us-east-1.sagemaker.aws/jupyterlab/default/files/model_train_score.png?_xsrf=2%7Ca854c8a1%7Cb3e9f383abb0754e74779710aced9554%7C1736778162

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

https://jnp4vhnpfldlgib.studio.us-east-1.sagemaker.aws/jupyterlab/default/files/model_test_score.png?_xsrf=2%7Ca854c8a1%7Cb3e9f383abb0754e74779710aced9554%7C1736778162


## Summary
The importance of exploratory analysis and feature engineering is really highlighted in this project. Autogluon can provide really powerful machine learning models even before hyperparameter tuning - so if someone can master this they can use it to solve real-world problems and predict future outcomes with a high level of confidence.
