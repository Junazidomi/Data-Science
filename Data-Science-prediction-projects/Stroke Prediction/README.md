# Stroke Prediction

## Business Understanding
### Background

### Purpose
## Data Understanding

According to the World Health Organization (WHO) stroke is the 2nd leading cause of death globally, responsible for approximately 11% of total deaths. This Dataset is used to predict whether a patient is likely to get stroke based on the input parameters like gender, age, various diseases, and smoking status. Each row in the data provides relavant information about the patient. [Stroke Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)

|     Features     |     Data Type     |                                   Description                                          |
|------------------|-------------------|----------------------------------------------------------------------------------------|
|        Id        |        Int        |  Uniqie identifier patient                                                             |
|       gender     |       String      | "Male", "Female" or "Other"                                                            |
|   hypertension   |        Int        | 0 if the patient does not have hypertension, 1 if the patient has hypertension         |
|   heart_disease  |        Int        | 0 if the patient does not have any heart disease, 1 if the patient has a heart disease |
|   ever_married   |       String      | "No" or "Yes"                                                                          |
|    work_type     |       String      | "children", "Gov_jov","Never_worked", "Private", or "Self-employed"                    | 
|  residence_type  |       String      | "Rural" or "Urban"                                                                     |
|avg_glucode_level |       Float       | average glucose level in blood                                                         |
|        bmi       |       Float       | body mass index                                                                        |
|  smoking_status  |       String      | "formely smoked", "never smoked", "smokes" or "Unknows"                                |
|      stroke      |       Int         | 1 if the patient had a stroke or 0 if not                                              | 

Note: "Unknown" in smoking status means that the information is unavailable for this patient

Key Findings:
- The dataset contains 12 columns and 5110 rows of data, including 7 numeric columns and 5 categorical columns. The id column will be dropped as it is irrelevant, while the stroke column will be used as the target variable
- After identifying duplicate data, it can be concluded that there is no duplicate data in the dataset
- After identifying process for missing data was carried out, 201 data with missing values were found, so the process of handling missing data was then carried out
- After the EDA process was carried out, in the gender column there was a value of “Other” which was invalid because there are only two genders. In addition, in the target column, namely stroke, there was an imbalance in values.
### EDA

The following are some of the visualisations such:

1. Visualization of Gender

   ![Viz1](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Stroke%20Prediction/Picture/Gender.png)

   Insight:

   Based on the visualisation of patient gender distribution, it can be concluded that female patients are the most numerous compared to other genders. In addition, the ‘Other’ category will undergo preprocessing because it is considered irrelevant, given that in this analysis gender is limited to two categories.
