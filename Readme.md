# Cardiovascular Risk Factor Analysis Using Naive Bayes

## 1. Introduction
<div align = "justify"> 
<p> Chronic Heart Disease (CHD) is a significant global health concern, contributing to a substantial number of deaths and disabilities worldwide. Identifying individuals at high risk of developing CHD and implementing appropriate preventive measures is crucial for reducing its impact on public health. The number of deaths caused by cardiovascular disease and stroke is predicted to reach 23.3 million in 2030 (Miranda et al., 2016). As a leading cause of death worldwide, CHD poses a considerable public health challenge, necessitating a comprehensive understanding of its etiology, risk factors, and effective prevention and management strategies. </p>

<p> For this project I have chosen “Cardiovascular Risk Factor Data" dataset, which is a comprehensive collection of health indicators that are closely associated with cardiovascular disease. The dataset contains an extensive range of health measurements and demographic information gathered from a diverse population. It encompasses factors such as age, gender, blood pressure, cholesterol levels, glucose levels, body mass index (BMI), and smoking habits. These variables are known to play a crucial role in determining an individual's risk of developing cardiovascular disease. </p>

<p> The primary objective of this project is to develop an accurate and interpretable model using Bayesian techniques that can assess the presence or absence of CHD. By identifying key risk factors and their influence on CHD, healthcare professionals can make informed decisions regarding prevention strategies, early detection, and targeted interventions .
The Naive Bayes model is a probabilistic machine learning algorithm based on Bayes' theorem. It is commonly used for classification tasks, where the goal is to predict the category or class of a given observation based on its features. Despite its simplicity, Naive Bayes often performs remarkably well in various applications. The "naive" in Naive Bayes stems from the assumption of feature independence given the class, meaning that features are considered to be unrelated to each other once the class is known. This assumption simplifies the model's computations and makes it computationally efficient, especially for high-dimensional datasets. advantage of the Naive Bayes model is its simplicity and ease of implementation. It requires a relatively small amount of training data to estimate the parameters, making it suitable for quick and effective classification tasks. Additionally, Naive Bayes can perform well even in situations where the independence assumption is not entirely met. </p>

</div>

## 2. Methodology

### 2.1 Description of the Dataset
The dataset provided information on over 4,000 patients and included 15 attributes, each representing a potential risk factor for Chronic Heart Disease (CHD). These attributes included demographic, behavioral, and medical risk factors.
Source: Kaggle
Link: https://www.kaggle.com/datasets/mamta1999/cardiovascular-risk-data

<ins> *Variable Description* </ins>
- Sex: Gender of the patient ("M" or "F").
- Age: Age of the patient .
- Education: The level of education of the patient (Levels- 1,2,3,4).
- is_smoking: whether or not the patient is a current smoker ("YES" or "NO").
- Cigs Per Day: the number of cigarettes that the patient smoked on average in one day.
- BP Meds: whether or not the patient was on blood pressure medication
- Prevalent Stroke: whether or not the patient had previously had a stroke
- Prevalent Hyp: whether or not the patient was hypertensive
- Diabetes: whether or not the patient had diabetes
- Tot Chol: total cholesterol level of the patient
- Sys BP: systolic blood pressure of the patient
- Dia BP: diastolic blood pressure of the patient
- BMI: Body Mass Index of the patient
- Heart Rate: heart rate of the patient
- Glucose: glucose level of the patient
- TenYearCHD: 10-year risk of CHD of a patient ( 1: “Yes”, 0 : “No”)

### 2.2 Key Steps
- Step 1. Data Importing & Handling Missing Values
          In this step the data set is imported and missing values are handled by removing them from the data set.

- Step 2. Explanatory Variable Analysis
          Explored variables, structure and summary statistics of the dataset by using various data visualization techniques.

- Step 3. Data Preprocessing
          Unnecessary ‘id’ variable is removed and the categorical variables are encoded using one-hot encoding technique.

- Step 4. Split the data into Training and Testing sets
          Divided the dataset into training and testing sets using an 80:20 ratio. Training set is used to train the model and testing set is used to evaluate the model performances.

- Step 5. Model Building
          In this step, the model is trained using the training set.

- Step 6. Model Evaluation
          Made predictions using the testing set and the confusion matrix, accuracy, precision, recall, and F1-score are used to evaluate the model performance.

- Step 7. Conclusion & Interpretation
          Final conclusions and interpretations are made.

### 2.3 Tools & Libraries

This project is conducted using R programming language.

<ins> *Libraries Used* </ins>
- readr – import data
- mice – handle missing values
- ggplot2 – data visualization (EDA)
- dplyr/ caret – data manipulation
- e1071 – naïve bayes model

## 3. Results and Discussion

### Results of the Model

<ins> Model Summary </ins>
|**Metric**|**Value**|
|:---|---:|
|Accuracy|0.8564|
|Precision|0.8862|
|Recall|0.9564|
|f1-score|0.9200|

<ins> Confusion Matrix </ins>
||0|1|
|0|483|62|
|1|22|28|

- The accuracy of 0.8564 indicates that the model correctly predicted cardiovascular risk factors for approximately 85.64% of   the instances in the dataset, suggesting effective classification for both positive and negative instances.

- The precision of 0.8862, the model correctly classified 88.62% of instances predicted as having cardiovascular risk factors, highlighting its tendency to accurately identify the presence of such factors and minimize false positives.

- The recall of 0.9564, the model accurately identified 95.64% of all actual instances with cardiovascular risk factors, reflecting its effectiveness in capturing the majority of such instances and minimizing false negatives.

- The F1-Score of 0.9200, the model achieves a strong balance between precision and recall, as it is the harmonic mean of these metrics. This balanced measure comprehensively considers both false positives and false negatives in assessing the model's performance.

## 4. Conclusion and Recommendation

The achieved accuracy of 85.64% indicates that the naïve bayes model performed well in predicting cardiovascular risk factors. This level of accuracy suggests that the model can be a valuable tool for identifying individuals at risk and aiding in early intervention and prevention strategies.
Accurate prediction of cardiovascular risk factors can have a significant impact on public health. By identifying high-risk individuals, public health initiatives can be targeted towards those who would benefit the most, thereby reducing the burden of cardiovascular disease on the population. The model can be further enhanced by removing correlated features and check whether the model performance increases. And also, since this is a binary classification other classification technique such as logistic regression, linear discriminant analysis, etc. may perform well than this naïve bayes model.
In this CHD classification, high precision (0.886) would mean minimizing the chances of incorrectly identifying individuals as having the disease when they do not. This is important if the consequences of unnecessary treatments or interventions are significant and high recall (0.956) would mean ensuring that the model captures the majority of individuals with the disease, minimizing the chances of missing positive cases. This is important when early detection and intervention are crucial for effective management. And by considering both precision and recall the f1-score(0.92) indicates a good balance between minimizing false positives and false negatives in CHD classification. By considering all of these factors, I can recommend this naïve bayes model as a good accurate model for classifying the patients.