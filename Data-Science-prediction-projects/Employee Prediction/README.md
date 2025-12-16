# Employee Predidction 

## Business Understanding

### Background

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Employee attrition is a significant challenge for companies because it can disrupt productivity and increase recruitment costs, which many companies in India face. Without a deep understanding of the factors that drive employees to resign, retention efforts are often ineffective.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Therefore, a data-driven approach is needed, utilizing historical employee data in India to identify patterns and predict employees who are likely to resign. This approach is expected to assist companies in strategic planning and policy improvement through predictive models built from historical company data.

### Purpose

The goal of this project is to create a model that can predict which employees are most likely to leave the company, so that the HR department can implement preventive measures before that happens.


## Data Understandings

This Dataset describes several features related to predicting employee resignations based on the criteri in this dataset. The following is an overview of the features contained in this dataset. [Link](https://www.kaggle.com/datasets/tejashvi14/employee-future-prediction)


|         Features          |     Data Type     |                Description                         |
|---------------------------|-------------------|----------------------------------------------------|
|     Education             |      String       |    Education Level                                 |
|   Joining Year            |       Int         |Year of joining year                                |
|      City                 |      String       |City office where posted                            |
|    Payment Tier           |       Int         |Payment tier:1:Highest, 2:Mide Level, 3:Lowest      |
|      Age                  |       Int         |Current age                                         |
|     Gender                |      String       |Gender of employee                                  |
|    EverBenched            |      String       |Ever kept out of projects for 1 month or more       |
|ExperienceInCurrentDomain	|        Int        |Experince in current field                          |
|    LeaveOrNot             |       Int         |Whether employee leaves the company in next 2 years |

Key Findings:
- Based on the dataset information, the dataset consists of 5 numerical features (Joining Year, Payment Tier, Age, ExperienceInCurrentDomain, and LeaveOrNot) and 4 categorical features (Education, City, Gender, and EverBenched), with a total of 4,653 rows.
- From the statistical summary, it is observed that the age range of the employees is 22–41 years, and their work experience ranges from 0–7 years, indicating that the company employs individuals from junior to professional levels.
- From the duplicate data identification, 1,889 duplicate rows were found, which could potentially cause bias in the analysis and modeling. Therefore, these duplicates should be removed to ensure accurate results during visualization and prediction.
- Based on the missing values identification, the dataset does not contain any missing values, so no preprocessing steps are required for handling missing data.

### EDA
#### Univariate

1. Visualization of Gender

   ![Gender](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Gender.png)

   Insight:

   Based on the Employee Gender chart, male employees constitue the largest gender group in the company, with a higher number than female employees
2. Visualization of Employee's Education

   ![Education](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Employee%20Education.png)

   Insight:

   The visualization shows that the majority of employees have a bachelor's degree. On the other hand, employees with a PhD are the smallest group in the company

3. Visualization of The Employees' Place of Residence

   ![City](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Visualization%20of%20Employee.png)

Insight:

Based on the visualization of Employee's hometowns, it appears that the majority of employees come from Bangalore. Although their total numbers are lower than those from Bangalore, employees from Pune and New Delhi also contribute to the total number of employees in the company. 

4. Visualization of Employee's Payment Tier

   ![Payment Tier](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Payment%20Tier.png)

   Insight:

   Based on the payment tier visualization, the majority of employees are in payment tier 3(High), which indicates that most employees receive high salaries

5. Visualization of Age Category
   
   ![Age Category](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Age%20Category.png)

   Insight:

   Based on the visualization of Age Categories, it can be seen that the junior age group is the biggest than other categories. Meanwhile, the manejerial category is the smallest category compare to other categories

6. Visualization of Employee Leaving

   ![Resign](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Leave%20or%20Not.png)
   
Insight:

Based on the visualization of employee resignation status, it appears that the majority of employees choose to remain working at the company. However, the number of employees who plan to resign is also quite significant, namely around half of the number of employees who choose to stay.

7. Visualization of Employee Join Year

   ![Join Year](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Employee%20Join%20Year.png)


Insight: 

Based on the visualization of the year employees joined the company, it can be seen that the highest number of employees joined in 2017. This year marked the peak of the company's recruitment. However, in 2018, there was a drastic decline in the number of employees joining, making it the year with the fewest recruitments. This sharp decline may indicate changes in labor needs, stricter recruitment policies, or different company conditions compared to the previous year.

#### Bivariate

1. Visualization of Payment VS Education

   ![Payment VS Education](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Payment%20vs%20Education.png)

Insight:

It was found that employees at every level of education were generally in the high payment tier (3), while only a small proportion of employees from each level of education were in the low payment tier (1).

2. Visualization of Gender VS Payment

   ![Age Category V Employee Leaving](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Gender%20vs%20Payment.png)

Insight: 

It was found that employees of both genders were mostly in the high payment tier (3), while the number of employees in the low payment tier (1) was the smallest for each gender.

3. Visualization of Join Year VS Leave or Not

   ![Join Year vs Leaver or Not](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Join%20Year%20VS%20Leave.png)

Insight:

It was found that the majority of employees who resigned from the company were those who joined in 2018, while the lowest number of resignations came from employees who joined in 2012. This indicates potential employee dissatisfaction with the company. In addition, the low resignation rate among employees who joined in 2012 shows that these employees have been able to adapt to the company environment.

4. Visualization of Leave or Not VS Payment Tier

   ![Leave or Not VS Payment Tier](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Employee%20Status%20VS%20Leave.png)

Insight: 

Based on this visualization, it was found that the highest number of resignations came from the high-income group. This indicates that even though employees receive high salaries, the company may have high work demands, such as excessive working hours. In addition, this condition may also indicate that employees choose to resign because they are attracted to job opportunities at other companies that offer higher compensation with lower work demands.

5. Visualization of Gender VS Leave or Not

   ![Gender VS Leave or Not](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Employee%20Status%20VS%20Gender.png)

Insight:

Based on the visualization above, it was found that female employees were the group that resigned from the company the most. This indicates the possibility that the company has not fully implemented the principle of gender equality in the work environment.

6. Visualization of Age Category vs Leave or Not

   ![Age Category vs Leave or Not](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Age%20Category%20vs%20Leave.png)

Insight:

Berdasarkan visualisasi di atas, ditemukan bahwa karyawan pada level junior memiliki jumlah pengunduran diri yang lebih tinggi dibandingkan dengan kategori lainnya.
   
## Data Preparation

The data preparation process is as follows:

1. Drop Data Duplicate

   At this stage, data is first identified to detect the existence of duplicate data. Once duplicate data is found, it is deleted to prevent bias in the data and maintain data consistency and quality.
   
2. Encoding
   
    This part of the process transforms categorical data into numerical data to facilitate model training. In addition, numerical data is required for modeling. The methods used are LabelEncoder, OrdinalEncoder, and others. 

3. Split the train data and test data

   In this section, train data and test data are split using the sklearn train_test_split library to split dependent data and independent data, which are then processed.
   
4. Oversample

   At this stage, after separating the data into training data and test data, oversampling is performed on the target variable. Oversampling is performed after the train–test split process with the aim of maintaining the authenticity of the test data. In addition, oversampling aims to improve model performance at the training stage and reduce bias towards minority classes.
   
5. Feature Selection

   At this stage, after modeling, if it is found that the model performance is not yet optimal, then feature selection is performed with the aim of selecting features or reducing the number of features related to the target variable. The method used in this project is Recursive Feature Elimination (RFE).

## Modelling
1. Logistic Regression
   
   Logistic Regression is an algorithm that estimates the probability of an event occuring, such as choosing or not choosing, based on a given dataset of independent variables
   
2. Random Forest

   Random Forest is a widely used machine learning algorithm that combines the results of several decision trees to achieve a single result that is easy to use and flexible
   
3. Decisin Tree

   Decision trees are supervised, non-parametric learning algorithms that  have a hierarchical tree structure, consisting of root nodes, branches, internal nodes, and leaf nodes.
   
4. SVM

   SVM is a classification algorithm that finds the optimal hyperplane to separate classes, performing well in high-dimensional spaces.
## Evaluation

Evaluate each algorithm used for both feature selection and parameter hypertuning

|                     Algoritma                                      |   Accuracy   |   Precision   |    Recall    |    F1 Score    |
|--------------------------------------------------------------------|--------------|---------------|--------------|----------------|
| Logistic Regression                                                |   0.640145   |   	0.542857   |   0.604545   |    0.572043    |
|  Random Forest                                                     |   0.737794   |    0.707182   |   0.581818   |    0.638404    | 
|  Decision Tree                                                     |   0.676311   |    0.594470   |   0.586364   |    0.590389    |
|       SVM                                                          |   0.524412   |    0.439437   |   0.709091   |    0.542609    |
| Logistic Regression (After Feature Selection)                      |   0.591320   |    0.489051   |   0.609091   |    0.542510    |
| Random Forest (After Feature Selection)                            |   0.755877   |    0.763975   |   0.559091   |    0.645669    |
| Decision Tree (After Feature Selection)                            |   0.764919   |    0.792208   |   0.554545   |    0.652406    |
| SVM (Feature Selection)                                            |   0.589512   |    0.487179   |   0.604545   |    0.539554    |
| Random Forest (After  Feature Selection and Hypertune Parameter )  |   0.772152	|    0.797468   |   0.572727   |    0.666667    |
| Decision Tree (After  Feature Selection and Hypertune Parameter)   |   0.757685   |    0.772152   |   0.554545   |    0.645503    |

**Confusion Matrix**

The best model is Random forest (After Feature Selection and Hypertune Parameter). The following is the confusion matrix of the Random Forest

![RF Test](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Metric/RF%20Test.png)

Conclusion:

- The best model for predicting employee resignations from a company is Random Forest, after feature selection and hyperparameter tuning.
- After feature selection, an improvement in metric performance was obtained for each algorithm. In addition, the feature selection results showed that the selected features were “JoiningYear, City, PaymentTier, Gender, and EverBenched”.
- The best model for predicting employee resignations from a company is the Random Forest model after feature selection and hyperparameter tuning, as it achieves the highest F1-score compared to other algorithms, although the SVM model has the highest recall score.
- Based on the confusion matrix, it can be concluded that the model performs well in predicting employees who will not resign. However, out of  220 employees who resigned, only 126 were correctly predicted. This shows that the model still has a significant number of false negatives. Thus, although the model is quite good overall, it tends to be more effective in predicting employees who will not resign than those who will resign.
