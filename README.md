# Sparkify-Project Readme
## Data Science Capstone - Churn Prediction at Sparkify
## Project Definition
### Overview
This project is part of my Data Science Nano-degree at Udacity. In this final project, i will attempt to create a machine learning model, which will be able to predict when users at Sparkify are about to churn.

### Problem
The high intensity of this project is because of the large amount of data, all of our data wrangling and model creating has to be done using Apache Spark. This adds another level of abstraction on top of the already well-established process, but it does enable us to work with bigger data than we would otherwise be able to.

### Expected Results
At the end of this project, a model for churn prediction should have been created and evaluated. The model should have been trained and tested on a subset of the 12GB of data, and the final testing should happen on completely separate validation set. An accuracy, F1-Score confusion matrix will be used to evaluate the performance and feasibility of the model.

### Actual Results
At the end of this project, two main iterations on a churn-prediction model were implemented and evaluated. The first model used a simple pivot of the event that seemed to contain the most relevant difference between churning and non-churning users.

Three models were trained with this data, given the following F1 Values:

Gradient Boosted Trees - 68.9%

Random Forest - 68.4%

SVM - 68.4%

While the values look promising, inspection of the confusion matrices revealed that SVM and Random Forest classified all users as non-churning, but because of the relative low number of churned users, the F1 score was still fairly high.

The best performing model for the first iteration was Gradient Boosted Trees, which managed to predict 17 churners correctly.

For the second iteration, two new features were introduced. Number of sessions and days from first to last recorded event.

Using these features, the Gradient Boosted Trees algorithm was once again trained.

The results were much better than the initial attempt. With a F1-score of 89.1% for validation data, and 294 correctly identified churners, the second iteration of the model is a great first model which could be fine-tuned and improved even more.

## Overview of Files
### Data Files

README.md - This readme

Sparkify.html/ipynb - notebook used for POC in Udacity Workspace

mini_sparkify_event_data.json - starting data file containing the streaming music provider's user logs

## Improvement
To achieve the optimal user experience, using more capable hardware and moving the text extraction process from the cloud to the device would be essential. This would reduce the processing time and give access to the outputs of all of the modules of the text extraction pipeline, which would, in turn, enable the following features:

❖ User-guided reading (e.g. read big text first, or read the text the user is pointing at)

❖ Better support for languages other than English

❖ Output filtering (e.g. ignore text smaller than some adjustable threshold)

❖ Passive text detection (auditory cue on text detection, perhaps with additional information encoded in the tone and volume)

The user experience could also be improved significantly by using MXNet, which is a deep learning library that is better optimized for mobile devices than TensorFlow. The speedup wouldn’t be enough for running text extraction on the device, but it would reduce the classification delay significantly.

### References
For this project, the course material at Udacity has been used for reference. On top of that, the official pySpark documentation has also been used ( https://spark.apache.org/docs/latest/api/python/index.html )
