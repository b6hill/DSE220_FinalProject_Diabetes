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

### 2.2 Correlation Matrix

<img width="1386" height="1190" alt="image" src="https://github.com/user-attachments/assets/aca13b7b-f881-4717-b79a-3c29efd74cf3" />

The heatmap shows that while most feature correlations are weak (close to 0.00), there are a few moderate/strong relationships. The strongest positive correlations observed are the following: General Health is strongly correlated with Poor Physical Health Days at 0.52 and moderately correlated with Difficulty Walking at 0.45, suggesting these variables measure similar physical traits. Other moderate relationships include Income and Education (0.42), and the connection between High Blood Pressure and High Cholesterol at 0.28.

### 2.3 Scatter Plot with PC1 v PC2 with output class coloring
<img width="857" height="547" alt="image" src="https://github.com/user-attachments/assets/e1afd32e-6877-44f7-be26-3e122ea55524" />

This PCA scatter plot projects the high-dimensional dataset onto a 2D plane using the first two principal components. The visualization reveals a significant overlap between the diabetic and healthy classes, with no distinct clusters or clear separation boundaries. While the left side of the graph seems to correlate to the non-diabetic and the right side seems to correlate to the diabetic, the separation boundary does not seem very clear.

### 2.4 Pair plots showing clustering with K=4 for PC1-12

<img width="3044" height="2946" alt="image" src="https://github.com/user-attachments/assets/78bac2e5-147d-4567-b43f-c747bcd4b049" />

### 2.5

<img width="3107" height="2946" alt="image" src="https://github.com/user-attachments/assets/1e1d848b-993c-4632-ad94-c0e76251bb81" />
This pair plot visualizes the distribution of diabetic and non-diabetic cases across the 12 different PC components. Since there are 12 PC components, it can be difficult to interpret how each component is contributing to the overall model. From this visualization its pretty easy to see that perfect classification is difficult with this data.

## 3 Methods

### 3.1 Data Exploration

- Checked for and removed missing values and duplicates from our data set. 
- We also checked the distribution of each attribute in out data set and determined which ones were continuous and which were categorical
- Looked at correlation matrix to see which attributes had the highest correlation with the target variable and also which attributes had a high level of correlation with each other

### 3.2 Data Preprocessing

#### 3.2.1 Pre-Processing for Decision Tree

- Applied min-max scaling to our continuous cols ('BMI', 'GenHlth', 'MentHlth', 'PhysHlth', 'Age', 'Education', 'Income')

```
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, stratify=y, random_state=42
)

cols_to_scale = ['BMI', 'GenHlth', 'MentHlth', 'PhysHlth', 'Age', 'Education', 'Income']

scaler = MinMaxScaler()
scaler.fit(X_train[cols_to_scale])

X_train[cols_to_scale] = scaler.transform(X_train[cols_to_scale])
X_test[cols_to_scale] = scaler.transform(X_test[cols_to_scale])
     
```
- Considered dropping some of the columns but based on our analysis of the correlation matrix, none of the attributes were overly correlated so we decided to keep all 
- Train-test split with ratio 80:20
- RandomOversampler applied to balance our train data

#### 3.2.2 Pre-Processing for XGBoost

In addition to the steps followed in Preprocessing for Decision Tree we also:

- Applied dimension reduction on our dataset using PCA (12 principal components)
- Applied Kmeans clustering (k=4) and added the cluster label as an addition input to our new model
- instead of RandomOversampler we decided to try using SMOTE resampling method on our training data
```
#rebalance training with SMOTE
smote = SMOTE(random_state=random_state)
X_train, y_train = smote.fit_resample(X_train, y_train)
```

### 3.3 Model 1 - Decision Tree Classifier

For our Decision Tree Classifier, we took an iterive approach to tuning our model.

- Iteration 1 - Baseline Decision Tree:
*Trained a simple Decision Tree classifier using default hyperparameters.
No oversampling, no hyperparameter tuning -- Served as the baseline to evaluate how the raw features performed.*
- Iteration 2 - Decision Tree With random Oversampling:
*Rebalanced the highly scewed training data.
Kept the Decision Tree hyperparameters mostly unchanged.
This iteration isolated the impact of addressing class imbalance.*
- Iteration 3 - Tuned Decision Tree:
*Performed hyperparameter tuning through multiple back to back runs and landed on using max_depth = 10 and min_samples_leaf = 20*


### 3.4 Model 2 - XGBoost along with PCA and clustering preprocessing techniques

