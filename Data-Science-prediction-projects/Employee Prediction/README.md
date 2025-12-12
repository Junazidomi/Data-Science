# Employee Predidction 

## Business Understanding
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

2. Visualization of Gender VS Payment

   ![Age Category V Employee Leaving](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Gender%20vs%20Payment.png)

3. Visualization of Join Year VS Leave or Not

   ![Join Year vs Leaver or Not](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Join%20Year%20VS%20Leave.png)

4. Visualization of Leave or Not VS Payment Tier

   ![Leave or Not VS Payment Tier](github.com/Junazidomi/Data-Science/blob/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Employee%20Status%20VS%20Leave.png?raw=true)

5. Visualization of Gender VS Leave or Not

   ![Gender VS Leave or Not](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Employee%20Status%20VS%20Gender.png)

6. Visualization of Age Category vs Leave or Not

   ![Age Category vs Leave or Not](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Age%20Category%20vs%20Leave.png)
   
## Data Preparation
## Modelling
1. Logistic Regression
   Logistic Regression is a simple and interpretable
3. Random Forest
4. Decisin Tree
5. SVM
## Evaluation

Evaluate each algorithm used for both feature selection and parameter hypertuning

|                     Algoritma                  |   Accuracy   |   Precision   |    Recall    |    F1 Score    |
|------------------------------------------------|--------------|---------------|--------------|----------------|
| Logistic Regression                            |   0.640145   |   	0.542857   |   0.604545   |    0.572043    |
|  Random Forest                                 |   0.737794   |    0.707182   |   0.581818   |    0.638404    | 
|  Decision Tree                                 |   0.676311   |    0.594470   |   0.586364   |    0.590389    |
|       SVM                                      |   0.524412   |    0.439437   |   0.709091   |    0.542609    |
| Logistic Regression (After Feature Selection)  |   0.591320   |    0.489051   |   0.609091   |    0.542510    |
| Random Forest (After Feature Selection)        |   0.755877   |    0.763975   |   0.559091   |    0.645669    |
| Decision Tree (After Feature Selection)        |   0.764919   |    0.792208   |   0.554545   |    0.652406    |
| SVM (Feature Selection)                        |   0.589512   |    0.487179   |   0.604545   |    0.539554    |
| Random Forest (After Hypertune Parameter)      |   0.772152	 |    0.797468   |   0.572727   |    0.666667    |
| Decision Tree (After Hypertune Parameter)      |   0.757685   |    0.772152   |   0.554545   |    0.645503    |

