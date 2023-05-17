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
 To answer What is the correlation between the variables? we tried to understand the difference of each variable between patients with stroke ande the general population within the data frame. We found the following

Stroke Patients are Overdeveloped in:

- Self Employment
- Formerly Smokers
- Married
- Hypertension
- Heart Disease
- Glucose levels
- Age

Factors balanced vs. Non Stroke: Residence & BMI

  To answer Can we cluster different attributes to better predict strokes? We decided to make clusters within the Stroke patients to identify if there were different patient profiles that could allow us to predict strokes given different sets of conditions 

In order to do this we had to get rid of categorical values to do a KMean analysis. We passed from a Data Frame of 14 columns to 21 Columns
  
We defining the number of clusters needed: Used the Codo de Jambu method (Elbow Method). WCSS is an indicator of how similar are the individuals within the clusters. The value of WCSS stopped the drastical diminish at cluster  #2 thus this is the optimal number of clusters

We used the Main components method to demonstrate there’s no overlap in the clusters 
  We compared the variables similarities and differences between clusters of patients that had suffered a stroke and also the patients without stroke to identify ranges, maximum values and possible main risk factors
  
  As initial observation we see that patients above 66-69 years old who has suffered hypertension and / or heart dis ease,married with glucose level around 210 showed more propensity to stroke

In order to get more accurate conclusions let’s analyze each variable separately

  References 
- merge data frames : https://www.youtube.com/watch?v=mEmNiPoqKAo&t=238s
- legend outside de chart : https://www.youtube.com/watch?v=b5I3D4eJtKQ
- rename columns : https://www.youtube.com/watch?v=0uBirYFhizE
- converting categorical values into binary : https://www.youtube.com/watch?v=fyHaUMX9y0A
- replacing values in columns = https://www.youtube.com/watch?v=CA4tSV-oJoY&t=153s
- k-means clustering = https://www.youtube.com/watch?v=s6PSSzeUMFk 

To answer the question of "What percentage of patients in the sample have suffered a stroke?" we took the total number of patients that have a stroke reported and divided by the total number of patients in the cleaned dataset. We added a pie chart to indicate the percentage from the total. 
  
For the question of "Percentage of strokes by gender" we got the total population divided by gender and the percentage of people that had a stroke in the dataset; showing in a bar chart. To see if there is evidence that one gender is more likely to suffer a stroke we made a hypotesis test; which resulted in both gender having the same likelyhood.
  
  
To answer the questions "Is smoking a key factor in increasing the probability of having a stroke?" and "Is having a heart disease and/or hypertension considered a risk factor?". First, we analyzed the data with the value counts and divided them into the ones that had a stroke and the ones that didn´t. A table with the summarized information was made, the table included: the total number of patients, the patients that had a stroke, and their respective percentages. With the help of a hypothesis analysis for the first question, conclusions were made.
