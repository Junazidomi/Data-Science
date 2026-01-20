# Car Price Prediction

## Business Understanding
### Background

Car prices are an important factor that influences consumer purchasing decisions, both in the new and used car markets. Car pricing is influenced by various factors, such as brand, vehicle type, year of manufacture, mileage, engine condition, features, and market trends. However, in practice, car pricing is often subjective and does not always reflect the actual market value, which can potentially harm both sellers and buyers.

With the increase in car sales, especially on digital platforms, the need for an accurate and objective pricing system has become increasingly important. Inaccurate pricing can result in cars being difficult to sell, financial losses, or unfair transactions. Therefore, a system is needed that can accurately predict car prices based on data and vehicle characteristics.

Technological developments in data science and machine learning have opened up opportunities to build reliable car price prediction models. By utilising historical car sales data and various vehicle attributes, machine learning models can learn the relationship patterns between car characteristics and market prices. This approach enables car price predictions to be made more objectively, consistently, and efficiently.

The Project Car Price Prediction aims to develop a car price prediction system that can assist sellers, buyers, and automotive industry players in determining fair and competitive prices. With this system in place, it is hoped that the transaction process will become more transparent, efficient, and profitable for all parties.

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
- This dataset consists of 18 columns, including 5 numeric columns and 13 categorical columns, and has 19,237 rows of data, with the Price column as the target column.
- After identifying missing data, it can be concluded that there are no missing values in the dataset.
- After identifying duplicate data, 483 duplicate data entries were found, requiring duplicate data handling to prevent bias in the model.
- After identifying the values in the dataset, irrelevant data was found in the cylinder column, namely values 1, 2, 9, and 14, which did not match the number of cylinders specified for cars. In addition, there was data on cars priced below 500, which was unrealistic, so it was necessary to process these values to maintain data quality.
- After identifying outliers in the cylinder, price, and airbags columns, outliers were found in the cylinder and price columns. However, this dataset contains cars with high prices due to their high specifications, so these outliers are considered normal and no outlier handling process was performed.

#### EDA

1. Visualization of Manufactured Cars Sold
   
   ![Viz](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Car%20Price%20Prediction/Picture/Manufacturer.png)

   Insight:

   Based on the visualisation of the number of cars sold by manufacturer, it can be concluded that in the dataset there are three top car manufacturers based on the number of cars, namely Hyundai, Toyota, and Mercedes-Benz.
   
2. Visualization of Car Models for Sale

   ![Viz1](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Car%20Price%20Prediction/Picture/Model.png)

   Insight:

   Based on the visualisation of the top 20 car models by sales, it can be concluded that the Prius, Sonata, Camry, and Elantra models have the highest number of cars compared to other models.
   
3. Visualization of Car Production by Year

   ![Viz1](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Car%20Price%20Prediction/Picture/Year.png)

   Insight:

   Based on the visualisation of the number of cars sold by year of manufacture, it can be concluded that the most cars sold were manufactured in 2012, followed by cars manufactured in 2014 and 2013. In addition, there are also cars manufactured in the 1900s that are still being sold today.
   
4. Visualization of Car Categories

   ![Viz1](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Car%20Price%20Prediction/Picture/Car%20Category.png)

   Insight:

   Based on the visualisation of the number of cars sold by category, it can be concluded that saloon cars are the most widely available category. Meanwhile, convertibles, limousines and pick-ups are the categories with the lowest availability.
   
5. Visualization of Car Fuel Types

   ![Viz2](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Car%20Price%20Prediction/Picture/Fuel%20Type.png)

   Insight:
   
   Based on the visualisation of the number of cars sold by fuel type, it can be concluded that petrol cars are the most numerous compared to other fuel types. Meanwhile, hydrogen and plug-in hybrid cars are the least numerous compared to other fuel types.
   
6. Visualization of Car Door Types

   ![Viz3](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Car%20Price%20Prediction/Picture/Doors%20Type.png)

   Insight:

    Based on the visualisation of the number of cars sold by door type, cars with 04-May doors are the most numerous and dominant compared to other door types. Meanwhile, cars with 02-May doors and more than >5 doors are fewer in number than cars with 4–5 doors.
   
7. Visualization of Car Cyclinder Type

   ![Viz3](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Car%20Price%20Prediction/Picture/Cyclinder.png)

   Insight:

    Based on the visualisation of the number of cars sold by cylinder count, it can be concluded that cars with 4 cylinders are the most common. However, the dataset contains unrealistic cylinder counts, such as 1, 2, 9, and 14 cylinders, which do not correspond to typical car specifications. Therefore, data rows with these cylinder counts need to be deleted (dropped) to maintain data quality.
   
