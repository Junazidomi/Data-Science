# House Price Prediction
## Business Understanding
### Background

One of the key factors in real estate transactions in India is property pricing. Property prices are influenced by various factors, such as area size, number of rooms, property condition, location, property type, and other charateristics. The wide range of prices and the numerous influencing factors pose a challenge for both consumers and sellers in determining a fair property value and making the right purchasing decisions.

With the development of information and communication technology, particularly in the fields of Artificial Intelligence (AI), these issues can be addressed through a data-driven approach. By utilizing historical real estate transaction data, a property price prediction model can be developed that estimates a property's value based on its characteristics. This model is expected to help consumers choose properties that fit their budget and needs, as well as assist sellers in setting more accurate and competitive asking prices. 

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

- The dataset has 12 columns, including 9 numeric columns and 3 categorical columns. The Target column (PRICE_IN_LACS) is used as the target variable, while the categorical columns will undergo feature transformation before being used in the model. In addition, the dataset has a total of 29,451 rows and 12 columns
- After identifying duplicate records, 401 duplicate record were found in the dataset. Therefore, this issue must be addressed to maintain data quality and improve the accuracy of the analysis results.
- After identifying the missing values, it was found that there were no missing values in the dataset. Therefore, no missing value handling was required durin the data preprocessing stage.
- After identifying outliers in the continous variables, such as SQUARE_FT, LATITUDE, and TARGET (PRICE_IN_LACS), outlier values were found in all columns. Therefore, outliers in the SQUARE_FT, LATITUDE, and LONGITUDE columns were handled through a data normalization process. Meanwhile, the TARGET (PRICE_IN_LACS) column was not normalized because it serves as the target variable in the modeling process, so its original values needed to be preserved.

### EDA

1. Distribution of Houses by Top 20 Houses
   
   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/ADDRESS.png" width="460"/>

   Insight:

   Based on the distribution of the top 20 locations by property address in India, it was found that the location with the highest number of properties is Zirakpur, Chandigarh, followed by Whitefield, Bangalore, and Raj Nagar Extension, Ghaziabad.
   
2. Visualization of Sold by Number of Rooms

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/Number%20of%20rooms.png" width="460"/>

   Insight:

   Based on a visualization of homes for sale by number of rooms, it was found that homes with 2 or 3 rooms are the most common compared to others.
   
3. Visualization of RERA Approval on Houses for Sale

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/RERA.png" width="460"/>

   Insight:

4. Visualization of Houses Sales Based Who is selling
   
   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/who%20is%20selling.png" width="460"/>

   Insight:

   Based on the visualization of the number of properties sold by seller type, it is evident that the "Deller" category has the highest number of properties compared to the other categories. The "Owner" category ranks second, while "Builder" has the fewest properties. This indicates that the majority of property transactions in the dataset are conducted through intermediaries or dealers, while direct sales by owners or developers account for a smaller proportion.
   
5. Visualization of Type of Property of Houses

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/Type%20property.png" width="460"/>

   Insight:

   Based on the visualization of property types, it was found that there are more BHK (Bedroom, Hall, and Kitchen) properties than RK (Room and Kithen) properties.
   
6. Visualization of Houses sold by Resale 

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/RESALE.png" width="460"/>

   Insight:

   Based on the visualization of the resale property status, it was found that about 93% of all properties sold were resale properties, while about 7% were non-resale properties or newly contructed properties.
   
7. Visualization of Status of Houses Under Construction

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/Under%20construction.png" width="460"/>

   Insight:

   Based on a visualization of properties for sale listed as "Under Construction". It was found that about 82% of the properties for sale are not currently under construction, while about 18% are still under construction.
   
8. Visualization of Number of House Ready to Move

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/Ready_to_move.png" width="460"/>

   Insight:

   Based on the "Ready to Move" status visualization it was found that about 82% of all properties for sale are move-in ready, while the remaining 18% are not yet move-in ready.
   
11. Visualization of Number of Houses Based on Address and Seller

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/ADDRESS%20VS%20SELLER.png" width="460"/>

    Insight:
   
12. Visualization of Houses Sales Based on Under Construction by Property Category

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/under%20construction%20by%20property%20category.png" width="460"/>

    Insight:
    
13. Visualization of Seller Type by House Status

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/SELLER%20TYPE%20VS%20HOUSE%20STATUS.png" width="460"/>

    Insight:
    
14. Visualization of Heatmap of Numerical Features

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/House_Price_Prediction_India/Picture/Heatmap.png" width="460"/>

    Insight:

    Based on the heatmap visualization of the continous numerical variables, it was found that the pair of variables with the strongest relationship is SQUARE_FT and TARGET (PRICE_IN_LACS), with a correlation cofficient of 0.4. This indicates a strong positive relationship between property area and property price.
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

