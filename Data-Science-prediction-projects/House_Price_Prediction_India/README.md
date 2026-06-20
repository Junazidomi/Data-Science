# House Price Prediction
## Business Understanding
### Background

### Purpose

The purpose of this project is to offer solutions that help consumers search for and purchase property in India in line with their budget, preferences and the criteria they specify

## Data Understandings

This dataset has been collected from various properties across India, where buyers wish to purchase property based on a number of factors; therefore a model is required to predict house prices based on these factors. [Dataset](https://www.kaggle.com/datasets/anmolkumar/house-price-prediction-challenge)

|     Feature           |    Data Type   |              Description               |
|-----------------------|----------------|----------------------------------------|
|    POSTED BY          |     String     | Category marking who has listed        |
| UNDER CONTRUCTION     |      Int       | Under Construction or Not              | 
|        RERA           |      Int       | Rera approved or not                   |
|       BHK_NO.         |     String     | Number of rooms                        |
|      BHK_OR_RK        |     Float      | Type of Property                       |
|      SQUARE_FT        |      Int       | Total area of the house in square feet |
|    READY_TO_MOVE      |      Int       | Category marking Ready to Move or not  |
|       RESALE          |     String     | Category marking Resale or Not         |
|      ADDRESS          |     String     | Address of the property                |
|      LONGITUDE        |     Float      | Longitude of the property              |
|      LATITUDE         |     Float      | Latitude of the property               |
| TARGET(PRICE_IN_LACS) | 	  Float      | Price of the Property                  |

Key Findings:

- The dataset has 

### EDA

1. Distribution of Houses by Top 20 Houses
   
   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/ADDRESS.png" width="460"/>

   Insight:
   
2. Visualization of Sold by Number of Rooms

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/Number%20of%20rooms.png" width="460"/>

   Insight:

3. Visualization of RERA Approval on Houses for Sale

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/RERA.png" width="460"/>

   Insight:

4. Visualization of Houses Sales Based Who is selling
   
   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/who%20is%20selling.png" width="460"/>

   Insight:
   
5. Visualization of Type of Property of Houses

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/Type%20property.png" width="460"/>

   Insight:
   
6. Visualization of Houses sold by Resale 

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/RESALE.png" width="460"/>

   Insight:
   
7. Visualization of Status of Houses Under Construction

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/Under%20construction.png" width="460"/>

   Insight:
   
8. Visualization of Number of House Ready to Move

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/Ready_to_move.png" width="460"/>

   Insight:
   
9. Visualization of Top 5 Number of Houses Based on Address and RERA authority

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/Address%20vs%20RERA.png" width="460"/>

   Insight:
   
10. Visualization of Number of Houses Based on Address and Seller

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/ADDRESS%20VS%20SELLER.png" width="460"/>

    Insight:
   
11. Visualization of Houses Sales Based on Under Construction by Property Category

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/under%20construction%20by%20property%20category.png" width="460"/>

    Insight:
    
12. Visualization of Seller Type by House Status

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/SELLER%20TYPE%20VS%20HOUSE%20STATUS.png" width="460"/>

    Insight:
    
13. Visualization of Heatmap of Numerical Features

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/Heatmap.png" width="460"/>
    
## Data Preparation

The data preparation process is as follows:

1. Drop Duplicate Data

   At this stage, data is first identified to detect the existence of duplicate data. Once duplicate data is found, it is deleted to prevent bias in the data and maintain data consistency and quality.
   
2. Normalization

   Normalization in machine learning is the process of converting the range of feature values (variables) in a dataset to a uniform scale. The purpose is to prevent features with a wide range of values from dominating the training process, so that the model can learn more quickly and accurately
   
3. Encode
   
   This part of the process transforms categorical data into numerical data facilitate model training. In addition, numerical data is required for modelling. In this project, the encoding methods used are One Hot Encoder, which converts categories into binary representations so that the data can be used effectively by machine learning models.
   
4. Split Training and Test Data

   In this section, train and test data are split using the sklearn train_test_split library to split dependent data and independent data, which are than processed.
   
## Modelling

In this project, several algorithms  for regression evaluation purpose such as:

1. Random Forest

   Random forest is an ensemble-based machine learning algorithm that combines several decision trees with the aim of accurately predicting numerical or continuous values
   
2. Decision Tree

   Decision tree is a machine learning algorithm that uses a tree structure to predict numerical or continuous values.
   
3. Gradient Boosting

   Gradient boosting is a machine learning technique that sequentially combines a series of weak predictive models based on decision trees.
   
4. XGB Regressor

   XGB is an algorithm that combines multiple models specifically with the purpose of correcting errors or residuals from the previous tree.
   
## Evalauation

The following is an evaluation of each algorithms used:

|     Algorithm     |     MAE     |     MSE      |      R2      |
|-------------------|-------------|--------------|--------------|
| Random Forest     |    32.536	  |   63332.382  |     0.884    |
| Decision Tree     |    35.668	  |   32833.118  |     0.940    |
| Gradient Boosting |    47.112   |   31274.307  |     0.943    |
| XGB Regressor     |    51.255	  |  173391.435	 |     0.683    |

## Conclusion

