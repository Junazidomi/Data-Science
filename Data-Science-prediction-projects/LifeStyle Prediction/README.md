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

- The dataset consists of 12 columns and 5,000 rows, with 5 numeric columns and 7 categorical columns, and Health Risk as the main variable (target).
- After identifying duplicate data, no duplicate data was found in the dataset.
- After identifying missing values, no missing data was found in the dataset.
- After identifying outliers in the numeric columns, no outliers were found in the dataset.
  
### EDA

The following are some of the visualizations such:

1. Visualization of Smoking Status
   
   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Smoking%20Status.png" width="370">

   Insight:

   Based on the visualization of smoking status, the number of patients who do not smoke is greater than the number of patients who smoke.
   
2. Visualization of Married Status

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Married%20Status.png" width="370">

   Insight:

   Based on marital status data, the number of unmarried patients is higher than the number of married patients.
   
3. Visualization of Risk Status

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Risk%20Status.png" width="370">

   Insight:
   
   Based on risk status data, the number of patients experiencing health risks is higher than the number of patients who do not experience health risks.
   
4. Visualization of Sugar Level

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Sugar%20Level.png"  width="370">

   Insight:

   Based on the visualization of sugar levels in patients, the number of patients with medium sugar levels was the highest compared to other categories, while the high category was the lowest.
   
5. Visualization of Alcohol Status

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Alcohol.png" width="370">

    Insight:

     Based on the visualization of alcohol consumption, patients who do not consume alcohol are in the majority, accounting for about 3/4 of the total number of patients, while patients who consume alcohol account for only about 1/4 of the total number of patients.
   
6. Visualization of Profession

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Profession.png" width="370">

    Insight:

    Based on the visualization of professions, patients with the occupation of Student were the most numerous compared to other occupational categories, although the difference was not particularly significant.
   
7. Visualization of Exercise Level

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Exercise.png" width="370">

    Insight:

    In the visualization of exercise levels, the majority of patients tend to exercise at a medium level, while fewer patients do not exercise at all.
    
8. Visualization of Exercise Level by Risk Status

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Exercise%20vs%20risk.png" width="370">

    Insight:
   
    It was found that the medium exercise level category had a high health risk level. In addition, at each exercise level, the number of patients with high health risks was greater than those with low health risks
   
9. Visualization of Exercise Level by Sugar Level

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/Exercise%20vs%20risk.png" width="370">

    Insight:

    Based on the visualization of patients according to exercise level and sugar level, patients with a medium exercise level also have a medium sugar level. In addition, each exercise level with a medium sugar level dominates  compared to other sugar levels at each exercise level.
   
10. Visualization of Numeric Feature by Risk Status

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/numerik%20vs%20risk.png" width="370">

    Insight:

    Based on the visualization of the relationship between numerical features and health risk, it can be seen that patients with high health risk generally have a median age of around 40–65 years. In terms of weight, the group with high health risk has a median of 70–110 kg, which indicates potential obesity that can increase health risk. In terms of height, patients with high health risk have a median height of around 155–182 cm, while those with low health risk have a median height of 165–190 cm. In addition, patients with high health risk have a median sleep time of around 6–7 hours, and a high BMI is also associated with an increased health risk.
    
11. Visualization of Risk Status vs Alcohol Status

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/risk%20vs%20alcoho%3B.png" width="370">

    Insight:

    Based on the visualization of the relationship between health risk and alcohol status, it appears that patients with high health risks are more likely to come from groups that consume alcohol than patients with high risks who do not consume alcohol.
    
12. Visualization of Risk Status vs Smoking Status

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/risk%20vs%20smoking.png" width="370">

    Insight:

    Based on the visualization of the relationship between health risk and smoking status, it can be seen that the number of patients in the high health risk category is highest among both smokers and non-smokers. However, this still shows that smoking has the potential to increase health risks.
    
13. Visualization of Heatmap

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/LifeStyle%20Prediction/Picture/heatmap.png" width="370">

    Insight:
    
    Based on the heatmap visualization, it is known that BMI has a high positive correlation with weight. In addition, height and BMI have the lowest correlation compared to the correlations between other numerical features.
    
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
   
3. Decision Tree

   a machine learning and data mining method that uses a tree like-structure to make decisions or predictions by breaking down complex data into series of simple rules.
   
4. SVM

   SVM is a machine learning algorithm that works by processing data to generate a hyperlane that separates the input space into two classes, starting from the grouping of linear cases seperated by the hyperlane
   
5. Gradient Boosting

   Gradient Boosting is a machine learning technique that combines several weak prediction models into one ensemble. These weak prediction models are usually decision trees, which are trained sequentially to minimize errors and improve accuracy.
   
6. XGboost Classifier

    XGboost (Xtreme Gradient Boosting) is a machine learning library that uses decision trees, a supervised learning algorithm that utilizes gradient descent. It is known for its speed, efficiency, and ability to scale well with large data sets.
   
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





