# DSE220_FinalProject_Diabetes
Final Project DSE220 - Diabetes data prediction

## 1 Introduction
We chose this project and dataset to explore how machine learning could be used to help public health. We specifically chose the CDC Diabetes Health Indicators dataset from the CDC to see how various lifestyle factors play an impact on an individual getting diabetes sometime in their life. 

We found this project cool because we were able to leverage what we learned from this class and utilize it on real-world data to make insights that could help others. Many of us know people who are diabetic or prediabetic, so being able to figure out what factors and things people can change in their lives can greatly help people from suffering from this disease. 

A good predictive model is important because healthcare providers could use this model to accurately predict diabetes status. If the model performs poorly, it would be detrimental to a patient if they were told that they were at a low risk for developing diabetes when they were actually at high risk. The patient could have instead been focusing on making lifestyle changes to lower the chances. 

## 2 Figures
### 2.1 Distribution for each attribute

#### 2.1.1 Diabetes_binary 
    
Description: Diabetes diagnosis status  
Continuous or Categorical: Categorical (Binary)  
Possible values: 0 = No diabetes, 1 = Prediabetes/diabetes

<img width="566" height="470" alt="image" src="https://github.com/user-attachments/assets/faeddaa9-9699-4704-a017-eb11433d7ee1" />

comments: The dataset is imbalanced, with a majority of respondents not diagnosed with diabetes (class 0) and a smaller portion classified as diabetic or prediabetic (class 1).

#### 2.1.2 HighBP 
Description: High blood pressure diagnosed  
Continuous or Categorical: Categorical (Binary)  
Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/4d5c8eb0-06b0-451d-aad3-605b7ca8a0a9" />

comments: Respondents with high blood pressure show a markedly higher proportion of diabetes, indicating strong correlation between hypertension and diabetes.

#### 2.1.3 HighChol 

Description: High cholesterol diagnosed  
Continuous or Categorical: Categorical (Binary)  
Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/0c990100-3d53-45e9-a881-731e907fdabd" />

comments: A noticeably larger fraction of individuals with high cholesterol are diabetic, suggesting elevated cholesterol is associated with diabetes risk.

#### 2.1.4 CholCheck
Description: Cholesterol check in last 5 years  
Continuous or Categorical: Categorical (Binary)  
Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/142671c0-379e-45a4-bd06-d0e0998e7d04" />

comments: Both diabetic and non-diabetic groups overwhelmingly report having had a cholesterol check, though diabetics have a slightly higher testing rate — likely due to medical monitoring.

#### 2.1.5 BMI 
Description: Body Mass Index  
Continuous or Categorical: Continuous (Integer)  
Possible values: Whole number BMI score

##### 2.1.5.1
<img width="713" height="470" alt="image" src="https://github.com/user-attachments/assets/efbc241d-0f99-4026-8d50-17380989486f" />

comments: The BMI distribution is approximately normal, centered around the overweight range (25–30), with a tail extending into obesity.

##### 2.1.5.2
<img width="695" height="547" alt="image" src="https://github.com/user-attachments/assets/bb470c4b-cb20-4084-8ede-0cdf2374aa28" />

comments: Diabetic folks on average seem to have higher BMIs based on the average of the two box plots

#### 2.1.6 Smoker
    
Description: Smoked ≥100 cigarettes in lifetime  
Continuous or Categorical: Categorical (Binary)  
Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/1dc164d7-2c84-46be-bc74-64d07fb5f9e0" />

comments: Smoking history shows only a slight difference between diabetics and non-diabetics, suggesting limited direct association.

#### 2.1.7 Stroke 
Description: Ever told you had a stroke  
Continuous or Categorical: Categorical (Binary)  
Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/7cf8594b-e106-4690-9189-66c07f6c3c90" />

comments: A much higher proportion of respondents with a history of stroke are diabetic, reflecting shared cardiovascular risk factors.

#### 2.1.8 HeartDiseaseorAttack

Description: CHD or heart attack history  
Continuous or Categorical: Categorical (Binary)  
Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/f3afa85a-31fa-4d37-9975-816c78a3f690" />

comments: Individuals with previous heart disease or heart attack have a significantly higher proportion of diabetes compared to those without.

