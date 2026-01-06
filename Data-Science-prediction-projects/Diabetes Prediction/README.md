# Diabetes Prediction

## Businees Understanding
### Background
### Purpose

The purpose of this project is to build a machine learning model that can predict diabetes in patients based on their previous medical history data and assist medical professionals in identifying diabetes to support medical decision-making.

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

   ![Visualization1](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Diabetes%20Status.png)

   Insight:

3. Visualization of Gender Patients

   ![Visualization2](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Gender.png)

   Insight:

5. Vizualization of Smoking History

   ![Visualization3](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Smoking%20History.png)

   Insight:
   
7. Visualization of Hypertension Status

   ![Visualization4](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Hypertension.png)

   Insight:
   
9. Visualization of Heart Disease

    ![Visualization5](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Heart%20Disease.png)

   Insight:
   
11. Visualization of Diabetes Status VS Medical Checkup

    ![Visualization6](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Diabetes%20Status%20vs%20medical%20checkup.png)

    Insight:
    
13. Visualization of Hearth Disease VS Medical Checkup

    ![Visualization7](https://github.com/Junazidomi/Data-Science/blob/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Heart%20Disease%20vs%20Medical%20Checkup.png?raw=true)

    Insight:
    
15. Visualization of Hypertension Status VS Medical Checkup
    
    ![Visualization8](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Hypertension%20vs%20medical%20checkup.png)

    Insight:
    
17. Visualization of Hearth Disease VS Diabetes Status

    ![Visualization9](https://github.com/Junazidomi/Data-Science/blob/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Heart%20vs%20Diabetes.png?raw=true)

    Insight:
    
19. Visualization of Hypertension VS Diabetes Status

    ![Visualization10](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Hypertension%20vs%20Diabetes.png)

    Insight:
    
21. Visualization of Smoking History VS Diabetes

    ![Visualization11](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Smoking%20history%20vs%20Diabetes.png)

    Insight:
    
23. Visualization of Numerical Feature

    ![Visualuzation12](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Heatmap.png)

    Insight:
    
## Data Preparation

The data preparation process is as follows:

1. Mismatch Data Handling

   In this process, after obtaining the data summary, data that is inaccurate or irrelevant is deleted (dropped) because it can affect the quality of the machine learning model in making predictions, such as the age column that has values below 0 and the gender column that has the value Other.
   
2. Drop Data Duplicated

   At this stage, data is first identified to detect the existence of duplicate data. Once duplicate data is found,  it is deleted to prevent bias in the data and maintain data consistency and quality.

3. Outlier Handling

   At this stage, the outlier handling process is applied to columns of a numeric type. After identfying outliers using Interquartile Range (IQR), rows of data indicated as outliers deleted (dropped)
   
4. Encoding
   This part of the process transforms categorical data into numerical data to facilitate model training.  In addition, numerical data is required for modeling. . In this project, the encoding methods used are Label Encoder, which performs encoding without regard to data order, and Ordinal Encoder, which performs encoding with regard to data order.
   
5. Split the train data and test data

   In this section, train data and test data are split using the sklearn train_test_split library to split dependent data and independent data, which are then processed
   
6. Oversample

    At this stage, after separating the data into training data and test data, oversampling is performed on the target variable. Oversampling is performed after the train–test split process with the aim of maintaining the authenticity of the test data. In addition, oversampling aims to improve model performance at the training stage and reduce bias towards minority classes.


   
## Modelling

In this project, several algorithms for classification testing and evaluation purposes, such as:

1. Logistic Regression

   Logistic Regression is a machine learning algorithm that estimates the probability of an event occuring, such as choosing or not choosing, based on a given dataset of independent variables
   
2. Random Forest

   An ensemble learning-based machine learning algorithm that combines multiple decision trees to produce more accurate and stable predictions than a single tree, working by taking random samples from data and features, then combining the results.
   
3. Decision Tree

   a machine learning and data mining method that uses a tree-like structure to make decisions or predictions by breaking down complex data into series of simple rules.
   
4. Support Vector Machine Learning (SVM)

   SVM ia a machine learning algorithm that works by processing data to generate a hyperlane that separates the input space into two classes, starting from the grouping of linear cases separated by the hyperlane

## Evaluation

The following is an evaluation of each algorithms used:

|                Algorithm                  |    Accuracy    |   Precision    |   Recall  |  F1 Score  |
|-------------------------------------------|----------------|----------------|-----------|------------|
| Random Forest                             |    0.965296    |    0.716547    | 0.546652  |  0.620174  |
| Logistic Regression                       |    0.844456	 |    0.232148    | 0.867179  |  0.366249  |
| Decision Tree                             |    0.560510    |    0.560510    | 0.579583  |  0.569887  |
| SVM                                       |    0.821187	 |    0.215741    | 0.929748  |  0.350217  |
| Random Forest (After Hypertune parameter) |    0.812425    |    0.210718    | 0.953897  |  0.345184  |
| Decision Tree (After Hypertune parameter) |    0.237948    |    0.237948    | 0.926454  |  0.378645  |


#### Confusion Matrix

There are several confusion metrics can predict diabetes status of patient. Such as:
1. Random Forest
   
   ![Metric](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Metric/RF%20Test.png)
   
3. SVM

   ![Metric1](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Metric/SVM%20Test.png)
   
5. Random Forest (After Hypertune Parameter)

   ![Metric2](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Metric/RF%20Hypertune%20parameter%20Test.png)
   
