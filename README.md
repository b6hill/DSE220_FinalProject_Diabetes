# DSE220_FinalProject_Diabetes
Final Project DSE220 - Diabetes data prediction

## Abstract
In this project, we explore the use of machine learning techniques for diabetes prediction. This Diabetes Health Indicators dataset from the CDC captures health and lifestyle information from patients and classifies them into one of three categories: diabetic, pre-diabetic, or healthy. The dataset contains 253,680 entries (each entry corresponding to one person in the study) and 21 features. These features include a wide range of indicators, such as demographics (age, income), vital signs (BMI, blood pressure), and lifestyle factors (physical activity, smoking status, alcohol consumption). Our goal is to use all these factors to predict if a person is diabetic, pre-diabetic, or healthy by creating a model that uses the most important risk factors for diabetes. These findings can be used to inform and improve the lives of the general public.

## Data Exploration
1)How many observations does your dataset have?
Number of rows in features dataset after droping duplicates: 229474

2)Describe all columns in your dataset their scales and data distributions. Describe the categorical and continuous variables in your dataset. Describe your target column and if you are using images plot some example classes of the images.


**Diabetes_binary**  
    Description: Diabetes diagnosis status  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No diabetes, 1 = Prediabetes/diabetes

<img width="566" height="470" alt="image" src="https://github.com/user-attachments/assets/faeddaa9-9699-4704-a017-eb11433d7ee1" />

comments:

**HighBP**  
    Description: High blood pressure diagnosed  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/4d5c8eb0-06b0-451d-aad3-605b7ca8a0a9" />

comments:

**HighChol**  
    Description: High cholesterol diagnosed  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/0c990100-3d53-45e9-a881-731e907fdabd" />

comments:

**CholCheck**  
    Description: Cholesterol check in last 5 years  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/142671c0-379e-45a4-bd06-d0e0998e7d04" />

comments:

**BMI**  
    Description: Body Mass Index  
    Continuous or Categorical: Continuous (Integer)  
    Possible values: Whole number BMI score

<img width="713" height="470" alt="image" src="https://github.com/user-attachments/assets/efbc241d-0f99-4026-8d50-17380989486f" />

<img width="695" height="547" alt="image" src="https://github.com/user-attachments/assets/bb470c4b-cb20-4084-8ede-0cdf2374aa28" />

comments:

**Smoker**  
    Description: Smoked ≥100 cigarettes in lifetime  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/1dc164d7-2c84-46be-bc74-64d07fb5f9e0" />

comments:

**Stroke**  
    Description: Ever told you had a stroke  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/7cf8594b-e106-4690-9189-66c07f6c3c90" />

comments:

**HeartDiseaseorAttack**  
    Description: CHD or heart attack history  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/f3afa85a-31fa-4d37-9975-816c78a3f690" />

comments:

**PhysActivity**  
    Description: Physical activity in past 30 days (not job-related)  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="598" height="450" alt="image" src="https://github.com/user-attachments/assets/51da6250-f258-4030-8cfd-781bc1cd6144" />

comments:

**Fruits**  
    Description: Fruit consumption ≥1 time per day  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/5de5b3e4-c834-4af2-a08f-db9c533f1060" />

comments:

**Veggies**  
    Description: Vegetable consumption ≥1 time per day  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/93887ffd-7979-4bd2-b08a-9072e40cae29" />

comments:

**HvyAlcoholConsump**  
    Description: Heavy alcohol consumption  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/783a71ed-28fd-49b3-b79e-70f51acc2354" />

comments:
    
**AnyHealthcare**  
    Description: Access to any healthcare coverage  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/26659993-59b4-42fa-9d82-b49998c0a8da" />

comments:

**NoDocbcCost**  
    Description: Could not see doctor due to cost  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/2e7d67de-4e32-4339-bebe-9f4427847238" />

comments:

