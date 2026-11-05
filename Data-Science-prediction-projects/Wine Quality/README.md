# Wine Quality Prediction

## Business Understanding


## Purpose


## Data Understandings

This dataset contains information about various types of wine and their chemical charateristics, such as pH, density, alcohol content, and other parameters related to wine quality. This dataset is used to train machine learning models to predict or classify wine quality based on these charateristics. [Dataset](https://www.kaggle.com/datasets/yasserh/wine-quality-dataset)

|          Feature        |  Data Type |                                                       Description                                                        |
|-------------------------|------------|-------------------------------------------------------------------------------------------------------------------------|
| fixed acidity           |    Float   | Measurinng the total acidity in wine, such as tartaric acid. This affects the wine's acidity and characteristics.                    |
| volatile acidity	      |    Float   | Measures the amount of volatile acids, particularly thar are too high can result in a vinegar-like taste and aroma |
| residual sugar          |    Float   | The amount of sugar remaining in the wine after fermentation is complete. A high value typically a sweeter wine. |
| chlorides               |    Float   | Measuring the salt (chloride) content in wine. High levels can make the wine taste saltier |
| free sulfur dioxide     |    Float   | The amount of sulfur dioxide (SO₂) in its free form, which acts as a preservative and helps prevent oxidation and the growth of microrganisms. |
| total sulfur dioxide    |    Float   | The total amount of sulfur dioxide, both free and bound, in wine. |
| density	                |    Float   | The density of wine. Its value can be influenced by the alcohol and sugar content in the wine. |
| pH                      |    Float   | Acidity level of wine. A lower pH value indicates a more acidic wine, while a higher values indicates a lower acidity level |
| sulphates               |    Float   | The sulfate content in wine can act as an antioxidant and affect the characteristics and stability of the wine |
| alcohol                 |    Float   | The percentage of alcohol content in wine by volume (ABV) |
| quality                 |    Int     | The wine quality score that serves as the target/label in the analysis. The higher the score, the better the wine's quality based on dataset's assessment |
| Id                      |    Int     | Unique number, or typically an identifier, rather than a key feature |

Key Findings:

- Based on the results of the data identification, the dataset consists of 13 columns, with 11 columns of type float and 2 columns of type integer. The Id column will be dropped because it not relevant to the analysis and modelling process. Meanwhile, the quality assesment column is used as the target variable in the modelling process.
- Based on the results of the analysis of missing values, it was found that the dataset contains no missing values.
- Based on the results of the analysis of duplicate data, it was found that the dataset contains no duplicate data. 

### Data Visualization
- Heatmap of Numerical Feature
- Histogram of Numerical Feature

## Data Preparation

The Data Preparation process is as follows:

1. Drop Irrelevant Column

   In this process, the dataset drops columns that are not relevant to the data. In this dataset, the columns that are unrelated or irrelevant are the ID columns.
   
2. Split Data Training and Test

   In this process, the dataset is split into two parts: training data and testing data. The training data is used to train the model to recognize and learn the patterns present in the dataset. The testing data is then used to evaluate the model's performance on data it has never seen before, thereby determining how well the model can recognize patterns and make accurate predictions.
   
3. Normalization
   
  Normalization is the process of converting numerical values to a common scale without distorting their original range differences.
  
## Modelling

In this project, several algorithms for regression evaluation purpose such as:

1. Linear Regression

   Linear Regression is a technique for predicting unknown data values using other related, know data values; creating a mathematical model of the unknown variable (dependent variable) and the known variables (independent variables) int the form of a linear equation
   
2. Random Forest

   Random Forest is an algorithm that combines the outputs of multiple decision trees to achieve better performance
   
3. Decision Tree

   Decision tree is a machine learning algorithm in the form of a tree structure consisting of nodes that represent of those decisions. Each node in a decision tree represent a variable in the dataset that influences the decision and its consequences.
   
4. SVM

   Support Vector Machine (SVM) Regression is a supervised learning algorithm used to predict the value of contionous variables. The basic objective of the SVR algorithm is to find the most appropriate decision line, whereby SVR attempts to adjust the best line within the threshold value (the distance between the hyperlane and the boundary line)

5. GBR (Gradient Boostinf Regressor)

   Gradient Boosting is an ensemble learning algorithm that produces accurate predictions by combining multiple decision trees into a single model.
   
6. XGBoost

   XGBoost uses ensemble learning techniques, which combine predictions from multiple models to improve overall performance. This approach is based on boosting techniques, where weak learners, usually simple decision trees, are combined into a strong learner.
   
   
## Evaluation

The following is an evaluation of each algorithms used:

|              Algoritm             |     MAE    |    MSE    |     R2     |
|-----------------------------------|------------|-----------|------------|
| Linear Regression                 |  0.477340  |  0.380032 |  0.317069  |
| Random Forest                     |  0.419651  |  0.304523 |  0.452762  |
| Decision Tree                     |  0.510917  |  0.606987 |	-0.090775 |
| SVM                               |  0.402766  |  0.301549 |  0.458106  |
| GBR (Gradient Boosting Regressor) |  0.446108  |  0.329243 |  0.408339  |
| XGBoost                           |  0.446108  |  0.330661 |  0.408339  |

## Conclusion
