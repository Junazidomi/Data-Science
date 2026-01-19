# Flood Prediction

## Business Understanding
### Background

Flooding is one of the most frequent natural disasters and has a significant impact on social, economic and environmental life. Increased rainfall intensity due to climate change, population growth, land use change and inadequate drainage systems are the main factors that increase the risk of flooding, especially in urban areas and river basins.

Until now, flood management has tended to be reactive, taking place after the disaster has occurred. This often results in delayed evacuations, significant material losses, and an increased risk of casualties. Therefore, a more proactive approach is needed through the development of a flood prediction system that can provide early warnings and support more effective decision-making.

With technological developments, particularly in the fields of data science and machine learning, there are opportunities to build more accurate flood prediction models. By utilising historical data such as rainfall, river water levels, soil conditions, and land use, flood prediction systems can identify patterns and predict the potential for flooding before it occurs.

The Flood Prediction Project aims to develop a flood prediction system that can assist the government and the community in disaster mitigation, thereby minimising the impact and damage caused by floods.

### Purpose

The purpose of this project is to build a machine learning model capable of predictappropriate action when floods occur.ing floods based on historical data, in order to help communities and authorities in carrying out mitigation measures, evacuations, and taking 

## Data Understanding

This dataset consists of historical data related to flood probability, geographical conditions, and rainfall data. The dataset aims to support the development of machine learning models to predict the probability of flooding, thereby assisting the government in reducing potential losses and providing an early warning system for flood disasters. [Dataset](https://www.kaggle.com/datasets/naiyakhalid/flood-prediction-dataset)

|              Features           |      Data Type      |                                                       Description                                                                  |
|---------------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------| 
| Monsoonnintensity               |         Int         |Higher volumes of rain during monsoons increase the probability of floods                                                           |
| TopographyDrainage              |         Int         |The drainage capacity based on the region's topography. Efficient drainage can help drain rainwater and reduce the risk of floods   |
|   RiverManagement               |         Int         |The quality and effectiveness of river management practices                                                                         |                                                                     
|   Deforestation                 |         Int         |The extent of deforestation in the area                                                                                             | 
|    Urbanization                 |         Int         |The level of urbanization in the region                                                                                             |
|   ClimateChange                 |         Int         |The impact of climate change on the region                                                                                          |
|    DamsQuality                  |         Int         |The quality and maintenance status of dams                                                                                          |
|     Silitation                  |         Int         |The extent of silitation in rivers and reservoirs                                                                                   |
|Agricultural Practices           |         Int         |The types and sustainability of agricultural practices                                                                              |
|     Encroachments               |         Int         | The degree of encroachment on flood plains and natural waterways                                                                   |
|IneffectiveDisasterPreparedness  |         Int         |The lack of emergency plans, warning systems, and simulations increases the negative impact of floods                               |
|   DrainageSystems               |         Int         |Well-maintained and adequately sized drainage systems help drain rainwater and reduce the risk of floods                            |
|CoastalVulnerability             |         Int         |Low-lying coastal areas are prone to flooding from storm surges and sea level rise                                                  |
|     Landslides                  |         Int         |Steep slopes and unstable soils are more prone to landslides                                                                        |
|     Watersheds                  |         Int         |Regions with more watersheds may have a higher or lower risk of flooding, depending on various factors                              |
|DeterioratingInfrastructure      |         Int         |Clogged culverts, damaged drainage channels, and other deficient infrastructure can increase the risk of floods                     |
|    PopulationScore              |         Int         |Densely populated areas can suffer more severe losses                                                                               |
|    WetlandLoss                  |          Int        |Wetlands act as natural sponges, absorbing excess water and helping to prevent floods                                               |
| InadquatePlanning               |         Int         |Urban planning that does not consider the risk of flooding increases the vulnerability of communities                               |
| PoliticalFactors                |         Int         |Factors such as corruption and a lack of political will to invest drainage infrastructure can make it diffcult to manage flood risk |
| Flood Probability               |         Float       |The overall probability of flooding in the region                                                                                   |

Key Findings:
- This dataset consists of 50,000 rows and 21 numeric columns, where the Flood Probability column acts as the target column with a value range of 0 to 1.
- After identifying duplicate data, it can be concluded that there is no duplicate data in the dataset
- After identifying missing data, it can be concluded that there are no missing values in the dataset
- During the process of identifying outliers in the dataset, it was found that all columns contained outlier values. Therefore, an outlier handling process was required, such as normalising or standardising the data, in order to stabilise the data distribution and prevent it from interfering with the model's performance.


### EDA (Exploratoey Data Analysis)

1. Heatmap of Numerical Feature

   ![Viz1](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Flood%20Prediction/Picture/Heatmap.png)

   Insight:

   Based on the heatmap visualisation of the numerical features, all numerical features correlate with the target column, with correlation values ranging from 0.22 to 0.23. Meanwhile, the correlation between numerical features other than the target column is relatively low or insignificant, indicating that each feature tends to stand alone and does not correlate strongly with one another.
## Data Preparation

The data preparation process is as follows:

1. Feature Scaling

   Feature scaling is a preprocessing technique that aims to convert feature values into a uniform scale, so that each feature can contribute equally to the model formation process. This technique is important because differences in range, units, or magnitude between features can affect the performance of machine learning models. In this study, the feature scaling technique used is standardisation.
   
2. Split the Training Data and Test Data
   
   In this section, train data and test data are split using the sklearn train_test_split library to split dependent data and independent data, which are then processed

## Modeling

In this project, several algorithms for regression evaluation purposes such as:

1. Linear Regression

   Linear regression is a data analysis technique that predicts unknown data values using other related and known data values. It mathematically models unknown or dependent variables and known or independent variables as linear equations.
   
2. Random Forest

   An ensemble learning-based machine learning algorithm that combines multiple decision trees to produce more accurate and stable predictions than a single tree, working by taking random samples from data and features, then combining the results.
   
3. Decision Tree

   A machine learning and data mining method that uses a tree-like structure to make decisions or predictions by breaking down complex data into series of simple rules.
   
4. SVM

   a machine learning and data mining method that uses a tree-like structure to make decisions or predictions by breaking down complex data into series of simple rules.


## Evaluation

The following is an evaluation of each algorithms used:

|              Algorithm              |      MAE      |      MSE      |     R2      |
|-------------------------------------|---------------|---------------|-------------|
| Linear Regression                   |	7.585599e-17  | 1.008725e-32  | 1.000000    |
| Random Forest                       | 2.045576e-02  | 6.725630e-04  | 0.729958    |
| Decision Tree                       | 3.732600e-02  | 2.224700e-03  | 0.106756    |
| SVM                                 | 2.017998e-02  | 6.984723e-04  | 0.719555    |
| Random Forest (Hypertune Parameter) | 2.047603e-02  | 6.737337e-04  | 0.729488    |
| Decision Tree (Hypertune Parameter) | 3.433849e-02  | 1.856252e-03  | 0.254693    |

## Conclusion
- Each independent variable correlates with the dependent variable, where all variables in the dataset are numerical data
- In the Linear Regression model, better performance was obtained compared to other models, with an R² value of 1 and MAE and MSE values close to 0. This indicates that the dataset has a very strong linear relationship between the independent and dependent variables.
- In the Decision Tree model, all evaluation metric values were the lowest compared to other models, with an R2 value of around 0.1
- In the Random Forest and Decision Tree models, after hyperparameter tuning, all evaluation metrics improved compared to before tuning.


