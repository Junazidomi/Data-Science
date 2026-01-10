# Car Price Prediction

## Business Understanding
### Background

### Purpose

The purpose of this project is to build a machine learning model to predict car prices based on car specifications from historical data, as well as to assist consumers in selecting cars in stores that match their desired specifications.

## Data Understandings

This dataset contains information about various cars, including features that can affect the selling price of a car which can bulid regression models based on technical specifications and other features. [Dataset](https://www.kaggle.com/datasets/deepcontractor/car-price-prediction-challenge)

|     Feature     |     Data Type     |         Description                                                    |
|-----------------|-------------------|------------------------------------------------------------------------|  
|        ID       |       Int         | Unique value from Car                                                  |
|      Price      |       Int         | The selling price of the car                                           |
|      Levy       |      String       | Tax or Additional fee associated with the car                          |
|  Manufacturer   |      String       | The Car's Manufacturer or brand                                        |
|      Model      |      String       | The specific model of the car                                          |
|     Prod.year   |        Int        | The production year of the car                                         |
|     Category    |      String       | The type or category of the car                                        |
|Leather Interior |      String       | indicates whether the car has a leather  interior ("Yes" Or "No")      |
|    Fuel Type    |      String       | The type of fuel used by the car                                       |
|  Engine Volume  |      String       | The Engine capacity (in liters), sometimes including "turbo"           |
|     Mileage     |      String       | The total distance driven by the car (in kilometers)                   |
|     Cylinders   |      Float        | The number of engine cylinders, more cylinders usually mean more power |
| Gear box type   |      String       | The Transmission type                                                  |
| Drive Wheels    |      String       | The drive type                                                         |
|      Doors      |      String       | The number of doors                                                    |
|     Wheel       |      String       | The steering wheel position                                            |
|     Color       |      String       | The exterior color of the car                                          |
|    Airbags      |       Int         | the total number of airbags in the car                                 |

Key Findings:
- s
- 
## Data Preparation
## Modelling

In this project, several algorithms for regression evaluation purpose such as:
1. Linear Regression

   Linear Regression is a data analysis technique that predicts unknown data values using other related and known data values mathematically model unknown or dependent variables and known for independent variables as linear equations
   
2. Random Forest

   Random Forest is a machine learning algorithm that combines the outputs of several decision trees to produce more accurate predictions, particularly in regression problems.
   
3. Decision Tree

   Decision tree is a machine learning algorithm in the form of a tree structure consisting of nodes that represent decisions and branches that represent the consequences of those decisions. Each node in a decision tree represents a variable in the dataset that influences the decision and its consequences.
   
4. SVM

   Support Vector Machine (SVM) Regression is a supervised learning algorithm used to predict the value of continuous variables. The basic objective of the SVR algorithm is to find the most appropriate decision line, whereby SVR attempts to adjust the best line within the threshold value (the distance between the hyperlane between the hyperlane and the boundary line).
 
5. XGBoost Regressor
   
## Evaluation

The following is an evaluation of each algorithms used:

|                     Algorithm                 |       MAE      |      MSE       |      R2      |
|-----------------------------------------------|----------------|----------------|--------------|
| Linear Regression                             |   8146.448512  | 	1.642749e+08  |   0.428804   |
| Random Forest                                 |   4760.929502  |  1.642749e+08  |   0.759145   |
| Decision Tree                                 |   6314.892416  |  1.325550e+08  |   0.539096   |
| SVM                                           |   11903.053403 |  3.037194e+08  |  -0.056055   |
| XGBoost Regressor                             |   6212.037159  |  9.607163e+07  |   0.665952   |
| Random Forest (After Hypertune Parameter)     |   5146.009025  |  9.607163e+07  |   0.666188   |
| Decision Tree (After Hypertune Parameter)     |   6397.834550  |  1.266703e+08	|   0.559558   |
| XGBoost Regressor (After Hypertune Parameter) |   5305.421718  |  8.790590e+07  |   0.694345   |

## Conclusion 
