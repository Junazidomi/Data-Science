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
| density	              |    Float   | The density of wine. Its value can be influenced by the alcohol and sugar content in the wine. |
| pH                      |    Float   | Acidity level of wine. A lower pH value indicates a more acidic wine, while a higher values indicates a lower acidity level |
| sulphates               |    Float   | The sulfate content in wine can act as an antioxidant and affect the characteristics and stability of the wine |
| alcohol                 |    Float   | The percentage of alcohol content in wine by volume (ABV) |
| quality                 |    Int     | The wine quality score that serves as the target/label in the analysis. The higher the score, the better the wine's quality based on dataset's assessment |
| Id                      |    Int     | Unique number, or typically an identifier, rather than a key feature |

Key Findings:

## Data Preparation

The Data Preparation process is as follows:

1. Drop Irrelevant Column
2. Split Data Training and Test
3. Normalization
  
## Modelling

In this project, several algorithms for regression evaluation purpose such as:

1. Linear Regression
2. Random Forest
3. Decision Tree
4. SVM
5. GBR (Gradient Boostinf Regressor)
6. XGBoost
   
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
