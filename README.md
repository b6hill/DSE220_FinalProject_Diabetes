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

comments: The dataset is imbalanced, with a majority of respondents not diagnosed with diabetes (class 0) and a smaller portion classified as diabetic or prediabetic (class 1).

**HighBP**  
    Description: High blood pressure diagnosed  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/4d5c8eb0-06b0-451d-aad3-605b7ca8a0a9" />

comments: Respondents with high blood pressure show a markedly higher proportion of diabetes, indicating strong correlation between hypertension and diabetes.

**HighChol**  
    Description: High cholesterol diagnosed  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/0c990100-3d53-45e9-a881-731e907fdabd" />

comments: A noticeably larger fraction of individuals with high cholesterol are diabetic, suggesting elevated cholesterol is associated with diabetes risk.

**CholCheck**  
    Description: Cholesterol check in last 5 years  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/142671c0-379e-45a4-bd06-d0e0998e7d04" />

comments: Both diabetic and non-diabetic groups overwhelmingly report having had a cholesterol check, though diabetics have a slightly higher testing rate — likely due to medical monitoring.

**BMI**  
    Description: Body Mass Index  
    Continuous or Categorical: Continuous (Integer)  
    Possible values: Whole number BMI score

<img width="713" height="470" alt="image" src="https://github.com/user-attachments/assets/efbc241d-0f99-4026-8d50-17380989486f" />

comments: The BMI distribution is approximately normal, centered around the overweight range (25–30), with a tail extending into obesity.

<img width="695" height="547" alt="image" src="https://github.com/user-attachments/assets/bb470c4b-cb20-4084-8ede-0cdf2374aa28" />

comments: Diabetic folks on average seem to have higher BMIs based on the average of the two box plots

**Smoker**  
    Description: Smoked ≥100 cigarettes in lifetime  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/1dc164d7-2c84-46be-bc74-64d07fb5f9e0" />

comments: Smoking history shows only a slight difference between diabetics and non-diabetics, suggesting limited direct association.

**Stroke**  
    Description: Ever told you had a stroke  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/7cf8594b-e106-4690-9189-66c07f6c3c90" />

comments: A much higher proportion of respondents with a history of stroke are diabetic, reflecting shared cardiovascular risk factors.

**HeartDiseaseorAttack**  
    Description: CHD or heart attack history  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/f3afa85a-31fa-4d37-9975-816c78a3f690" />

comments: Individuals with previous heart disease or heart attack have a significantly higher proportion of diabetes compared to those without.

**PhysActivity**  
    Description: Physical activity in past 30 days (not job-related)  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="598" height="450" alt="image" src="https://github.com/user-attachments/assets/51da6250-f258-4030-8cfd-781bc1cd6144" />

comments: Those reporting no physical activity are notably more likely to have diabetes, highlighting physical inactivity as a risk factor.

**Fruits**  
    Description: Fruit consumption ≥1 time per day  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/5de5b3e4-c834-4af2-a08f-db9c533f1060" />

comments: Respondents who do not eat fruit daily show a slightly higher rate of diabetes, suggesting diet quality differences between groups.

**Veggies**  
    Description: Vegetable consumption ≥1 time per day  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/93887ffd-7979-4bd2-b08a-9072e40cae29" />

comments: Similar to fruit consumption, those who eat fewer vegetables are marginally more likely to be diabetic, though the difference is smaller.

**HvyAlcoholConsump**  
    Description: Heavy alcohol consumption  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/783a71ed-28fd-49b3-b79e-70f51acc2354" />

comments:Heavy alcohol consumers show a somewhat lower proportion of diabetics, possibly reflecting confounding effects (e.g., health screening or small sample size).
    
**AnyHealthcare**  
    Description: Access to any healthcare coverage  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/26659993-59b4-42fa-9d82-b49998c0a8da" />

comments: Both groups mostly have healthcare coverage, with negligible difference in diabetes prevalence by coverage status.

**NoDocbcCost**  
    Description: Could not see doctor due to cost  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/2e7d67de-4e32-4339-bebe-9f4427847238" />

comments: Those unable to see a doctor due to cost have a slightly higher proportion of diabetes, indicating potential healthcare access disparities.

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

comments: Respondents rating their health as “fair” or “poor” have a much higher prevalence of diabetes, while those reporting “excellent” or “very good” health are rarely diabetic.

**MentHlth**  
    Description: Days mental health not good  
    Continuous or Categorical: Continuous (Integer)  
    Possible values: 0–30

<img width="721" height="470" alt="image" src="https://github.com/user-attachments/assets/9d139ecb-19ac-4de0-a827-8643ccbc6da7" />

comments: The distribution of poor mental health days is similar between groups, though diabetics show a slight rightward shift toward more unhealthy days.

**PhysHlth**  
    Description: Days physical health not good  
    Continuous or Categorical: Continuous (Integer)  
    Possible values: 0–30

<img width="721" height="470" alt="image" src="https://github.com/user-attachments/assets/9a77b12d-dc86-4639-a2f6-6e51ee944875" />

comments: Diabetics tend to report more days of poor physical health than non-diabetics, with a heavier right tail indicating chronic physical challenges.