#### 2.1.9 PhysActivity
Description: Physical activity in past 30 days (not job-related)  
Continuous or Categorical: Categorical (Binary)  
Possible values: 0 = No, 1 = Yes

<img width="598" height="450" alt="image" src="https://github.com/user-attachments/assets/51da6250-f258-4030-8cfd-781bc1cd6144" />

comments: Those reporting no physical activity are notably more likely to have diabetes, highlighting physical inactivity as a risk factor.

#### 2.1.10 Fruits

Description: Fruit consumption ≥1 time per day  
Continuous or Categorical: Categorical (Binary)  
Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/5de5b3e4-c834-4af2-a08f-db9c533f1060" />

comments: Respondents who do not eat fruit daily show a slightly higher rate of diabetes, suggesting diet quality differences between groups.

#### 2.1.11 Veggies
Description: Vegetable consumption ≥1 time per day  
Continuous or Categorical: Categorical (Binary)  
Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/93887ffd-7979-4bd2-b08a-9072e40cae29" />

comments: Similar to fruit consumption, those who eat fewer vegetables are marginally more likely to be diabetic, though the difference is smaller.

#### 2.1.12 HvyAlcoholConsump

Description: Heavy alcohol consumption  
Continuous or Categorical: Categorical (Binary)  
Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/783a71ed-28fd-49b3-b79e-70f51acc2354" />

comments:Heavy alcohol consumers show a somewhat lower proportion of diabetics, possibly reflecting confounding effects (e.g., health screening or small sample size).
    
#### 2.1.13 AnyHealthcare
Description: Access to any healthcare coverage  
Continuous or Categorical: Categorical (Binary)  
Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/26659993-59b4-42fa-9d82-b49998c0a8da" />

comments: Both groups mostly have healthcare coverage, with negligible difference in diabetes prevalence by coverage status.

#### 2.1.15 NoDocbcCost

Description: Could not see doctor due to cost  
Continuous or Categorical: Categorical (Binary)  
Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/2e7d67de-4e32-4339-bebe-9f4427847238" />

comments: Those unable to see a doctor due to cost have a slightly higher proportion of diabetes, indicating potential healthcare access disparities.

#### 2.1.16 GenHlth

Description: Self-rated overall health  
Continuous or Categorical: Categorical (Ordinal)  
Possible values:  
    1 = Excellent  
    2 = Very good  
    3 = Good  
    4 = Fair  
    5 = Poor

<img width="589" height="450" alt="image" src="https://github.com/user-attachments/assets/3e6cfa8e-ec5f-490b-b147-1ce4a14e2877" />

comments: Respondents rating their health as “fair” or “poor” have a much higher prevalence of diabetes, while those reporting “excellent” or “very good” health are rarely diabetic.

#### 2.1.17 MentHlth

Description: Days mental health not good  
Continuous or Categorical: Continuous (Integer)  
Possible values: 0–30

<img width="721" height="470" alt="image" src="https://github.com/user-attachments/assets/9d139ecb-19ac-4de0-a827-8643ccbc6da7" />

comments: The distribution of poor mental health days is similar between groups, though diabetics show a slight rightward shift toward more unhealthy days.

#### 2.1.17 PhysHlth

Description: Days physical health not good  
Continuous or Categorical: Continuous (Integer)  
Possible values: 0–30

<img width="721" height="470" alt="image" src="https://github.com/user-attachments/assets/9a77b12d-dc86-4639-a2f6-6e51ee944875" />

comments: Diabetics tend to report more days of poor physical health than non-diabetics, with a heavier right tail indicating chronic physical challenges.

#### 2.1.18 DiffWalk

Description: Difficulty walking/climbing stairs  
Continuous or Categorical: Categorical (Binary)  
Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/bafbea77-9b6d-468b-854c-1bd37ec03eab" />

comments: A strikingly higher proportion of those with walking difficulty are diabetic, showing strong association between mobility limitations and diabetes.

#### 2.1.5 Sex
Description: Biological sex  
Continuous or Categorical: Categorical (Binary)  
Possible values: 0 = Female, 1 = Male

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/5a914e46-87c6-4e0a-8e51-138f2b4dd5f6" />

comments: Males show a slightly higher proportion of diabetes than females, though the difference is modest.

#### 2.1.19 Age

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

