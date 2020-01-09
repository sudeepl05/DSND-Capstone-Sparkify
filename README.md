# Sparkify-Project Readme
## Data Science Capstone - Churn Prediction at Sparkify
## Project Definition
### Overview
This project is part of my Data Science Nano-degree at Udacity. In this final project, i will attempt to create a machine learning model, which will be able to predict when users at Sparkify are about to churn.

### Blog
I published a post on Medium to go through the Analysis. Please find the link here
https://medium.com/@sudeeplaha/predict-user-churn-using-pyspark-sparkify-e18d28cce5c7

### Problem
The high intensity of this project is because of the large amount of data, all of our data wrangling and model creating has to be done using Apache Spark. This adds another level of abstraction on top of the already well-established process, but it does enable us to work with bigger data than we would otherwise be able to.

### Methodology
1. ETL
2. Define customer churn and EDA
3. Feature engineering
4. Modeling
5. Evaluation
6. Feature Import analysis

### Packages
PySpark, Pandas, Seaborn, Matplotlot.pylpot

### Models:
Logistic Regression, Gradient Boosted Trees, Support Vector Machines, Random Forest

### Expected Results
At the end of this project, a model for churn prediction should have been created and evaluated. The model should have been trained and tested on a subset of the 12GB of data, and the final testing should happen on completely separate validation set. An running time and F1-Score will be used to evaluate the performance and feasibility of the model.

### Actual Results

At the end of this project, two main iterations on a churn-prediction model were implemented and evaluated. The first model used a simple pivot of the event that seemed to contain the most relevant difference between churning and non-churning users.

- Logistic Regression - 73.2%
- Random Forest - 71.6%

### Improvements

To achieve the optimal user experience, using more capable hardware and moving the text extraction process from the cloud to the device would be essential. This would reduce the processing time and give access to the outputs of all of the modules of the text extraction pipeline, which would, in turn, enable the following features:

- User-guided reading (e.g. read big text first, or read the text the user is pointing at)
- Better support for languages other than English
- Output filtering (e.g. ignore text smaller than some adjustable threshold)
- Passive text detection (auditory cue on text detection, perhaps with additional information encoded in the tone and volume)

The user experience could also be improved significantly by using MXNet, which is a deep learning library that is better optimized for mobile devices than TensorFlow. The speedup wouldn’t be enough for running text extraction on the device, but it would reduce the classification delay significantly.

### References
For this project, the course material at Udacity has been used for reference. On top of that, the official pySpark documentation has also been used ( https://spark.apache.org/docs/latest/api/python/index.html )
