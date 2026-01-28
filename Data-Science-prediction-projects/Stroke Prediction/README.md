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

   ![](https://raw.githubusercontent.com/Junazidomi/Data-Science/refs/heads/main/Data-Science-prediction-projects/Stroke%20Prediction/Picture/Gender.png)

   Insight:

   Based on the visualisation of patient gender distribution, it can be concluded that female patients are the most numerous compared to other genders. In addition, the ‘Other’ category will undergo preprocessing because it is considered irrelevant, given that in this analysis gender is limited to two categories.
3. Visualization of Heart Disease
4. Visualization of Hypertension Status
5. Visualization of Stroke Status
6. Visualization of Married Status
7. Visualization of Resident Type
8. Visualization of Work Type
9. Visualization of Smoking Status
10. Stroke vs Medical Data
11. Categorical Feature vs Stroke Status
12. Heatmap of Numerical Feature

## Data Preparation

The data preparation process is as follows:
1. Drop irrelevant Column
2. Missing Data Handling
3. Drop irrelevant value in column
4. Encode
5. Normalization
6. Split the Training Data and Test Data
7. Oversample

## Modeling
In this project, several algorithms for regression evaluation purpose such as:
1. Logistic Regression
2. Random Forest
3. Decision Tree
4. SVM
## Evaluation

The following is an evaluation of each algorithms used:

|     Algorithm                                   |   Accuracy   |   Precision   |    Recall   |   F1-Score   |
|-------------------------------------------------|--------------|---------------|-------------|--------------|
| Logistic Regression                             |   0.738748   |    0.161716	 |   0.790323  |   0.268493   |
| Random Forest                                   |   0.936399   | 	  0.200000	 |   0.016129  |   0.029851   |
| Decision Tree                                   |   0.916830   |    0.189189   |   0.112903  |   0.141414   |
| SVM                                             |   0.728963   |    0.152104	 |   0.758065  |   0.253369   |
| Logistic Regression (After Hypertune Parameter) |   0.736791	 |    0.160656   |   0.790323  |   0.267030   |
| SVM (After Hypertune Parameter)                 |   0.860078   |    0.106796	 |   0.177419  |   0.133333   |
 

## Conclusion

