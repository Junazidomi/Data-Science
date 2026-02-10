# Lifestyle and Health Risk Prediction

## Business Understanding
### Background

### Purpose

The purpose of this project is to build a machine learning model capable of predicting a person's health condition to support further decision making. In addition, this project also aims to assist the community and health workers in predicting health conditions based on lifestyle.

## Data Understanding

This synthetic health dataset simulates real-world lifestyle and wellness data for individuals. It is designed to help data scientists, machine learning engineers and students build and test health risk prediction models safely - without using sensitive medical data. The dataset includes such as age, weight, height, exercise habits, sleep hours, sugar intake, smoking, alcohol consumption, marital status, and profession, aling with a synthetic health_risk label generated using a heuristic rule-based algorithm that mimics realistic risk behaviour patterns. Dataset: [Lifestyle and Health Dataset](https://www.kaggle.com/datasets/miadul/lifestyle-and-health-risk-prediction)

|        Feature        |       Data Type       |        Descriptions                              |
|-----------------------|-----------------------|--------------------------------------------------|
|        age            |          Int          | Age of the person (years)                        |
|       weight          |          Int          | Body weight in kilograms                         |
|       height          |          Int          | Height in centimeters                            |
|      exercise         |         String        |Exercise frequency level(none, low, medium, high) |
|       sleep           |         Float         |Average hours of sleep per night                  |
|      sugar_intake     |         String        | Level of sugar consumption (low, medium, high)   |
|      smoking          |         String        | Smoking habit (yes,no)                           |
|      alcohol          |         String        | Alcohol consumption habit (yes,no)               |
|      married          |         String        | Marital Status (yes, no)                         |
|     profession        |         String        |Type of work or profession                        |
|       bmi             |         Float         | Body Mass Index calculated as weight / (height²) |
|    health_risk        |         String        | Health risk (low, high)                          |

Key Findings:

### EDA

The following are some of the visualizations such:

1. Visualization of Smoking Status
   
   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Smoking%20Status.png" width="370">

   Insight:
   
3. Visualization of Married Status

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Married%20Status.png" width="370">

   Insight:
   
4. Visualization of Risk Status

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Risk%20Status.png" width="370">

   Insight:
   
   
8. Visualization of Sugar Level

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Sugar%20Level.png"  width="370">

   Insight:

10. Visualization of Alcohol Status

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Alcohol.png" width="370">

    Insight:
    
12. Visualization of Profession

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Profession.png" width="370">

    Insight:
    
13. Visualization of Exercise Level

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Exercise.png" width="370">

    Insight:

15. Visualization of Exercise Level by Risk Status

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Exercise%20vs%20risk.png" width="370">

    Insight:
    
17. Visualization of Exercise Level by Sugar Level

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Exercise%20vs%20risk.png" width="370">

    Insight:
    
17. Visualization of Numeric Feature by Risk Status

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/numerik%20vs%20risk.png" width="370">

    Insight:
    
19. Visualization of Risk Status vs Alcohol Status

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/risk%20vs%20alcoho%3B.png" width="370">
    
21. Visualization of Risk Status vs Smoking Status

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/risk%20vs%20smoking.png" width="370">

    Insight:
    
23. Visualization of Heatmap

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/heatmap.png" width="370">

    Insight:
    
## Data Preparation

The data preparation is as follows:

1. Encoding

   Encoding is the process of converting categorical data into a numerical format so that it can be processed by machine learning models. The goal is to make it easier for models to capture patterns or relationships in the data by representing categories as sequential numbers or binary numbers.
   
2. Split the Training Data and Test Data

 In this process, the target variable is handled. When the class distribution in the target variable is unbalanced, the model tends to predict the majority class, resulting in unstable performance. Therefore, data balancing is performed using the oversampling method, which increases the amount of data in the minority class so that the class distribution becomes balanced.
   
3. Balance Target Data

   In this process, the target variable is handled. When the class distribution in the target variable is unbalanced, the model tends to predict the majority class, resulting in unstable performance. Therefore, data balancing is performed using the oversampling method, which increases the amount of data in the minority class so that the class distribution becomes balanced.
   
## Modelling

In this project, several algorithms for classification evaluation purpose such as:

1. Logistic Regression

   Logistic Regression is machine learning algorithm that estimates the probability of an event occuring, such as choosing or not choosing, based on a given dataset of independent variables
   
2. Random Forest

   An ensemble learning-based machine learning algorithm that combines multiple decision trees to produce more accurate and stable predictions than a single tree, working by taking random samples from data and features, then combining the results.
   
4. Decision Tree
   
6. SVM
7. Gradient Boosting
8. XGboost Classifier

## Evaluation

The following is an evaluation of each algorithms used:

|      Algorithm       |    Accuracy    |    Precision    |     Recall   |     F1 Score   |
|----------------------|----------------|-----------------|--------------|----------------|
| Logistic Regression  |      0.866	    |      0.936170	  |    0.870056  |    0.901903    |
| Random Forest        |      0.979	    |      0.991416	  |    0.978814  |    0.985075    |
| Decision Tree        |      0.980	    |      0.984507	  |    0.987288  |	  0.985896    |
| SVM                  |      0.756	    |      0.871795   |	   0.768362	 |    0.816817    |
| Gradient Boosting    |      0.978	    |      0.995665	  |    0.973164  |	  0.984286    |
| XGB Classifier       |      0.977	    |      0.994228	  |    0.973164	 |    0.983583    |


