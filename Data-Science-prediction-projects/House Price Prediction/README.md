# House Price Prediction
## Businees Understanding
### Background
### Purpose
## Data Undertanding

The house price dataset contains information  about  of various charateristics of houses and their surroundings that are used to predict house prices. [Dataset](https://www.kaggle.com/datasets/shree1992/housedata)
|     Features     |     Data Type     |                                                        Description                                                                              |
|------------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
|       date       |        String     | The sales data of the house                                                                                                                     |
|       price      |        Float      | The selling price of the house                                                                                                                  |                  
|     bedrooms     |        Float      | The number of bedroom in the house                                                                                                              |
|     bathrooms    |        Float      | The number of bedrooms, if the "x.5" represents a half bathroom, a bathroom that typically has a toilet and sink but has not  shower or bathtub | 
|    sqft_living   |         Int       | The living area of the house in square feet                                                                                                     |
|    sqft_lot      |         Int       | The total area of property, including outdoor spaces, in square feet                                                                            |
|     floors       |        Float      | The number of floors or levels in the house. May contain decimals for partial floors                                                            |
|   waterfront     |         Int       | indicates whether the house is located near or facing a body of water                                                                           |
|      view        |         Int       | Represents the quality or rating of the house's view                                                                                            |
|    condition     |         Int       | The overall condition of the hoyse, typically on a scale from 1 to 5, where 5 indicates excellent condition                                     |
|    sqft_above    |         Int       | The square footage of the house above ground level                                                                                              |
|    sqft_basement |         Int       | The area of basement (if present) in square feet                                                                                                | 
|    yr_built      |         Int       | The year the house was built. Newer houses generally have higher prices                                                                         |
|    yt_renovated  |         Int       | The year the house was last renovated. A value of 0 means it has never been renovated                                                           |
|      street      |        String     | The name of the street where the house is located                                                                                               |
|       city       |        String     | The city where the house is located                                                                                                             |
|     state_zip    |        String     | The state and postal code (ZIP Code) of the house                                                                                               |
|     country      |        String     | The country where the house is located                                                                                                          |

Key Findings:

### EDA

The following are some of the visualization such:

1. Visualization of the Number of Bathrooms on the House
2. Visualization of the Number of Bedrooms on the House
3. Visualization of Where the House Located
4. Visualization of Number of Floors on the House
5. Visualization of the House Condition
6. Visualization of the Quality View on the House
7. Visualization of the Waterfront on the House
8. Visualization of the House Condition by Price
9. Visualization of the Number of Floors by Price
10. Visualization of the Waterfront on the House by Price
11. Heatmap of Numerical Feature
    
## Data Preparation

The data preparation process is as follows

1. Drop Irreleveant Column
2. Outlier Handling
3. Encoding
4. Split The Training Data and Test Data
## Modelling

In this project, several algorithms for regression evaluation purpose such as:

1. Linear Regression

   Linear regression is a data analysis technique that predicts unknown data values using other related and known data values. Mathematically, it models unknown or dependent variables and known or independent variables as linear equations.
   
2. Random Forest

   Random Forest is a machine learning algorithm that combines the outputs of several decision trees to produce more accurate predictions, particularly in regression problems.
   
3. Decision Tree

   Decision Tree is a predictive modelling method in data analysis that uses a tree structure. The purpose of decision tree is to describe and make decisions based on a series of rules and conitions
   
4. SVM

   Support Vector Machine (SVM) is one of the algorithms in supervised learning. The Support Vector Machine algorithm is used to find the best hyperplane in N-dimensional space that clearly classifies data points.

5. XGBoost

   XGBoost (eXtreme Gradient Boosting) is a distributed open-source machine learning library that uses decision trees, a supervised learning boosting algorithm that utilises gradient descent.
   
## Evaluation

The following is an evaluation of each algorithm used:

|                   Algorithm               |     MAE       |      MSE     |    R2      |
|-------------------------------------------|---------------|--------------|------------|
| Linear Regression                         | 103673.231440 | 2.228953e+10 |  0.485460  |
| Random Forest                             | 75147.222672  | 1.303552e+10 |  0.699083  |
| Decision Tree                             | 96835.269135	| 2.158672e+10 |  0.501684  |
| SVM                                       | 165826.203831 | 4.564509e+10 | -0.053689  |
| XGB Regressor                             | 74548.188969  | 1.234265e+10 | 	0.715077  |
| Random Forest (After Hypertune Parameter) | 75697.038238	| 1.302851e+10 |  0.699245  |
| Decision Tree (After Hypertune Parameter) | 99620.123791  |	1.948329e+10 |  0.550240  |
| XGB Regressor (After Hypertune Parameter) | 69872.950412  |	1.155641e+10 |	0.733227  |
