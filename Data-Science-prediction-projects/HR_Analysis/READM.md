# HR and Job Analysis Prediction

## Business Understanding
### Background
### Purpose
## Data Understanding

This dataset contains historical data on employees working at a company, covering various information related to employee conditions, such as number of working hours, department, salary, and other supporting data.

|       Feature         |  Data Type  |                                                Description                                                                                                 |                    
|-----------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| satisfaction_level    |    Float    | Employee satisfication level is a measured used to assess the extent to which employees feel satisfied with their jobs and work envirotment at the company |
| last_evaluation       |    Float    | Final evaluation score for employees                                                                                                                       | 
| number_project        |     Int     | The number of projects employees work on                                                                                                                   |
| average_montly_hours  |     Int     | Average working hours of employee                                                                                                                          |
| time_spend_company    |     Int     | Number of years an employee has been with the company                                                                                                      |
| Work_accident         |     Int     | Did employees experince any incidents while working at the company                                                                                         | 
| left                  |     Int     | Are employees leaving the company                                                                                                                          |
| promotion_last_5years |     Int     | Did the employee receive a promotion in the last 5 years                                                                                                   | 
| Department            |    String   | Employee Department                                                                                                                                        |
| salary                |    String   | Employee' salaries during their employment at the company each month                                                                                       | 

Key Findings:

1. 
### EDA

The following are some of the visualization such:
1. Visualization of 
## Data Preparation

1. Drop Duplicate Data

   At this stage, duplicate data is deleted to prevent bias in the model during the training process.
   
2. Encoding

   At this stage, feature transformation is performed, which involves converting categorical data in the dataset into  numerical data. The method used is One Hot Encoding, a technique that converts categorical data into numerical data representations without showing any order or hierarchy between categories.
   
3. Split Training Data and Test Data

   In this process, the dataset is divided into training data and testing data. The purpose of this division is so that after the model is trained using the training data, the model's performance can be evaluated using the testing data to determine the model's ability to predict new data.
    
4. Balance Data

   At this stage, after separating the data into training data and test data, oversampling is performed on the target variable. Oversampling is performed after the train–test split process with the aim of maintaining the authenticity of the test data. In addition, oversampling aims to improve model performance at the training stage and reduce bias towards minority classes.
   
## Modelling

In this project, several algorithms for classfication evaluation purpose such as:

1. Logistic Regression
2. Random Forest
3. Decision Tree
4. Gradient Boosting
5. XGBoost
   
## Evaluation
Evaluate each algorithm used :

|        Algorithm       |      Accuracy      |      Precision      |     Recall      |      F1-Score      |
|------------------------|--------------------|---------------------|-----------------|--------------------|
| Logistic Regression    |      0.781992      |       0.422785      |    0.832918     |      0.560873      | 
| Random Forest          |      0.979158      |       0.978202      |    0.895262     |      0.934896      |
| Decision Tree          |      0.970821      |       0.921120      |    0.902743     |      0.934896      |
| Gradient Boosting      |      0.967486      |       0.896806      |    0.910224     |      0.903465      |
| XGBoost                |      0.969987      |       0.908189      |    0.912718     |      0.910448      |
