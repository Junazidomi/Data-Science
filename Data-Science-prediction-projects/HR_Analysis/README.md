 # HR and Job Analysis Prediction

## Business Understanding
### Background

In an increasingly digital age, organizations are required to manage their human resources more effectively and in a data-driven manner. Human resources (HR) is not longer limited to administrative and operational tasks but also plays a strategic role in decision-making

However, the company is facing a trend of employees leaving their jobs, which poses a challenge for the HR department. The process of recruiting new employees requires significant time and resources, forcing the company to invest additional effort. Therefore, a system is needed that can predict whether an employee will leave or not, based on historical employee data within the company. 

### Purpose

The objective of this project is to analyze and predict employee leave based on historical data, as well as to assist Human Resources (HR) in managing employees who are likely to leave the company and those who are likely to stay. In addition, this project also aims to assist the company in evaluating policies or regulations related to employees.

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

1. The dataset consists of 10 columns and 14999 rows, with 6 columns of integer data type, 2 columns of float data type, and 2 columns of object data type. The columns with the object data type will perform a feature transformation.
   
2. After identifying missing data in the dataset, there is no missing data

3. After identifying duplicate data in the dataset, 3008 rows were found to be potential duplicates, necessitating futher action to address the issue

4. After identifying outliers, no outliers were found in the dataset.

### EDA

The following are some of the visualization such:

1. Visulization of 5 Years Promoting

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/HR_Analysis/Picture/5%20Years%20Promotion.png" width="350"/>

   Insight:

   Based on the visualization above, it can be seen that the number of employees who have received promotions over the past five years is relative small.
   
2. Visualization of Department

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/HR_Analysis/Picture/Department.png" width="350"/>

   Insight:

   Based on the visualization of employee numbers, it can be seen that the Sales department has the largest number of employees, followed by the IT department, while the department with the fewest employees is the Management department.
   
3. Visualization of Left Status

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/HR_Analysis/Picture/Left%20Status.png" width="350"/>

   Insight:

   Based on the visualization of the number of employees who have left the company, it can be seen that the number of employees who have left is smaller than the number of employees who remain with the company. 
   
4. Visualization of Salary

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/HR_Analysis/Picture/Salary.png" width="350"/>

   Insight:

   Based on the visualization of employees levels by salary, it can be seen that the number employees in the medium salary category is the highest compared to other salary categories.
   
5. Visualization of Time Spend Company

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/HR_Analysis/Picture/Time%20spend%20company.png" width="350"/>

   Insight:

   Based on the visualization of employees’ tenure at the company, it can be seen that the number of employees who have been with the company for 3 years is the highest compared to other tenure periods. In addition, the number of employees who have been with the company for 7, 8, and 10 years is the lowest. This indicates that most employees at the company do not stay for very long.
   
6. Visualization of Work Accident

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/HR_Analysis/Picture/Work%20Accident.png" width="350"/>

   Insight:

   Based on the visualisation of workplace accidents, it can be seen that only a small proportion of employees—namely 15.4%—have suffered workplace accidents, whilst the majority of employees have not had any accidents at work.
   
7. Visualization of Number of Project

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/HR_Analysis/Picture/Number%20of%20project.png" width ="350"/>

   Insight:

   Based on the visualization of the number of projects taken on by employees, it can be seen that the majority of employees took on 3 projects, followed by 4 projects. Meanwhile, the number of employees who took on 7 projects was the lowest
   
8. Visualization of Department by Salary

   <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/HR_Analysis/Picture/Department%20by%20salary.png" width="350"/>

   Insight:

   Based on the visualization of employees by department and salary level, it can be seen that the Sales department has the largest number of employees, but the majority of its staff fall into the low and medium salary categories. Meanwhile, the Technical department has the highest number of employees in the high salary category compared to other departments. Overall, in every department, the majority of employees fall into the low and medium salary categories.
   
9. Visualization of Left Status VS Numerical Columns

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/HR_Analysis/Picture/Left%20Status%20vs%20Numerical%20Columns.png" width="350"/>

    Insight:
    
    Based on the visualisation of employees by departure status using numerical columns, it can be seen that in the visualisation of departure rates against satisfaction levels, employees who have left the company have a different range of values compared to those who remain in employment. Furthermore, based on the last evaluation, employees who have resigned tend to have higher evaluation scores than those who have not resigned
   
10. Visualization of Department by Left

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/HR_Analysis/Picture/department%20by%20left.png" width="350"/>

    Insight:

    Based on the visualisation by department on the left, it can be seen that the Sales department has the highest number of resignations, whilst also having the largest number of employees compared to the other departments. Meanwhile, the department with the fewest resignations is the Management department.
    
11. Heatmap of Numerical Feature

    <img src="https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/HR_Analysis/Picture/heatmap.png" width="350"/>

    Insight:
    
    Based on the heatmap visualisation of the numerical columns, it can be seen that the highest correlation is between average_monthly_hours and number_project, with a correlation coefficient of 0.33. Meanwhile, the lowest correlation is between time_spend_company and satisfaction_level, with a correlation coefficient of -0.15.
    
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

   Logistic Regression is an algorithm that estimates the probability of an event occuring, such as choosing or not choosing, based on a given dataset of independent variables
   
2. Random Forest

   Random Forest is a widely used machine learning algorithm that combines the results of several decision trees to achieve single result that is easy to use and flexible
   
3. Decision Tree

   Decision Trees are supervised, non-parametric learning algorithms that have a hierarchical tree structure, consisting of root nodes, branches, internal nodes, and leaf nodes.
   
4. Gradient Boosting

   Gradient Boosting is a powerful ensemble machine learning technique that builds predictive models, typically decision trees, in a sequential, iterative manner to minimize errors used for tabular data, regression and classification
   
5. XGBoost

   XGBoost (eXtreme Gradient Boosting) is a very fast, efficient, and accurate ensemble learning (boosting approach) machine learning algorithm for classification and regression.
   
## Evaluation
Evaluate each algorithm used :

|        Algorithm       |      Accuracy      |      Precision      |     Recall      |      F1-Score      |
|------------------------|--------------------|---------------------|-----------------|--------------------|
| Logistic Regression    |      0.781992      |       0.422785      |    0.832918     |      0.560873      | 
| Random Forest          |      0.979158      |       0.978202      |    0.895262     |      0.934896      |
| Decision Tree          |      0.970821      |       0.921120      |    0.902743     |      0.911839      |
| Gradient Boosting      |      0.967486      |       0.896806      |    0.910224     |      0.903465      |
| XGBoost                |      0.969987      |       0.908189      |    0.912718     |      0.910448      |

### Confusion Matrix
The best model is Random forest. The following is the confusion matrix of the Random Forest.


Conculusion
- After the training process using several algorithms, the results showed that the most suitable algorithm  for this dataset was Random Forest, with the highest F1 Score of 0.934896 and the highest precision of 0.9780202. Meanwhile, the least suitable algorithm for this dataset was Logistic Regression, as seen from its evaluation metrics, which were the lowest compared to other algorithms.
- Based on the result of the confusion matrix, it can be seen that the model is able to predict the data very well. This is evident from the relatively small number of false negatives, amounting to 42. Futhermore, the model is also able to distinguish between the two classes effectively, as the number of correct predictions is significantly higher than the number of incorrect predictions.
- Hyperparameter tuning was not performed in this project because the metrics obtained already showed excellent performance.
- In this project, all features or variables in the dataset support predictions about whether employees will stay or leave.
