# Project_1
## Project title: Predictive analysis of stroke risk factors and contributors 
<p align="center">
A patient's likelihood of having a stroke based on certain parameters

---
  
An ischemic stroke occurs when the blood supply to part of the brain is interrupted or reduced, preventing brain tissue from getting oxygen and nutrients. Brain cells begin to die in minutes.

Principal signs and symptoms:
  - Trouble speaking and understanding what others are saying.
  - Paralysis or numbness of the face, arm or leg.
  - Problems seeing in one or both eyes.
  - Headache
  - Trouble walking.
  
A stroke is a medical emergency, and prompt treatment is crucial. Early action can reduce brain damage and other complications. Predicting the likelihood of stroke can help to prevent and manage the disease. This project aims to identify the key risk factors and contributors that affect stroke prediction using a large dataset.  The goal is to identify and analyze the risk factors that could increase the probability of a patient getting a stroke. 

In this project, we analyzed a stroke prediction dataset, which contains 12 columns and 5110 rows that each correspond to a patient. The information in the columns is:

1) id: unique identifier
2) gender: "Male", "Female" or "Other"
3) age: age of the patient
4) hypertension: 0 if the patient doesn't have hypertension, 1 if the patient has hypertension
5) heart_disease: 0 if the patient doesn't have any heart diseases, 1 if the patient has a heart disease
6) ever_married: "No" or "Yes"
7) work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"
8) Residence_type: "Rural" or "Urban"
9) avg_glucose_level: average glucose level in blood
10) bmi: body mass index
11) smoking_status: "formerly smoked", "never smoked", "smokes" or "Unknown"*
12) stroke: 1 if the patient had a stroke or 0 if not
  
### Cleaning process: 
 In the cleaning process, we saw the information on the columns and the database shape. We tested if there were any duplicated values. We saw that in the column "gender" were 3 different categories and we realized that in the category "other" it was just one entry, so we decided to delete that one entry because it is not enough to make any conclusions about the whole category. We searched for missing values in any column and saw that the column "BMI" had 201 N/A values, so we decided to drop them. 
Finally, we made the index as the id column and created a un csv with the cleaned data. 

### Analysis
 ##Rodolfo 
   
 ##Alex 
  
 ##Esteban 
  
To answer the questions "Is smoking a key factor in increasing the probability of having a stroke?" and "Is having a heart disease and/or hypertension considered a risk factor?". First, we analyzed the data with the value counts and divided them into the ones that had a stroke and the ones that didn´t. A table with the summarized information was made, the table included: the total number of patients, the patients that had a stroke, and their respective percentages. With the help of a hypothesis analysis for the first question, conclusions were made.
