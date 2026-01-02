# diabetes-classification-prediction
A machine learning project predicting diabetes risk using Python and ML algorithms.
# Diabetes Classification: Predictive Analytics for Employee Health 🏥

## 📌 Project Overview
[cite_start]Type 2 Diabetes Mellitus (DM2) creates a massive economic impact in the U.S., with a total annual economic burden of **$404B** as of 2017[cite: 7, 8]. [cite_start]This project utilizes the **CDC Health Indicators Dataset** to build a predictive model aimed at the early identification of individuals at risk of undiagnosed diabetes[cite: 2, 63]. 

[cite_start]The primary objective is to support employers in targeting prevention resources to reduce long-term medical costs and improve workforce health outcomes[cite: 67, 68].

## 📊 Dataset Description
- [cite_start]**Source:** CDC Diabetes Health Indicators via Kaggle[cite: 71, 72].
- [cite_start]**Size:** 253,680 rows and 22 columns[cite: 73].
- [cite_start]**Target Variable:** `Diabetes_binary` (0 = No, 1 = Yes)[cite: 74].
- [cite_start]**Class Distribution:** The dataset is highly imbalanced, with only **13.9%** (35,346 cases) of respondents diagnosed with diabetes[cite: 87, 93, 96].

## 🔍 Key Insights from Exploratory Data Analysis (EDA)
- [cite_start]**Clinical Predictors:** Strong associations were found between diabetes and factors such as hypertension, hypercholesterolemia, high BMI, and sedentary lifestyles[cite: 100, 135].
- [cite_start]**Physical vs. Mental Health:** While both are correlated, physical health proved to be a much stronger discriminator for diabetes risk than mental health[cite: 136].
- [cite_start]**Interaction Effects:** Our analysis confirmed that the effect of mobility issues (`DiffWalk`) on diabetes risk is heavily dependent on the patient's age[cite: 426].
- [cite_start]**Unexpected Findings:** Heavy alcohol consumption appeared inversely related to diabetes risk in this specific dataset[cite: 103].

## ⚙️ Model Strategy & Evaluation
- [cite_start]**Data Partition:** 60% Train / 20% Validation / 20% Test[cite: 174].
- [cite_start]**Primary Metric:** **Recall (Class 1)**[cite: 176]. [cite_start]In a healthcare context, False Negatives are dangerous; we prioritized maximizing the detection of actual diabetic cases[cite: 179].
- [cite_start]**Handling Imbalance:** Applied **SMOTE (Oversampling)** on the training set to balance the classes (~130,000 samples each), allowing the model to learn minority-class patterns effectively[cite: 473, 474, 476].

## 🏆 Best Model Performance
[cite_start]The **Logistic Regression Model with Oversampling** was selected as the final model for screening purposes[cite: 235, 504].

| Metric | Training Set | Validation Set | Test Set |
| :--- | :--- | :--- | :--- |
| **Recall (Class 1)** | 0.78 | 0.76 | **0.77** |
| **Accuracy** | 0.75 | 0.73 | 0.73 |
| **AUC** | 0.83 | 0.83 | 0.82 |

[cite_start]*Note: While Precision dropped to ~0.32, this trade-off is acceptable for a screening tool where identifying a sick person is more critical than re-testing a healthy one[cite: 505, 535].*

## 💡 Business Recommendations
- [cite_start]**Targeted Screening:** Prioritize employees with High Blood Pressure, High Cholesterol, and High BMI for screening programs[cite: 585, 594].
- [cite_start]**Wellness Investment:** Subsidize nutrition coaching and meal plan support to combat strong lifestyle predictors[cite: 595].
- [cite_start]**Mobility Support:** Provide ergonomic workstations and physical therapy, especially for the older workforce experiencing movement limitations[cite: 589, 596].
- [cite_start]**Financial Support:** Lower copays for screenings and offer free annual checks for lower-income groups to reduce barriers to care[cite: 591, 598].

---
[cite_start]*Created by: Group 2B (Nell Hanna, Tracie Le, Jonathan Trippett)* [cite: 3, 4]
