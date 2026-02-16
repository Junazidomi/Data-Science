# Student Test Score Predictions
## Business Understanding
### Background
### Purpose

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

### EDA

The following is the visualization obtained:

1. Visualization of Access Resources Level of Student
2. Visualization of Extracurricular Activities of Student
3. Visualization of Distance From Home Level of Student
4. Visualization of Family Income of Students
5. Visualization of Gender of Student
6. Visualization of Internet Access of Students
7. Visualization of Motivation Level of Students
8. Visualization of Parental Involvement Level of Students
9. Visualization of School Type of Students
10. Visualization of Gender VS Categorical Columns
11. Visualization of School Type VS Teacher Quality
12. Visualization of Exam Score VS School Condition
13. Visualization of Exam Score VS Parental Condition
14. Visualization of Exam Score VS Student Factor
15. Heatmap of Numerical Feature
    
## Data Preparation

The data preparation is as follows: 
1. Encoding
2. Normalization
3. Split the Training Data and Test Data
   
## Modelling

In this project, several algorithms for regression evaluation purpose such as:

1. Linear Regression
2. Random Forest
3. Decision Tree
4. SVM
5. Gradient Boosting
6. XGBoost
   
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