- We first applied PCA with just two principle components but found PC1 and PC2 were only able to capture about 28.2% of the variance in the dataset. We instead opted to pick enough components to capture roughly 85% and therefore went with 12 components which captured, more precisly, 86.7%.
```
N = 12
pca = PCA(n_components=N)
X_pca_values = pca.fit_transform(X_scaled)

X_pca = pd.DataFrame(X_pca_values, columns=[f'PC{x+1}' for x in range(N)])
```

<img width="590" height="390" alt="image" src="https://github.com/user-attachments/assets/b8072d90-823a-4d74-ac82-98fef1e91d43" />


- Next we applied k-means clustering. In order to choose an optimal value for k we used the elbow method and ran the clustering for k from 1-9 and founmd k=4 to be the most optimal

```
k_range = range(1, 10)
inertia = []

print("Calculating inertia for k=1 to 9")

for k in k_range:
    kmeans = KMeans(n_clusters=k, random_state=42, n_init=10)
    kmeans.fit(X_pca)
    inertia.append(kmeans.inertia_)

# WCSS values
wcss_df = pd.DataFrame({'Number of Clusters (k)': k_range, 'WCSS (Inertia)': inertia})
print("\nWCSS Table:")
display(wcss_df)

# Plot Elbow Curve
plt.figure(figsize=(8, 5))
plt.plot(k_range, inertia, marker='o')
plt.xlabel('Number of clusters (k)')
plt.ylabel('Inertia')
plt.title('Elbow Method for Optimal k')
plt.grid(True)
plt.xticks(k_range)
plt.show()
```
<img width="722" height="470" alt="image" src="https://github.com/user-attachments/assets/8a62d263-cf34-42aa-b42d-499e7d4c4b53" />

- Using the cluster labels as inputs in addition to our PC1-12, we rebalanced our training data using SMOTE and created an XGBoost model to predict our output class





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

For Model 2, we wanted to understand the data better before building the final classifier. The dataset has many features, and some of them overlap with each other. So first, we used PCA to reduce the number of features and keep only the important information. After that, we used K-Means to group people into clusters based on these PCA features. We added the cluster number as a new feature and trained XGBoost on this combined data. The main idea was that the clusters might give the model extra patterns to learn from.
When we checked the results, the clusters did not match the diabetes labels very well. XGBoost performed strong on the training data, but the performance dropped on the test data. This shows clear overfitting — the model learned the training patterns too closely and could not generalize. The results make sense because the data is imbalanced, and SMOTE may create synthetic cases that are not fully realistic.
There are also some limitations. PCA mixes features together, so it’s hard to understand what each component means. K-Means might not find the true groups because it assumes simple cluster shapes. SMOTE can also create samples that may not match real-world patterns. And XGBoost is a powerful model that can overfit if not tuned carefully.
Overall, Model 2 gave us a different way to explore the data, but the extra PCA and clustering steps did not improve accuracy much. In the future, trying different clustering methods, fewer PCA components, or more regularization might help the model perform better.

## 6 Conclusion

Overall, we were able to go from cleaning the original CDC data to training and tuning various models to being able to predict with decent accuracy if someone is likely to have diabetes or not. While some models performed better than others, we were able to show that machine learning could be used to benefit the public health. 
One thing we wish we did differently was instead of just using one decision tree, we could have tried an ensemble method and tried using Random Forest instead. This would’ve potentially averaged out possible errors and boosted performance. Since single decision trees can be unstable and prone to overfitting, averaging them out would likely have raised our low precision score while keeping our recall high. We also wish we could have spent more time working with SMOTE and seeing how creating data points could be better than duplicating existing ones. Generating new, synthetic examples would have helped our model learn actual patterns in the minority class, rather than just memorizing the repeated rows that came from simple random oversampling.
For final thoughts, this project taught us the reality of working with real-world data.We discovered that a lot of effort happens before modeling, such as the data preparation, cleaning, and feature selection. Working with real-world issues like class imbalance gave us practical experience that datasets can be challenging to work with and analyze. Overall, we learned a lot about working with teammates on real-world issues that have real consequences on our society.


## 7 Statement of Colaboration

Brian Hill - Project Manager, Coder
Contribution: Brian created the GitHub repository and took the lead on organizing the project. He coordinated collaboration, managed timelines, handled the submission process, and reviewed all code, adding some additional inputs in EDA and preprocessing and training the XGBoost model.
Arvind Krish - Lead Coder
Contribution: Arvind worked on code development and focused heavily on data analysis. He completed most of the Milestone 3 work and contributed to preparing intermediate results and documentation.
Rathan Anireddy - Lead Coder
Contribution: Rathan worked on code development and completed most of the Milestone 4 tasks. This included implementing the PCA + K-Means + XGBoost pipeline, generating visualizations, producing evaluation metrics, and writing the corresponding analysis.
