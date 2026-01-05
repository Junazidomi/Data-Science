# Diabetes Prediction

## Businees Understanding
### Background
### Purpose
## Data Understanding

This dataset is a collection of medical and demographic data from patients, along with their diabetes status (positive or negative). The dataset includes features such as age, gender, body mass index (BMI), hypertension, heart disease, smoking history HbA1c level, and blood glucose level. This can be useful for healthcare professionals in identifying patients who may be risk of developing diabetes and in developing personalized treatment plans. [Dataset](https://www.kaggle.com/datasets/iammustafatz/diabetes-prediction-dataset)

|     Feature         |      Data Type     |                                                  Description                                                        |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------|
|     gender          |        String      | Gender refers to the biological sex of the individual, which can have an impact on their susceptibility to diabates |
|      age            |        Float       | Age is an important factor as diabetes is more commonly diagnoses in older adult                                    |
|   hypertension      |         Int        | Hypertension is a medical condition in which the blood pressure in the arteries is persistently elevated            |
|  heart_disease      |         Int        | Heart disease is another medical condition that is associated with an increased risk of developing diabetes         |
| smoking_history     |        String      | Smoking history is also considered a risk factor for diabetes and can exacerbate the comploications                 |
|      bmi            |        Float       | BMI(Body Mass Index) is a measure of body fat base on weighr and height                                             | 
|   HbA1c_level       |        Float       | HbA1c (Hemoglobin A1c) level is a measure of a person's average blood sugar level over the past 2-3 months          |
| blood_glucose_level |        Int          | Blood glucose level refers to the amount of glucose in the bloodstream at a given time                             | 
|   diabetes          |         Int        | Diabetes is a target variable being predicted                                                                       |

Key Findings:

- 1


### EDA

1. Visualization of Diabetes Status

   ![Visualization1]()

   Insight:

   
3. Visualization of Gender Patients

   ![Visualization2]()
5. Vizualization of Smoking History
6. Visualization of Hypertension Status
7. Visualization of Heart Disease
8. Visualization of Diabetes Status VS Medical Checkup
9. Visualization of Hearth Disease VS Medical Checkup
10. Visualization of Hypertension Status VS Medical Checkup
11. Visualization of Hearth Disease VS Diabetes Status
12. Visualization of Hypertension VS Diabetes Status
13. Visualization of Smoking History VS Diabetes
14. Visualization of Numerical Feature
    
## Data Preparation

The data preparation process is as follows:

1. Mismatch Data Handling
2. Drop Data Duplicated
3. Outlier Handling
4. Encoding
5. Split the train data and test data
6. Oversample
   
## Modelling

In this project, several algorithms for classification testing and evaluation purposes, such as:

1. Logistic Regression
2. Random Forest
3. Decision Tree
4. SVM

## Evaluation

The following is an evaluation of each algorithms used:

|                Algorithm                  |    Accuracy    |   Precision    |   Recall  |  F1 Score  |
|-------------------------------------------|----------------|----------------|-----------|------------|
| Random Forest                             |    0.965296    |    0.716547    | 0.546652  |  0.620174  |
| Logistic Regression                       |    0.844456	   |    0.232148    | 0.867179  |  0.366249  |
| Decision Tree                             |    0.560510    |    0.560510    | 0.579583  |  0.569887  |
| SVM                                       |    0.821187	   |    0.215741    | 0.929748  |  0.350217  |
| Random Forest (After Hypertune parameter) |    0.812425    |    0.210718    | 0.953897  |  0.345184  |
| Decision Tree (After Hypertune parameter) |    0.237948    |    0.237948    | 0.926454  |  0.378645  |

