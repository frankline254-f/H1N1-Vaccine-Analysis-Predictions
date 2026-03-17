![h1n1 vaccine](https://github.com/user-attachments/assets/d29f0a24-0d37-407b-9c3e-b327e8587334)
# H1N1-Vaccine-Analysis-Predictions
## Stakeholder
### Public Health Authorities
## Project Overview
This project uses machine learning to predict whether an individual received the **H1N1 flu vaccine** based on demographic information, health behavior, opinions, and healthcare-related factors from the **National 2009 H1N1 Flu Survey** dataset.

The goal is to help **public health authorities** understand the factors that influence vaccine uptake and support **targeted vaccination campaigns**.
## Problem Statement
Public health authorities need to increase vaccination uptake to reduce the spread of infectious diseases and protect vulnerable population. However, many individuals choose not to receive vaccines due to differences in beliefs, health behaviors, risk perception and access to healthcare. Without understanding which groups are less likely to vaccinate, it is diicult for health organisation to design effective outreach and vaccination campaigns.
## Business Understanding
## KEY QUESTION FOR PREDICTING H1N1 VACCINE UPTAKE
1.Which factors influence whether an individual receives the H1N1 flu vaccine and can we accurately predict who is likely or unlikely to get vaccinated?

2.Which demographic group is less likely to vaccinate? Understanding differences in vaccination behavior across age, gender, education level, and income helps identify high-risk populations.

3.Do doctors' recommendations influence vaccination behavior? Medical professionals are trusted sources of health advice. Analysing whether individuals who receive recommendations from their doctors are more likely to vaccinate can guide strategies for improving outreach through healthcare providers.

4.Which health conditions are associated with vaccination? People with chronic medical conditions may be more motivated to vaccinate. identifying these patterns helps príoritize interventions for high-risk groups.
## Data Understanding
The dataset used in this project is the **H1N1 and Seasonal Flu Vaccines dataset** from the National 2009 H1N1 Flu Survey. It contains 26,707 observations and 38 variables, including demographic, health, behavioral, and opinion-related features. For this project, the selected target variable is **h1n1_vaccine**, making it a binary classification problem aimed at predicting whether an individual received the H1N1 vaccine.
## Data Preprocessing
The following preprocessing steps were performed:
  -Remove unnecessary target column(**seasonal_vaccine**)
  -Define the **x** that is predictor variables and the **y** that is **H1N1_Vaccine**
  -Split data into **80% training** and **20% testing** also used **stratified sampling** to maintain class balance
  -Identifying **Numeric** and **Categorical** columns they were processed differently Numeric missing values were filled with the median, and Categorical missing values were filled with most frequent value. Categorical variables were also converted into numbers using **one-hot encoding**.
  -Combined preprocessing steps using a **pipeline** and **ColumnTransformer**
## Model Used
This project follows an **iterative modeling approach**, starting from a simple baseline model and improving progressively.
 -We start with **logistic regression** as the baseline model because it is simple and easy to interpret also it works well for binary classification.
 -Improved Model we used **Random Forest** Why use the Random Forest model? It often performs better than logistic regression on complex datasets, and it handles non-linear relationships well.
## Evaluation Matrics
Because thise is a **binary classification problem**, the following metrics were used to evaluate models on both **training** and **testing** data:
   **Accuracy**
   **Precision**
   **Recall**
   **F1 Score**
   **Confusion Matrix**