8. Visualization of Car Colour Types

   ![Viz4](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Car%20Price%20Prediction/Picture/Colour.png)

   Insight:

   Based on the visualisation of the number of cars sold by colour, it can be concluded that black cars have the highest number of cars compared to other colours. In addition, white and silver cars also have a relatively high number of cars after black. Meanwhile, pink cars are the colour with the fewest number of cars compared to other colours.
   
9. Visualization of Car Gearbox Types

    ![Viz6](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Car%20Price%20Prediction/Picture/Gearbox%20Type.png)

   Insight:

   Based on the visualisation of the number of cars sold by gearbox type, it can be concluded that cars with automatic gearboxes are the most sold compared to other types, accounting for more than half of the total cars sold. Meanwhile, cars with variator gearboxes have the lowest sales compared to other gearbox types.
   
10. Visualization of Car Wheel Types

    ![Viz4](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Car%20Price%20Prediction/Picture/Wheels%20Type.png)

    Insight:

    Based on the visualisation of the number of cars sold by wheel type, it can be concluded that cars with Front wheel type have the largest proportion, which is around 66.9% of the total cars sold. Meanwhile, cars with Rear  wheel type have the smallest proportion compared to other categories, which is around 12%.
    
11. Visualisation of a leather-interior car

    ![Viz8](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Car%20Price%20Prediction/Picture/Leather%20Interior.png)

    Insight:

    Based on the visualisation of the number of cars sold based on leather interiors, it can be concluded that cars with leather interiors are sold more than cars without leather interiors.
    
12. Visualization of Top 10 Manufactured Car by Price

    ![Viz7](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Car%20Price%20Prediction/Picture/Manufacturer%20by%20Price.png)

    Insight:
    
    Based on the visualisation of the top 15 car manufacturers sold by average price, it can be concluded that cars manufactured by Lamborghini have the highest average price compared to other manufacturers. This shows that Lamborghini cars are classified as premium vehicles.
    
13. Visualization of Top 10 Model by Price

    ![Viz9](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Car%20Price%20Prediction/Picture/Model%20by%20Price.png)

    Insight:
    
    Berdasarkan visualisasi top 15 mobil yang dijual berdasarkan model dan rata-rata Harga, mobil dengan tipe Urus memiliki rata-rata Harga paling tinggi dibandingkan model lain disusul model Combo dan G 65 AMG 63ANG. Selain itu, dari top 15 mobil tersebut , mobil denga model F TYPE R dan Range Rover velar paling sedikit rata-rata harganya dari top 15 mobil tersebut
    
## Data Preparation

The data preparation process is as follows:

1. Drop Irrelevant Column

   In this process, irrelevant columns are removed (dropped) so that the model can work optimally and avoid performance degradation and unnecessary bias.
   
2. Fix Column Type
   
   In this process, there are several numeric columns that appear to be stored in string or text format, requiring data type correction. This is necessary to ensure that the model runs properly, avoids bias, and facilitates the preprocessing stage in the next phase.

3. Drop Missing Data

   In this process, missing data is dropped so that no errors occur in the modelling.
   
4. Drop Duplicate Data
   
   At this stage, data is first identified to detect the existence of duplicate data. Once duplicate data is found, it is deleted to prevent bias in the data and maintain data consistency and quality.
   
5. Mismatch Data Handling, after obtaining the data summary

   In this process, after obtaining the data summary, inaccurate or irrelevant data are removed (dropped) because they can negatively affect the performance of the machine learning model. For example, in the Cylinder column, there are mismatched or unrealistic values such as cars with 1, 2, 9, or 14 cylinders, as well as car prices below 500, which are considered invalid and therefore excluded from the datas
 
6. Encoding

   This part of the process transforms categorical data into numerical data facilitate model training. In addition, numerical data is required for modelling. In this project, the encoding methods used are One Hot Encoder, which converts categories into binary representations so that the data can be used effectively by machine learning models.
   
7. Split the Training Data and Test Data

    In this section, train data and test data are split using the sklearn train_test_split library to split dependent data and independent data, which are then processed
   
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

   XGBoost uses ensemble learning techniques, which combine predictions from multiple models to improve overall performance. This approach is based on boosting techniques, where weak learners, usually simple decision trees, are combined into a strong learner.
   
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
- Based on the analysis results, it can be concluded that each feature contributes to determining the price of a car.
- In the Random Forest model, higher evaluation metric values were obtained compared to other models, indicating that this model is capable of effectively capturing data patterns in predicting car prices.
- In the SVM model, the model was unable to capture data patterns in predicting car prices. This was demonstrated by the lowest evaluation metric value compared to other models, as well as a negative R² value in the SVM model.
- After hyperparameter tuning, the Random Forest model experienced a decline in all evaluation metrics compared to before tuning. Meanwhile, the Decision Tree model experienced an increase in every evaluation metric after hyperparameter tuning.
