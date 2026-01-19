# Flood Prediction

## Business Understanding
### Background
### Purpose

## Data Understanding

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

### EDA (Exploratoey Data Analysis)

1. Heatmap of Numerical Feature

## Data Preparation

The data preparation process is as follows:

1. Normalization
2. Split the Training Data and Test Data 

## Modeling

In this project, several algorithms for regression evaluation purposes such as:

1. Linear Regression
2. Random Forest
3. Decision Tree
4. SVM


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
