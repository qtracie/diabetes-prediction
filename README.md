# Diabetes Classification: Predictive Analytics for Employee Health 🏥

## 📌 Project Overview
Type 2 Diabetes Mellitus (DM2) creates a massive economic impact in the U.S., with a total annual economic burden of **$404B** as of 2017.  
This project utilizes the **CDC Health Indicators Dataset** to build a predictive model aimed at the early identification of individuals at risk of undiagnosed diabetes. 

The primary objective is to support employers in targeting prevention resources to reduce long-term medical costs and improve workforce health outcomes.

## 📊 Dataset Description
- **Source:** CDC Diabetes Health Indicators via Kaggle.
- **Size:** 253,680 rows and 22 columns.
- **Target Variable:** `Diabetes_binary` (0 = No, 1 = Yes).
- **Class Distribution:** The dataset is highly imbalanced, with only **13.9%** (35,346 cases) of respondents diagnosed with diabetes.

## 🔍 Key Insights from Exploratory Data Analysis (EDA)
- **Clinical Predictors:** Strong associations were found between diabetes and factors such as hypertension, hypercholesterolemia, high BMI, and sedentary lifestyles.
- **Physical vs. Mental Health:** While both are correlated, physical health proved to be a much stronger discriminator for diabetes risk than mental health.
- **Interaction Effects:** Our analysis confirmed that the effect of mobility issues (`DiffWalk`) on diabetes risk is heavily dependent on the patient's age.
- **Unexpected Findings:** Heavy alcohol consumption appeared inversely related to diabetes risk in this specific dataset.

## ⚙️ Model Strategy & Evaluation
- **Data Partition:** 60% Train / 20% Validation / 20% Test.
- **Primary Metric:** **Recall (Class 1)**. In a healthcare context, False Negatives are dangerous; we prioritized maximizing the detection of actual diabetic cases.
- **Handling Imbalance:** Applied **SMOTE (Oversampling)** on the training set to balance the classes (~130,000 samples each), allowing the model to learn minority-class patterns effectively.

## 🏆 Best Model Performance
The **Logistic Regression Model with Oversampling** was selected as the final model for screening purposes.

| Metric | Training Set | Validation Set | Test Set |
| :--- | :--- | :--- | :--- |
| **Recall (Class 1)** | 0.78 | 0.76 | **0.77** |
| **Accuracy** | 0.75 | 0.73 | 0.73 |
| **AUC** | 0.83 | 0.83 | 0.82 |

*Note: While Precision dropped to ~0.32, this trade-off is acceptable for a screening tool where identifying a sick person is more critical than re-testing a healthy one.*

## 💡 Business Recommendations
- **Targeted Screening:** Prioritize employees with High Blood Pressure, High Cholesterol, and High BMI for screening programs.
- **Wellness Investment:** Subsidize nutrition coaching and meal plan support to combat strong lifestyle predictors.
- **Mobility Support:** Provide ergonomic workstations and physical therapy, especially for the older workforce experiencing movement limitations.
- **Financial Support:** Lower copays for screenings and offer free annual checks for lower-income groups to reduce barriers to care.
