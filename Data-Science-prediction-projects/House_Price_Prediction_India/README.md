# House Price Prediction
## Business Understanding
### Background
### Purpose
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

- 

### EDA
## Data Preparation
## Modelling

In this project, several algorithms  for regression evaluation purpose such as:

1. Random Forest
2. Decision Tree
3. Gradient Boosting
4. XGB Regressor 
## Evalauation

The following is an evaluation of each algorithms used:

|     Algorithm     |     MAE     |     MSE      |      R2      |
|-------------------|-------------|--------------|--------------|
| Random Forest     |    32.536	  |   63332.382  |     0.884    |
| Decision Tree     |    35.668	  |   32833.118  |     0.940    |
| Gradient Boosting |    47.112   |   31274.307  |     0.943    |
| XGB Regressor     |    51.255	  |  173391.435	 |     0.683    |
## Conclusion

