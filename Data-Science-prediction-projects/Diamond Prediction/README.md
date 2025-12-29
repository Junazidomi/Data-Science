# Diamond Prediction

## Business Understanding
### Background
### Purpose
## Data Understandings

This dataset contains information about various type of diamonds, which have a number of features to describe the characteristics of each diamond related to the prediction process in the dataset. The following is an explanation of each contained in this dataset. [Link](https://www.kaggle.com/datasets/shivam2503/diamonds/data)


|     Feature     |     Data Type    |     Description                                                                              |
|-----------------|------------------|----------------------------------------------------------------------------------------------| 
|      Price      |        Int       | Price of Diamond in US Dollars                                                               |
|      Carat      |       Float      | Weight of Diamonds                                                                           |
|       Cut       |       String     | Quality of the cut(Fair, Good, Very Good, Premium, Ideal)                                    |
|      Color      |       String     | Diamond colour from J (worst) to D (Best)                                                    |
|     Clarity     |       String     | A measurement of how clear the diamonds is (I1 (Worst), SI2, SI1, VS2, VVS2, VVS1,IF (best)) | 
|        x        |       Float      | Length in mm                                                                                 |
|        y        |       Float      | Width in mm                                                                                  |
|        z        |       Float      | Depth in mm                                                                                  |
|      Depth      |       Float      | Total depth percentage= z/mean(x,y)=2*z/x+y                                                  |
|      Table      |       Float      | Width of top diamond relative to widest point                                                |

Key Findings:
- Based on the dataset information, the dataset consists of 7 numerical features (Price, Carat, x, y, z, Depth, Table) and 3 categorical features (Cut, Color, Clarity), with a total of 53940 rows
- Based on the results of missing data identification in the dataset, there are no rows or columns with missing values
- Based on the duplicate data identification process, it can be concluded that there are no duplicate data rows
- Based on the results of identifying outlier data in the numeric columns, outliers were found in the carat, depth, table, price, x, y and z columns, thus requiring the handling of such outlier data

## EDA

## Data Preparation

## Modelling

In this project, several algorithms were used for regression testing and evaluation purposes, such as:

1. Linear Regression

   Linear Regression is a data analysis technique that predicts unknown data values using other related and known data values mathematically model unknown or dependent variables and known or independent variables as linear equations.
2. Random Forest

   Random Forest is an ensemble learning-based machine learning method that combines multiple decision tree to predict continous numerical values by averaging the predictions from each tree to improve accuracy and stability, as well as reduce overfitting.
   
3. SVM Regression 

   Support Vector Machine (SVM) Regression is a supervised learning algorithm  used to predict the value of continuous variables. The basic objective of the SVR algorithm is to find the most appropriate decision line, whereby SVR attempts to adjust the best line within the threshold value (the distance between the hyperlane between the hyperlane and the boundary line).
   
4. Decision Tree

Decision Tree is a machine learning that builds a predictive tree model to predict continuous numerical values by recursively dividing the dataset based on rules or data features until it reaches the leaf node containing the final prediction value, usually the average of the data groups in that leaf.

## Evaluation

The following is an evaluation of each algorithm used:

|       Algorithm       |     MAE     |     MSE     |     R2     |
|-----------------------|-------------|-------------|------------|
|   Linear Regression   | 	529.884   | 570437.214  |    0.915   | 
|   Random Forest       |   189.021   | 115020.735  |    0.983   |
|     SVM               |  1952.409   | 7522209.915 |   -0.117   |
|   Decision Tree       |   251.154   |  213275.198 |    0.968   |

