# Diabetes Prediction

## Businees Understanding
### Background

Diabetes is one of the chronic diseases that continues to increase worldwide. This disease occurs when the human body experiences disturbances in regulating blood sugar levels, causing serious complications such as heart disease, kidney failure, and others. Therefore, early detection in predicting diabetes is very important in preventing this disease.

With the advancement of technology, particularly in the field of machine learning, large amounts of patient health data can be utilised to assist in the diagnosis of diseases. By utilising patient health history data, such as age, gender, medical history, and other supporting factors, machine learning models are able to learn patterns related to diabetes status.

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

- The dataset in this project has 8 numerical features (age, hypertension, hearth_disease, bmi, HbA1c_level,  blood_glucose_level, and diabetes ) and 2 categorical features (gender and smoking_history )
- Based on the results of dataset identification, two problematic were found. The age column has values less than 0, which causes inaccurate data because it is imposibble for diabetes patients to be less than 0 years old or the same age as baby. In addition, the gender column contains the unique value ‘Other’, so adjustments or changes to the data are necessary.
- Based on the missing values identification, the dataset does not contain any missing values, so no preprocessing  steps are requeired for handling missing data.
- From the duplicate data identification, there are 3584 duplicate rows were found, which could potentially cause bias in the analysis and modelling. Therefore, these duplicates should be removed to ensure accurate results during visualization and prediction.
- Based on the results of identifying outlier data in the numeric columns, outliers were found in the bmi, blood_glucose_level and HbA1c_level columns, thus requiring the handling of such outlier data.


### EDA

1. Visualization of Diabetes Status

   ![Visualization1](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Diabetes%20Status.png)

   Insight:

   Based on the visualisation of diabetes status, it was found that there were more people who did not have diabetes than those who did. In addition, because this column is an unbalanced target column, oversampling or undersampling must be performed. 

2. Visualization of Gender Patients

   ![Visualization2](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Gender.png)

   Insight:

   Based on the visualisation of patient gender, it was found that the majority of patients were female. In addition, there was a unique value of ‘Other’ in the gender column, so data preprocessing was necessary to clean the data and make it usable in the model training process.
   
3. Vizualization of Smoking History

   ![Visualization3](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Smoking%20History.png)

   Insight:

   Based on the visualization of patient's smoking history status, it can be seen the number of patients in the "No Info" category is the highest than other category, followed by patients who have never smoked. In addition, the number of patients with a history of smoking is relatively lower than in other categories
   
4. Visualization of Hypertension Status

   ![Visualization4](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Hypertension.png)

   Insight:
   Based on the visualisation of hypertension status, there are fewer patients with hypertension than patients without hypertension.
   
5. Visualization of Heart Disease

    ![Visualization5](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Heart%20Disease.png)

   Insight:

   Based on the visualisation of heart disease status, it was found that the number of patients with heart disease was lower than the number of patients without heart disease.
   
6. Visualization of Diabetes Status VS Medical Checkup

    ![Visualization6](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Diabetes%20Status%20vs%20medical%20checkup.png)

    Insight:

    Based on the visualisation of the relationship between diabetes status and medical check-up results, there are significant differences between patients with diabetes and those without diabetes. These differences can be observed in the variables of blood glucose level, BMI, and HbA1c, where patients with diabetes have higher values than patients without diabetes. In addition, patients who are susceptible to or have diabetes have a median age in the range of 50–70 years.
   
7. Visualization of Hearth Disease VS Medical Checkup

    ![Visualization7](https://github.com/Junazidomi/Data-Science/blob/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Heart%20Disease%20vs%20Medical%20Checkup.png?raw=true)

    Insight:

    Based on the visualisation of the relationship between heart disease and medical check-up results, it was found that patients suffering from heart disease were generally in the 60–80 age range. In addition, patients with heart disease had a slightly higher median BMI than patients without heart disease.
   
8. Visualization of Hypertension Status VS Medical Checkup
    
    ![Visualization8](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Hypertension%20vs%20medical%20checkup.png)

    Insight:

    Based on the visualisation of the relationship between hypertension status and medical check-up results, it was found that patients with hypertension had a median age in the range of 60–80 years. In addition, patients with hypertension tended to have higher median BMI, HbA1c, and blood glucose levels compared to patients without hypertension.
   
9. Visualization of Hearth Disease VS Diabetes Status

    ![Visualization9](https://github.com/Junazidomi/Data-Science/blob/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Heart%20vs%20Diabetes.png?raw=true)

    Insight:

    Based on the visualisation of the relationship between heart disease and diabetes status, it can be seen that the number of patients with diabetes is higher in the group of patients without heart disease. This is due to the dominance of patients without heart disease in the dataset. Meanwhile, the number of diabetic patients in the group with heart disease is relatively lower.
    
10. Visualization of Hypertension VS Diabetes Status

    ![Visualization10](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Hypertension%20vs%20Diabetes.png)

    Insight:

    Based on the visualisation of the relationship between hypertension status and diabetes status, it can be seen that the number of patients with diabetes is higher in the group of patients without hypertension. This is due to the dominance of patients without hypertension in the dataset. Meanwhile, the number of diabetic patients in the group with hypertension is relatively lower.
    
11. Visualization of Smoking History VS Diabetes

    ![Visualization11](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Smoking%20history%20vs%20Diabetes.png)

    Insight:

    Based on the visualisation of smoking history versus diabetes status, the highest number of diabetes cases was found among patients who had never smoked. Meanwhile, patients who had smoked had the lowest diabetes rate compared to other smoking categories.
    
12. Visualization of Numerical Feature

    ![Visualuzation12](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Picture/Heatmap.png)

    Insight:

    Based on the visualisation of the correlation between numerical features, age has a higher correlation with BMI than the correlation between numerical features. Furthermore, none of the correlations between numerical features have negative values.
    
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
   
2. SVM

   ![Metric1](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Metric/SVM%20Test.png)
   
3. Random Forest (After Hypertune Parameter)

   ![Metric2](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Diabetes%20Prediction/Metric/RF%20Hypertune%20parameter%20Test.png)

## Conculusion
- Based on the results of data analysis, patients with diabetes tend to have higher blood sugar levels and BMI compared to patients without diabetes. In addition, patients who are susceptible to or suffer from diabetes are generally between the ages of 55 and 70. The results of the analysis also show a link between diabetes and heart disease and hypertension.
- The best models for making predictions are Random Forest, Random Forest (After Hypertune parameter) and SVM.
- After hyperparameter tuning was performed on the Decision Tree and Random Forest, it was found that the R2 values for both algorithms decreased, while the recall values actually increased
