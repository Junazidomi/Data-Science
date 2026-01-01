# Laptop Price Prediction

## Business Understanding
### Background

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Technological developments have accelerated, driving an increase in public demand for computing devices, particularly laptops. Laptops are important devices because they are used in various activities, such as education, work, business, and entertainment. As the number of laptop brands and specifications available on the market increases, consumers often find it difficult to choose a laptop that suits their needs and budget.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The use of machine learning to predict laptop prices based on specifications, such as brand, RAM capacity, storage capacity, screen size, and weight, can make it easier for consumers to make a choice. By utilising historical data on laptops and their specifications, the prediction system can help consumers obtain recommendations for laptops with more accurate and suitable prices.

Translated with DeepL.com (free version)
### Purpose

The objective of the project to predict laptop prices based on specifications is to develop a system capable of predicting laptop prices for users who wish to purchase laptops based on their characteristics or specifications.

## Data Understandings

This dataset emulates laptop prices, capturing various features commonly associated with laptops and their corresponding simulated prices. The dataset encompasses key attribute such as brand, processor speed, RAM size, storage capacity, screen size and weight. The following is an explanation of each contained in this dataset. [Dataset](https://www.kaggle.com/datasets/mrsimple07/laptoppriceprediction)
|     Feature     |     Data Type   |  Description                                                                             | 
|-----------------|-----------------|------------------------------------------------------------------------------------------|
|      Brand      |      String     |Represents the laptop brand.                                                              |
| Processor Speed |       Float     | Indicates the speed of the laptop's processor generated uniformly between 1.5 and 40 GHz |
|   RAM_Size      |        Int      | Represents the random selection of RAM sizes.                                            |
|Storage_Capacity |        Int      | Simulates different storage capacities.                                                  |
|   Screen_Size   |       Float     | Represents the size of the laptop screnn                                                 |
|      Weight     |       Float     | Indicates the weight of the laptop in kilograms                                          |
|      Price      |       Float     | Represents laptop price                                                                  |

Key Findings

- The dataset contains of 7 numerical features (Prcessor_Speed, RAM_Size, Storage_Capacity, Screen_Size, Weight, Price) and 1 categorical features (Brand), with a total of 1000 rows
- Based on the results of missing data identification in the dataset, there are no rows or columns with missing values
- Based on the duplicate data identification process, it can be concluded there are no rows with duplicate data
- Based on the data outlier identification process, it can be concluded there are no data outlier in dataset
### EDA 

The following is a vizualization of this project:
1. Visualization of Laptop's Brand Sold
   
   ![Dashboard1](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Laptop%20Price%20Prediction/Picture/Laptop%20Brand.png)

   Insight
   
2. Visualization of Type Storage Capacity

   ![Dashboard2](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Laptop%20Price%20Prediction/Picture/Storage%20Capacity.png)

   Insight:
   
3. Visualization of Processor Speed vs Laptop Brand

   ![Dashboard3](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Laptop%20Price%20Prediction/Picture/Processor%20Speed%20vs%20Laptop%20brand.png)

   Insight:
4. Visualization of RAM vs Brand

   ![Dashboard4](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Laptop%20Price%20Prediction/Picture/RAM%20VS%20Brand.png)

   Insight:
   
5. Visualization of Laptop's Weight vs Brand
   
   ![Dashboard5](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Laptop%20Price%20Prediction/Picture/laptop%20weight%20vs%20brand.png)

   Insight:
   
6. Visualization of Laptop Price vs Brand

   ![Dashboard6](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Laptop%20Price%20Prediction/Picture/laptop%20price%20vs%20brand.png)

   Insight:
   
7. Visualization of Screen Size vs Brand

   ![Dashboard7](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Laptop%20Price%20Prediction/Picture/screen%20size%20vs%20brand.png)

   Insight:
   
8. Heatmap of Numerical Feature

   ![Dashboard8](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Laptop%20Price%20Prediction/Picture/Heatmap.png)

   Insight
## Data Preparation

1. Encoding

   This process converts categorical data into numerical data to enable model training, since machine learning models require numerical input. Label Encoding is       used for this transformation.

2. Normalization

   Normalization is a data preprocessing technique used to convert numerical values in a dataset to a common scale for example 0 to 1. The purpose is to ensure        that no single feature (data column) dominates the others, especially when the features have very different value ranges
   
3. Split the train data and test data
   
   In this section, the data are divided into training and testing sets using the train_test_split function provided by the scikit-learn library. The independent      and dependent variables are subsequently processed.

   
## Modelling

In this project, several algorithms were used for regression testing and evaluation purposes, such as:

1. Linear Regression

   Linear Regression is a data analysis technique that predicts unknown data values using other related and known data values mathematically model unknown or dependant variables and known or independent variables as linear equations.
   
2. Random Forest

   Random Forest is an ensemble learning-based machine learing method that combines multiple decision tree to predict continuous numerical values by averaging the predictions from each tree to improve accuracy and stability, as well as reduce overfitting.

3. Decision Tree
   Decision Tree is a machine learning that builds a predictive tree model to predict continuous numerical values by recursively dividing the dataset based on rules or data features until it reaches the leaf node containing the final prediction value, usually the average of the data groups in that leaf.

4. SVM
   Support Vector Machine (SVM) Regression is a supervised learning algorithm used to predict the value of continuous variables. The basic objective of the SVR algorithm is to find the most appropriate decision line, whereby SVR attempts to adjust the best line within the threshold value (the distance between the hyperlane between the hyperlane and the boundary line).


## Evaluation
The following is an evaluation of each algorithm:

|       Algorithm         |       MAE       |       MSE       |       R2      |
|-------------------------|-----------------|-----------------|---------------|
| Linear Regression       | 145.272350      | 31.969,58       |  0.999648     |
| Random Forest           | 163.792227      | 40.617,91       |  0.999553     |
| Decision Tree           | 225.440922      | 79.515,84       |  0.999124     |
| SVM                     | 7925.300530     | 94.436.640      |  -0.040091    |

## Conclusion
