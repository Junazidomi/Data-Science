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

2. Visualization of Employee's Education

   ![Education](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Employee%20Education.png)

3. Visualization of The Employees' Place of Residence

   ![City](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Visualization%20of%20Employee.png)

4. Visualization of Employee's Payment Tier

   ![Payment Tier](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Payment%20Tier.png)

5. Visualization of Age Category
   
   ![Age Category](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Age%20Category.png)

6. Visualization of Employee Leaving

   ![Resign](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Leave%20or%20Not.png)

7. Visualization of Employee Join Year

   ![Join Year](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Employee%20Prediction/Picture/Employee%20Join%20Year.png)

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

6. Visualization of 
## Data Preparation
## Modelling
## Evaluation