**DiffWalk**  
    Description: Difficulty walking/climbing stairs  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = No, 1 = Yes

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/bafbea77-9b6d-468b-854c-1bd37ec03eab" />

comments: A strikingly higher proportion of those with walking difficulty are diabetic, showing strong association between mobility limitations and diabetes.

**Sex**  
    Description: Biological sex  
    Continuous or Categorical: Categorical (Binary)  
    Possible values: 0 = Female, 1 = Male

<img width="597" height="450" alt="image" src="https://github.com/user-attachments/assets/5a914e46-87c6-4e0a-8e51-138f2b4dd5f6" />

comments: Males show a slightly higher proportion of diabetes than females, though the difference is modest.

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

comments: The prevalence of diabetes increases sharply with age — older respondents (especially 55+) have much higher rates of diabetes than younger adults.

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

comments: Diabetes prevalence decreases with higher education levels; individuals with less formal education show a notably greater share of diabetes.

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

comments: Diabetes is more common in lower income brackets, with prevalence steadily declining as income rises — highlighting a clear socioeconomic gradient.

3)Do you have missing and duplicate values in your dataset?

No missing values but there are 24206 duplicates which we will drop


## Data Preprocessing Steps
- Dropped duplicate values
- Scaled our numerical colums ('BMI', 'GenHlth', 'MentHlth', 'PhysHlth', 'Age', 'Education', 'Income') using min max scaler to ensure all these values are between 0 and 1
- Used a RandomOverSampler to balance our training data


## Model Training

For our first model for this project we chose to use Deciscion Tree Classifier

**Decision Tree One**
*Used unabalenced training data with default values for hyperparams*
These results from the initial Decision Tree model (trained on the imbalanced data) demonstrate overfitting (right side of the graph). The model has a 99% accuracy on the training data and only a 77% accuracy on the unseen test data. The model is failing to predict the positive class (Class 1, diabetes) and achieving a very poor recall of 0.32 and precision of 0.29. This means the model is only correctly identifying 32% of the actual diabetes cases in the test set. Next, we will oversample the data to try to balance it more, and then see if that helped the model.

**Decision Tree Two**
*Rebalanced the training data using random over sampler along with default values for hyperparams*
Applying oversampling didn't fix the problem and actually made the model's performance slightly worse (more right on the graph). The training results show the model is  even more overfit than before. It achieved a 100% accuracy on the balanced training set, and the accuracy only went up a little bit to 78% on the testing set compared to the previous model. The model's ability to find the minority class (Class 1, diabetes) worsened, with the recall dropping from 0.32 down to 0.28. This means the model is still failing to identify over 70% of the actual diabetes cases, indicating simply oversampling was not the right solution.

**Decision Tree Three**
By setting min_samples_leaf to 20 and max_depth to 10, we were able to address the overfitting of the previous 2 models. (Closer to the middle on the graph) The train and test accuracies (75% and 70%) are now much closer, which proves the model is generalizing well. This new model is far more effective at the actual goal, as the recall for the positive (diabetes) class dramatically improved from 0.28 to 0.77. This means the model now correctly identifies 77% of the diabetes cases in the test set. The drawback of this model is that it has a lower precision (0.31).

<img width="1238" height="696" alt="image" src="https://github.com/user-attachments/assets/950af762-1783-4476-b543-c0036d0ee628" />


## Decision Tree Conclusion

In this milestone, we trained and tuned a Decision Tree classifier to predict diabetes from the CDC health indicators dataset. Initial models trained on both the original imbalanced data and on a randomly oversampled dataset showed overfitting, with training accuracies near 100% but test accuracies around 77-78%. These initial models failed to identify the minority (diabetes) class, achieving a very low test recall of only 0.28-0.32. By applying hyperparameter tuning and setting max_depth=10 and min_samples_leaf=20 to the balanced, oversampled data, we created a final model that resolved the overfitting, showing a 75% training and 70% testing accuracy. This tuned model improved the test recall for the diabetes class to 0.77. To further improve this, we could move to ensemble models like Random Forest, which should reduce the high number of false positives and improve our low precision . Additionally, using a more sophisticated balancing technique like SMOTE, instead of just duplicating samples, would likely create a better-performing model.


## Next Steps

For the next steps,  our next model we plan to try is a Random Forest model. This model is an ensemble model and is well-suited to fix the two main problems we had. First, it addresses the severe overfitting by averaging the results of many models, making it much more stable and generalizable. Second, while our (Model 3) achieved good recall (0.77), it suffered from very low precision (0.31). A Random Forest is likely to find a better balance between precision and recall, ultimately leading to a more accurate and reliable model for predicting diabetes.



## Environment setup
We are running our project in Google Colab - recommended to also run the code there as well, as this should be seemless. However if you do chose to run this in your own notebook environment we have provided a requirements.txt to install the exact lib versions we using.

## Sources
dataset link: 
https://archive.ics.uci.edu/dataset/891/cdc+diabetes+health+indicators

Recommend to import directly through python like below:

cdc_diabetes_health_indicators = fetch_ucirepo(id=891)

X = cdc_diabetes_health_indicators.data.features
y = cdc_diabetes_health_indicators.data.targets
