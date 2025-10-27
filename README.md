# DSE220_FinalProject_Diabetes
Final Project DSE220 - Diabetes data prediction

##Abstract
In this project, we explore the use of machine learning techniques for diabetes prediction. This Diabetes Health Indicators dataset from the CDC captures health and lifestyle information from patients and classifies them into one of three categories: diabetic, pre-diabetic, or healthy. The dataset contains 253,680 entries (each entry corresponding to one person in the study) and 21 features. These features include a wide range of indicators, such as demographics (age, income), vital signs (BMI, blood pressure), and lifestyle factors (physical activity, smoking status, alcohol consumption). Our goal is to use all these factors to predict if a person is diabetic, pre-diabetic, or healthy by creating a model that uses the most important risk factors for diabetes. These findings can be used to inform and improve the lives of the general public.

##Data Exploration
1)How many observations does your dataset have?
Number of rows in features dataset after droping duplicates: 229474

2)Describe all columns in your dataset their scales and data distributions. Describe the categorical and continuous variables in your dataset. Describe your target column and if you are using images plot some example classes of the images.


**Diabetes_binary**  
    Description: Diabetes diagnosis status  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No diabetes, 1 = Prediabetes/diabetes

<img width="566" height="470" alt="image" src="https://github.com/user-attachments/assets/faeddaa9-9699-4704-a017-eb11433d7ee1" />









3)Do you have missing and duplicate values in your dataset?

No missing values but there are 24206 duplicates which we will drop


##Data Preprocessing Plan
How will you preprocess your data? Handle data imbalance if needed. You should only explain (do not perform pre-processing as that is in MS3) this in your README.md file and link your Jupyter notebook to it. All code and  Jupyter notebooks have be uploaded to your repo. (3 points)


##Environment setup
We are running our project in Google Colab - recommended to also run the code there as well, as this should be seemless. However if you do chose to run this in your own notebook environment we have provided a requirements.txt

##Sources
dataset link: 
https://archive.ics.uci.edu/dataset/891/cdc+diabetes+health+indicators

Recommend to import directly through python like below:

cdc_diabetes_health_indicators = fetch_ucirepo(id=891)

X = cdc_diabetes_health_indicators.data.features
y = cdc_diabetes_health_indicators.data.targets
