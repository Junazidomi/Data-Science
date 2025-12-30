# Diamond Prediction

## Business Understanding
### Background

Diamond prices are influenced by various factors such as carat, cut, colour, and clarity, which make the pricing process complex and potentially subjective. These differences in characteristics can lead to significant price variations, requiring a more accurate and objective method for predicting diamond prices. By utilising historical data and a machine learning approach, the Diamond Price Prediction project was developed to study the relationship between diamond characteristics and market prices, with the aim of helping to generate more accurate price predictions and supporting decision-making for industry players and consumers.

### Purpose

This project focuses on building a machine learning model to predict diamond prices based on diamond charateristics and quality, with goal of generating accurate and reliable price estimates based on optimal metric evaluation.

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

### EDA

The following is a visualization of this project:

1. Categorical Distribution

   ![Visualization1](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diamond%20Prediction/Picture/Kategorikal%20Distribution.png)

   Insight:

   Based on this visualisation, it can be seen that diamonds with an Ideal cut category are the most prevalent in the dataset, followed by the Premium category.      In the colour column visualisation, diamonds with a G colour have the highest number compared to other colours, while J colour diamonds are the least              prevalent. Meanwhile, in the clarity column, the SI1 category is the most dominant compared to other categories.
   
2. Carat vs Cut

   ![Visualization2](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diamond%20Prediction/Picture/Carat%20vs%20Cut.png)

   Insight:

   Based on the Carat vs Cut visualisation, diamonds with an Ideal cut tend to have a lower carat weight than other categories. Meanwhile, the Fair and Premium       categories show a higher median carat weight than Ideal and Very Good. This indicates that diamond size (carat) is not directly proportional to cut quality,       meaning that both are independent features that are equally important in predicting diamond prices.
   
3. Color vs Clarity

   ![Visualization3](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diamond%20Prediction/Picture/Color%20vs%20Clarity.png)

   Insight:
   Based on the Visualisation of Colour vs Clarity, diamonds with G and E colours are the most numerous in almost all clarity categories, indicating that these       two colours are the most common in the dataset. Furthermore, in each colour category (D to J), SI1 and VS2 clarity grades consistently dominate over other         clarity grades, indicating that diamonds with medium clarity are the most widely available
 
4. Color vs Cut

   ![Visualization4](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diamond%20Prediction/Picture/Color%20vs%20Cut.png)

   Insight:

   Based on the Colour vs Cut visualisation, diamonds with a G colour have the largest distribution compared to other colours. In addition, in each colour            category, Fair cut diamonds have the smallest number compared to other cut categories. Meanwhile, Ideal and Premium cuts show the highest distribution in          almost all colour categories compared to other cuts.
5. Cut vs Clarity

   ![Visualization5](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diamond%20Prediction/Picture/Cut%20vs%20Clarity.png)

   Insight:

   Based on the visualisation of Clarity VS Cut, diamonds with an ideal cut have the highest number across almost all clarity grades, especially in the SI1 and       VS2 categories. This shows that most diamonds in the dataset have good cut quality with medium clarity.  In addition, across all cut types (ideal, premium,        very good, good, and fair), the SI1 clarity category consistently has the highest number compared to other clarity categories.

6. Cut vs Quality

   ![Visualization6](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diamond%20Prediction/Picture/cut%20vs%20Quality.png)

   Insight:

   Based on the visualisation Comparison of Diamond Dimension y across Cut Grades, all cut categories have relatively similar median values. In the visualisation     Comparison of Diamond Price across Cut Grades, the Premium cut category shows a higher median price than other categories. Meanwhile, in the visualisation         Comparison of Diamond Dimension z across Cut Grades, the Fair cut has the highest median compared to other cuts. In addition, in the visualisation Comparison      of Diamond Dimension x across Cut Grades, the Premium cut has the highest median compared to other cut categories.
   
## Data Preparation

The data preparation process is as follows:

1. Outlier Handling
   
   At this stage, the outlier handling process is applied to columns of a numeric type. After identfying outliers using Interquartile Range (IQR), rows of data indicated as outliers deleted (dropped)
   
2. Drop Column
   In this section, the ‘Unnamed: 0’ column is removed because it is the index of the dataset. Furthermore, this column does not contain relevant information and does not affect the quality of the modelling.
   
3. Encoding
   
   At this stage, categorical data is converted into numerical data so that it can be used in the training and modelling process. The encoding technique used is ordinal encoding, because the categorical variables used have ordinal properties.

4. Split the train data and test data
   In this section, train data and test data are split using the sklearn train_test_split library to split dependent data and independent data, which are then processed.

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

## Conclusion 

After the model training process, Random Forest showed the best performance in predicting diamond prices with an R² value of 0.983, which was higher than the other models. Meanwhile, the Support Vector Machine (SVM) model was unable to predict well, as indicated by an R² value of -0.117, making it unsuitable for use in diamond price prediction.