2. Visualization of Heart Disease

   ![Viz](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Stroke%20Prediction/Picture/Heart%20Disease'.png)

   Insight:

   Based on the visualization of heart disease status, it can be concluded that there are more patients who do not have heart disease than those who do.
   
3. Visualization of Hypertension Status

   ![Viz3](https://github.com/Junazidomi/Data-Science/blob/main/Data-Science-prediction-projects/Stroke%20Prediction/Picture/Hypertension%20Status.png?raw=true)

   insight:

   Based on the visualization of hypertension status, it can be concluded that there are more patients who do not have hypertension than those who do.
   
4. Visualization of Stroke Status

   ![Viz4](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Stroke%20Prediction/Picture/Stroke%20Status.png)

   Insight:

   Based on the visualisation of stroke status, it can be concluded that there are far less patients who have had a stroke compared to those who have not. Therefore, as this feature is used as the target column, data balancing is performed between patients who have had a stroke and those who have not.
   
5. Visualization of Married Status
   
   ![Viz5](https://github.com/Junazidomi/Data-Science/blob/main/Data-Science-prediction-projects/Stroke%20Prediction/Picture/Married%20Status.png?raw=true)

   Insight:
   Based on the visualisation of marital status, it can be concluded that there are more married patients than unmarried patients.
   
6. Visualization of Resident Type

   ![Viz6](https://github.com/Junazidomi/Data-Science/blob/main/Data-Science-prediction-projects/Stroke%20Prediction/Picture/Resident%20Type.png?raw=true)

   insight:

   Based on the visualisation of residence type, it can be concluded that patients living in urban areas are slightly more numerous than those living in rural areas, although the difference is not particularly significant.
   
7. Visualization of Work Type

   ![Viz7](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Stroke%20Prediction/Picture/Work%20Type.png)

   Insight:

   Based on the visualisation of work types, it can be concluded that the Private category is the most numerous compared to other categories, while the Government Job category has the smallest number compared to other categories.
   
8. Visualization of Smoking Status

    ![Viz8](https://github.com/Junazidomi/Data-Science/blob/main/Data-Science-prediction-projects/Stroke%20Prediction/Picture/Smoking%20Status.png?raw=true)

    Insight:

    Based on the visualisation of smoking status, it can be concluded that patients who have never smoked have the largest percentage, around 37% followed by the ‘Unknown’ category at 30.2%, indicating that information on the patient's smoking history is unavailable. Meanwhile, the category with the smallest percentage is smokers, around 15.4%.
   
9. Stroke vs Medical Data

    ![Viz9](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Stroke%20Prediction/Picture/Stroke%20vs%20Medical.png)

   Insight:

   Based on the visualisation of the relationship between patients' numerical features and stroke status, it can be seen that for the age feature, patients who experienced a stroke had a median age in the range of 60–80 years, while patients who did not experience a stroke had a median age of around 20–60 years. For the avg_glucose_level feature, patients who experienced a stroke had a median in the range of 100–200, which was higher than patients who did not experience a stroke. Meanwhile, for the BMI feature, patients who experienced a stroke had a slightly higher median than patients who did not experience a stroke.
   
10. Categorical Feature vs Stroke Status

    ![Viz10](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Stroke%20Prediction/Picture/Categorical%20Feature%20vs%20stroke%20status.png)

    Insight:

    Based on the visualisation of the relationship between work type and stroke status, it can be seen that patients with private sector jobs had the highest number of stroke cases. Furthermore, in the visualisation of gender in relation to stroke status, female patients have a higher number of stroke cases compared to other genders. Meanwhile, in terms of residence type, there is no significant difference between patients who experience stroke in urban and rural areas. In addition, based on the visualisation of smoking status, it was found that patients who have never smoked also have a number of stroke cases.
    
11. Heatmap of Numerical Feature

    ![Viz11](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Stroke%20Prediction/Picture/Heatmap.png)

    Insight:

    Based on the visualisation of correlations between numerical features, it can be concluded that there is a positive relationship between several variables. The highest correlation is seen in age and BMI with a value of 0.33, which indicates that an increase in age tends to be followed by an increase in BMI. Furthermore, age and avg_glucose_level have a correlation of 0.24, which indicates that average glucose levels tend to increase with age. Meanwhile, BMI and avg_glucose_level have a correlation of 0.18, which indicates a positive but relatively weak relationship. Overall, although there are correlations between numerical features, their strength is still classified as low to moderate, so that each feature still provides relatively independent information in the analysis.
    
## Data Preparation

The data preparation process is as follows:
1. Drop irrelevant Column
 
   In this process, irrelevant columns are removed (dropped) so that the model can work optimally and avoid performance degradation and unnecessary bias
   
2. Missing Data Handling
   
   In this process, missing data is dropped so that no errors occur in the modelling.
   
3. Mismatch Data Handling

   In this process, after obtaining the data summary, data that is inaccurate or irrelevant is deleted (dropped) because it can affect the quality of the machine learning model in making predictions, such as the age column that has values below 0 and the gender column that has the value Other.

4. Encoding

   This part of the process converts categorical data into numerical data to facilitate model training. In addition, numerical data is required for modelling. In this project, the method used is standard encoding that does not take order into account.
   
5. Feature Scaling

   Feature scaling is a preprocessing technique that aims to convert feature values into a uniform scale, so that each feature can contribute equally to the model formation process. This technique is important because differences in range, units, or magnitude between features can affect the performance of machine learning models. In this study, the feature scaling technique used is standardisation.
   
6. Split the Training Data and Test Data

   In this section, train data and test data are split using the sklearn train_test_split to split dependent data and independent data, which are then processed.
   
7. Oversample

   At this stage, after separating the data into training data and test data, oversampling is performed on the target variable. Oversampling is performed after the train–test split process with the aim of maintaining the authenticity of the test data. In addition, oversampling aims to improve model performance at the training stage and reduce bias towards minority classes.
   

## Modeling
In this project, several algorithms for regression evaluation purpose such as:
1. Logistic Regression

   Logistic regression is a machine learning algorithm that estimates the probability of an event occuring, such as choosing or not choosing, based on a given dataset of independent variables
   
2. Random Forest

   Random Forest is a machine learning algorithm that uses multiple decision trees to make more accurate predictions. Each tree examines a different random portion of the data, and the results are combined. This helps to improve accuracy and reduce errors.
   
3. Decision Tree
   
   A decision tree is a data analysis method and machine learning algorithm in the form of a hierarchical tree-like structure that breaks down data into smaller subsets (splitting) to predict the final outcome based on decision rules.
   
4. SVM

   SVM is a classification algorithm that finds the optimal hyperplane to separate classes, performing well in high-dimensional spaces.
   
## Evaluation

The following is an evaluation of each algorithms used:

|     Algorithm                                   |   Accuracy   |   Precision   |    Recall   |   F1-Score   |
|-------------------------------------------------|--------------|---------------|-------------|--------------|
| Logistic Regression                             |   0.738748   |    0.161716	|   0.790323  |   0.268493   |
| Random Forest                                   |   0.936399   | 	  0.200000	|   0.016129  |   0.029851   |
| Decision Tree                                   |   0.916830   |    0.189189   |   0.112903  |   0.141414   |
| SVM                                             |   0.728963   |    0.152104	|   0.758065  |   0.253369   |
| Logistic Regression (After Hypertune Parameter) |   0.736791	  |    0.160656   |   0.790323  |   0.267030   |
| SVM (After Hypertune Parameter)                 |   0.860078   |    0.106796	|   0.177419  |   0.133333   |
 

## Conclusion