**GenHlth**  
    Description: Self-rated overall health  
    Continuous or Categorical: Categorical (Ordinal)  
    Possible values:  
    1 = Excellent  
    2 = Very good  
    3 = Good  
    4 = Fair  
    5 = Poor

<img width="589" height="450" alt="image" src="https://github.com/user-attachments/assets/3e6cfa8e-ec5f-490b-b147-1ce4a14e2877" />

comments:

**MentHlth**  
    Description: Days mental health not good  
    Continuous or Categorical: Continuous (Integer)  
    Possible values: 0–30

<img width="721" height="470" alt="image" src="https://github.com/user-attachments/assets/9d139ecb-19ac-4de0-a827-8643ccbc6da7" />

comments:

**PhysHlth**  
    Description: Days physical health not good  
    Continuous or Categorical: Continuous (Integer)  
    Possible values: 0–30

<img width="721" height="470" alt="image" src="https://github.com/user-attachments/assets/9a77b12d-dc86-4639-a2f6-6e51ee944875" />

comments:

**DiffWalk**  
    Description: Difficulty walking/climbing stairs  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/bafbea77-9b6d-468b-854c-1bd37ec03eab" />

comments:

**Sex**  
    Description: Biological sex  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = Female, 1 = Male

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/5a914e46-87c6-4e0a-8e51-138f2b4dd5f6" />

comments:

**Age**  
    Description: Age category (5-year groups)  
    Continuous or Categorical: Categorical (Ordinal)  
    Possible values:  
    1 = 18–24  
    2 = 25–29  
    3 = 30–34  
    4 = 35–39  
    5 = 40–44  
    6 = 45–49  
    7 = 50–54  
    8 = 55–59  
    9 = 60–64  
    10 = 65–69  
    11 = 70–74  
    12 = 75–79  
    13 = 80+

<img width="589" height="458" alt="image" src="https://github.com/user-attachments/assets/d6690705-3718-4f28-b69a-2e78dfacb502" />

comments:

**Education**  
    Description: Highest education level  
    Continuous or Categorical: Categorical (Ordinal)  
    Possible values:  
    1 = No school / Kindergarten only  
    2 = Grades 1–8  
    3 = Grades 9–11  
    4 = High school graduate / GED  
    5 = Some college / Tech school  
    6 = College graduate (4+ years)

<img width="589" height="450" alt="image" src="https://github.com/user-attachments/assets/0f6f99a4-22de-46ec-a79e-a42929ac7a8c" />

comments:

**Income**  
    Description: Annual household income level  
    Continuous or Categorical: Categorical (Ordinal)  
    Possible values:  
    1 = < $10,000  
    2 = $10,000–$15,000  
    3 = $15,000–$20,000  
    4 = $20,000–$25,000  
    5 = $25,000–$35,000  
    6 = $35,000–$50,000  
    7 = $50,000–$75,000  
    8 = ≥ $75,000

<img width="589" height="453" alt="image" src="https://github.com/user-attachments/assets/9ba1d555-83bd-40c2-bbbf-aa8b1889ec14" />

comments:

3)Do you have missing and duplicate values in your dataset?

No missing values but there are 24206 duplicates which we will drop


## Data Preprocessing Plan
How will you preprocess your data? Handle data imbalance if needed. You should only explain (do not perform pre-processing as that is in MS3) this in your README.md file and link your Jupyter notebook to it. All code and  Jupyter notebooks have be uploaded to your repo. (3 points)


## Environment setup
We are running our project in Google Colab - recommended to also run the code there as well, as this should be seemless. However if you do chose to run this in your own notebook environment we have provided a requirements.txt

## Sources
dataset link: 
https://archive.ics.uci.edu/dataset/891/cdc+diabetes+health+indicators

Recommend to import directly through python like below:

cdc_diabetes_health_indicators = fetch_ucirepo(id=891)

X = cdc_diabetes_health_indicators.data.features
y = cdc_diabetes_health_indicators.data.targets