comments: The prevalence of diabetes increases sharply with age — older respondents (especially 55+) have much higher rates of diabetes than younger adults.

#### 2.1.20 Education

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

comments: Diabetes prevalence decreases with higher education levels; individuals with less formal education show a notably greater share of diabetes.

#### 2.1.21 Income

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

comments: Diabetes is more common in lower income brackets, with prevalence steadily declining as income rises — highlighting a clear socioeconomic gradient.

## 3 Methods

### 3.1

## 4 Results

### 4.1 Decision Tree

Training Data Predictions:

| Class            | Precision | Recall | F1-Score | Support |
| ---------------- | --------- | ------ | -------- | ------- |
| 0                | 0.78      | 0.70   | 0.73     | 155,501 |
| 1                | 0.72      | 0.80   | 0.76     | 155,501 |
| **Accuracy**     | -         | -      | 0.75     | 311,002 |
| **Macro Avg**    | 0.75      | 0.75   | 0.75     | 311,002 |
| **Weighted Avg** | 0.75      | 0.75   | 0.75     | 311,002 |

Test Data Predictions:
| Class            | Precision | Recall | F1-Score | Support |
| ---------------- | --------- | ------ | -------- | ------- |
| 0                | 0.94      | 0.69   | 0.80     | 38,876  |
| 1                | 0.31      | 0.77   | 0.44     | 7,019   |
| **Accuracy**     | -         | -      | 0.70     | 45,895  |
| **Macro Avg**    | 0.63      | 0.73   | 0.62     | 45,895  |
| **Weighted Avg** | 0.85      | 0.70   | 0.74     | 45,895  |




Confusion Matrix:

<img width="531" height="470" alt="image" src="https://github.com/user-attachments/assets/325a44dc-cfcc-4a7f-a2c2-9bf5fd8396b1" />


### 4.2 XGBOOST

Training Data Predictions:
| Class            | Precision | Recall | F1-Score | Support |
| ---------------- | --------- | ------ | -------- | ------- |
| 0                | 0.80      | 0.70   | 0.75     | 155,564 |
| 1                | 0.73      | 0.82   | 0.78     | 155,564 |
| **Accuracy**     | -         | -      | 0.76     | 311,128 |
| **Macro Avg**    | 0.77      | 0.76   | 0.76     | 311,128 |
| **Weighted Avg** | 0.77      | 0.76   | 0.76     | 311,128 |

Testing Data Predictions:

| Class            | Precision | Recall | F1-Score | Support |
| ---------------- | --------- | ------ | -------- | ------- |
| 0                | 0.93      | 0.69   | 0.79     | 38,813  |
| 1                | 0.30      | 0.72   | 0.42     | 7,082   |
| **Accuracy**     | -         | -      | 0.69     | 45,895  |
| **Macro Avg**    | 0.61      | 0.71   | 0.61     | 45,895  |
| **Weighted Avg** | 0.83      | 0.69   | 0.73     | 45,895  |




Confustion Matrix:

<img width="527" height="393" alt="image" src="https://github.com/user-attachments/assets/15a9a11c-2211-4427-88e8-051e99b23a64" />


### 4.3 Result Comparison
Both the tuned Decision Tree and XGBoost models achieve similar overall accuracy, with the Decision Tree at 70% on the test set and XGBoost slightly lower at 69%. Both models perform well on the majority class (non-diabetic), with high precision and moderate recall, but struggle to predict the minority class (diabetes), showing low precision and moderate-to-high recall. The Decision Tree slightly outperforms XGBoost in recall for diabetes cases (0.77 vs 0.72), meaning it correctly identifies more positive cases. XGBoost achieves slightly higher F1-scores during training, reflecting a better balance between precision and recall, but this advantage does not carry over to the test set. Both models exhibit some overfitting, with training performance higher than test performance, though XGBoost’s ensemble approach reduces extreme overfitting compared to the single Decision Tree. The limited improvement with XGBoost suggests that feature preprocessing, including PCA and cluster labels, largely drives model performance. Overall, the Decision Tree is simpler and more interpretable, while XGBoost offers marginal gains in training metrics but similar generalization.


## 5 Discusion

### 5.1

## 6 Conclusion

## 7 Statement of Colaboration
