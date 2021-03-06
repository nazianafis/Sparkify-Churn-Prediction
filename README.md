# Sparkify-Churn-Prediction
Customer churn can be tricky for businesses. In this project, I develop a machine learning model to help predict churn.

Check out my [blog post](https://nazianafis.medium.com/predicting-customer-churn-for-music-streaming-service-sparkify-3e281a93273) for a write-up on the findings!

## Table of Contents

1. [Overview](#overview)
2. [File Description](description)
3. [Getting Started](#getting-started)
    1. [Dependencies](#dependencies)
    2. [Installation](#installation)
4. [Achievements](#achievements)
    1. [What has been achieved?](#achieved)
    2. [What more can be achieved?](#moreachieve)
6. [Conclusion](#reflect) 
7. [Author](#author)

## Overview <a name="overview"></a>
Business need to retain their customers in order to thrive. Churn (the process of losing customers) is therefore an important business problem.

This project makes use of a tiny subset (~128MB) of the full dataset (~12GB), provided by Udacity, to practice machine learning. The goal is to assist a fictitious music streaming service 'Sparkify' in retaining its customers by predicting the tendency to churn even before they actually do it.

![header](https://github.com/nazianafis/Sparkify-Churn-Prediction/blob/main/img/ss1.png)

## Getting Started <a name="getting-started"></a>

### File Description <a name="description"></a>
    Disaster-Response-Pipeline
        ├── app                   
        │   ├── Sparkify-1.ipynb                  # Exploratory data analysis, data preprocessing, and development of machine learning model locally.
        ├── data
        |   ├── mini_sparkify_event_data.zip      # Zipped 128 MB subset of the 12 GB main dataset
        ├── img     
        │   ├── slogo.png
        │   ├── slogo(2).png
        |   ├── ss1.png
        |   └── ss2.png
        └── README.md
    

### Dependencies <a name="dependencies"></a>
*    Python 3.5+
*    Libraries: PySpark, Pandas, Seaborn
*    Data Visualization: Matplotlib

### Installation <a name="installation"></a>

Datasets: The dataset is provided by Udacity. It can also be obtained from [here](https://github.com/nazianafis/Sparkify-Churn-Prediction/blob/main/data/mini_sparkify_event_data.zip).

#### To run the project:

Clone the repository:
```
  $  git clone https://github.com/nazianafis/Sparkify-Churn-Prediction.git
```
Run the 'spark' ipython notebook that is in 'app' folder:
```
  $ python3 spark.ipynb
```

#### Achievements <a name="achievements"></a>

### What has been achieved? <a name="achieved"></a>

1. Data loading
    1. Load the dataset
    2. Check for missing values
2. Exploratory data analysis
    1. Overview of numerical columns
    2. Overview of non-numerical columns
    3. Define churn
    4. Explore in terms of churn vs data
3. Feature Engineering
    1. Create features on per user basis
    2. Check multicollinearity
    3. Feature transformation
    4. Compile feature engineering code for future
4. Modeling
    1. Train - Test split
    2. Choose evaluation metrics
    3. Create functions to build, train, and evaluate model
    4. Initial model evaluation with:
        1. Naive predictor
        2. Logistic regression
        3. Random forest
    5. Hyperparameter tuning

![performance](https://github.com/nazianafis/Sparkify-Churn-Prediction/blob/main/img/ss3.png)

### What more can be achieved? <a name="moreachieve"></a>

The machine learning task can be scaled up on the large dataset (~12GB) on a cloud service such as Amazon AWS.

## Conclusion <a name="reflect"></a>

* The machine learning model is able to predict churn reasonably well (with f1 score of 0.74).
    * Model performance can further be improved by tuning the hyperparameters or incorporating additional features.
* The most important features in churn prediction are the time since user’s registration, the amount of advertisements that user has encountered and the number of thumbs up/thumbs down the user has given.
    * This information can be utilized by Sparkify to chart out a plan as to what actions to take. Reducing the amount of advertisements could be one. Another could be to figure out why relatively newer customers are churning more.

## Author <a name="author"></a>
* [Nazia N.](https://github.com/nazianafis)
