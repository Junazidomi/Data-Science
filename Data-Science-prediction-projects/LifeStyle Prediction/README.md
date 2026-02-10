# Lifestyle and Health Risk Prediction

## Business Understanding
### Background
### Purpose
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
2. Visualization of Married Status
3. Visualization of Risk Status
4. Visualization of Smoking Status
5. Visualization of Sugar Level
6. Visualization of Profession
7. Visualization of Exercise Level
8. Visualization of Exercise Level by Risk Status
9. Visualization of Exercise Level by Sugar Level
10. Visualization of Numeric Feature by Risk Status
11. Visualization of Risk Status vs Alcohol Status
12. Visualization of Risk Status vs Smoking Status
13. Visualization of Heatmap

## Data Preparation

The data preparation is as follows:

1. Encoding
2. Split the Training Data and Test Data
3. Balance Target Data

## Modelling

In this project, several algorithms for classification evaluation purpose such as:

1. Logistic Regression
2. Random Forest
3. Decision Tree
4. SVM
5. Gradient Boosting
6. XGboost Classifier

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
