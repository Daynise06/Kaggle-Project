# Kaggle-Project
![](UTA-DataScience-Logo.png)

# Metastatic TNBC

* **One Sentence Summary** This repository contains a machine learning pipeline to predict whether a patient received a metastatic cancer diagnosis based on demographic and health-related features.

## Overview

* This section could contain a short paragraph which include the following:
  * **Definition of the tasks / challenge**  Metastatic TNBC is considered one of the most aggressive forms of breast cancer and requires urgent diagnosis and treatment. Delays in identifying and treating this condition can have severe consequences. This project aims to help identify patients who are likely to be diagnosed with metastatic cancer, allowing for more timely care.

  * **Your approach** Formulates this problem as a binary classification task using structured patient-level data. The model predicts whether a patient has received a metastatic cancer diagnosis. We use a gradient boosting classifier (HistGradientBoostingClassifier) that handles missing values natively and performs well on tabular dat
  
  * **Summary of the performance achieved** Validation sample, the model achieved solid classification accuracy and balanced precision/recall.
## Summary of Workdone

Include only the sections that are relevant an appropriate.

### Data

* Data:
  * Type: Tabular CSV file with demographic, environmental, and medical attributes.
  * Size: Approximately 5,000–10,000 patient rows and 80+ features.
  * Instances (Train, Test, Validation Split): 80% training (with stratified class balance), 20% validation.
#### Preprocessing / Clean up

* Describe any manipulations you performed to the data.

#### Data Visualization

Plotted histograms of key features like BMI, age, income, and pollution metrics (e.g., PM25, Ozone) separated by metastatic diagnosis outcome. These revealed potential patterns, such as age and BMI distributions differing across classes.

### Problem Formulation

* Define:
  * Input: Tabular patient data with demographic and environmental features.
  * Output: Binary label (1 = diagnosed with metastatic cancer, 0 = not diagnosed)
  * Models
    * HistGradientBoostingClassifier from scikit-learn.

### Training

* Describe the training:
  * Software: Python, scikit-learn, pandas, seaborn.
  * Hardware: Standard laptop (no GPU required).
  * Training Time: Under 10 seconds.
  * Training Curves: Not applicable
  * Stopping Criterion: Used full training data with stratified validation split.
  * Difficulties: Initial errors with missing values and categorical features were resolved by switching to a model that handles NaNs natively and dropping non-numeric columns.

### Performance Comparison

* Metric: Accuracy, Precision, Recall, F1-score.
* Validation Accuracy: ~80% (exact score varies depending on train/val split).
* Confusion Matrix and Classification Report were used to evaluate class balance.

### Conclusions

* HistGradientBoostingClassifier performed well out-of-the-box and was ideal for messy, real-world health data with missing values. It required minimal preprocessing and delivered strong results without extensive tuning.

### Future Work

* Incorporate categorical features using one-hot encoding.

## How to reproduce results

* In this section, provide instructions at least one of the following:
   * Reproduce your results fully, including training.
   * Apply this package to other data. For example, how to use the model you trained.
   * Use this package to perform their own study.
* Also describe what resources to use for this package, if appropirate. For example, point them to Collab and TPUs.

### Overview of files in repository

* Describe the directory structure, if any.
* List all relavent files and describe their role in the package.
* utils.py	Helper functions for data cleaning
* preprocess.ipynb	Loads raw data and performs cleaning and feature engineering
* visualization.ipynb	Exploratory data analysis and plotting
* model-training.ipynb	Trains the classifier and evaluates on validation set
* submission.ipynb	Applies model to test data and generates submission.csv


* Note that all of these notebooks should contain enough text for someone to understand what is happening.

### Software Setup
* List all of the required packages.
* If not standard, provide or point to instruction for installing the packages.
* Describe how to install your package.

### Data

* Training data: test.csv

### Training

* model = HistGradientBoostingClassifier()




## Citations

* Provide any references.
