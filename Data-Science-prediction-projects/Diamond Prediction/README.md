# Diamond Prediction

## Business Understanding
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
## Data Preparation
## Data Modelling
## Evaluation

The following is an evaluation of each algorithm used:

|       Algorithm       |     MAE     |     MSE     |     R2     |
|-----------------------|-------------|-------------|------------|
|   Linear Regression   | 	529.884   | 570437.214  |    0.915   | 
|   Random Forest       |   189.021   | 115020.735  |    0.983   |
|     SVM               |  1952.409   | 7522209.915 |   -0.117   |
|   Decision Tree       |   251.154   |  213275.198 |    0.968   |

