# Student Test Score Predictions
## Business Understanding
### Background
### Purpose

The purpose of the Student Test Score Predictions is to help teachers and parent monitor student progress, particularly in monitoring test scores based on student`s internal and external conditions, as well as supporting decision-making to improve the student learning process.

## Data Understanding

This dataset provides a comprehensive overview of various factors affecting student performance in exams It includes information on study, habits, attedance, parental involvement, and other aspects influencing academic success. Dataset:[Student Performance Dataset](https://www.kaggle.com/datasets/lainguyn123/student-performance-factors).

|            Feature            |     Data Type     |                                  Descriptions                                  |
|-------------------------------|-------------------|--------------------------------------------------------------------------------|
| Hours_Studied                 |       Int         | Number of Hours spend studying per week                                        |
| Attedance                     |       Int         | Percentage of classes attended                                                 |
| Parental_involvement          |      String       | Level of parental involvement in the student's education  (Low, Medium, High). |
| Access_to_Resources           |      String       | Availability of educational resources (Low, Medium, High).                     |
| Extracurricular_Activities    |      String       | Participation in extracurricular activities (Yes, No).                         |
| Sleep_Hours                   |       Int         | Average number of hours of sleep per night                                     |
| Previous_Scores               |       Int         | Scores from previous  exams.                                                   |
| Motivation_Level              |      String       | Student's level of motivation (Low, Medium, High).                             |
| Internet_Access               |      String       | Availability of internet access (Yes, No).                                     |
| Tutoring_Sessions             |       Int         | Number of tutoring sessions attended per month                                 |
| Family_Income                 |      String       | 	Family income level (Low, Medium, High).                                     |
| Teacher_Quality               |      String       | Quality of the teachers (Low, Medium, High).                                   |
| School_Type                   |      String       | Type of school attended (Public, Private).                                     |
| Peer_Influence                |      String       | Influence of peers on academic performance (Positive, Neutral, Negative).      |
| Physical_Activity             |       Int         | Average number of hours of physical activity per week.                         |
| Learning_Disabilities         |      String       | Presence of learning disabilities (Yes, No).                                   |
| Parental_Education_Level      |      String       | Highest education level of parents (High School, College, Postgraduate).       |
| Distance_from_Home            |      String       | Distance from home to school (Near, Moderate, Far).                            |
| Gender                        |      String       | Gender of the student (Male, Female).                                          |
| Exam_Score                    |       Int         | Final exam score.                                                              |

Key Findings:

- The dataset consists of 20 columns and 6,607 rows, covering 13 categorical columns and 7 numeric columns, with Exam Score as the dependent variable. In addition, categorical data will undergo feature transformation, which is the process of converting categorical data into numerical representations so that it can be processed by machine learning models.
- After identifying missing values, it was found that there was missing data in the Teacher_Quality for 78 cases, Parental_Education_Level for 90 cases and Distance_From_Home for 67 cases. Therefore, it was necessary to process this data before proceeding to the analysis and modelling stages
- After identifying the data, an invalid value was found in Exam_Score column, namely a value of 101. Therefore, it is necessary to handle irrelevant data in that column before the analysis and modelling process is carried out.
- After the duplicate data identification process was carried out, no duplicate data was found in the dataset
- After the outlier identification process was carried out, outliers were found in the Hours Studied, Tutoring Sessions, and Exam Score features. Therefore, outlier handling is required, for example by deleting outlier data or performing feature transformation.
  
### EDA

The following is the visualization obtained:

1. Visualization of Access Resources Level of Student

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/StudentPerformAnalysis/Picture/Access%20To%20Resource.png" width="350">

   Insight:
   
3. Visualization of Extracurricular Activities of Student

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/StudentPerformAnalysis/Picture/Activities.png" width="350">

   Insight:
   
5. Visualization of Distance From Home Level of Student

   <img src="https://github.com/Junazidomi/Data-Science/blob/main/Data-Science-prediction-projects/StudentPerformAnalysis/Picture/Distance%20From%20Home.png" width="350">

   Insight:
   
7. Visualization of Family Income of Students

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/StudentPerformAnalysis/Picture/Family%20Income.png" width="350">
   
9. Visualization of Gender of Student

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/StudentPerformAnalysis/Picture/Gender.png" width="350">

    Insight:
   
11. Visualization of Internet Access of Students

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/StudentPerformAnalysis/Picture/Internet%20Access.png" width="350">

    Insight:
    
13. Visualization of Motivation Level of Students

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/StudentPerformAnalysis/Picture/Motivation%20Level.png" width="350">

    Insight:
    
15. Visualization of Parental Involvement Level of Students

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/StudentPerformAnalysis/Picture/Parental%20Involvement.png" width="350">

    Insight:
    
17. Visualization of School Type of Students

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/StudentPerformAnalysis/Picture/School%20Type.png" width="350">

    Insight:
    
19. Visualization of Gender VS Categorical Columns

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/StudentPerformAnalysis/Picture/Gender%20vs%20Kategorikal%20Columns.png" width="370">

    Insight:
    
21. Visualization of School Type VS Teacher Quality

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/StudentPerformAnalysis/Picture/School%20Type%20vs%20Teacher%20Quality.png" width="350">

    Insight:
    
23. Visualization of Exam Score VS School Condition

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/StudentPerformAnalysis/Picture/Student%20Factor%201%20by%20Exam%20Score.png" width="370">

    Insight:
    
25. Visualization of Exam Score VS Parental Condition

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/StudentPerformAnalysis/Picture/Student%20Factor%203%20by%20Exam%20Score.png" width="350">

    Insight:
    
27. Visualization of Exam Score VS Student Factor

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/StudentPerformAnalysis/Picture/Student%20Factor%20by%20Exam%20Score.png" width="370">

    Insight:
    
29. Heatmap of Numerical Feature

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/StudentPerformAnalysis/Picture/Heatmap%20of%20Numerical%20Features.png" width="350">

    Insight:
    
## Data Preparation

The data preparation is as follows:


1. Drop Data Missing

   The purpose of this process is to maintain the consistency of the dataset used for training, as most machine learning models cannot handle missing values, except for certain algorithms such as XGBoost and CatBoost.
   
2. Drop Irrelevant Value
   
   Remove irrelevant values to maintain dataset consistency.
   
3. Encoding

   This process is often referred to as feature transformation, which involves converting categorical columns into numerical or binary form so that it can be used in the model training process and fulfill the mathematical requirements of machine learning algorithms.
   
4. Normalization

   Normalization is the process of converting numerical data using into a specific scale with the purpose of equalizing the range  of values for each numerical feature used in the model training process
   
5. Split the Training Data and Test Data

   In this section, train data and test data are split using sklearn train_test_split library to split dependent and independent data, which are then processed.
   
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
   
5. Gradient Boosting
   
   Gradient boosting is an ensemble machine learning algorithm that builds predictive models incrementally by combining several weak models (usually decision trees) into a strong model.
   
6. XGBoost

   XGBoost uses ensemble learning techniques, which combine predictions from multiple models to improve overall performance. This approach is based on boosting techniques, where weak learners, usually simple decision trees, are combined into a strong learner
   
## Evaluation

The following is an evaluation of each algorithm used:
|                   Algorithm                   |      MAE      |      MSE      |      R2      |
|-----------------------------------------------|---------------|---------------|--------------|
| Linear Regression                             |    0.481179   |    4.153024   |   0.732741   |
| Random Forest                                 |    1.127241   |    5.781225   |   0.627962   |
| Decision Tree                                 |    1.803292   |    3.831505   |   0.109903   |
| SVM                                           |    0.472190   |    4.191744   |   0.730249   |
| Gradient Boosting                             |    0.824530   |    4.630725   |   0.702000   |
| XGBoost                                       |    0.797267   |    4.780617   |   0.692354   |
| Random Forest (After Hypertune Parameter)     |    1.077207   |    5.312493   |   0.658126   |
| XGBoost (After Hypertune Parameter)           |    0.797267   |    4.780617   |   0.692354   |
| Gradient Boosting (After Hypertune Parameter) |    0.677934   |    4.476078   |   0.711952   |







